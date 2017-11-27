---
title: Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgaver bruges til at synkronisere salgsordrehoveder og -linjer fra Finance and Operations til Sales:

- **Navnet på skabelonen i dataintegration:** Salgsordrer Orders (Fin and Ops til Sales) – Direkte
- **Navne på opgaverne i dataintegrationsprojektet:**

    - OrderHeader
    - OrderLine

Følgende synkroniseringsopgaver kræves, før salgsfakturahoveder og -linjer kan synkroniseres:

- Produkter (Fin and Ops til Sales) - Direkte
- Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)
- Kontakter til Debitorer (Sales til Fin and Ops) – Direkte (hvis det bruges)

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations  | Salg             |
|-------------------------|-------------------|
| CDS-salgsordrehoveder | SalesOrders       |
| CDS-salgsordrelinjer   | SalesOrderDetails |

## <a name="entity-flow"></a>Enhedsflow

Salgsordrer oprettes i Finance and Operations og synkroniseres til Sales.

Filtre i skabelonen hjælper med til at sikre, at kun relevante salgsordrer medtages i synkroniseringen:

- På salgsordren medtages både bestillings- og faktureringskunden, der stammer fra Sales, i synkroniseringen. I Finance and Operations bruges felterne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at spore synkroniseringen i dataenheder.
- Salgsordren i Finance and Operations skal bekræftes. Det er kun de bekræftede salgsordrer eller salgsordrer, der har en højere behandlingsstatus, f.eks. status som **Leveret** eller **Faktureret**, der synkroniseres til Sales.
- Når en salgsordre oprettes eller redigeres, skal batchkørslen **Beregn salgstotaler** i Finance and Operations udføres. Kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales.

> [!NOTE]
> Moms vedrørende gebyrer på salgsordrehovedet indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales. Sales understøtter ikke momsoplysninger på hovedniveau. Men moms, som er relateret til gebyrer på linjeniveau, er imidlertid inkluderet i synkroniseringen.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Nye felter er føjet til enheden **Ordre** og vises på siden:

- **Vedligeholdes eksternt** - Angiv denne indstilling til **Ja**, når ordren kommer fra Finance and Operations.
- **Behandlingsstatus** – Dette felt viser behandlingsstatussen for ordren i Finance and Operations. Følgende værdier er tilgængelige:

    - Aktive
    - Bekræftet
    - Følgeseddel
    - Er faktureret
    - Plukket
    - Delvist plukket
    - Delvist pakket
    - Afsendt
    - Delvist afsendt
    - Delvist faktureret
    - Annulleret

Indstillingen **Har kun eksternt vedligeholdte produkter** bruges i andre salgsordrescenarier (f.eks. ved synkronisering fra Sales til Finance and Operations) til konsekvent at holde styr på, om salgsordren består udelukkende af eksternt vedligeholdte produkter. Hvis en salgsordre kun består af eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations. Denne indstilling er med til at sikre, at du ikke forsøger at synkronisere salgsordrelinjer, der har produkter, som er ukendte i Finance and Operations.

Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales. Ordresiden kan ikke redigeres, fordi salgsordreoplysninger synkroniseres fra Finance and Operations efter aktiveringen.

Status for en salgsordre forbliver **Aktiv** for at sikre, at ændringer fra Finance and Operations kan flyde til salgsordren i Sales. For at styre denne funktion, skal standardværdien for **Statecode \[[Status]\]** angives til **Aktiv** i dataintegrationsprojektet.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet. Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang. Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.

    Gå til **Indstillinger** > **Sikkerhed** > **Teams**, vælg det relevante team, vælg **Administrer roller**, og vælg en rolle med de ønskede tilladelser, f.eks. **systemadministrator**.

- Gå til **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, og sørg for, at der bruges til følgende indstillinger:

    - Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
    - Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="setup-in-finance-and-operations"></a>Konfiguration i Finance and Operations

Gå til **Salg og marketing** > **Periodiske opgaver** > **Beregne Salgstotaler**, og Indstil jobbet til at køre som et batchjob. Angiv indstillingen **Beregn totaler for salgsordrer** til **Ja**. Dette trin er vigtigt, fordi kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales. Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="salesheader-task"></a>Opgaven SalesHeader

- Kontrollér, at den nødvendige tilknytning findes for **InvoiceCountryRegionId** til **BillingAddress\_Country** og for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.

- Der kræves en prisliste for at kunne oprette ordrer i Sales. Opdater værditilknytningen **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta. Du kan bruge standardprislisten til en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.

    Standardskabelonværdien for **pricelevelid.name \[prislistenavnet\]** er **CRM Service USA (eksempel)**.

#### <a name="salesline-task"></a>Opgaven SalesLine

- Du skal sikre, at den nødvendige tilknytning findes for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.

- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.

    En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **Quantity\_UOM**

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE]
> Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration. 

> [!NOTE]
> Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Skabelontilknytning i dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Skabelontilknytning i dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Finance and Operations med produkter i Sales](products-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)




