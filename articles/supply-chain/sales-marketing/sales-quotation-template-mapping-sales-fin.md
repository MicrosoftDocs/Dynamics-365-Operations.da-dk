---
title: Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: a39b6b5fff88a02b71d81fd870e8c92ab055bc4d257e14c9b84cac0deac2c5c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771317"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.

> [!NOTE]
> Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Dataflow i kundeemne til kontant

Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales. Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales. I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.

[![Dataflow i kundeemne til kontant.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management:

- **Navnet på skabelonen i dataintegration:** Salgstilbud (Sales til Supply Chain Management) - Direkte
- **Navne på opgaverne i dataintegrationsprojektet:**

    - QuoteHeader
    - QuoteLine

Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:

- Produkter (Supply Chain Management til Sales) - Direkte
- Konti (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)
- Kontakter til kunder (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)

## <a name="entity-set"></a>Enhedssæt

| Sales        | Supply Chain Management     |
|--------------|----------------------------|
| Citater       | Dataverse-salgstilbudshoved |
| QuoteDetails | Dataverse-salgstilbudslinjer  |

## <a name="entity-flow"></a>Enhedsflow

Salgstilbud oprettes i Sales og synkroniseres til Supply Chain Management.

Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:

- Alle tilbudsprodukter på salgstilbuddet vedligeholdes eksternt.
- Når du klikker på **Aktivér tilbud**, bliver salgstilbuddet aktivt.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemne til kontantløsning for Sales

Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet **Tilbud** for konsekvent at spore, om salgstilbuddet består udelukkende af eksternt vedligeholdte produkter. Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Supply Chain Management. Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer, der har produkter, som er ukendte i Supply Chain Management.

Alle tilbudsprodukter på salgstilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra salgstilbudshovedet. Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden **QuoteDetails**.

En rabat kan føjes til tilbudsproduktet og synkroniseres til Supply Chain Management. Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Supply Chain Management. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design vedligeholdes og håndteres felterne **Pris**, **Rabat**, **Gebyr** og **Moms** i Supply Chain Management.

I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres til Supply Chain Management:

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

- Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Supply Chain Management.
- Sørg for, at de krævede enheder er defineret i Sales.

    En skabelonværdi, der har en værditilknytning, er defineret for **oumid.name** til **SalesUnitSymbol**.

- Valgfrit: Du kan tilføje følgende tilknytninger for at sikre, at salgstilbudslinjerne importeres til Supply Chain Management, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:

    - **SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Supply Chain Management. Der er ingen standardskabelonværdi for **SiteId**.
    - **WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Supply Chain Management. Der er ingen standardskabelonværdi for **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Tilknytning af skabelon i dataintegrator

> [!NOTE]
> - Felterne **Rabat**, **Gebyrer** og **Moms** styres af en kompleks opsætning i Supply Chain Management. Denne opsætning understøtter ikke aktuelt integrationstilknytning. I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Supply Chain Management.
> - Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne. Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.

Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Tilknytning af skabelon i dataintegrator.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Tilknytning af skabelon i dataintegrator.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterede emner

[Kundeemne til kontanter](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]