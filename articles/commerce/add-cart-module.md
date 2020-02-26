---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025430"
---
# <a name="cart-module"></a>Indkøbsvognmodul


[!include [banner](includes/banner.md)]

Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et indkøbsvognmodul bruges til at få vist de varer, der er føjet til indkøbsvognen, før kunden fortsætter med at betale. Det omfatter f.eks. alle de varer, der er føjet til indkøbsvognen og en ordreoversigt. Det giver også kunden mulighed for at anvende eller fjerne kampagnekoder.

Indkøbsvognmodulet understøtter udtjekning og udlevering via gæst. Den understøtter også et **Tilbage til indkøb**-link. Du kan konfigurere ruten for dette link på **Indstillinger for webside \> Udvidelser \> Ruter**.

Indkøbsvognmodulet gengiver data på basis af indkøbsvogn-id'et. Indkøbsvogn-id'et er en browsercookie, der er tilgængelig på hele webstedet.

## <a name="cart-module-properties-and-slots"></a>Egenskaber og pladser i indkøbsvognmodulet

Indkøbsvognmodulet har en **Overskrift**-egenskab, der kan angives til værdier som f.eks. **Indkøbspose** og **Varer i indkøbsvognen**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler, der kan bruges i et indkøbsvognmodul

- **Tekstblok** – Dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet. Meddelelserne styres af CMS (Content Management system). Der kan tilføjes en hvilken som helst besked f.eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med din ordre".
- **Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden. Modulet Butiksvælger er integreret med Bing Maps Geocoding-API'en (Application Programming Interface) til at konvertere det sted, som kunden indtastede, til en bredde- og en længdegrad. Der kræves en Bing Maps-API-nøgle, og den skal føjes til den delte Retail-parameterside i Dynamics 365 Retail. Dette modul understøtter to egenskaber **Søgeradius** og **Link til vilkår for tjeneste**. Egenskaben **Søgeradius** definerer søgeradiussen for butikker, i miles. Hvis der ikke er angivet en værdi, bruges standardradiussen, som er 50 miles. Hvis Bing Maps eller en ekstern tjeneste bruges, kan egenskaben for **Link til vilkår for tjeneste** bruges til at angive et link til servicebetingelserne. Tjenesten Bing Maps kræver et link til et serviceprogram. 

## <a name="cart-module-settings"></a>Indstillinger for indkøbsvognmodul

Indkøbsvognmoduler har følgende indstillinger, der kan konfigureres på **Indstillinger for websted \> Udvidelser**:

- **Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager. Denne lagerkontrol udføres både for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken. Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.
- **Lagerbuffer** – Denne egenskab bruges til at angive et buffernummer til lageret. Lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling. Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager. Når salg sker hurtigt via flere kanaler, og lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.
- **Tilbage til indkøb** – Denne egenskab bruges til at angive ruten for linket **Tilbage til indkøb**. Denne rute kan konfigureres på webstedsniveau. Detailhandlere kan bruge denne konfiguration til at føre kunden tilbage til startsiden eller en anden side på webstedet.

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Indkøbsvognmodulet henter produktoplysninger vha. Commerce Scale Unit-API'er. Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Føje et indkøbsvognmodul til en side

Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret et fragment med navnet **Indkøbsvognfragment**, og føj et indkøbsvognmodul til det.
1. Føj en overskrift til indkøbsvognmodulet.
1. Føj et butiksvælgermodul til indkøbsvognmodulet.
1. Gem fragmentet, afslut redigeringen, og udgiv den.
1. Opret en skabelon med navnet **Indkøbsvognskabelon**, og føj det indkøbsvognfragment, som du netop har oprettet, til det.
1. Gem skabelonen, afslut redigeringen, og udgiv den.
1. Opret en side, der bruger den nye skabelon.
1. Gem siden, og se en forhåndsvisning af den.
1. Afslut redigeringen af siden, og udgiv den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
