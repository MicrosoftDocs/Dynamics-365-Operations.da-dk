---
title: "Arbejdsområde til mobile enheder til salgsordrer til Microsoft Dynamics 365 for Operations-app"
description: "Med arbejdsområdet til mobile enheder til salgsordrer kan du kan holde dig ajour på salgsordrer hvor som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Arbejdsområde til mobile enheder til salgsordrer til Microsoft Dynamics 365 for Operations-app

Med arbejdsområdet til mobile enheder til salgsordrer kan du kan holde dig ajour på salgsordrer hvor som helst og hvor som helst. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics 365 for Operations-mobilplatformen | [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Sørg for, at du bruger et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og Microsoft Dynamics for Operations platformsopdatering 3 (november 2016). |
| Hotfix KB 3215650                                                    | Installer hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Microsoft Dynamics 365 for Operations.                                                                       |
| Mobileenhed, hvor Dynamics 365 for Operations-appen er installeret | Hent og installer Dynamics 365 for Operations-appen fra din mobilapp-butik.                                                                                                      |

## <a name="overview"></a>Overblik
Dette arbejdsområde til mobile enheder har adgang til Dynamics-365 for Operations-programmet, og du kan få vist detaljerede oplysninger om de enkelte salgsordrer, f.eks. ordrestatus, kundekontaktoplysninger og kontaktoplysning om ordretager. Arbejdsområdet til mobile enheder giver en øjeblikkelig visning af salgsordrerne. Du kan få vist salgsordrer pr. kunde, eller få vist alle salgsordrer, eller få vist oplysninger om en bestemt salgsordre. Arbejdsområdet til mobile enheder indeholder to visninger, der hjælper dig med at analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer

Denne visning viser alle salgsordrer.

-   Brug ét af følgende filtre til at vælge de salgsordrer, du vil have vist.
    -   Søg efter salgsordre
    -   Søg efter kundekonto
    -   Søg efter kundenavn
    -   Søg efter status
    -   Søg efter status for frigivelse
    -   Søg efter dato og klokkeslæt for oprettelse

<!-- -->

-   Når du har valgt salgsordrerne, kan du få vist detaljerede oplysninger om bestemte ordrer. Specifikt, kan du se:
    -   Oplysninger om kundens navn og adresse
    -   Andre salgsordredatoer, f.eks. ønsket afsendelsesdato og bekræftet afsendelsesdato
    -   Ordretagers kontaktoplysninger
    -   Kundekontaktoplysninger
    -   Ordrelinjer
    -   Forsendelser, der viser, hvordan og hvornår en salgsordre er blevet leveret

### <a name="view-orders-for-a-customer-"></a>Vis ordrer for en kunde** **

Denne visning angiver salgsordrer pr. kunde.

-   Brug et af følgende filtre til at se ordrer for en kunde.
    -   Søg efter navn
    -   Søg efter konto

<!-- -->

-   Når du vælger en kunde, kan du se:
    -   Kundenavn og -gruppe
    -   Kundekontaktoplysninger
    -   Salgsordrer for kunden og oplysninger om salgsordrerne:
        -   Oplysninger om kundens navn og adresse
        -   Andre salgsordredatoer
        -   Ordretagers kontaktoplysninger
        -   Kundekontaktoplysninger
        -   Ordrelinjer
        -   Forsendelser, der viser, hvordan og hvornår en salgsordre er blevet leveret

## <a name="get-started"></a>Introduktion
Følg disse trin for at komme i gang med at bruge arbejdsområdet til mobile enheder til salgsordrer på din mobilenhed.

1.  På din mobilapp-store skal du hente og installere Microsoft Dynamics 365 for Operations-appen.
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

## <a name="view-information-about-sales-orders-for-a-customer"></a>Vis oplysninger om salgsordrer for en kunde
1.  På din mobilenhed skal du vælge arbejdsområdet **Salgsordrer**.
2.  Vælg **Vis ordrer for en kunde**.
3.  Brug oplysningerne **Konto** eller **Kundenavn** til at finde den ønskede kunde.
4.  Vælg kunden.
5.  Vælg **Kontaktoplysninger** eller **Salgsordrer**.
6.  Hvis **Salgsordrer** er valgt, vises der en liste over salgsordrer for kunden.
7.  Vælg **Salgsordre**.
8.  Her kan du få vist oplysninger om salgsordrelinjer, leverancer, kundekontaktoplysninger og kontaktoplysninger for ordretager.




