---
title: Synkronisering af salgsordrer direkte mellem Sales og Finance and Operations
description: "Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at køre tovejssynkronisering af salgsordrehoveder og -linjer direkte mellem Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 568c33a63efdc58a179dadcb617634dcf533fd4b
ms.openlocfilehash: c31d65328250539fbe172f220272eec9d8b59bbf
ms.contentlocale: da-dk
ms.lasthandoff: 11/13/2017

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Synkronisering af salgsordrer direkte mellem Sales og Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at køre tovejssynkronisering af salgsordrehoveder og -linjer direkte mellem Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at køre tovejssynkronisering af salgsordrehoveder og -linjer direkte mellem Sales og Finance and Operations:

- **Navne på skabeloner i dataintegration:** 

    - Salgsordrer (Sales til Fin and Ops) – Direkte
    - Salgsordrer (Fin and Ops til Sales) – Direkte

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

Salgsordrer oprettes i Sales og synkroniseres med Finance and Operations, når **Kør projekt** udløses for et projekt baseret på skabelonen **Salgsordrer (Sales til Fin and Ops) - Direkte**. Du kan kun aktivere og synkronisere ordrer fra Sales, hvis alle **Produktbestillinger** består af varer, der vedligeholdes eksternt. Derfor kan der ikke være nogen produkter, der skal rekvireres. Når ordren er aktiveret, bliver salgsordren skrivebeskyttet i brugergrænsefladen (UI). På dette tidspunkt foretages opdateringerne fra Finance and Operations. Når salgsordren har status **Bekræftet**, så kan et projekt, der er baseret på skabelonen **Salgsordrer (Fin and Ops til Sales) – Direkte**, bruges til at synkronisere opdateringer eller ordreopfyldelsesstatus fra Finance and Operations til Sales.

Du behøver ikke at oprette ordrer i Sales. Du kan oprette nye salgsordrer i Finance and Operations i stedet for. Når en salgsordre har status **Bekræftet**, synkroniseres den til Sales som beskrevet i forrige afsnit.

I Finance and Operations hjælpe filtre i skabelonen med til at sikre, at kun de relevante salgsordrer medtages i synkroniseringen:

- På salgsordren skal både bestillings- og faktureringskunden stamme fra Sales for at blive inkluderet i synkroniseringen. I Finance and Operations bruges felterne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at filtrere salgsordrer fra dataenhederne.
- Salgsordren i Finance and Operations skal bekræftes. Det er kun de bekræftede salgsordrer eller salgsordrer, der har en højere behandlingsstatus, f.eks. status som **Leveret** eller **Faktureret**, der synkroniseres til Sales.
- Når en salgsordre oprettes eller redigeres, skal batchkørslen **Beregn salgstotaler** i Finance and Operations udføres. Kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales.

## <a name="freight-tax"></a>Moms af fragt

Sales understøtter ikke moms på overskriftsniveau, da momsen er gemt på linjeniveauet. For at understøtte moms på overskriftsniveau fra Finance and Operations, f.eks. moms på fragt, synkroniserer systemet moms til Sales som et produkt, der skal rekvireres, med navnet **Moms af fragt**, som har momsbeløbet fra Finance and Operations. På denne måde kan den almindelige prisberegning i Sales bruges til totaler, selv når der er moms på overskriftsniveau fra Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Beregning og afrunding af rabat

Rabatberegningsmodellen i Sales adskiller sig fra rabatberegningsmodellen i Finance and Operations. I Finance and Operations kan endelige rabatbeløbet på en salgslinje være resultatet af en kombination af rabatbeløb og rabatprocenter. Hvis dette endelige rabatbeløb divideres med antallet på linjen, kan afrunding forekomme. Men denne afrunding tages ikke i betragtning, hvis et afrundet rabatbeløb pr. enhed synkroniseres med Sales. For at sikre at det fulde rabatbeløb fra en salgslinje i Finance and Operations synkroniseres korrekt til Sales, skal det fulde beløb synkroniseres uden at blive divideret med linjeantallet. Derfor skal du definere **rabatberegningsmetoden** som **linjeelement** i Sales.

Når en salgsordrelinje synkroniseres fra Sales til Finance and Operations, bruges hele linjerabatbeløbet. Da Finance and Operations ikke har noget felt, der kan gemme det fulde rabatbeløb for en linje, divideres beløbet med antallet og gemmes i feltet **Linjerabat**. En eventuel afrunding, der opstår i denne division, gemmes i felter **Salgsgebyrer** på salgslinjen.

### <a name="example"></a>Eksempel

**Synkronisering fra Sales til Finance and Operations**

- **Sales:** Antal = 3, pr. linje-rabat = $10,00
- **Finance and Operations:** Antal = 3, linjerabatbeløb = $3,33, salgsgebyr =-$0,01 

**Synkronisering fra Finance and Operations til Sales**

- **Finance and Operations:** Antal = 3, linjerabatbeløb = $3,33, salgsgebyr =-$0,01
- **Sales:** Antal = 3, pr. linje-rabat = (3 × $3,33) + $0,01 = $10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Nye felter er føjet til enheden **Ordre** og vises på siden:

- **Vedligeholdes eksternt** - Angiv denne indstilling til **Ja**, når ordren kommer fra Finance and Operations.
- **Behandlingsstatus** – Dette felt viser behandlingsstatussen for ordren i Finance and Operations. Følgende værdier er tilgængelige:

    - **Kladde** – Den første status, når en ordre oprettes i Sales. I Sales kan kun ordrer med denne behandlingsstatus redigeres.
    - **Aktiv** – Status, når ordren er blevet aktiveret i Sales ved hjælp af knappen **Aktiver**.
    - **Bekræftet**
    - **Følgeseddel**
    - **Faktureret**
    - **Plukket**
    - **Delvist plukket**
    - **Delvist pakket**
    - **Afsendt**
    - **Delvist afsendt**
    - **Delvist faktureret**
    - **Annulleret**

Indstillingen **Har kun eksternt vedligeholdte produkter** bruges under ordreaktiveringen for konsekvent at spore, om en salgsordre udelukkende består af eksternt vedligeholdte produkter. Hvis en salgsordre kun består af eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations. Denne indstilling er med til at sikre, at du ikke aktiverer og forsøger at synkronisere salgsordrelinjer, der har produkter, som er ukendte i Finance and Operations.

Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales. Disse ordrer kan ikke redigeres, fordi salgsordreoplysninger synkroniseres fra Finance and Operations efter aktiveringen.

Salgsordrestatus forbliver **Aktiv** for at sikre, at ændringer fra Finance and Operations kan flyde til salgsordren i Sales. For at styre denne funktion, skal standardværdien for **Statecode \[[Status]\]** angives til **Aktiv** i dataintegrationsprojektet.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet. Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang. Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.

    Gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Teams**, vælg det relevante team, vælg **Administrer roller**, og vælg en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.

- Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:

    - Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
    - Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="setup-in-finance-and-operations"></a>Konfiguration i Finance and Operations

- Gå til **Salg og marketing** &gt; **Periodiske opgaver** &gt; **Beregn salgstotaler**, og Indstil jobbet til at køre som et batchjob. Angiv indstillingen **Beregn totaler for salgsordrer** til **Ja**. Dette trin er vigtigt, fordi kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales. Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Opsætning i salgsordrer (Sales til Fin and Ops) – Direkte dataintegrationsprojekt

- Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**. Du kan gør tom til en standardværdi i værditilknytningen for at undgå at skulle skrive landet i nationale ordrer. Indstil den venstre side til 'Tom', og indstil den højre side til det ønskede land eller område.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor 'Tom' = DK.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Opsætning i salgsordrer (Fin and Ops til Sales) – Direkte dataintegrationsprojekt

#### <a name="salesheader-task"></a>Opgaven SalesHeader

- Der kræves en prisliste for at kunne oprette ordrer i Sales. Opdater værditilknytningen for **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta. Du kan bruge standardprislisten til en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.

    Standardskabelonværdien for **pricelevelid.name \[prislistenavnet\]** er **CRM Service USA (eksempel)**.

#### <a name="salesline-task"></a>Opgaven SalesLine

- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.
- Sørg for, at de krævede enheder er defineret i Sales.

    En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE]
> Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.

> [!NOTE]
> Tilknytningen viser, hvilke feltoplysninger der synkroniseres fra Sales til Finance and Operations, eller fra Finance and Operations til Sales.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Salgsordrer (Fin and Ops til Sales) – Direkte: OrderHeader

[![Skabelontilknytning i dataintegration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Salgsordrer (Fin and Ops til Sales) – Direkte: OrderLine

[![Skabelontilknytning i dataintegration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Salgsordrer (Sales til Fin and Ops) – Direkte: OrderHeader

[![Skabelontilknytning i dataintegration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Salgsordrer (Sales til Fin and Ops) – Direkte: OrderLine

[![Skabelontilknytning i dataintegration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

