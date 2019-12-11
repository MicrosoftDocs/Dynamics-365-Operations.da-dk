---
title: Købefeltmodul
description: Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811135"
---
# <a name="buy-box-module"></a>Købefeltmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Termen *købefelt* refererer normalt til det område på en produktdetaljeside, der er "over folden", og som omfatter alle de vigtigste oplysninger, der kræves for at foretage et produktkøb. (et område, der er "over folden", er synligt med det samme, når siden indlæses, så brugerne ikke behøver at rulle ned for at se den).

Et købefeltmodul er en særlig container, der omfatter alle de moduler, som vises i købefeltområdet på en side med produktdetaljer.

URL-adressen for siden produktdetaljer indeholder produkt-id'et. Alle de oplysninger, der kræves for at gengive et købefeltmodul, er afledt af dette produkt-id. Hvis der ikke er angivet et produkt-ID, gengives købefeltmodulet ikke korrekt på en side. Derfor kan et købefeltmodul ikke bruges på en side, hvor der ikke er en produktkontekst (f. eks. en startside eller en marketingside).

## <a name="buy-box-module-properties-and-slots"></a>Egenskaber og pladser i købefeltmodulet 

I sin egenskab af container styrer et købefeltmodul nogle grundlæggende egenskaber, f. eks. bredden. Breddeindstillingen bestemmer, om modulerne i containeren skal passe til den pågældende container, eller om de må udfylde skærmen.

På siden med produktdetaljer er et købefelt opdelt i to områder: et medieområde til venstre og et indholdsområde til højre. Disse to områder repræsenteres af pladser i købefeltmodulet. Hver plads er forudkonfigureret til kun at acceptere bestemte moduler, der understøttes af pladsen. Pladsen **Medier** understøtter f. eks. kun mediegallerimodulet.

Forholdet mellem kolonnebredder for medieområdet og indholdsområdet er som standard 2:1. Kolonnebredderne kan dog tilsidesættes af temaet. Derudover er de to områder i mobilenheder stablet, så det ene område vises under det andet område.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler, der kan bruges i et købefeltmodul

- **Mediegalleri** – dette modul bruges til at vise billeder af et produkt på en side med produktdetaljer. Den kan understøtte fra ét til mange billeder. Det understøtter også miniaturebilleder. Miniaturebillederne kan arrangeres enten vandret (som en række under billedet) eller lodret (som en kolonne ved siden af billedet). Du kan føje mediegallerimodulet til pladsen **Medier** i købefeltmodulet. Det understøtter i øjeblikket kun billeder og videoer.
- **Produkttitel** – dette modul viser produkttitlen på en side med produktdetaljer. Som standard bruges overskriftskoden **H1**, men den kan ændres efter behov.
- **Produktanmeldelser** – dette modul viser et antal stjerner, der er baseret på kundernes anmeldelser af et produkt. Købefeltmodulet henter produktanmeldelserne for hvert produkt fra anmeldelsestjenesten.
- **Produktpris** – dette modul viser produktets pris. Prisen omfatter gennemstregning af priser og rabatter.
- **Produktbeskrivelse** – dette modul viser en beskrivelse af produktet.
- **Produktkonfiguration** – dette modul vises produktets størrelse, typografi og dimensioner. Dimensionsvælgerne kan stables lodret eller vises ved siden af hinanden. Når der er valgt en produktvariant, opdateres andre egenskaber i købefeltet (f. eks. produktbeskrivelsen og -billederne), så de afspejler variantoplysningerne.
- **Produktantal** – dette modul bruges til at konfigurere produktantallet. En indstilling begrænser det antal for et produkt eller en variant, der kan føjes til indkøbsvognen.
- **Føj til indkøbsvogn** – dette modul bruges til at udføre handlingen "føj til indkøbsvogn". Der kan kun føjes et produkt eller en variant til indkøbsvognen. Det vil sige, at et masterprodukt ikke kan føjes til indkøbsvognen. Modulet omfatter egenskaben **Naviger til indkøbsvogn**, som forfatteren af webstedet kan angive. Når denne egenskab er angivet til **Sand**, overføres brugeren til indkøbsvognsiden, hver gang handlingen "føj til indkøbsvogn" udløses. Når den er angivet til **Falsk**, kan kunden fortsætte med at søge på siden med produktdetaljer, efter at der er føjet varer til indkøbsvognen.
- **Føj til ønskelisten** – dette modul bruges til at føje en vare til kundens ønskeliste. Der kan kun føjes et produkt eller en variant til en ønskeliste. Desuden skal kunden være logget på webstedet. Modulet indeholder fejlhåndteringslogik for at sikre, at begge betingelser opfyldes.
- **Søg i butik** – dette modul udløser processen "køb online, hent i butik".
- **Afhent i butik** – dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Dette modul viser som standard butikker, der er inden for en radius på 80 km fra kundens placering. Søgeradius kan dog tilpasses i modulet. For hver butik udføres der en lagerkontrol, hvis funktionen til lagerkontrol er slået til, og der vises en relevant meddelelse om, hvorvidt varen er på lager eller ej.
- **Søg efter butik vha. Bing Maps** – dette modul kan bruges inde i afhent i butik-modulet. Her kan kunder søge efter butikker ved at angive et sted. Bing Maps-API'en (Application Programming Interface – brugergrænseflade til program) til geokodning bruges til at konvertere det angivne sted til en bredde- og en længdegrad. Hvis dette modul bruges, vises kun de butikker, der findes i nærheden af kundens aktuelle placering, og kunden kan ikke søge efter et andet sted.
- **Indholdsrig blok** – dette modul kan vise en meddelelse, som webstedets opretter eller forhandler vil vise i købefeltet, f. eks. "Kontakt 1-800-FABRIKAM", hvis der er problemer med ordren" eller "Gratis levering af ordrer over $100". Meddelelserne styres af CMS (Content Management system).

## <a name="buy-box-module-settings"></a>Indstillinger for købefeltmodul

Købefeltmoduler har tre indstillinger, der kan konfigureres:

- **Maks. antal** – det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager. Denne lagerkontrol udføres både for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken. Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.
- **Lagerbuffer** – lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling. Derfor kan der defineres en buffer til lageret. Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager. Når salg sker hurtigt via flere kanaler, hvor lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.

## <a name="retail-server-interaction"></a>Interaktion med Retail Server

Købefeltmodulet henter produktoplysninger ved hjælp af Retail Server-API'er. Produkt-id'et fra siden med produktdetaljer bruges til at hente alle oplysninger.

## <a name="add-a-buy-box-module-to-a-page"></a>Føje et købefeltmodul til en side

Hvis du vil føje et købefeltmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret et fragment med navnet **købefeltfragment**, og føj et købefeltmodul til det.
1. Tilføj et mediegallerimodul til pladsen **Medier** i købefeltmodulet.
1. Tilføj følgende moduler på pladsen **Indhold** i købefeltmodulet: produkttitel, produktanmeldelse, produktpris, produktbeskrivelse, produktkonfiguration, føj til indkøbsvogn, føj til ønskeliste, og søg i butik. Du kan flytte rundt på modulerne på pladsen **Indhold** for at opnå det ønskede layout.
1. Vælg søg i butik-modulet. Tilføj et afhent i butik-modul på pladsen inde i dette modul.
1. Tilføj et søg efter butik vha. Bing Maps-modul på pladsen i afhent i butik-modulet.
1. Tjek siden ind, og publicer den.
1. Opret en skabelon til en side med produktdetaljer, og navngiv den **PDP-skabelonen**.
1. Tilføj en standardside.
1. Tilføj et købefeltfragment på pladsen **Hoved** på standardsiden.
1. Gem skabelonen, tjek den ind, og publicer den.
1. Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **PDP-side**.
1. Tilføj et købefeltfragment på pladsen **Hoved** på den nye side.
1. Gem siden, og se en forhåndsvisning af den. Føj forespørgselsstrengparameteren **?productid=&lt;product id&gt;** til URL-adressen for eksempelsiden. På denne måde bruges produktkonteksten til at indlæse og gengive eksempelsiden.
1. Tjek siden ind, og publicer den. Der vises et købefelt på siden med produktdetaljer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Container](add-container-module.md)

[Indkøbsvognmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
