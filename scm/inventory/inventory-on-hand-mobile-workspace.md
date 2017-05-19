---
title: "Disponibelt lager i arbejdsområde til mobilenheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet Disponibelt lager på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. I dette arbejdsområde på mobilenheder kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e703ae80800b993ebca1c7bee455af1be41c7d5f
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Disponibelt lager i arbejdsområde til mobilenheder

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om arbejdsområdet Disponibelt lager på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. I dette arbejdsområde på mobilenheder kan du få indblik i reserveret og tilgængelig lagerplads, når som helst og hvor som helst på mobilenheden.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Oversigt over arbejdsområdet Disponibelt lager på mobilenhed
--------------------------------------------------

Virksomheder har typisk flere forsendelser og flere tilgange på lageret hver dag. Disse bevægelser ændrer konstant status for den disponible lagerbeholdning. I arbejdsområdet **Disponibelt lager** på mobilenheder kan du se status for den disponible interne lagerbeholdning, så du kan få den nyeste indsigt i lagerdata på mobilenheder efter eget valg. Uanset om du arbejder på lageret, i indkøb, salg, produktion eller administration eller har andre roller, kan du få adgang til dataene for lagerbeholdningen når som helst og hvor som helst. Arbejdsområdet på mobilenheder giver en øjeblikkelig visning af den disponible lagerstatus på tværs af faciliteter. Her kan du få vist den disponible lagerbeholdning på tværs af faciliteter, aktuelle materialereservationer og ikke-reserveret disponibel lagerbeholdning. Du kan også angive varenumre for at forespørge på disponibel lagerbeholdning og udføre en søgning, der er filtreret efter disponible varer eller varianter. Arbejdsområdet til mobilenheder indeholder især disse funktioner:

-   Du kan søge efter produktnummer eller produktnavn for at finde produkter, som du vil se den disponible lagerbeholdningsstatus for.
-   Du kan få vist følgende oplysninger for de valgte produkter:
    -   Disponibelt lager pr. sted
    -   Disponibel lagerbeholdning pr. lagersted
    -   Disponibel lagerbeholdning pr. lokalitet
    -   Disponibel lagerbeholdning pr. batch (for batchstyrede produkter)
    -   Disponibel lagerbeholdning pr. lagerstatus
-   Disponibel produktlagerbeholdning vises på følgende måder:
    -   Efter fysisk lager (denne visning repræsenterer det samlede antal).
    -   Efter fysisk reserveret (denne visning repræsenterer det reserverede antal).
    -   Efter fysisk beholdning (denne visning repræsenterer tilgængelige antal, der ikke har nogen reservationer).

## <a name="prerequisites"></a>Forudsætninger
Før du kan bruge arbejdsområdet **Disponibelt lager** på mobilenheder, skal systemadministratoren have sørget for, at følgende forudsætninger er opfyldt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere skal være implementeret.</td>
<td>Systemadministrator</td>
<td>Hvis Dynamics 365 for Operations ikke allerede er installeret i organisationen, kan systemadministratoren se under <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Installere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4013633 (en X ++ opdatering eller et metadatahotfix) indeholder fire arbejdsområder til mobilenheder til supply chain management. For at implementere KB 4013633 skal systemadministratoren benytte følgende fremgangsmåde:
<ol>
<li>Hent KB 4013633 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installere metadatahotfixet</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Anvend den installerbare pakke</a> på dit Microsoft Dynamics 365 for Operations-system.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Arbejdsområdet <strong>Disponibelt lager</strong> på mobilenheder skal være publiceret til Dynamics 365 for Operations-mobilappen.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Start Dynamics 365 for Operations i din browser.</li>
<li>På siden <strong>Systemparametre</strong> skal du vælge <strong>Administrer arbejdsområder til mobile enheder</strong>.</li>
<li>Vælg arbejdsområdet <strong>Disponibelt lager</strong>.</li>
<li>Klik på <strong>Publicer arbejdsområde til mobilenheder</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Hent og installer Dynamics 365 for Operations-mobilappen
Hent og installer Microsoft Dynamics 365 for Operations-mobilappen i din mobilappbutik.

-   Til Android: [Dynamics 365 for Operations i Google Play Butik](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Til iPhone: [Dynamics 365 for Operations i iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Log på Dynamics 365 for Operations-mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv din URL til Dynamics 365 for Operations.
3.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
4.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Dynamics 365 for Operations-konto. Angiv dine legitimationsoplysninger.
5.  Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren senere publicerer et nyt arbejdsområde, kan du trække for at opdatere listen over arbejdsområder til mobilenheder. 

    [![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Få vist oversigten over disponibel lagerbeholdning for et produkt ved hjælp af arbejdsområdet Disponibelt lager på mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Disponibel lagerbeholdning**.
2.  Vælg **Kontrollér disponibel lagerbeholdning for en vare**. Der vises en liste over de produkter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Dynamics 365 for Operations-mobilplatform](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/).
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






