---
title: Købefeltmodul
description: Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154057"
---
# <a name="buy-box-module"></a>Købefeltmodul


[!include [banner](includes/banner.md)]

Dette emne omhandler købefeltmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Termen *købefelt* refererer normalt til det område på en produktdetaljeside, der er "over folden", og som omfatter alle de vigtigste oplysninger, der kræves for at foretage et produktkøb. (et område, der er "over folden", er synligt med det samme, når siden indlæses, så brugerne ikke behøver at rulle ned for at se den).

Et købefeltmodul er en særlig container, der omfatter alle de moduler, som vises i købefeltområdet på en side med produktdetaljer.

URL-adressen for siden produktdetaljer indeholder produkt-id'et. Alle de oplysninger, der kræves for at gengive et købefeltmodul, er afledt af dette produkt-id. Hvis der ikke er angivet et produkt-ID, gengives købefeltmodulet ikke korrekt på en side. Derfor kan et købsfeltmodul kun bruges på sider med en produktkontekst. Hvis du vil bruge den på en side, der ikke har en produktkontekst (f.eks. en startside eller en marketingside), skal du udføre flere tilpasninger.

## <a name="buy-box-module-properties-and-slots"></a>Egenskaber og pladser i købefeltmodulet 

På siden med produktdetaljer er et købefelt opdelt i to områder: et medieområde til venstre og et indholdsområde til højre. Forholdet mellem bredden af kolonnen med medieområder og bredden af kolonnen med indholdsområder er som standard 2:1. På mobile enheder er de to områder stablet, så det ene område vises under det andet område. Du kan bruge temaer til at tilpasse kolonnebredder og stablingsrangering.

I et købsfeltmodul vises titlen, beskrivelsen, prisen og klassifikationen for et produkt. Kunderne kan også vælge produktvarianter, der har forskellige produktattributter, f.eks. størrelse, typografi og farve. Når der er valgt en produktvariant, opdateres andre egenskaber i købefeltet (f. eks. produktbeskrivelsen og -billederne), så de afspejler variantoplysningerne. 

Der angives en mængdevælger, så debitorer kan angive antallet af varer, der skal købes. Det maksimale antal, der kan købes, kan defineres i indstillingerne for webstedet.
 
Fra købsfeltet kan kunderne også udføre handlinger, som f.eks. føje et produkt til indkøbsvognen, føje et produkt til ønskelisten og vælge et afhentningssted. Disse handlinger kan udføres på et produkt eller en produktvariant. Hvis du vil føje et produkt til en ønskeliste, skal kunden være logget på.

Temaer kan bruges til at fjerne eller ændre rækkefølgen af købsfeltets produktegenskaber og handlingskontroller. 

## <a name="module-properties"></a>Modulegenskaber

- **Overskriftskode** – Denne egenskab definerer overskriftskoden for produkttitlen. Hvis købsfeltet vises øverst på siden, skal denne egenskab indstilles til **h1** for at overholde tilgængelighedsstandarder. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler, der kan bruges i et købefeltmodul

- **Mediegalleri** – dette modul bruges til at vise billeder af et produkt på en side med produktdetaljer. Den kan understøtte fra ét til mange billeder. Det understøtter også miniaturebilleder. Miniaturebillederne kan arrangeres enten vandret (som en række under billedet) eller lodret (som en kolonne ved siden af billedet). Du kan føje mediegallerimodulet til pladsen **Medier** i købefeltmodulet. Det understøtter i øjeblikket kun billeder. 
- **Butiksvælger** – Dette modul viser en liste over butikker i nærheden, hvor en vare kan afhentes. Det giver brugerne mulighed for at angive en placering for butikker, der er i nærheden. Yderligere oplysninger om dette modul finder du i [Modulet Butiksvælger](store-selector.md).

## <a name="buy-box-module-settings"></a>Indstillinger for købefeltmodul

Købefeltmoduler har tre indstillinger, der kan konfigureres på **Indstillinger for websted \> Udvidelser**:

- **Maks. antal** – Denne egenskab bruges tl at angive det maksimale antal af hver vare, der kan føjes til indkøbsvognen. En detailhandler kan f. eks. beslutte, at der kun kan sælges 10 stk. af hvert produkt i en enkelt transaktion.
- **Lagerkontrol** – når værdien er angivet til **Sand**, føjes der først en vare til indkøbsvognen, når købefeltmodulet har sikret, at varen er på lager. Denne lagerkontrol udføres både for de scenarier, hvor varen skal afsendes, og for scenarier, hvor den afhentes i butikken. Hvis værdien er angivet til **Falsk**, udføres der ingen lagerkontrol, før der føjes en vare til indkøbsvognen, og ordren afgives.
- **Lagerbuffer** – Denne egenskab bruges til at angive et buffernummer til lageret. Lageret vedligeholdes i realtid, og når mange kunder afgiver ordrer, kan det være vanskeligt at bevare en nøjagtig lageroptælling. Når der foretages en lagerkontrol, og lageret er mindre end bufferantallet, behandles produktet, som om det ikke er på lager. Når salg sker hurtigt via flere kanaler, og lageroptællingen ikke er synkroniseret, er der derfor mindre risiko for, at der sælges en vare, som ikke er på lager.

## <a name="commerce-scale-unit-interaction"></a>Enhedsinteraktion i Commerce Scale

Købsfeltmodulet henter produktoplysninger ved hjælp af Commerce Scale Unit-API'er. Produkt-id'et fra siden med produktdetaljer bruges til at hente alle oplysninger.

## <a name="add-a-buy-box-module-to-a-page"></a>Føje et købefeltmodul til en side

Hvis du vil føje et købefeltmodul til en ny side og angive de påkrævede egenskaber, skal du følge disse trin.

1. Opret et fragment med navnet **købefeltfragment**, og føj et købefeltmodul til det.
1. Tilføj et mediegallerimodul til pladsen **Medier** i købefeltmodulet.
1. Tilføj et butiksvælgermodult i pladsen **Butiksvælger** af købsfeltmodulet.
1. Tjek siden ind, og publicer den.
1. Opret en skabelon til en side med produktdetaljer, og navngiv den **PDP-skabelonen**.
1. Tilføj en standardside.
1. Tilføj et købefeltfragment på pladsen **Hoved** på standardsiden.
1. Gem skabelonen, afslut redigeringen, og udgiv den.
1. Brug den skabelon, som du netop har oprettet, til at oprette en side med navnet **PDP-side**.
1. Tilføj et købefeltfragment på pladsen **Hoved** på den nye side.
1. Gem siden, og se en forhåndsvisning af den. Føj forespørgselsstrengparameteren **?productid=&lt;product id&gt;** til URL-adressen for eksempelsiden. På denne måde bruges produktkonteksten til at indlæse og gengive eksempelsiden.
1. Gem siden, afslut redigeringen, og udgiv den. Der vises et købefelt på siden med produktdetaljer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over startsæt](starter-kit-overview.md)

[Modulet Butiksvælger](store-selector.md)

[Container-modul](add-container-module.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Betalingsmodul](add-checkout-module.md)

[Ordrebekræftelsesmodul](order-confirmation-module.md)

[Sidehovedmodul](author-header-module.md)

[Sidefodsmodul](author-footer-module.md)
