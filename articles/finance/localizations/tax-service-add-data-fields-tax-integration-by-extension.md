---
title: Tilføje datafelter i momsintegrationen ved hjælp af udvidelser
description: Dette emne forklarer, hvordan du kan bruge X++ udvidelser til at tilføje datafelter i momsintegrationen.
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830334"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="77411-103">Tilføje datafelter i momsintegrationen ved hjælp af udvidelse</span><span class="sxs-lookup"><span data-stu-id="77411-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="77411-104">Dette emne forklarer, hvordan du kan bruge X++ udvidelser til at tilføje datafelter i momsintegrationen.</span><span class="sxs-lookup"><span data-stu-id="77411-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="77411-105">Disse felter kan udvides til momsdatamodellen for momstjenesten og bruges til bestemmelse af momskoder.</span><span class="sxs-lookup"><span data-stu-id="77411-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="77411-106">Du kan finde flere oplysninger i [Tilføje datafelter i momskonfigurationer](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="77411-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="77411-107">Datamodel</span><span class="sxs-lookup"><span data-stu-id="77411-107">Data model</span></span>

<span data-ttu-id="77411-108">Dataene i datamodellen udføres af objekter og implementeres af klasser.</span><span class="sxs-lookup"><span data-stu-id="77411-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="77411-109">Her er en liste over de vigtigste objekter:</span><span class="sxs-lookup"><span data-stu-id="77411-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="77411-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="77411-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="77411-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="77411-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="77411-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="77411-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="77411-113">I følgende illustration vises, hvordan disse objekter er relateret.</span><span class="sxs-lookup"><span data-stu-id="77411-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="77411-114">[![Datamodelobjektrelation](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="77411-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="77411-115">Et **Document**-objekt kan indeholde mange **Line**-objekter.</span><span class="sxs-lookup"><span data-stu-id="77411-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="77411-116">Hvert objekt indeholder metadata til momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="77411-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="77411-117">`TaxIntegrationDocumentObject` har `originAddress`-metadata, som indeholder oplysninger om kildeadressen, og `includingTax`-metadata, der angiver, om linjebeløbet inkluderer moms.</span><span class="sxs-lookup"><span data-stu-id="77411-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="77411-118">`TaxIntegrationLineObject` har `itemId`, `quantity` og `categoryId` som metadata.</span><span class="sxs-lookup"><span data-stu-id="77411-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="77411-119">`TaxIntegrationLineObject` implementerer også **Charge**-objekter.</span><span class="sxs-lookup"><span data-stu-id="77411-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="77411-120">Integrationsflow</span><span class="sxs-lookup"><span data-stu-id="77411-120">Integration flow</span></span>

<span data-ttu-id="77411-121">Dataene i flowet manipuleres af aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="77411-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="77411-122">Nøgleaktiviteter</span><span class="sxs-lookup"><span data-stu-id="77411-122">Key activities</span></span>

* <span data-ttu-id="77411-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="77411-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="77411-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="77411-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="77411-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="77411-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="77411-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="77411-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="77411-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="77411-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="77411-128">Aktiviteterne køres i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="77411-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="77411-129">Hentning af indstilling</span><span class="sxs-lookup"><span data-stu-id="77411-129">Setting Retrieval</span></span>
2. <span data-ttu-id="77411-130">Datahentning</span><span class="sxs-lookup"><span data-stu-id="77411-130">Data Retrieval</span></span>
3. <span data-ttu-id="77411-131">Beregningstjeneste</span><span class="sxs-lookup"><span data-stu-id="77411-131">Calculation Service</span></span>
4. <span data-ttu-id="77411-132">Valutakurs</span><span class="sxs-lookup"><span data-stu-id="77411-132">Currency Exchange</span></span>
5. <span data-ttu-id="77411-133">Datapersistens</span><span class="sxs-lookup"><span data-stu-id="77411-133">Data Persistence</span></span>

<span data-ttu-id="77411-134">Udvid f.eks. **Hentning af data** før **Beregningstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="77411-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="77411-135">Datahentningsaktiviteter</span><span class="sxs-lookup"><span data-stu-id="77411-135">Data Retrieval activities</span></span>

<span data-ttu-id="77411-136">**Datahentning**-aktiviteter henter data fra databasen.</span><span class="sxs-lookup"><span data-stu-id="77411-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="77411-137">Der er adaptere til forskellige transaktioner, som kan hente data fra forskellige transaktionstabeller:</span><span class="sxs-lookup"><span data-stu-id="77411-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="77411-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="77411-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="77411-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="77411-145">I disse **Datahentning**-aktiviteter kopieres data fra databasen til `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="77411-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="77411-146">Da alle disse aktiviteter udvider den samme abstrakte skabelonklasse, har de almindelige metoder.</span><span class="sxs-lookup"><span data-stu-id="77411-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="77411-147">Aktiviteter for beregningstjeneste</span><span class="sxs-lookup"><span data-stu-id="77411-147">Calculation Service activities</span></span>

<span data-ttu-id="77411-148">Aktiviteten **Beregningstjeneste** er linket mellem momstjenesten og momsintegrationen.</span><span class="sxs-lookup"><span data-stu-id="77411-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="77411-149">Denne aktivitet er ansvarlig for følgende funktioner:</span><span class="sxs-lookup"><span data-stu-id="77411-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="77411-150">Konstruere anmodningen.</span><span class="sxs-lookup"><span data-stu-id="77411-150">Construct the request.</span></span>
2. <span data-ttu-id="77411-151">Bogføre anmodningen til momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="77411-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="77411-152">Få svaret fra momstjenesten.</span><span class="sxs-lookup"><span data-stu-id="77411-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="77411-153">Analysere svaret.</span><span class="sxs-lookup"><span data-stu-id="77411-153">Parse the response.</span></span>

<span data-ttu-id="77411-154">Et datafelt, du føjer til anmodningen, bogføres sammen med andre metadata.</span><span class="sxs-lookup"><span data-stu-id="77411-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="77411-155">Implementering af udvidelse</span><span class="sxs-lookup"><span data-stu-id="77411-155">Extension implementation</span></span>

<span data-ttu-id="77411-156">Dette afsnit indeholder detaljerede trin, der forklarer, hvordan du implementerer udvidelsen.</span><span class="sxs-lookup"><span data-stu-id="77411-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="77411-157">Til dette formål bruges **Bærer** og **Projekt** som eksempler på de økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="77411-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="77411-158">Trin 1.</span><span class="sxs-lookup"><span data-stu-id="77411-158">Step 1.</span></span> <span data-ttu-id="77411-159">Tilføje datavariablen i objektklassen</span><span class="sxs-lookup"><span data-stu-id="77411-159">Add the data variable in the object class</span></span>

<span data-ttu-id="77411-160">Objektklassen indeholder datavariablen og henter/sætter-metoderne for dataene.</span><span class="sxs-lookup"><span data-stu-id="77411-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="77411-161">Føj datafeltet til enten `TaxIntegrationDocumentObject` eller `TaxIntegrationLineObject` afhængigt af feltets niveau.</span><span class="sxs-lookup"><span data-stu-id="77411-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="77411-162">I følgende eksempel bruges linjeniveauet, og filnavnet er `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="77411-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="77411-163">Hvis det datafelt, du tilføjer, er på dokumentniveau, skal du ændre filnavnet til `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="77411-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="77411-164">**Bærer** og **Projekt** tilføjes som private variabler.</span><span class="sxs-lookup"><span data-stu-id="77411-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="77411-165">Opret henter- og sættermetoder for disse datafelter for at manipulere dataene.</span><span class="sxs-lookup"><span data-stu-id="77411-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="77411-166">Trin 2.</span><span class="sxs-lookup"><span data-stu-id="77411-166">Step 2.</span></span> <span data-ttu-id="77411-167">Hente data fra databasen</span><span class="sxs-lookup"><span data-stu-id="77411-167">Retrieve data from the database</span></span>

<span data-ttu-id="77411-168">Angiv transaktionen, og udvid de relevante adapterklasser for at hente dataene.</span><span class="sxs-lookup"><span data-stu-id="77411-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="77411-169">Hvis du f.eks. bruger transaktionen **Indkøbsordre**, skal du udvide `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="77411-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="77411-170">`TaxIntegrationPurchParmTableDataRetrieval` er nedarvet fra `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="77411-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="77411-171">Den må ikke ændres, medmindre logikken i `purchTable`- og `purchParmTable`-tabellerne er forskellig.</span><span class="sxs-lookup"><span data-stu-id="77411-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="77411-172">Hvis datafeltet skal tilføjes for alle transaktioner, skal du udvide alle `DataRetrieval`-klasser.</span><span class="sxs-lookup"><span data-stu-id="77411-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="77411-173">Da alle aktiviteter for **Datahentning** udvider den samme skabelonklasse, er klassestrukturerne, variablerne og metoderne ens.</span><span class="sxs-lookup"><span data-stu-id="77411-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="77411-174">I følgende eksempel vises den grundlæggende struktur, når tabellen `PurchTable` bruges.</span><span class="sxs-lookup"><span data-stu-id="77411-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="77411-175">Når metoden `CopyToDocument` kaldes, findes `this.purchTable`-bufferen allerede.</span><span class="sxs-lookup"><span data-stu-id="77411-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="77411-176">Formålet med denne metode er at kopiere alle de påkrævede data fra `this.purchTable` til objektet `document` ved hjælp af den sættermetode, der blev oprettet i `DocumentObject`-klassen.</span><span class="sxs-lookup"><span data-stu-id="77411-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="77411-177">På samme måde findes der allerede en `this.purchLine`-buffer i `CopyToLine`-metoden.</span><span class="sxs-lookup"><span data-stu-id="77411-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="77411-178">Formålet med denne metode er at kopiere alle de påkrævede data fra `this.purchLine` til objektet `_line` ved hjælp af den sættermetode, der blev oprettet i `LineObject`-klassen.</span><span class="sxs-lookup"><span data-stu-id="77411-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="77411-179">Den mest ligetil fremgangsmåde er at udvide metoderne `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="77411-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="77411-180">Det anbefales dog, at du prøver metoderne `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable` først.</span><span class="sxs-lookup"><span data-stu-id="77411-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="77411-181">Hvis de ikke virker efter behov, skal du implementere din egen metode og kalde den i `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="77411-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="77411-182">Der er tre almindelige situationer, hvor du kan bruge denne metode:</span><span class="sxs-lookup"><span data-stu-id="77411-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="77411-183">Det påkrævede felt er i `PurchTable` eller `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="77411-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="77411-184">I denne situation kan du udvide `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="77411-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="77411-185">Her er eksempelkoden.</span><span class="sxs-lookup"><span data-stu-id="77411-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="77411-186">De påkrævede data findes ikke i standardtabellen for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="77411-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="77411-187">Der findes dog visse join-relationer til standardtabellen, og feltet skal udfyldes på de fleste linjer.</span><span class="sxs-lookup"><span data-stu-id="77411-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="77411-188">I denne situation skal du erstatte `getDocumentQueryObject` eller `getLineObject` for at forespørge på tabellen ved hjælp af en join-relation.</span><span class="sxs-lookup"><span data-stu-id="77411-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="77411-189">I følgende eksempel er feltet **Levér nu** integreret med salgsordren på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="77411-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="77411-190">I dette eksempel erklæres en `mcrSalesLineDropShipment`-buffer, og forespørgslen defineres i `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="77411-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="77411-191">Forespørgslen bruger relationen `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="77411-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="77411-192">Når du udvider i denne situation, kan du erstatte `getLineQueryObject` med dit eget konstruerede forespørgselsobjekt.</span><span class="sxs-lookup"><span data-stu-id="77411-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="77411-193">Men bemærk følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="77411-193">However, note the following points:</span></span>

    * <span data-ttu-id="77411-194">Da returværdien af metoden `getLineQueryObject` er `SysDaQueryObject`, skal du opbygge dette objekt ved hjælp af metoden SysDa.</span><span class="sxs-lookup"><span data-stu-id="77411-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="77411-195">Den eksisterende tabel kan ikke fjernes.</span><span class="sxs-lookup"><span data-stu-id="77411-195">Can't remove existed table.</span></span>

- <span data-ttu-id="77411-196">De påkrævede data er relateret til transaktionstabellen af en kompliceret join-relation, eller relationen er ikke en til en (1:1), men en til mange (1:N).</span><span class="sxs-lookup"><span data-stu-id="77411-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="77411-197">I denne situation bliver det lidt kompliceret.</span><span class="sxs-lookup"><span data-stu-id="77411-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="77411-198">Denne situation gælder for eksemplet med økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="77411-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="77411-199">I denne situation kan du implementere din egen metode for at hente dataene.</span><span class="sxs-lookup"><span data-stu-id="77411-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="77411-200">Her er eksempelkoden i `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`-filen.</span><span class="sxs-lookup"><span data-stu-id="77411-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="77411-201">Trin 3.</span><span class="sxs-lookup"><span data-stu-id="77411-201">Step 3.</span></span> <span data-ttu-id="77411-202">Føje data til anmodningen</span><span class="sxs-lookup"><span data-stu-id="77411-202">Add data to the request</span></span>

<span data-ttu-id="77411-203">Udvid metoden `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` eller `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` for at føje data til anmodningen.</span><span class="sxs-lookup"><span data-stu-id="77411-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="77411-204">Her er eksempelkoden i `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`-filen.</span><span class="sxs-lookup"><span data-stu-id="77411-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

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

<span data-ttu-id="77411-205">I denne kode er `_destination` det ombryderobjekt, der bruges til at generere bogføringsanmodningen, og `_source` er `TaxIntegrationLineObject`-objektet.</span><span class="sxs-lookup"><span data-stu-id="77411-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="77411-206">Definer den nøgle, der bruges i anmodningsformularen, som `private const str`.</span><span class="sxs-lookup"><span data-stu-id="77411-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="77411-207">Angiv feltet i metoden `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` ved hjælp af `SetField`-metoden.</span><span class="sxs-lookup"><span data-stu-id="77411-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="77411-208">Datatypen for den anden parameter skal være `string`.</span><span class="sxs-lookup"><span data-stu-id="77411-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="77411-209">Hvis datatypen ikke er `string`, skal du konvertere den til `string`.</span><span class="sxs-lookup"><span data-stu-id="77411-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="77411-210">Appendiks</span><span class="sxs-lookup"><span data-stu-id="77411-210">Appendix</span></span>

<span data-ttu-id="77411-211">Dette appendiks viser den komplette eksempelkode til integration af økonomiske dimensioner (**Bærer** og **Projekt**) på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="77411-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="77411-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="77411-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="77411-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="77411-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="77411-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="77411-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

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
