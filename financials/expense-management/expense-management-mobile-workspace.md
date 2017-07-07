---
title: "Arbejdsområde til udgiftsstyring på mobilenhed"
description: "Dette emne indeholder oplysninger om arbejdsområdet til udgiftsstyring på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Finance and Operations-mobilappen. I dette arbejdsområde kan brugerne hente og sende en kvittering, så de senere kan knytte den til en udgiftsrapport. I arbejdsområdet til mobilenheder kan brugerne også hurtigt oprette en udgiftslinje ved hjælp af en tilknyttet kvittering."
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0e52d1c5dde7f79c4a8ac5ac2d9c3b25bba9c2cd
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017


---

# <a name="expense-management-mobile-workspace"></a>Arbejdsområde til udgiftsstyring på mobilenhed

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om arbejdsområdet til udgiftsstyring på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Finance and Operations-mobilappen. I dette arbejdsområde kan brugerne hente og sende en kvittering, så de senere kan knytte den til en udgiftsrapport. I arbejdsområdet til mobilenheder kan brugerne også hurtigt oprette en udgiftslinje ved hjælp af en tilknyttet kvittering.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Oversigt over arbejdsområde til udgiftsstyring på mobilenhed
---------------------------------------------------

Mange organisationer kræver, at der knyttes en kopi af en kvittering til en rejse-relaterede eller forretningsrelateret udgiftsrapport, som en medarbejder sender for refusion. I arbejdsområdet **Udgiftsstyring** til mobilenheder kan brugerne hurtigt oprette nye udgiftslinjer på mobilenheden efter eget valg ved hjælp af et tilknyttet billede af en kvittering. Brugerne kan også hente et billede af en kvittering og senere knytte det til en udgiftsrapport. I arbejdsområdet **Udgiftsstyring** til mobilenheder kan en bruger specifikt:

-   Tage et billede af en kvittering, og overføre det til Microsoft Dynamics 365 for Finance and Operations. En bruger kan derefter knytte billedet til en udgiftsrapport senere.
-   Overføre en fil som hentet kvittering. En bruger kan derefter knytte filen til en udgiftsrapport senere.
-   Oprette en ny udgiftslinje ved hjælp af en tilknyttet kvittering. En bruger kan derefter føje linjeelementet til en udgiftsrapport senere og sende det til godkendelse og refusion.

De resterende afsnit i dette emne beskriver, hvordan du implementerer og bruger arbejdsområdet **Udgiftsstyring** til mobilenheder.

## <a name="prerequisites"></a>Forudsætninger
Før du kan implementere arbejdsområdet **Udgiftsstyring** til mobilenheder, skal systemadministratoren have sørget for, at følgende forudsætninger er opfyldt.

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
<td>Hvis Finance and Operations ikke allerede er installeret i organisationen, kan systemadministratoren se under <a href="/dynamics365/unified-operations/dev-itpro/deployment/deploy-demo-environment">Installere et Microsoft Dynamics 365 for Finance and Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4019015 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4019015 (en X ++ opdatering eller et metadatahotfix) indeholder fire arbejdsområder til mobilenheder til supply chain management. For at implementere KB 4019015 skal systemadministratoren benytte følgende fremgangsmåde:
<ol>
<li>Hent KB 4019015 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>ApplicationSuite</strong>- og <strong>ExpenseMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a> på dit Finance and Operations-system.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Arbejdsområdet <strong>Udgiftsstyring</strong> til mobilenheder skal være publiceret til Finance and Operations-mobilappen.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Start Finance and Operations i browseren.</li>
<li>På siden <strong>Systemparametre</strong> skal du vælge <strong>Administrer arbejdsområder til mobile enheder</strong>.</li>
<li>Vælg arbejdsområdet <strong>Udgiftsstyring</strong>.</li>
<li>Klik på <strong>Publicer arbejdsområde til mobilenheder</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-finance-and-operations-mobile-app"></a>Hent og installer Finance and Operations-mobilappen
Hent og installer Finance and Operations-mobilappen i din mobilappbutik.

-   For Android: [Finance and Operations i Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Til iPhone: [Finance and Operations i iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-finance-and-operations-mobile-app"></a>Log på Finance and Operations-mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv din URL-adresse til Finance and Operations.
3.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
4.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Finance and Operations-konto. Angiv dine legitimationsoplysninger.
5.  Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, kan du trække for at opdatere listen over arbejdsområder til mobilenheder. 

[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Hent en kvittering ved hjælp af arbejdsområdet til udgiftsstyring på mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Udgiftsstyring**.
2.  Vælg **Hent kvittering**.
3.  Vælg **Tag foto** eller **Vælg billede**.
4.  Hvis du har valgt **Tag foto**, skal du gøre følgende:
    1.  Du føres til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du har taget billedet, skal du klikke på **OK** for at acceptere billedet.
    2.  Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

     **Eller:** Hvis du har valgt **Vælg billede**, skal du gøre følgende:
    1.  Vælg en billede på listen.
    2.  Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

5.  Vælg **Udført**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Hurtig angivelse af udgifter ved hjælp af arbejdsområdet til udgiftsstyring på mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Udgiftsstyring**.
2.  Vælg **Hurtig angivelse af udgifter**.
3.  Vælg udgiftsarten. Der vises en liste over de udgiftsarter, der er indlæst i din app til offlinebrug. Op til 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Finance and Operations-mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Hvis den aktuelle art ikke står på listen, skal du vælge **Søg** for foretage en onlinesøgning i Finance and Operations. Søg på udgiftsart, eller skift for at søge på udgiftstypen.
4.  Angiv posteringsdatoen for udgiften.
5.  Valgfrit: Angiv forhandleren for udgiften.
6.  Angiv beløbet for udgiften.
7.  Vælg valutaen for udgiften. Der vises en liste over de valutakoder, der er indlæst i din app til offlinebrug. Op til 400 valutaer er indlæst som standard, men en udvikler kan ændre dette tal. Der findes flere oplysninger for udviklere under [Finance and Operations-mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Hvis den aktuelle valuta ikke står på listen, skal du vælge **Søg** for foretage en onlinesøgning i Finance and Operations. Søg på valuta, eller skift for at søge på navn.
8.  Vælg **Tag foto** eller **Vælg billede**.
9.  Hvis du har valgt at **Tag foto**, føres du til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du har taget billedet, skal du klikke på **OK** for at acceptere billedet.  Eller hvis du har valgt **Vælg billede**, skal du vælge et billede på listen.
10. Vælg **Udført**.






