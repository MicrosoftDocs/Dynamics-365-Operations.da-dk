---
title: Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations
description: I emnet beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0894f4728d3f1df21db130cd9e87d9881726e7fa
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743365"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Finance and Operations

[!include [banner](../includes/banner.md)]

I emnet beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.

[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Finance and Operations:

- **Navnet på skabelonen i dataintegration:** Sales Quotes (Sales to Fin and Ops) - Direct
- **Navne på opgaverne i dataintegrationsprojektet:**

    - QuoteHeader
    - QuoteLine

Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:

- Produkter (Fin and Ops til Sales) - Direkte
- Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)
- Kontakter til Debitorer (Sales til Fin and Ops) – Direkte (hvis det bruges)

## <a name="entity-set"></a>Enhedssæt

| Salg        | Finance and Operations     |
|--------------|----------------------------|
| Citater       | CDS-salgstilbudshoved |
| QuoteDetails | CDS-salgstilbudslinjer  |

## <a name="entity-flow"></a>Enhedsflow

Salgstilbud oprettes i Sales og synkroniseres til Finance and Operations.

Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:

- Alle tilbudsprodukter på salgstilbuddet vedligeholdes eksternt.
- Når du klikker på **Aktivér tilbud**, bliver salgstilbuddet aktivt.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet **Tilbud** for konsekvent at spore, om salgstilbuddet består udelukkende af eksternt vedligeholdte produkter. Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations. Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer, der har produkter, som er ukendte i Finance and Operations.

Alle tilbudsprodukter på salgstilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra salgstilbudshovedet. Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden **QuoteDetails**.

En rabat kan føjes til tilbudsproduktet og synkroniseres til Finance and Operations. Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Finance and Operations. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design vedligeholdes og håndteres felterne **Pris**, **Rabat**, **Gebyr** og **Moms** i Finance and Operations.

I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres for Finance and Operations:

- Skrivebeskyttede felter i salgstilbudshovedet: **Rabatprocent**, **Rabat** og **Fragtbeløb**
- Skrivebeskyttede felter på tilbudsprodukter: **Moms**

## <a name="preconditions-and-mapping-setup"></a>Betingelserne og tilknytningsopsætning

Før salgstilbud synkroniseres, er det vigtigt, at du opdaterer følgende indstillinger.

### <a name="setup-in-sales"></a>Konfiguration i Sales

- Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet. Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang. Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.

    Du kan angive tilladelser for teamet ved at gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Team** og vælge det relevante team. Vælg **Administrer roller**, og vælg derefter en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.

- Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:

    - Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.
    - Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.

### <a name="setup-in-the-data-integration-project"></a>Opsætning af dataintegrationsprojektet

#### <a name="quoteheader"></a>QuoteHeader

- Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**. I værditilknytningen kan du definere en standardværdi, der bruges, hvis værdien er tom. Du skal blot lade den venstre side være tom, og indstille den højre side til det ønskede land eller område. På denne måde behøver du ikke at skrive landet eller området for nationale ordrer.

    Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor en tom værdi svarer til værdien **DK**.

#### <a name="quoteline"></a>QuoteLine

- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.
- Sørg for, at de krævede enheder er defineret i Sales.

    En skabelonværdi, der har en værditilknytning, er defineret for **oumid.name** til **SalesUnitSymbol**.

- Valgfrit: Du kan tilføje følgende tilknytninger for at sikre, at salgstilbudslinjerne importeres til Finance and Operations, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:

    - **SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations. Der er ingen standardskabelonværdi for **SiteId**.
    - **WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations. Der er ingen standardskabelonværdi for **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

> [!NOTE]
> - Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.
> - Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)

