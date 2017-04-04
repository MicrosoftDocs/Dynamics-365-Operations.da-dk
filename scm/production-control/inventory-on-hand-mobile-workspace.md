---
title: "Lager beholdning mobile arbejdsområde for Microsoft Dynamics 365 for operationer app"
description: "Disponibel lagerbeholdning mobile arbejdsområdet kan du få mobil indblik i reserverede og tilgængelige lager, når som helst og hvor som helst."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Lager beholdning mobile arbejdsområde for Microsoft Dynamics 365 for operationer app

Disponibel lagerbeholdning mobile arbejdsområdet kan du få mobil indblik i reserverede og tilgængelige lager, når som helst og hvor som helst. 

<a name="prerequisites"></a>Forudsætninger
-------------

| Forudsætning                                                         | Betegnelse                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Læs om Microsoft Dynamics-365 for operationer mobilplatform | [Dynamics 365 for operationer mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 til operationer                                          | Et miljø, der har Microsoft Dynamics 365 for operationer version 1611 opdager og Microsoft Dynamics for operationer platform update 3 (November 2016) |
| Hotfix KB 3215650                                                    | Installere hotfixet, hvis du vil aktivere de arbejdsområder, der findes i din Microsoft Dynamics-365 for operationer.                                       |
| Mobile enhed, der har den Dynamics 365 for operationer app installeret | Hent den Dynamics 365 for operationer app fra din mobile app butik.                                                                           |

## <a name="introduction"></a>Introduktion
Virksomheder har typisk flere forsendelser og flere tilgange på lageret hver dag. Disse bevægelser Ændringsstatus konstant disponibel lagerbeholdning. Disponibel lagerbeholdning mobile arbejdsområdet kan du se status for intern disponibel lagerbeholdning, så du kan få de nyeste indsigt i lagerdata på den mobile enhed efter eget valg. Uanset om du arbejder i det lager, indkøb, salg, produktion eller management eller har andre roller, du kan få adgang til dataene i lagerbeholdningen, når som helst og hvor som helst. Arbejdsområdet mobile giver et øjeblikkeligt overblik over disponible status på tværs af faciliteter og giver mulighed for at få vist disponibel lagerbeholdning på tværs af faciliteter, aktuelle materiale reservationer og ureserverede disponibel lagerbeholdning. Du kan også angive varenumre til forespørgsel disponibel lagerbeholdning og udfører en søgning, der er filtreret efter disponible varer eller varianter. Specielt indeholder mobile arbejdsområdet disse funktioner:

-   Du kan søge efter produkt eller produktnavn for at finde produkter til at få vist status for den disponible lagerbeholdning.
-   For de valgte produkter, kan du få vist følgende oplysninger:
    -   Disponibel lagerbeholdning pr. websted
    -   Disponibel lagerbeholdning pr. lagersted
    -   Disponibel lagerbeholdning pr. lokation
    -   Disponibel lagerbeholdning pr. parti (for varer, der styres af batch)
    -   Disponibel lagerbeholdning pr. lagerstatus

<!-- -->

-   Produktet disponible lagerbeholdning vises på følgende måder:
    -   Ved lageropgørelse (denne visning repræsenterer det samlede beløb).
    -   Ved fysisk reserveret (denne visning repræsenterer det reserverede beløb).
    -   Som ledig fysisk (denne visning repræsenterer beløb til rådighed, der er ingen reservationer.)

## <a name="get-started"></a>Introduktion
At komme i gang på din mobilenhed:

1.  Fra din mobile app butik, Hent og Installer Microsoft Dynamics-365 for operationer app.
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

## <a name="view-the-onhand-inventory-for-a-product"></a>Få vist oversigten over onhand for et produkt
1.  På din mobilenhed, skal du vælge den **beholdning** arbejdsområde.
2.  Vælg **Kontroller beholdninger for en vare**. Du kan se en liste over de produkter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men du kan ændre dette tal. Yderligere oplysninger finder du under forhånd læse håndbogen.
3.  Hvis din vare ikke er på listen, skal du vælge **søge mere** foretage en online søgning i Dynamics 365 for operationer. Søge efter produkt, eller Skift til en søgning efter produktnavn.
4.  Vælg et produkt. Hvis varen har et billede, vises billedet.
5.  Vælg en af følgende indstillinger for at få vist status for den disponible lagerbeholdning:
    -   Få vist disponibel lagerbeholdning pr. websted
    -   Få vist disponibel lagerbeholdning pr. lagersted
    -   Få vist disponibel lagerbeholdning pr. lokation
    -   Vis den disponible pr. parti (for varer, der styres af batch)
    -   Få vist disponibel lagerbeholdning pr. lagerstatus

    Produktet disponible lagerbeholdning vises på følgende måder:
    -   Ved lageropgørelse (denne visning repræsenterer det samlede beløb).
    -   Ved fysisk reserveret (denne visning repræsenterer det reserverede beløb).
    -   Som ledig fysisk (denne visning repræsenterer det disponible beløb, der er ingen reservationer).




