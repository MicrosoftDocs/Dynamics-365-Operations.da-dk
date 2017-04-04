---
title: "Salgsordrer mobile arbejdsområde for Microsoft Dynamics 365 for operationer app"
description: "Med arbejdsområdet salgsordrer mobil du kan holde dig ajour på salgsordrer hvor som helst og hvor som helst."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Salgsordrer mobile arbejdsområde for Microsoft Dynamics 365 for operationer app

Med arbejdsområdet salgsordrer mobil du kan holde dig ajour på salgsordrer hvor som helst og hvor som helst. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics-365 for operationer mobilplatform | [Dynamics 365 for operationer mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 til operationer                                          | Sørg for, at du bruger et miljø, hvor Microsoft Dynamics 365 for operationer version 1611 opdager og Microsoft Dynamics for operationer platform update 3 (November 2016). |
| Hotfix KB 3215650                                                    | Installere hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Microsoft Dynamics 365 for operationer.                                                                       |
| Mobile enhed, der har den Dynamics 365 for operationer app installeret | Hent den Dynamics 365 for operationer app fra din mobile app butik.                                                                                                      |

## <a name="overview"></a>Overblik
Denne mobile workspace har adgang til Dynamics-365 for operationer program og kan du få vist detaljerede oplysninger om de enkelte salgsordrer som ordrestatus, oplysninger om kontaktpersoner og rækkefølge taker kontaktoplysninger. Arbejdsområdet mobile giver en hurtig visning af salgsordrerne. Du kan få vist salgsordrer pr. kunde, eller få vist alle salgsordrer, eller få vist oplysninger om en bestemt salgsordre. Mobile arbejdsområdet indeholder to visninger for at hjælpe dig med at analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Få vist alle salgsordrer

Denne visning viser alle salgsordrer.

-   Brug en af følgende filtre til at vælge de ordrer, du vil have vist.
    -   Søg efter salgsordre
    -   Søg efter debitorkonto
    -   Søge efter Kundenavn
    -   Søge efter status
    -   Søge efter status for udgivelse
    -   Søg efter oprettelsesdato og tid

<!-- -->

-   Når du vælger de salgsordrer, kan du få vist detaljerne om bestemte ordrer. Specifikt, kan du se:
    -   Oplysninger om kundens navn og adresse
    -   Anden salgsordre datoer, som ønsket afsendelsesdato og bekræftet afsendelsesdato.
    -   Ordre taker kontaktoplysninger
    -   Oplysninger om kontaktpersoner
    -   Ordrelinjer
    -   Forsendelser, der viser, hvordan og hvornår en salgsordre, der er leveret

### <a name="view-orders-for-a-customer-"></a>Få vist ordrer for en kunde ** **

Denne visning viser en liste over salgsordrer pr. kunde.

-   Brug en af følgende filtre til at se ordrer for en kunde.
    -   Søg efter navn
    -   Søge efter firma

<!-- -->

-   Når du vælger en kunde, kan du se:
    -   Kundenavn og gruppe
    -   Oplysninger om kontaktpersoner
    -   Salgsordrer for kunden og oplysninger om de salgsordrer:
        -   Oplysninger om kundens navn og adresse
        -   Anden salgsordre datoer
        -   Ordre taker kontaktoplysninger
        -   Oplysninger om kontaktpersoner
        -   Ordrelinjer
        -   Forsendelser, der viser, hvordan og hvornår en salgsordre, der er leveret

## <a name="get-started"></a>Introduktion
Følg disse trin for at komme i gang ved hjælp af salgsordrer mobile arbejdsområdet på din mobilenhed.

1.  Din mobile app store, Hent og Installer Microsoft Dynamics-365 for operationer app.
2.  Du kan starte programmet på din enhed.
3.  Angiv URL-adressen for din Dynamics 365.
4.  Angiv firma til at logge på. F.eks. **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics-365 for operationer konto. Angiv dine legitimationsoplysninger. Når du logger på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed.

For at få vist arbejdsområder på din mobile app, skal du først udgive de ønskede arbejdsområder til Dynamics-365 for operationer app.

1.  Start Dynamics 365 for operationer.
2.  Gå til **systemadministration**&gt;**Setup**&gt;**systemparametre**.
3.  Vælg **Manage mobile app**.
4.  Vælg arbejdsområdet til at udgive til mobil platform.
5.  Vælg **udgive arbejdsområde**.
6.  Opdater din enhed for at se de udgivne arbejdsområder.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Få vist oplysninger om salgsordrer for en kunde
1.  På din mobilenhed, skal du vælge den **salgsordrer** arbejdsområde.
2.  Vælg **se ordrer for en kunde**.
3.  Brug ** konto ** eller ** kundenavn ** oplysninger til at finde den ønskede kunde.
4.  Vælg kunden.
5.  Vælg **kontaktoplysninger for** eller **salgsordrer**.
6.  Hvis **salgsordrer** er valgt, vises en liste over salgsordrer for debitoren skal være.
7.  Vælg **salgsordre**.
8.  Her kan du få vist oplysninger om salgsordrelinjer, leverancer, oplysninger om kontaktpersoner og rækkefølge taker kontaktoplysninger.




