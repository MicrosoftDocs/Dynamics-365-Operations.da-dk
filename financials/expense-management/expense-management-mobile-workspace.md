---
title: "Arbejdsområde til udgiftsstyring på mobilenhed"
description: "Dette emne indeholder oplysninger om arbejdsområdet Udgiftsstyring på mobilenheder. I dette arbejdsområde kan brugerne hente og sende en kvittering, så de senere kan knytte den til en udgiftsrapport. Brugerne kan også hurtigt oprette en udgiftslinje ved hjælp af en vedhæftet kvittering, og oprette og administrere deres udgiftsrapporter."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: db41b3873755f93895aea7a32b65f2a8ed6a57fd
ms.openlocfilehash: 58d36505461ea89bf466209d3da968d1357e58ae
ms.contentlocale: da-dk
ms.lasthandoff: 08/10/2017

---

# <a name="expense-management-mobile-workspace"></a>Arbejdsområde til udgiftsstyring på mobilenhed

[!include[banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Udgiftsstyring** på mobilenheder. I dette arbejdsområde kan brugerne hente og sende en kvittering, så de senere kan knytte den til en udgiftsrapport. Brugerne kan også hurtigt oprette en udgiftslinje ved hjælp af en vedhæftet kvittering, og oprette og administrere deres udgiftsrapporter. Godkendere kan desuden bruge arbejdsområdet **Udgiftsstyring** på mobilenheder til at få vist udgiftsrapporter, der er knyttet til dem, og enten godkende eller afvise udgiftsrapporter.


Dette arbejdsområdet til mobilenheder er beregnet til brug med Microsoft Dynamics 365 for Unified Operations-mobilappen.


## <a name="overview"></a>Overblik

Mange organisationer kræver, at der knyttes en kopi af en kvittering til en rejse-relaterede eller forretningsrelateret udgiftsrapport, som en medarbejder sender for refusion. I arbejdsområdet **Udgiftsstyring** til mobilenheder kan brugerne hurtigt oprette nye udgiftslinjer på mobilenheden efter eget valg ved hjælp af et tilknyttet billede af en kvittering. Brugerne kan også hente et billede af en kvittering og senere knytte det til en udgiftsrapport. Medarbejdere kan også oprette og administrere deres udgiftsrapporter og derefter sende dem til godkendelse og refusion fra deres mobilenhed.


Med arbejdsområdet **Udgiftsstyring** på mobilenheder kan brugerne udføre disse opgaver:

- Tage et billede af en kvittering, og overføre det til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Du kan derefter knytte billedet til en udgiftsrapport senere.
- Overføre en fil som hentet kvittering. Du kan derefter knytte filen til en udgiftsrapport senere.
- Oprette en ny udgiftslinje ved hjælp af en tilknyttet kvittering. Du kan derefter føje linjeelementet til en udgiftsrapport senere og sende det til godkendelse og refusion.

Hvis du bruger opdateringen til Microsoft Dynamics 365 for Finans and Operations, Enterprise edition fra juli 2017, kan du også bruge disse funktioner:

- Oprette en ny udgiftsrapport.
- Tilknytte kreditkorttransaktioner og andre udgifter, der tidligere er oprettet, til en udgiftsrapport.
- Oprette nye udgifter til en udgiftsrapport.
- Knytte en kvittering til omkostninger for en udgiftsrapport, enten ved at tage et billede af kvitteringen eller ved at overføre en fil som en hentet kvittering.
- Afhængigt af firmaets udgiftspolitik kan du føje listen over gæster til en udgift.
- Afhængigt af firmaets udgiftspolitik kan du specificere udgifterne.
- Sende en udgiftsrapport til godkendelse og refusion.
- Godkende eller afvise udgiftsrapporter, du tildelt godkender for.

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne varierer, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Forudsætninger, hvis du bruger opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017 
Hvis opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017 er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Udgiftsstyring** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

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
<td>Implementere KB 4019015.</td>
<td>Systemadministrator</td>
<td>KB 4019015 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Udgiftsstyring</strong> til mobilenheder. For at implementere KB 4019015 skal systemadministratoren gøre følgende.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>ApplicationSuite</strong>- og <strong>ExpenseMobile</strong>-modeller, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Publicere arbejdsområdet <strong>Udgiftsstyring</strong> på mobilenhed.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Hent og installer Dynamics 365 for Operations-mobilappen
Download og installer Dynamics 365 for Unified Operations-mobilappen:

- [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1. Start appen på din mobilenhed.
2. Angiv URL-adressen til din Dynamics 365.
4. Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
5. Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.


[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Hent en kvittering ved hjælp af arbejdsområdet til udgiftsstyring på mobilenheder

1. På din mobilenhed skal du åbne arbejdsområdet **Udgiftsstyring**.
2. Vælg **Hent kvittering**.
3. Vælg **Tag foto** eller **Vælg billede**.
4. Udfør ét af følgende trin:

    - Hvis du har valgt **Tag foto**, skal du gøre følgende:

        1. Du føres til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du har taget billedet, skal du vælge **OK** for at acceptere billedet.
        2. Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

    - Hvis du har valgt **Vælg billede**, skal du gøre følgende:

        1. Vælg en billede på listen.
        2. Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

5. Vælg **Udført**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Hurtigt angive udgifter ved hjælp af arbejdsområdet Udgiftsstyring på mobilenheder
1. På din mobilenhed skal du åbne arbejdsområdet **Udgiftsstyring**.
2. Vælg **Hurtig angivelse af udgifter**.
3. Vælg udgiftsarten. Der vises en liste over de udgiftsarter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis kategorien ikke er på listen. Søg på udgiftsart, eller skift for at søge på udgiftstypen.
4. Angiv posteringsdatoen for udgiften.
5. Valgfrit: Angiv forhandleren for udgiften.
6. Angiv beløbet for udgiften.
7. Vælg valutaen for udgiften. Der vises en liste over de valutakoder, der er indlæst i din app til offlinebrug. 400 valutaer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis valutaen ikke er på listen. Søg på valuta, eller skift for at søge på navn.
8. Vælg **Tag foto** eller **Vælg billede**.
9. Udfør ét af følgende trin:

    - Hvis du har valgt at **Tag foto**, føres du til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du har taget billedet, skal du vælge **OK** for at acceptere billedet.
    - Hvis du har valgt **Vælg billede**, skal du vælge et billede på listen.

10. Vælg **Udført**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Godkende en udgiftsrapport ved hjælp af arbejdsområdet Udgiftsstyring på mobilenheder (hvis du bruger opdateringen fra juli 2017)
1. På din mobilenhed skal du åbne arbejdsområdet **Udgiftsstyring**.
2. **Godkendelser af udgifter** viser antallet af udgiftsrapporter, der er tildelt til dig til godkendelse. Antallet opdateres ca. hvert 30. minut. Vælg **Godkendelser af udgifter**.

    Listen over udgiftsrapporter, der er tildelt til dig til godkendelse, vises.
    
3. Vælg en udgiftsrapport for at få vist udgiftsdetaljerne for den.
4. Vælg en udgift for at få vist detaljerne for den. De oplysninger, der vises for en udgift, omfatter kvitteringer, gæster og specifikationer.
5. På siden **Udgiftsrapport** skal du vælge at godkende eller afvise udgiftsrapporten.
6. Skriv eventuelle kommentarer til godkendelseshandlingen.
7. Vælg **Udført**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Oprette en ny en udgiftsrapport og sende den til godkendelse ved hjælp af arbejdsområdet Udgiftsstyring på mobilenheder (hvis du bruger opdateringen fra juli 2017)
1. På din mobilenhed skal du åbne arbejdsområdet **Udgiftsstyring**.
2. Vælg **Udgiftsregistrering**.
3. Vælg **Ny rapport**, eller vælg en eksisterende udgiftsrapport på listen.
4. Angiv formålet og eventuelt yderligere oplysninger for nye udgiftsrapporter. Disse oplysninger varierer, afhængigt af på den måde, udgiftsstyringen er konfigureret i dit firma.
5. Vælg **Udført**.
6. Vælg **Vedhæft** for at tilføje eksisterende udgifter, f.eks. kreditkorttransaktioner, i udgiftsrapporten.
7. Vælg en eller flere udgifter på listen.
8. Vælg **Udført**.
9. Vælg **Ny udgift** for at tilføje en ny udgift til udgiftsrapporten.
10. Vælg udgiftsarten. Der vises en liste over de udgiftsarter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis kategorien ikke er på listen. Søg på udgiftsart, eller skift for at søge på udgiftstypen.
11. Valgfrit: Angiv forhandleren for udgiften.
12. Angiv posteringsdatoen for udgiften.
13. Angiv beløbet for udgiften.
14. Vælg valutaen for udgiften. Der vises en liste over de valutakoder, der er indlæst i din app til offlinebrug. 400 valutaer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis valutaen ikke er på listen. Søg på valuta, eller skift for at søge på navn.
15. Vælg **Udført**.
16. Du kan tilføje flere oplysninger om udgiften ved at vælge **Tilføj flere oplysninger**. Hvilke felter der er tilgængelige afhænger af konfigurationen af udgiftsstyringen i dit firma.
17. Hvis virksomhedens politik kræver en kvittering for udgiften, skal du vælge **Kvitteringer** og derefter følge disse trin:

    1. Vælg **Hent kvittering** eller **Vedhæft kvittering**.
    2. Udfør ét af følgende trin:

        - Hvis du har valgt **Hent kvittering**, skal du gøre følgende:

            1. Vælg **Tag foto** eller **Vælg billede**.
            2. Udfør ét af følgende trin:

                - Hvis du har valgt **Tag foto**, skal du gøre følgende:

                    1. Du føres til kameraet på din mobilenhed, så du kan tage et billede af kvitteringen. Når du har taget billedet, skal du vælge **OK** for at acceptere billedet.
                    2. Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

                - Hvis du har valgt **Vælg billede**, skal du gøre følgende:

                    1. Vælg en billede på listen.
                    2. Valgfrit: Angiv et navn til billedet, og angiv evt. noter.

            3.  Vælg **Udført**.

        - Hvis du har valgt **Vedhæft kvittering**, skal du gøre følgende:

            1.  Vælg en eller flere billeder på listen.
            2.  Vælg **Udført**.

    3. Vælg knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

18. Hvis virksomhedens politik kræver gæster for udgiften, skal du vælge **Gæster** og derefter følge disse trin:

    1. Vælg **Gæst**, **Tidligere gæster** eller **Kolleger**.
    2. Udfør ét af følgende trin:

        - Hvis du har valgt **Gæst**, skal du gøre følgende:

            1. Indtast et navn til gæsten.
            2. Valgfrit: Angiv gæstens organisation og/eller land.
            3. Valgfrit: Angiv gæstens titel.
            4. Vælg **Udført**.

        - Hvis du har valgt **Tidligere gæster**, skal du gøre følgende:

            1. Vælg en eller flere tidligere gæster på listen. Du kan se en liste over tidligere gæster, som du har tilføjet i tidligere udgiftsrapporter, der er indlæst i din app til brug offline. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis den tidligere gæst ikke er på listen. Søg på navn, eller skift for at søge på organisation, land eller titel.
            2. Vælg **Udført**.

        - Hvis du har valgt **Kolleger**, skal du gøre følgende:

            1. Vælg en eller flere kolleger på listen. Der vises en liste over de kolleger, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis kollegaen ikke er på listen. Søg på navn, eller skift for at søge på virksomhed eller titel.
            2. Vælg **Udført**.

    3. Vælg knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

19. Hvis virksomhedens politik kræver, at en kvittering specificeres, skal du vælge **Specificer** og derefter følge disse trin:

    1. Vælg den første dato, der skal specificeres.
    2. Vælg **Tilføj specifikation**.
    3. Vælg underkategorien for specifikationen af udgiften. Der vises en liste over de underkategorier af udgifter, der er indlæst i din app til offlinebrug. 50 varer er indlæst som standard, men en udvikler kan ændre dette tal. Udviklere kan finde flere oplysninger under [Mobilplatform](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page). Vælg **Søg** for at søge online, hvis underkategorien ikke er på listen. Søg på navnet på udgiftsunderkategorien.
    4. Angiv transaktionsbeløbet for specifikationen.
    5. Rediger transaktionsdatoen, hvis det er påkrævet.
    6. Vælg **Udført**.
    7. Gentag de foregående trin, indtil du har tilføjet alle specificeringer for den valgte dato.
    8. For yderligere dage kan du vælge **Kopiér til næste dag** for at kopiere specificeringer til den næste dag. Du kan også vælge den dato, der skal specificeres, og derefter tilføje specificeringer, som du gjorde for den første dato.
    9. Når du er færdig med at specificere udgiften, skal du vælge knappen **Tilbage** for at vende tilbage til udgiftsdetaljerne.

20. Vælg knappen **Tilbage** for at vende tilbage til siden **Udgiftsrapport**.
21. Gentag de foregående trin, indtil du er færdig med at tilføje alle udgifter.
22. Vælg **Send**.
23. Skriv eventuelle kommentarer til godkenderen.
24. Vælg **Udført**.

