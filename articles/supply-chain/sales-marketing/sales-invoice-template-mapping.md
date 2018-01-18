---
title: Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgsfakturahoveder og -linjer fra Finance and Operations til Sales:

- **Navnet på skabelonen i dataintegration** 

     - Salgsfakturaer (Fin og Ops til Sales)

- **Navnene på opgaverne i dataintegrationsprojekt**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Synkroniseringsopgaver, der kræves før synkronisering af salgsfakturahoved og -linjer:
-   Produkter (Fin og Ops til Sales)
-   Konti (Sales til Fin og Ops) (hvis det bruges)
-   Kontakter (Sales til Fin og Ops) (hvis det bruges)
-   Salgsordrehoved og -linjer (Fin og Ops til Sales)

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations                               | Common Data Service              | Salg          |
|------------------------------------------------------|------------------|----------------|
| Eksternt vedligeholdte kundesalgsfakturahoveder | SalesInvoice     | Fakturaer       |
| Eksternt vedligeholdte kundesalgsfakturalinjer   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Enhedsflow

Salgsfakturaer oprettes i Finance and Operations og synkroniseres til Sales.

> [!NOTE]
> Moms vedrørende gebyrer på **salgsfakturahovedet** indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales. Det skyldes, at Sales ikke understøtter momsoplysninger på hovedniveau. Moms, der er relateret til gebyrer på linjeniveau er inkluderet.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

-  Et **Fakturanummerfelt** er føjet til enheden **Faktura** og vises på siden.
 
-  Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Finance and Operations.
 
-  Feltet **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Finance and Operations er blevet synkroniseret til Sales. Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen. Det giver ejeren af salgsordren mulighed for at få vist fakturaen.
 
## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsfakturaer, er det vigtigt at opdatere systemerne med følgende indstilling:

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Brug systemets prisberegningssystem** er angivet til **Ja**. 

- Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Rabatberegningsmetode** er angivet til **Linjeelement**. 

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="salesinvoiceheader-task"></a>Opgaven SalesInvoiceHeader

- Opdater tilknytningen til **CDS-organisations-id** i **Kilde** > **CDS**. 

    -  Standardskabelonværdien for **SalesOrder_Organization_OrganizationId** er ORG001.
    -  Standardskabelonværdien for **Account_Organization_OrganizationId** er ORG001.
    -  Standardskabelonværdien for **Organization_OrganizationId** er ORG001.

- Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS til InvoiceCountryRegionId** til **BillingAddress_Country**.

    -  Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.

- **Prisliste** er nødvendig for at kunne oprette fakturaer i Sales. Opdater **ValueMap** i **CDS** > **Destination for pricelevelid.name [prislistenavnet]** til den **Prisliste**, der bruges i Sales pr. valuta. Du kan enten bruge **standardprislisten** til hver enkelt valuta eller bruge **ValueMap**, hvis du har **prislister** i flere valutaer.

    -  Skabelonværdi for **pricelevelid.name [prislistenavnet]** er **ValueMap** baseret på **valuta**.
    -  USD: CRM-tjenesten USA (eksempel). 

#### <a name="salesinvoiceline-task"></a>Opgaven SalesInvoiceLine

- Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS til måleenhed**.

- Du skal sikre, at den påkrævede **ValueMap** for **SalesUnitSymbol** i Finance and Operations findes i **Kilde** > **CDS-tilknytning**. 
    
    - Skabelonværdi med **ValueMap** er defineret for **SalesUnitSymbol til Quantity_UOM**.
    
-  Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**. 

    -  Standardskabelonværdien for **SalesInvoicer_Organization_OrganizationId** er ORG001.
    -  Standardskabelonværdien for **Product_Organization_OrganizationId** er ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Skabelontilknytning i dataintegrator

> [!NOTE]
> **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Tilknytning af disse felter kræver angivelse af en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterede emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere konti fra Sales med debitorer i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales med kontakter eller debitorer i Finance and Operations](contacts-template-mapping.md)

[Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)


