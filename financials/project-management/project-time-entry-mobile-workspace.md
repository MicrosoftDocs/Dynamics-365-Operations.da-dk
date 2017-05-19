---
title: "Projekttidsregistrering i arbejdsområde på mobilenheder til Dynamics 365 for Operations-appen"
description: "Dette emne indeholder oplysninger om arbejdsområdet til projekttidsregistrering på mobilenheder. I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Projekttidsregistrering i arbejdsområde til mobilenheder

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dette emne indeholder oplysninger om arbejdsområdet til projekttidsregistrering til Dynamics 365 for Operations-mobilappen. I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Oversigt over arbejdsområdet til projekttidsregistrering på mobilenheder
---------------------------------------------------

Som led i deres daglige arbejde er projektressourcer ofte ude på et sted eller på rejse. I arbejdsområdet **Projekttidsregistrering** til mobilenheder kan brugerne angive deres fakturerbare eller ikke-fakturerbar tid på et projekt på en mobilenhed efter eget valg. Derfor kan projektressourcer foretage tidsregistreringer når som helst og hvor som helst. De kan også få vist tidsregistreringer, der allerede er registreret. 

Specifikt indeholder arbejdsområdet til **Projekttidsregistrering** på mobilenheder disse funktioner:

-   Angiv det antal timer, du har brugt på en bestemt opgave, for den valgte dato.
-   Søg på projektnavn eller kunde for at finde det projekt, du vil registrere tiden for.
-   Angiv kategori og aktivitet for den tid, du har brugt.
-   Registrer tiden som fakturerbar eller ikke-fakturerbar for projektet.
-   Angiv eventuelt eksterne eller interne bemærkninger.

Du kan finde oplysninger om implementering af arbejdsområdet **Projekttidsregistrering** til mobilenheder i følgende afsnit i dette emne.

## <a name="prerequisites"></a>Forudsætninger
Før du kan implementere arbejdsområdet **Projekttidsregistrering** til mobilenheder, skal systemadministratoren have sørget for, at følgende forudsætninger er opfyldt.

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
<td>Hvis Dynamics 365 for Operations ikke allerede er installeret i organisationen, kan systemadministratoren se under <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Installere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4018050 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4018050 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Projekttidsregistrering</strong> til mobilenheder. For at implementere KB 4018050 skal systemadministratoren gøre følgende.
<ol>
<li>Hent KB 4018050 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>ApplicationSuite</strong>- og <strong>ProjectMobile</strong>-modellerne, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a> på dit Microsoft Dynamics 365 for Operations-system.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Arbejdsområdet <strong>Projekttidsregistrering</strong> til mobilenheder skal være publiceret til Dynamics 365 for Operations-mobilappen.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Start Dynamics 365 for Operations i din browser.</li>
<li>På siden <strong>Systemparametre</strong> under fanen <strong>Administrer arbejdsområder til mobile enheder</strong> skal du vælge arbejdsområdet <strong>Projekttidsregistrering</strong>.</li>
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
5.  Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, kan du trække for at opdatere listen over arbejdsområder til mobilenheder.

[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Angiv tid ved hjælp af arbejdsområdet Projekttidsregistrering til mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Projekttidsregistrering**.
2.  Vælg **Tidsregistrering**. Du kan se kalenderdatoerne for den aktuelle uge.
3.  Vælg **Handlinger** &gt; **Ny registrering** for en valgt dato.
4.  Angiv antallet af timer, der skal registreres.
5.  Vælg projektet for tidsregistreringen. Der vises en liste over de projekter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Hvis dit projekt ikke står på listen, skal du vælge **Søg** for foretage en onlinesøgning i Dynamics 365 for Operations. Søg på navn, eller skift for at søge på projektnavn eller kunde.
7.  Vælg en kategori. Der vises en liste over de kategorier, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Hvis den aktuelle art ikke står på listen, skal du vælge **Søg** for foretage en onlinesøgning i Dynamics 365 for Operations. Søg på kategori, eller skift for at søge på kategorinavn.
9.  Vælg en aktivitet. Der vises en liste over de aktiviteter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Dynamics 365 for Operations-mobilplatform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Hvis den aktuelle aktivitet ikke står på listen, skal du vælge **Søg** for foretage en onlinesøgning i Dynamics 365 for Operations. Søg på aktivitetsnummer, eller skift for at søge på formål.
11. Vælg linjeegenskaben.
12. Valgfrit: Angiv eventuelt eksterne og interne bemærkninger.
13. Vælg **Udført**.






