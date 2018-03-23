---
title: Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 347509a9556f15e7d880508e36516f04bc6964b7
ms.contentlocale: da-dk
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere salgsfakturahoveder og -linjer fra Finance and Operations til Sales:

- **Navnet på skabelonen i dataintegration:** Salgsfakturaer (Fin and Ops til Sales) - Direkte
- **Navne på opgaverne i dataintegrationsprojektet:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Følgende synkroniseringsopgaver kræves, før salgsfakturahoveder og -linjer kan synkroniseres:

- Produkter (Fin and Ops til Sales) - Direkte
- Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)
- Kontakter (Sales til Fin and Ops) - Direkte (hvis den bruges)
- Salgsordrehoved og -linjer (Fin and Ops til Sales) - Direkte

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations                               | Salg          |
|------------------------------------------------------|----------------|
| Eksternt vedligeholdte kundesalgsfakturahoveder | Fakturaer       |
| Eksternt vedligeholdte kundesalgsfakturalinjer   | InvoiceDetails |

## <a name="entity-flow"></a>Enhedsflow

Salgsfakturaer oprettes i Finance and Operations og synkroniseres til Sales.

> [!NOTE]
> Moms vedrørende gebyrer på salgsfakturahovedet indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales. Sales understøtter ikke momsoplysninger på hovedniveau. Men moms, som er relateret til gebyrer på linjeniveau, er imidlertid inkluderet i synkroniseringen.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

- Feltet **Fakturanummer** er føjet til enheden **Faktura** og vises på siden.
- Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Finance and Operations.
- Værdien **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Finance and Operations er blevet synkroniseret til Sales. Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen. Ejeren af salgsordren kan derfor få vist fakturaen.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsfakturaer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-sales"></a>Konfiguration i Sales

Gå til **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, og sørg for, at der bruges til følgende indstillinger:

- Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
- Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="salesinvoiceheader-task"></a>Opgaven SalesInvoiceHeader

- Du skal sikre, at den nødvendige tilknytning findes for **InvoiceCountryRegionId** til **BillingAddress\_Country**.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.

- Der kræves en prisliste for at kunne oprette fakturaer i Sales. Opdater værditilknytningen **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta. Du kan bruge standardprislisten til en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.

    Skabelonværdien for **pricelevelid.name \[prislistenavnet\]** er en værditilknytning, der er baseret på valuta med USD = CRM Service USA (eksempel).  
    
#### <a name="salesinvoiceline-task"></a>Opgaven SalesInvoiceLine

- Du skal sikre, at den nødvendige tilknytning findes for **Måleenhed**.
- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.

    En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **Quantity\_UOM**

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE]
> Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Skabelontilknytning i dataintegration](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Skabelontilknytning i dataintegration](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere produkter fra Finance and Operations direkte med produkter i Sales](products-template-mapping-direct.md)

[Synkronisere kontakter fra Sales direkte med kontakter eller debitorer i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct-two-ways.md)







