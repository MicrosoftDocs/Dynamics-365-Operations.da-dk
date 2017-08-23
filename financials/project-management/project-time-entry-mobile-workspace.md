---
title: "Projekttidsregistrering i arbejdsområde til mobile enheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet til projekttidsregistrering på mobilenheder. I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 83899969255a9b771fc5e62e66e3c5ffdca0296e
ms.contentlocale: da-dk
ms.lasthandoff: 08/10/2017

---

# <a name="project-time-entry-mobile-workspace"></a>Projekttidsregistrering i arbejdsområde til mobile enheder

[!include[banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Tidsregistrering for projekt** på mobilenheder. I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed.

Dette arbejdsområdet til mobilenheder er beregnet til brug med Microsoft Dynamics 365 for Unified Operations-mobilappen. 

## <a name="overview"></a>Overblik
Som led i deres daglige arbejde er projektressourcer ofte ude på et sted eller på rejse. I arbejdsområdet **Projekttidsregistrering** til mobilenheder kan brugerne angive deres fakturerbare eller ikke-fakturerbar tid på et projekt på en mobilenhed efter eget valg. Derfor kan projektressourcer foretage tidsregistreringer når som helst og hvor som helst. De kan også få vist tidsregistreringer, der allerede er registreret. 

Specifikt i mobilarbejdsområdet **Tidsregistrering for projekt** kan brugerne kan udføre disse opgaver:

-   Angiv det antal timer, du har brugt på en bestemt opgave, for den valgte dato.
-   Søg på projektnavn eller kunde for at finde det projekt, du vil registrere tiden for.
-   Angiv kategori og aktivitet for den tid, du har brugt.
-   Registrer tiden som fakturerbar eller ikke-fakturerbar for projektet.
-   Angiv eventuelt eksterne eller interne bemærkninger.

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Forudsætninger, hvis du bruger opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017 
Hvis opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017 er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Tidsregistrering for projekt** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere.
Hvis Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, kan systemadministratoren skal opfylde følgende forudsætninger. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementere KB 4018050.</td>
<td>Systemadministrator</td>
<td>KB 4018050 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Projekttidsregistrering</strong> til mobilenheder. For at implementere KB 4018050 skal systemadministratoren gøre følgende.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>ApplicationSuite</strong>- og <strong>ProjectMobile</strong>-modellerne, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Publicer arbejdsområdet <strong>Tidsregistrering for projekt</strong> til mobile enheder.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen

Download og installer Dynamics 365 for Unified Operations-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv URL-adressen til din Dynamics 365.
3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Angiv tid ved hjælp af arbejdsområdet Projekttidsregistrering til mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Projekttidsregistrering**.
2.  Vælg **Tidsregistrering**. Kalenderdatoerne for den aktuelle uge vises.
3.  Vælg **Handlinger** &gt; **Ny registrering** for en valgt dato.
4.  Angiv antallet af timer, der skal registreres.
5.  Vælg projektet for tidsregistreringen. Der vises en liste over de projekter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Du kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).
6.  Vælg **Søg**, hvis projektet ikke er på listen. Søg på navn, eller skift for at søge på projektnavn eller kunde.
7.  Vælg en kategori. Der vises en liste over de kategorier, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Du kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).
8.  Vælg **Søg**, hvis kategorien ikke er på listen. Søg på kategori, eller skift for at søge på kategorinavn.
9.  Vælg en aktivitet. Der vises en liste over de aktiviteter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Du kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page).
10. Vælg **Søg**, hvis aktiviteten ikke er på listen. Søg på aktivitetsnummer, eller skift for at søge på formål.

11. Vælg linjeegenskaben.
12. Valgfrit: Angiv eventuelt eksterne og interne bemærkninger.
13. Vælg **Udført**.

