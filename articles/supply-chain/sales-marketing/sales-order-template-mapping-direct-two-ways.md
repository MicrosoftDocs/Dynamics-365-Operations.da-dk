---
title: Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at køre synkronisering af salgsordrer direkte mellem Dynamics 365 Sales og Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: eb41a21395a5d115b779e6b1ef71e9eb1176e28e
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061512"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management

[!include [banner](../includes/banner.md)]



I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at køre synkronisering af salgsordrer direkte mellem Dynamics 365 Sales og Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.

[![Dataflow i kundeemne til kontant.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

For at få adgang til de tilgængelige skabeloner skal du åbne [Power Apps Administration](https://preview.admin.powerapps.com/dataintegration). Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at køre synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management.

- **Navne på skabeloner i dataintegration:** 

    - Salgsordrer (Sales til Supply Chain Management) - Direkte
    - Salgsordrer (Supply Chain Management til Sales) - Direkte

- **Navne på opgaverne i dataintegrationsprojektet:**

    - OrderHeader
    - OrderLine

Følgende synkroniseringsopgaver kræves, før salgsfakturahoveder og -linjer kan synkroniseres:

- Produkter (Supply Chain Management til Sales) - Direkte
- Konti (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)
- Kontakter til kunder (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)

## <a name="entity-set"></a>Enhedssæt

| Supply Chain Management  | Sales             |
|-------------------------|-------------------|
| Dataverse-salgsordrehoveder | SalesOrders       |
| Dataverse-salgsordrelinjer   | SalesOrderDetails |

## <a name="entity-flow"></a>Enhedsflow

Salgsordrer oprettes i Sales og synkroniseres med Supply Chain Management, når **Kør projekt** udløses for et projekt baseret på skabelonen **Salgsordrer (Sales til Supply Chain Management) - Direkte**. Du kan kun aktivere og synkronisere ordrer fra Sales, hvis alle **Produktbestillinger** består af varer, der vedligeholdes eksternt. Derfor kan der ikke være nogen produkter, der skal rekvireres. Når ordren er aktiveret, bliver salgsordren skrivebeskyttet i brugergrænsefladen (UI). På dette tidspunkt foretages opdateringerne fra Supply Chain Management. Når salgsordren har status af **Bekræftet**, så kan et projekt, der er baseret på skabelonen **Salgsordrer (Supply Chain Management til Sales) – Direkte**, bruges til at synkronisere opdateringer eller ordreopfyldelsesstatus fra Supply Chain Management til Sales.

Du behøver ikke at oprette ordrer i Sales. Du kan oprette nye salgsordrer i Supply Chain Management i stedet for. Når en salgsordre har status **Bekræftet**, synkroniseres den til Sales som beskrevet i forrige afsnit.

I Supply Chain Management er filtre i skabelonen med til at sikre, at kun de relevante salgsordrer medtages i synkroniseringen:

- På salgsordren skal både bestillings- og faktureringskunden stamme fra Sales for at blive inkluderet i synkroniseringen. I Supply Chain Management bruges kolonnerne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at filtrere salgsordrer fra datatabellerne.
- Salgsordren i Supply Chain Management skal bekræftes. Det er kun de bekræftede salgsordrer eller salgsordrer, der har en højere behandlingsstatus, f.eks. status som **Leveret** eller **Faktureret**, der synkroniseres til Sales.
- Når en salgsordre oprettes eller redigeres, skal batchkørslen **Beregn salgstotaler** i Supply Chain Management udføres. Kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales.

## <a name="freight-tax"></a>Moms af fragt

Sales understøtter ikke moms på overskriftsniveau, da momsen er gemt på linjeniveauet. For at understøtte moms på overskriftsniveau fra Supply Chain Management, f.eks. moms på fragt, synkroniserer systemet moms til Sales som et produkt, der skal rekvireres, med navnet **Moms af fragt**, som har momsbeløbet fra Supply Chain Management. På denne måde kan den almindelige prisberegning i Sales bruges til totaler, selv når der er moms på overskriftsniveau fra Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Beregning og afrunding af rabat

Rabatberegningsmodellen i Sales adskiller sig fra rabatberegningsmodellen i Supply Chain Management. I Supply Chain Management kan det endelige rabatbeløb på en salgslinje være resultatet af en kombination af rabatbeløb og rabatprocenter. Hvis dette endelige rabatbeløb divideres med antallet på linjen, kan afrunding forekomme. Men denne afrunding tages ikke i betragtning, hvis et afrundet rabatbeløb pr. enhed synkroniseres med Sales. For at sikre at det fulde rabatbeløb fra en salgslinje i Supply Chain Management synkroniseres korrekt til Sales, skal det fulde beløb synkroniseres uden at blive divideret med linjeantallet. Derfor skal du definere **rabatberegningsmetoden** som **linjeelement** i Sales.

Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, bruges hele linjerabatbeløbet. Da Supply Chain Management ikke har noget felt, der kan gemme det fulde rabatbeløb for en linje, divideres beløbet med antallet og gemmes i feltet **Linjerabat**. En eventuel afrunding, der opstår i denne division, gemmes i felter **Salgsgebyrer** på salgslinjen.

### <a name="example"></a>Eksempel

**Synkronisering fra Sales til Supply Chain Management**

- **Sales:** Antal = 3, pr. linje-rabat = $10,00
- **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr =-$0,01 

**Synkronisering fra Supply Chain Management til Sales**

- **Supply Chain Management:** antal = 3, linjerabatbeløb = $3,33, salgsgebyr =-$0,01
- **Sales:** Antal = 3, pr. linje-rabat = (3 × $3,33) + $0,01 = $10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Nye kolonner er føjet til tabellen **Ordre** og vises på siden:

- **Vedligeholdes eksternt** - Angiv denne indstilling til **Ja**, når ordren kommer fra Supply Chain Management.
- **Behandlingsstatus** – Denne kolonne viser behandlingsstatussen for ordren i Supply Chain Management. Følgende værdier er tilgængelige:

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

Indstillingen **Har kun eksternt vedligeholdte produkter** bruges under ordreaktiveringen for konsekvent at spore, om en salgsordre udelukkende består af eksternt vedligeholdte produkter. Hvis en salgsordre kun består af eksternt vedligeholdte produkter, vedligeholdes produkterne i Supply Chain Management. Denne indstilling er med til at sikre, at du ikke aktiverer og forsøger at synkronisere salgsordrelinjer, der har produkter, som er ukendte i Supply Chain Management.

Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Supply Chain Management og synkroniseres til Sales. Disse ordrer kan ikke redigeres, fordi salgsordreoplysninger synkroniseres fra Supply Chain Management efter aktiveringen.

Salgsordrestatus forbliver **Aktiv** for at sikre, at ændringer fra Supply Chain Management kan flyde til salgsordren i Sales. For at styre denne funktion, skal standardværdien for **Statecode \[[Status]\]** angives til **Aktiv** i dataintegrationsprojektet.

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før du synkroniserer salgsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet. Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang. Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.

    Gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Teams**, vælg det relevante team, vælg **Administrer roller**, og vælg en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.

- For at sikre korrekt beregning af rabatter i både Sales og Supply Chain Management skal **Rabatberegningsmetode** indstilles til **Linjeelement**.
- Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:

    - Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
    - Kolonnen **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="setup-in-supply-chain-management"></a>Opsætning i Supply Chain Management

- Gå til **Salg og marketing** &gt; **Periodiske opgaver** &gt; **Beregn salgstotaler**, og Indstil jobbet til at køre som et batchjob. Angiv indstillingen **Beregn totaler for salgsordrer** til **Ja**. Dette trin er vigtigt, fordi kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales. Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.

Hvis du også bruger arbejdsordreintegration, skal du konfigurere salgets oprindelse. Salgsoprindelsen bruges til at skelne salgsordrer i Supply Chain Management, der er oprettet ud fra arbejdsordrer i Field Service. Når en salgsordre har en salgsoprindelse af typen **Arbejdsordreintegration**, vises feltet **Status for ordre på eksternt arbejde** i salgsordrehovedet. Desuden sikrer salgsoprindelsen, at salgsordrer, der er oprettet ud fra arbejdsordrer i Field Service, filtreres fra under synkronisering af salgsordrer fra Supply Chain Management til Field Service.

1. Gå til **Salg og marketing** \> **Opsætning** \> **Salgsordrer** \> **Salgsoprindelse**.
2. Vælg **Ny** for at oprette en ny salgsoprindelse.
3. I kolonnen **Salgsoprindelse** skal du angive et navn til salgsoprindelsen, f.eks. **Salgsordre**.
4. Angiv en beskrivelse i kolonnen **Beskrivelse** som f.eks. **Salgsordre fra Sales**.
5. Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.
6. Angiv kolonnen **Salgsoprindelsestype** til **Salgsordreintegration**.
7. Vælg **Gem**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Opsætning i salgsordrer (Sales til Supply Chain Management) – Direkte dataintegrationsprojekt

- Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**. Du kan gør tom til en standardværdi i værditilknytningen for at undgå at skulle skrive landet i nationale ordrer. Indstil den venstre side til 'Tom', og indstil den højre side til det ønskede land eller område.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor 'Tom' = DK.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Opsætning i salgsordrer (Supply Chain Management til Sales) – Direkte dataintegrationsprojekt

#### <a name="salesheader-task"></a>Opgaven SalesHeader

- Der kræves en prisliste for at kunne oprette ordrer i Sales. Opdater værditilknytningen for **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta. Du kan bruge standardprislisten til en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.

    Standardskabelonværdien for **pricelevelid.name \[prislistenavnet\]** er **CRM Service USA (eksempel)**.

#### <a name="salesline-task"></a>Opgaven SalesLine

- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Supply Chain Management.
- Sørg for, at de krævede enheder er defineret i Sales.

    En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

> [!NOTE]
> Kolonnerne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse kolonner, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som tabellen synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.

> [!NOTE]
> Tilknytningen viser, hvilke kolonneoplysninger der synkroniseres fra Sales til Supply Chain Management, eller fra Supply Chain Management til Sales.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Salgsordrer (Supply Chain Management til Sales) - Direkte: OrderHeader

[![Skabelontilknytning i dataintegration, salgsordrer (Sales til Supply Chain Management) – Direkte: OrderHeader](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Salgsordrer (Supply Chain Management til Sales) - Direkte: OrderLine

[![Skabelontilknytning i dataintegration, salgsordrer (Sales til Supply Chain Management) – Direkte: OrderLine](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Salgsordrer (Sales til Supply Chain Management) - Direkte: OrderHeader

[![Skabelontilknytning i dataintegration, salgsordrer (Sales til Supply Chain Management) – Direkte: OrderHeader](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Salgsordrer (Sales til Supply Chain Management) - Direkte: OrderLine

[![Skabelontilknytning i dataintegration, salgsordrer (Sales til Supply Chain Management) – Direkte: OrderLine](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]