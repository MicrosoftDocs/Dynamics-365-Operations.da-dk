---
title: Power BI-indhold til driftsregnskab
description: I denne emne beskrives Microsoft Dynamics 365 for Operations-indholdspakken for driftsregnskab til Microsoft Power BI. Emnet beskriver dashboard og rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bb9a12dd45e227e86ba47c19f0850a73b77bc735
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Power BI-indhold til driftsregnskab

[!include[banner](../includes/banner.md)]


I denne emne beskrives Microsoft Dynamics 365 for Operations-indholdspakken for driftsregnskab til Microsoft Power BI. Emnet beskriver dashboard og rapporter, der er inkluderet i indholdspakken, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

<a name="accessing-the-content-pack"></a>Adgang til indholdspakken
--------------------------

Der findes to versioner af indholdspakken for driftsregnskab. Én version er tilgængelig fra Microsoft Dynamics Lifecycle Services (LCS), og den anden er tilgængelig fra PowerBI.com.

-   **Version, der er tilgængelige fra LCS:** Den indholdspakke for driftsregnskab, der er tilgængelig fra LCS, understøtter Microsoft Dynamics 365 for Operations version 1611. Du kan finde indholdspakken i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du henter indholdspakken og forbinder den med dine Microsoft Dynamics-365 for Operations-data, under [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).
-   **Version, der er tilgængelige fra PowerBI.com:** Den indholdspakke for driftsregnskab, der er tilgængelig fra PowerBI.com, understøtter Microsoft Dynamics AX-version 7.0 og 7.0.1. Du kan finde flere oplysninger om, hvordan du forbinder og indlæser dine Dynamics 365 for Operations-data, under [Adgang til Power BI-indhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Konfiguration af hovedkonto
Da organisationer ønsker, at passiver og omsætningsbeløb skal vises som positive beløb i rapporter, er konfigurationen af hovedkonti i Dynamics 365 for Operations vigtig. For at disse hovedkonti skal kunne vises som positive beløb, skal hovedkontotypen indstilles til **Passiv** eller **Indtægter**. Når disse kontotyper bruges, bruger rapportering via Microsoft Power BI omvendt fortegn og viser beløbene som positive beløb.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard og rapporter, der er inkluderet i indholdspakken
Når du har knyttet indholdspakken til dine Dynamics 365 for Operations-data, viser dashboardet og rapporterne de finansielle data. Hvis du aldrig har brugt Power BI før, kan du finde oplysninger om det under [Guidet indføring i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Dashboardet indeholder opsummerende datafelter, der er baseret på underliggende rapporter. Hvert felt indeholder opsummerende oplysninger for det indeværende år på tværs af alle virksomheder i en organisation. Her er nogle af felterne:

-   Indløsning
-   Samlet omsætning i år
-   Samlede udgifter i år
-   Nettoresultat i år
-   Likviditetsgrad på kort sigt
-   Samlede udgifter i år efter kontokategori
-   Aktuel dækningsgrad
-   Gæld/Samlede aktiver
-   Faktisk vs budgetteret omsætning
-   Faktureret omsætning i år
-   Driftsudgiftsgrad i år
-   Overskudsgrad i år
-   Faktiske vs. budgetterede udgifter – Alle firmaer

Hvert felt er understøttet af en supplerende rapport. Disse rapporter indeholder både diagrammer og tabeller, der indeholder flere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                      | Rapportens oplysninger omfatter:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengestrømsanalyse               | Kontanter efter juridisk enhed, kontanter pr. kvartal, samlede kontanter og kontanter efter konto **Bemærk!** Rapporten **Kontanter pr. kvartal** indeholder ikke primosaldi i det samlede beløb for første kvartal. Det viser det samlede nye posteringer, der bogføres i hvert kvartal.                                                                                |
| Analyse af aktuel dækningsgrad      | Aktuel dækningsgrad efter juridisk enhed, aktuel dækningsgrad pr. kvartal og saldi for omsætningsaktiver og kortfristet gæld                                                                                                                                                                                                                              |
| Analyse af likviditetsgrad på kort sigt        | Likviditetsgrad på kort sigt efter juridisk enhed, likviditetsgrad på kort sigt pr. kvartal og saldi for kontanter, tilgodehavender og kortfristet gæld                                                                                                                                                                                                                      |
| Analyse af vareforbrug | Vareforbrug (COGS) efter juridisk enhed, vareforbrug i år og sidste år pr. kvartal, vareforbrug i forhold til salg efter juridisk enhed, samlet vareforbrug og vareforbrug i forhold til salg i procent                                                                                                                                                                                   |
| Analyse af arbejdskapital    | Arbejdskapital efter juridisk enhed, arbejdskapital pr. kvartal, omsætningsaktiver, kortfristet gæld og samlet arbejdskapital                                                                                                                                                                                                                   |
| Analyse af aktiver og gæld     | Afkast af samlede aktiver og gæld i forhold til de samlede aktiver efter juridisk enhed, gæld i forhold til samlede aktiver og afkast for samlede aktiver pr. kvartal i forhold til dato, aktiver og passiver                                                                                                                                                                                     |
| Analyse af overskudsgrad      | Faktisk og budgetteret overskudsgrad efter juridisk enhed, overskudsmarkering pr. kvartal, overskudsgrad i procent og overskudsgrad                                                                                                                                                                                                                       |
| Analyse af nettoresultat         | Faktisk og budgetteret nettoresultat efter juridisk enhed, nettoresultat i år og sidste år og udgifter i forhold til nettoresultat i procent                                                                                                                                                                                                                       |
| Analyse af indtjening           | Faktisk og budgetteret overskud før renter og skat (EBIT) efter juridisk enhed, EBIT i år og sidste år, udgifter i forhold til omsætning i procent og faktiske og budgetterede udgifter i forhold til indtægter                                                                                                                                                          |
| Analyse af omsætning            | Samlet omsætning, samlede faktiske og budgetterede omsætning efter juridisk enhed, samledt omsætning i år og sidste år, afvigelse i omsætningsbudget efter juridisk enhed og samlet af omsætning i indeværende og sidste periode                                                                                                                                                 |
| Udgiftsanalyse            | Samlede udgifter, faktiske i forhold til budgetterede samlede udgifter efter juridisk enhed, samlede faktiske og budgetterede samlede udgifter pr. kvartal, samlede udgifter efter kontokategori og driftsudgiftsgrad                                                                                                                                                                 |
| Analyse af faktureret omsætning     | samlede tilgodehavender, samlede tilgodehavender efter juridisk enhed, samlede tilgodehavender pr. kvartal, og saldi for konti med tilgodehavender **Bemærk!** Rapporterne medtager ikke primosaldi for debitorfinanskonti. De viser totalen for nye transaktioner, der er bogført til debitorer. |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Hvis du vil finde flere oplysninger om filtrering og fastgørelse i Power BI, skal du se [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
De data, der udfylder dashboard og rapporter i indholdspakken for driftsregnskab, er Dynamics 365 for Operations-data. Følgende enheder blev brugt som grundlag for indholdspakken: **Aggregér dataenheder**

-   **GeneralLedgerActivities** – Denne enhed aggregerer finanssaldi efter kontokategori.
-   **BudgetActivities** – Denne enhed aggregerer budgetsaldi efter kontokategori.

**Dataenheder**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Finans
-   ChartofAccounts

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. De beregnede mål bruges til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdspakken. Som standard omfatter indholdspakken data for de sidste tre år og et år frem. Hvis du vil medtage yderligere beregninger i rapporter og dashboard, kan du redigere [Microsoft Excel-projektmappen](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne projektmappe er den standarddatamodel, der blev brugt til at oprette indholdspakken. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)





