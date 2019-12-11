---
title: Indkøbsvognmodul
description: Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696755"
---
# <a name="cart-module"></a>Indkøbsvognmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler indkøbsvognmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Et indkøbsvognmodul er en container, der bruges som vært for alle de moduler, der kræves for at vise de varer, der findes i indkøbsvognen. Det omfatter f. eks. alle de varer, der er føjet til indkøbsvognen, ordreoversigten og kampagnekoderne.

Indkøbsvognmodulet gengiver data på basis af indkøbsvogn-id'et. Indkøbsvogn-id'et er en browsercookie, der er tilgængelig på hele webstedet.

## <a name="cart-module-properties-and-slots"></a>Egenskaber og pladser i indkøbsvognmodulet

I sin egenskab af container styrer et indkøbsvognmodul nogle grundlæggende egenskaber, f. eks. overskriften og bredden. Overskriften er normalt tekst som **Indkøbspose** **Din indkøbsvogn** eller **Varer i din indkøbsvogn**. Breddeindstillingen bestemmer, om modulerne i containeren skal passe til den pågældende container, eller om de må udfylde skærmen.

Indkøbsvognsiden er opdelt i flere områder: linjevarer i indkøbsvogn, ordreoversigt og betaling samt funktionen "find i butik". De enkelte områder er knyttet til en plads i indkøbsvognmodulet, og alle pladser accepterer et foruddefineret sæt moduler.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler, der kan bruges i et indkøbsvognmodul

- **Linjevarer i indkøbsvogn** – dette modul viser en oversigt over alle de varer, der er føjet til indkøbsvognen. Oplysningerne omfatter produkttitlen, valgte dimensioner, pris, antal og rabatter. Dette modul understøtter også handlinger som "fjern fra Indkøbsvogn" og "føj til ønskeliste". For hver linjevare er der mulighed for at afsende varen eller afhente den i butikken. Denne indstilling skal konfigureres separat i afhent i butik-modulet.
- **Ordreoversigt** – dette modul viser en ordreoversigt. Oplysningerne omfatter subtotalen, forsendelse, moms og besparelser. Der kan konfigureres en overskrift for dette modul.
- **Kampagnekode** – i dette modul kan kunden indløse kampagnekoder. En kampagnekode kan anvendes eller fjernes.
- **Betaling** – dette modul starter betalingshandlingen omdirigerer brugeren til betalingssiden. Der skal konfigureres tre links til dette modul:

    - **Betaling** – dette link tvinger kunderne til at logge på, hvis de ikke allerede er logget på.
    - **Gæstekasse** – dette link gør det muligt for anonyme kunder at afgive ordrer. Det vises kun, når kunderne ikke er logget på.
    - **Shop videre** – dette link gør det muligt for kunderne at gå til startsiden eller en anden side, så de kan fortsætte med at handle.

- **Indholdsrig blok** – dette modul understøtter brugerdefinerede meddelelser i indkøbsvognmodulet. Meddelelserne styres af CMS (Content Management system). Der kan tilføjes en hvilken som helst besked, f. eks. "Kontakt 1-800-Fabrikam, hvis der er problemer med ordren".
- **Afhent i butik** – dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Dette modul viser som standard butikker, der er inden for en radius på 80 km fra kundens placering. Søgeradius kan dog tilpasses i modulet. For hver butik udføres der en lagerkontrol, hvis funktionen til lagerkontrol er slået til, og der vises en relevant meddelelse om, hvorvidt varen er på lager eller ej.
- **Søg efter butik vha. Bing Maps** – dette modul kan bruges inde i afhent i butik-modulet. Her kan kunder søge efter butikker ved at angive et sted. Bing Maps-API'en (Application Programming Interface – brugergrænseflade til program) til geokodning bruges til at konvertere det sted, som kunden indtastede, til en bredde- og en længdegrad. Hvis dette modul ikke bruges, vises kun de butikker, der findes i nærheden af kundens aktuelle placering, og kunden kan ikke søge efter et andet sted.

## <a name="cart-module-settings"></a>Indstillinger for indkøbsvognmodul

Indkøbsvognmoduler har tre indstillinger, der kan konfigureres:

- **Maks. antal** – det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager. Denne lagerkontrol udføres både for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken. Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.
- **Lagerbuffer** – lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling. Derfor kan der defineres en buffer til lageret. Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager. Når salg sker hurtigt via flere kanaler, hvor lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.

## <a name="retail-server-interaction"></a>Interaktion med Retail Server

Indkøbsvognmodulet henter produktoplysninger ved hjælp af Retail Server-API'er. Indkøbs-id'et fra browsercookien bruges til at hente alle produktoplysningerne fra Retail Server.

## <a name="add-a-cart-module-to-a-page"></a>Føje et indkøbsvognmodul til en side

Hvis du vil føje et indkøbsvognmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret et fragment med navnet **indkøbsvognfragment**, og føj et indkøbsvognmodul til det.
1. Tilføj et linjevarer i indkøbsvogn-modul på pladsen **Linjevarer i indkøbsvogn** i indkøbsvognmodulet.
1. Tilføj et ordreoversigtsmodul på pladsen **Ordreoversigt**.
1. Tilføj et kampagnekodemodul på pladsen **Kampagnekode**.
1. Tilføj et betalingsmodul på pladsen **Betaling**.
1. Tilføj et afhent i butik-modul på pladsen **Søg i butik**.
1. Vælg pladsen **Søg efter butik** i afhent i butik-modulet, og tilføj et søg efter butik vha. Bing Maps-modul.
1. Tjek fragmentet ind, og publicer det.
1. Opret en skabelon med navnet **indkøbsvognskabelon**, og føj det indkøbsvognfragment, som du netop har oprettet, til det.
1. Gem skabelonen, tjek den ind, og publicer den.
1. Opret en side, der bruger den nye skabelon.
1. Gem siden, og se en forhåndsvisning af den.
1. Tjek siden ind, og publicer den.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Købefeltmodul](add-buy-box.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Overskriftsmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
