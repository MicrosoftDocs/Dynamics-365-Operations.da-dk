---
title: "Arbejdsområde for disponibelt lager på mobilenheder i Microsoft Dynamics 365 for Operations-app"
description: "I arbejdsområdet for disponibelt lager på mobilenheder kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Arbejdsområde for disponibelt lager på mobilenheder i Microsoft Dynamics 365 for Operations-app

I arbejdsområdet for disponibelt lager på mobilenheder kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics 365 for Operations-mobilplatformen | [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og Microsoft Dynamics for Operations platformsopdatering 3 (november 2016) |
| Hotfix KB 3215650                                                    | Installer hotfixet, hvis du vil aktivere de arbejdsområder, der findes i din Microsoft Dynamics 365 for Operations.                                       |
| Mobileenhed, hvor Dynamics 365 for Operations-appen er installeret | Hent og installer Dynamics 365 for Operations-appen fra din mobilapp-butik.                                                                           |

## <a name="introduction"></a>Introduktion
Virksomheder har typisk flere forsendelser og flere tilgange på lageret hver dag. Disse bevægelser ændrer konstant status for den disponible lagerbeholdning. I arbejdsområdet for disponibelt lager på mobilenheder kan du se status for den disponible interne lagerbeholdning, så du kan få den nyeste indsigt i lagerdata på mobilenheder efter eget valg. Uanset om du arbejder på lageret, i indkøb, salg, produktion eller administration eller har andre roller, kan du få adgang til dataene for lagerbeholdningen når som helst og hvor som helst. Arbejdsområdet på mobileenheder giver et øjeblikkeligt overblik over den disponible beholdningsstatus på tværs af faciliteter og giver dig mulighed for at se disponibel lagerbeholdning på tværs af faciliteter, aktuelle materialereservationer og ikke-reserveret disponibel lagerbeholdning. Du kan også angive varenumre for at forespørge på disponibel lagerbeholdning og udføre en søgning, der er filtreret efter disponible varer eller varianter. Arbejdsområdet til mobilenheder indeholder især disse funktioner:

-   Du kan søge efter produktnummer eller produktnavn for at finde produkter, som du vil se den disponible lagerbeholdningsstatus for.
-   Du kan få vist følgende oplysninger for de valgte produkter:
    -   Disponibelt lager pr. sted
    -   Disponibel lagerbeholdning pr. lagersted
    -   Disponibel lagerbeholdning pr. lokalitet
    -   Disponibel lagerbeholdning pr. batch (for batchstyrede produkter)
    -   Disponibel lagerbeholdning pr. lagerstatus

<!-- -->

-   Disponibel produktlagerbeholdning vises på følgende måder:
    -   Efter fysisk lager (denne visning repræsenterer det samlede antal).
    -   Efter fysisk reserveret (denne visning repræsenterer det reserverede antal).
    -   Efter fysisk beholdning (denne visning repræsenterer tilgængelige antal, der ikke har nogen reservationer).

## <a name="get-started"></a>Introduktion
Sådan kommer du i gang på din mobilenhed:

1.  I din mobilappbutik skal du hente og installere Microsoft Dynamics 365 for Operations-appen.
2.  Start appen på din enhed.
3.  Angiv URL-adressen til din Dynamics 365.
4.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics 365 for Operations-konto. Angiv dine legitimationsoplysninger. Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed.

For at få vist arbejdsområder på din mobilapp skal du først publicere de ønskede arbejdsområder til Dynamics 365 for Operations-appen.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministration** &gt; **Opsætning** &gt; **systemparametre**.
3.  Vælg **Administrer mobilapp**.
4.  Vælg arbejdsområdet for at publicere til mobilplatformen.
5.  Vælg **Publicer arbejdsområde**.
6.  Opdater din enhed for at se de publicerede arbejdsområder.

## <a name="view-the-onhand-inventory-for-a-product"></a>Vise den disponibel lagerbeholdning for et produkt
1.  På din mobilenhed skal du vælge arbejdsområdet **Disponibel lagerbeholdning**.
2.  Vælg **Kontrollér disponibel lagerbeholdning for en vare**. Der vises en liste over de produkter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men du kan ændre dette tal. Du kan finde flere oplysninger i håndbogen til læsning på forhånd.
3.  Hvis din vare ikke er på listen, skal du vælge **Søg efter flere** for foretage en onlinesøgning i Dynamics 365 for Operations. Søg efter produktnummer, eller skift til en søgning efter produktnavn.
4.  Vælg et produkt. Hvis varen har et billede, vises billedet.
5.  Vælg en af følgende indstillinger for at få vist status for den disponible lagerbeholdning:
    -   Vise disponibel lagerbeholdning pr. websted
    -   Vise disponibel lagerbeholdning pr. lagersted
    -   Vise disponibel lagerbeholdning pr. lokalitet
    -   Vise disponibel beholdning pr. batch (for batchstyrede produkter)
    -   Vise beholdning pr. lagerstatus

    Disponibel produktlagerbeholdning vises på følgende måder:
    -   Efter fysisk lager (denne visning repræsenterer det samlede antal).
    -   Efter fysisk reserveret (denne visning repræsenterer det reserverede antal).
    -   Efter fysisk beholdning (denne visning repræsenterer det tilgængelige antal, der ikke har nogen reservationer).




