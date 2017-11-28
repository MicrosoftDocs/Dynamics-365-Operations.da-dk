---
title: Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgsordrehoveder og -linjer fra Finance and Operations til Sales:

- **Navnet på skabelonen i dataintegration** 

    - Salgsordrer (Fin and Ops til Sales)
    
- **Navnene på opgaverne i dataintegrationsprojekt**

    - OrderHeader
    - OrderLine

Synkroniseringsopgaver, der kræves før synkronisering af salgsfakturahoved og -linjer:

- Produkter (Fin og Ops til Sales)
- Konti (Sales til Fin og Ops) (hvis det bruges)
- Kontakter til Debitorer (Sales til Fin and Ops) (hvis det bruges)

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations |    Common Data Service         |     Salg      |
|------------------------|----------------|----------------|
| CDS-salgsordrehoveder| SalesOrder     | SalesOrders |
| CDS-salgsordrelinjer  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Enhedsflow

Salgsordrer oprettes i Finance and Operations og synkroniseres til Sales.

Filtre i skabelonen sikrer, at kun relevante salgsordrer medtages i synkroniseringen:

- Både bestillings- og faktureringskunden på salgsordren, der stammer fra Sales, medtages i synkroniseringen. I Finance and Operations bruges felterne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at spore synkroniseringen i dataenheder.

- **Salgsordren** i Finance and Operations skal bekræftes. Det er kun de bekræftede salgsordrer eller salgsordrer med højere behandlingsstatus, f.eks. status som leveret eller faktureret, der synkroniseres til Sales.

- Når du opretter eller redigerer en salgsordre, skal batchkørslen **Beregn salgstotaler** i Finance and Operations udføres. Kun salgsordrerne med beregnede salgstotaler synkroniseres med CDS og Sales.

> [!NOTE]
> Moms vedrørende gebyrer på **salgsordrehovedet** indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales. Det skyldes, at Sales ikke understøtter momsoplysninger på hovedniveau. Moms, der er relateret til gebyrer på linjeniveau er inkluderet.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Nye felter er føjet til enheden **Ordre** og vises på siden:

- **Vedligeholdes eksternt** - Angivet til **Ja** når ordren kommer fra Finance and Operations.

- **Behandlingsstatus** – Bruges til at vise behandlingsstatussen for ordren i Finance and Operations. Værdierne er:

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

Indstillingen **Har kun eksternt vedligeholdte produkter** bruges i andre salgsordrescenarier (ved synkronisering fra Sales to Finance and Operation) til konsekvent at holde styr på, om salgsordren består udelukkende af **eksternt vedligeholdte produkter**, hvorved produkter vedligeholdes i Finance and Operations. Dette sikrer, at du ikke forsøger at synkronisere salgsordrer med produkter, der er ukendte i Finance and Operations.
 
Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** knapperne på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales. Siden Ordre kan ikke redigeres, da salgsordreoplysninger synkroniseres fra Finance and Operations.
 
Feltet **Salgsordrestatus** forbliver aktivt for at sikre, at ændringer fra Finance and Operations kan flyde fra **salgsordren** i Sales. Dette styres ved at angive standarden for **Statecode [Status]** til **Aktiv** i dataintegrationsprojektet.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning 

Før du synkroniserer salgsordrer, er det vigtigt at opdatere systemerne med følgende indstilling:

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Sikre tilladelser for det team, som brugeren (fra **Forbindelsessæt** i Sales) er tilknyttet. Hvis du bruger demodata, har brugeren normalt administratoradgang, men ikke teamet. Uden dette får du en fejl, der angiver, at det primære team mangler, når du kører projektet fra dataintegrator. 

    - Under **Indstillinger** > **Sikkerhed** > **Team** skal du vælge det relevante team, klikke på **Administrer roller** og vælge en rolle med de ønskede tilladelser, f.eks. systemadministrator.

- Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Brug systemets prisberegningssystem** er angivet til **Ja**. 

- Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Rabatberegningsmetode** er angivet til **Linjeelement**. 

### <a name="setup-in-finance-and-operations"></a>Konfiguration i Finance and Operations

Angiv **Salg og marketing** > **Periodiske opgaver** > **Beregn salgstotaler** til at køre som et batchjob med **Beregn totaler for salgsordrer** angivet til **Ja**. Det er vigtigt, fordi kun salgsordrerne med beregnede salgstotaler synkroniseres med CDS og Sales. Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="salesheader-task"></a>Opgaven SalesHeader

- Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**.

    - Standardskabelonværdien for **Account_Organization_OrganizationId** er ORG001.
    - Standardskabelonværdien for **InvoiceAccount_Organization_OrganizationId** er ORG001.
    - Standardskabelonværdien for **Organization_OrganizationId** er ORG001.

- Kontrollér, at den nødvendige tilknytning findes i **Kilde** > **CDS til InvoiceCountryRegionId to BillingAddress_Country** og for **DeliveryCountryRegionId til DeliveryAddress_Country**.

    - Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.

- **Prisliste** er nødvendig for at kunne oprette ordrer i Sales. Opdater **ValueMap** i **CDS** > **Destination** for **pricelevelid.name [prislistenavnet]** til den **prisliste**, der bruges i Sales pr. valuta. Du kan enten bruge **standardprislisten** til hver enkelt valuta eller bruge **ValueMap**, hvis du har **prislister** i flere valutaer.
    
    - Standardskabelonværdien for **pricelevelid.name [prislistenavnet]** er CRM Service USA (eksempel). 

#### <a name="salesline-task"></a>Opgaven SalesLine

- Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**. 
    
    - Standardskabelonværdien for **SalesOrder_Organization_OrganizationId** er ORG001.
    - Standardskabelonværdien for **Product_Organization_OrganizationId** er ORG001.

- Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS** for **DeliveryCountryRegionId** til **DeliveryAddress_Country**.

    - Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.
    
- Du skal sikre, at den påkrævede **ValueMap** for **SalesUnitSymbol** i Finance and Operations findes i **Kilde** > **CDS-tilknytning**.

    - Skabelonværdi med **ValueMap** er defineret for **SalesUnitSymbol til Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

> [!NOTE]
> Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

### <a name="orderheader"></a>OrderHeader

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterede emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere konti fra Sales med debitorer i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales med kontakter eller debitorer i Finance and Operations](contacts-template-mapping.md)

[Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)


