---
title: Tilføje datafelter i momsintegrationen ved hjælp af udvidelser
description: Dette emne forklarer, hvordan du kan bruge X++ udvidelser til at tilføje datafelter i momsintegrationen.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a3da8e1b8176eb25fe4e0a320aa3e907c06e09c5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021386"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Tilføje datafelter i momsintegrationen ved hjælp af udvidelse

[!include [banner](../includes/banner.md)]


Dette emne forklarer, hvordan du kan bruge X++ udvidelser til at tilføje datafelter i momsintegrationen. Disse felter kan udvides til momsdatamodellen for momstjenesten og bruges til bestemmelse af momskoder. Du kan finde flere oplysninger i [Tilføje datafelter i momskonfigurationer](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Datamodel

Dataene i datamodellen udføres af objekter og implementeres af klasser.

Her er en liste over de vigtigste objekter:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

I følgende illustration vises, hvordan disse objekter er relateret.

[![Datamodelobjektrelation](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

Et **Document**-objekt kan indeholde mange **Line**-objekter. Hvert objekt indeholder metadata til momstjenesten.

- `TaxIntegrationDocumentObject` har `originAddress`-metadata, som indeholder oplysninger om kildeadressen, og `includingTax`-metadata, der angiver, om linjebeløbet inkluderer moms.
- `TaxIntegrationLineObject` har `itemId`, `quantity` og `categoryId` som metadata.

> [!NOTE]
> `TaxIntegrationLineObject` implementerer også **Charge**-objekter.

## <a name="integration-flow"></a>Integrationsflow

Dataene i flowet manipuleres af aktiviteter.

### <a name="key-activities"></a>Nøgleaktiviteter

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Aktiviteterne køres i følgende rækkefølge:

1. Hentning af indstilling
2. Datahentning
3. Beregningstjeneste
4. Valutakurs
5. Datapersistens

Udvid f.eks. **Hentning af data** før **Beregningstjeneste**.

#### <a name="data-retrieval-activities"></a>Datahentningsaktiviteter

**Datahentning**-aktiviteter henter data fra databasen. Der er adaptere til forskellige transaktioner, som kan hente data fra forskellige transaktionstabeller:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

I disse **Datahentning**-aktiviteter kopieres data fra databasen til `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`. Da alle disse aktiviteter udvider den samme abstrakte skabelonklasse, har de almindelige metoder.

#### <a name="calculation-service-activities"></a>Aktiviteter for beregningstjeneste

Aktiviteten **Beregningstjeneste** er linket mellem momstjenesten og momsintegrationen. Denne aktivitet er ansvarlig for følgende funktioner:

1. Konstruere anmodningen.
2. Bogføre anmodningen til momstjenesten.
3. Få svaret fra momstjenesten.
4. Analysere svaret.

Et datafelt, du føjer til anmodningen, bogføres sammen med andre metadata. 

## <a name="extension-implementation"></a>Implementering af udvidelse

Dette afsnit indeholder detaljerede trin, der forklarer, hvordan du implementerer udvidelsen. Til dette formål bruges **Bærer** og **Projekt** som eksempler på de økonomiske dimensioner.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>Trin 1. Tilføje datavariablen i objektklassen

Objektklassen indeholder datavariablen og henter/sætter-metoderne for dataene. Føj datafeltet til enten `TaxIntegrationDocumentObject` eller `TaxIntegrationLineObject` afhængigt af feltets niveau. I følgende eksempel bruges linjeniveauet, og filnavnet er `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Hvis det datafelt, du tilføjer, er på dokumentniveau, skal du ændre filnavnet til `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Bærer** og **Projekt** tilføjes som private variabler. Opret henter- og sættermetoder for disse datafelter for at manipulere dataene.

### <a name="step-2-retrieve-data-from-the-database"></a>Trin 2. Hente data fra databasen

Angiv transaktionen, og udvid de relevante adapterklasser for at hente dataene. Hvis du f.eks. bruger transaktionen **Indkøbsordre**, skal du udvide `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` er nedarvet fra `TaxIntegrationPurchTableDataRetrieval`. Den må ikke ændres, medmindre logikken i `purchTable`- og `purchParmTable`-tabellerne er forskellig.

Hvis datafeltet skal tilføjes for alle transaktioner, skal du udvide alle `DataRetrieval`-klasser.

Da alle aktiviteter for **Datahentning** udvider den samme skabelonklasse, er klassestrukturerne, variablerne og metoderne ens.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

I følgende eksempel vises den grundlæggende struktur, når tabellen `PurchTable` bruges.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

Når metoden `CopyToDocument` kaldes, findes `this.purchTable`-bufferen allerede. Formålet med denne metode er at kopiere alle de påkrævede data fra `this.purchTable` til objektet `document` ved hjælp af den sættermetode, der blev oprettet i `DocumentObject`-klassen.

På samme måde findes der allerede en `this.purchLine`-buffer i `CopyToLine`-metoden. Formålet med denne metode er at kopiere alle de påkrævede data fra `this.purchLine` til objektet `_line` ved hjælp af den sættermetode, der blev oprettet i `LineObject`-klassen.

Den mest ligetil fremgangsmåde er at udvide metoderne `CopyToDocument` og `CopyToLine`. Det anbefales dog, at du prøver metoderne `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable` først. Hvis de ikke virker efter behov, skal du implementere din egen metode og kalde den i `CopyToDocument` og `CopyToLine`. Der er tre almindelige situationer, hvor du kan bruge denne metode:

- Det påkrævede felt er i `PurchTable` eller `PurchLine`. I denne situation kan du udvide `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`. Her er eksempelkoden.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- De påkrævede data findes ikke i standardtabellen for transaktionen. Der findes dog visse join-relationer til standardtabellen, og feltet skal udfyldes på de fleste linjer. I denne situation skal du erstatte `getDocumentQueryObject` eller `getLineObject` for at forespørge på tabellen ved hjælp af en join-relation. I følgende eksempel er feltet **Levér nu** integreret med salgsordren på linjeniveau.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    I dette eksempel erklæres en `mcrSalesLineDropShipment`-buffer, og forespørgslen defineres i `getLineQueryObject`. Forespørgslen bruger relationen `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Når du udvider i denne situation, kan du erstatte `getLineQueryObject` med dit eget konstruerede forespørgselsobjekt. Men bemærk følgende punkter:

    * Da returværdien af metoden `getLineQueryObject` er `SysDaQueryObject`, skal du opbygge dette objekt ved hjælp af metoden SysDa.
    * Den eksisterende tabel kan ikke fjernes.

- De påkrævede data er relateret til transaktionstabellen af en kompliceret join-relation, eller relationen er ikke en til en (1:1), men en til mange (1:N). I denne situation bliver det lidt kompliceret. Denne situation gælder for eksemplet med økonomiske dimensioner. 

    I denne situation kan du implementere din egen metode for at hente dataene. Her er eksempelkoden i `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-filen.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>Trin 3. Føje data til anmodningen

Udvid metoden `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` eller `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` for at føje data til anmodningen. Her er eksempelkoden i `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-filen.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

I denne kode er `_destination` det ombryderobjekt, der bruges til at generere bogføringsanmodningen, og `_source` er `TaxIntegrationLineObject`-objektet. 

> [!NOTE]
> * Definer den nøgle, der bruges i anmodningsformularen, som `private const str`.
> * Angiv feltet i metoden `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` ved hjælp af `SetField`-metoden. Datatypen for den anden parameter skal være `string`. Hvis datatypen ikke er `string`, skal du konvertere den til `string`.

## <a name="appendix"></a>Appendiks

Dette appendiks viser den komplette eksempelkode til integration af økonomiske dimensioner (**Bærer** og **Projekt**) på linjeniveau.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
