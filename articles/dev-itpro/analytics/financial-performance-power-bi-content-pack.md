---
title: Driftsregnskab i Power BI-indhold
description: I dette emne beskrives Power BI-indhold til Driftsregnskab. I emnet beskrives dashboardet og de rapporter, som er inkluderet, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a501fcb851f1c201e03b59bb3ea951684c6e552
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="financial-performance-power-bi-content"></a>Driftsregnskab i Power BI-indhold

[!include[banner](../includes/banner.md)]

I dette emne beskrives Microsoft Power BI-indholdet til **Driftsregnskab**. I emnet beskrives dashboardet og de rapporter, som er inkluderet, og der er oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdspakken.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold

Du kan få adgang til Power BI-indhold til **Driftsregnskab** fra Microsoft Dynamics Lifecycle Services (LCS) og fra PowerBI.com.

### <a name="available-from-lcs"></a>Tilgængelig fra LCS
Power BI-indholdet til **Driftsregnskab**, som er tilgængeligt fra LCS, understøtter følgende versioner:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)
- Microsoft Dynamics 365 for Operations version 1611 

Du kan finde Power BI-indhold i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indholdspakken og implementerer den i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

### <a name="available-from-powerbicom"></a>Tilgængelig fra PowerBI.com
Power BI-indholdet til **Driftsregnskab**, der er tilgængeligt fra PowerBI.com, understøtter Microsoft Dynamics AX-version 7.0 og 7.0.1. Du kan finde flere oplysninger om, hvordan du forbinder og indlæser dine Dynamics AX-data, under [Adgang til Power BI-indhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Konfiguration af hovedkonto
Da organisationer ønsker, at passiver og omsætningsbeløb skal vises som positive beløb i rapporter, er konfigurationen af hovedkonti vigtig. For at disse hovedkonti skal kunne vises som positive beløb, skal hovedkontotypen indstilles til **Passiv** eller **Indtægter**. Når disse kontotyper bruges, bruger rapportering via Power BI omvendt fortegn og viser beløbene som positive beløb.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Dashboard og rapporter, der er inkluderet i Power BI-indholdet
Dashboardet indeholder opsummerende datafelter, der er baseret på underliggende rapporter. Hvert felt indeholder opsummerende oplysninger for det indeværende år på tværs af alle virksomheder i en organisation. Her er nogle af felterne:

- Indløsning
- Samlet omsætning i år
- Samlede udgifter i år
- Nettoresultat i år
- Likviditetsgrad på kort sigt
- Samlede udgifter i år efter kontokategori
- Aktuel dækningsgrad
- Gæld/Samlede aktiver
- Faktisk vs budgetteret omsætning
- Faktureret omsætning i år
- Driftsudgiftsgrad i år
- Overskudsgrad i år
- Faktiske vs. budgetterede udgifter – Alle firmaer

Hvert felt er understøttet af en supplerende rapport. Disse rapporter indeholder både diagrammer og tabeller, der indeholder flere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                      | Rapportens oplysninger omfatter: |
|-----------------------------|--------------------------------------|
| Pengestrømsanalyse               | Kontanter efter juridisk enhed, kontanter pr. kvartal, samlede kontanter og kontanter efter konto<blockquote>[!NOTE]<br>Oplysningerne om kontanter pr. kvartal omfatter ikke primosaldi i det samlede beløb for første kvartal. Det viser det samlede nye posteringer, der bogføres i hvert kvartal.</blockquote> |
| Analyse af aktuel dækningsgrad      | Aktuel dækningsgrad efter juridisk enhed, aktuel dækningsgrad pr. kvartal og saldi for omsætningsaktiver og kortfristet gæld |
| Analyse af likviditetsgrad på kort sigt        | Likviditetsgrad på kort sigt efter juridisk enhed, likviditetsgrad på kort sigt pr. kvartal og saldi for kontanter, tilgodehavender og kortfristet gæld |
| Analyse af vareforbrug | Vareforbrug (COGS) efter juridisk enhed, vareforbrug i år og sidste år pr. kvartal, vareforbrug i forhold til salg efter juridisk enhed, samlet vareforbrug og vareforbrug i forhold til salg i procent |
| Analyse af arbejdskapital    | Arbejdskapital efter juridisk enhed, arbejdskapital pr. kvartal, omsætningsaktiver, kortfristet gæld og samlet arbejdskapital |
| Analyse af aktiver og gæld     | Afkast af samlede aktiver og gæld i forhold til de samlede aktiver efter juridisk enhed, gæld i forhold til samlede aktiver og afkast for samlede aktiver pr. kvartal i forhold til dato, aktiver og passiver |
| Analyse af overskudsgrad      | Faktisk og budgetteret overskudsgrad efter juridisk enhed, overskudsmarkering pr. kvartal, overskudsgrad i procent og overskudsgrad |
| Analyse af nettoresultat         | Faktisk og budgetteret nettoresultat efter juridisk enhed, nettoresultat i år og sidste år og udgifter i forhold til nettoresultat i procent |
| Analyse af indtjening           | Faktisk og budgetteret overskud før renter og skat (EBIT) efter juridisk enhed, EBIT i år og sidste år, udgifter i forhold til omsætning i procent og faktiske og budgetterede udgifter i forhold til indtægter |
| Analyse af omsætning            | Samlet omsætning, samlede faktiske og budgetterede omsætning efter juridisk enhed, samledt omsætning i år og sidste år, afvigelse i omsætningsbudget efter juridisk enhed og samlet af omsætning i indeværende og sidste periode |
| Udgiftsanalyse            | Samlede udgifter, faktiske i forhold til budgetterede samlede udgifter efter juridisk enhed, samlede faktiske og budgetterede samlede udgifter pr. kvartal, samlede udgifter efter kontokategori og driftsudgiftsgrad |
| Analyse af faktureret omsætning     | Samlede tilgodehavender, samlede tilgodehavender efter juridisk enhed, samlede tilgodehavender pr. kvartal, og saldi for konti med tilgodehavender<blockquote>[!NOTE]<br>Oplysningerne omfatter ikke primosaldi for debitorfinanskonti. De viser totalen for nye transaktioner, der er bogført til Debitorer.</blockquote> |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Hvis du vil finde flere oplysninger om filtrering og fastgørelse i Power BI, skal du se [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
Følgende enheder blev brugt som grundlag for Power BI-indholdet til **Driftsregnskab**:

**Aggregér dataenheder**

- **GeneralLedgerActivities** – Denne enhed aggregerer finanssaldi efter kontokategori.
- **BudgetActivities** – Denne enhed aggregerer budgetsaldi efter kontokategori.

**Dataenheder**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Finans
- ChartofAccounts

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. De beregnede mål bruges til at beregne nøgletal (KPI'er) og rapporter, der bruges i indholdet. Som standard omfatter indholdet data for de sidste tre år og et år frem. Hvis du vil medtage yderligere beregninger i rapporter og dashboard, kan du redigere [Microsoft Excel-projektmappen](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne projektmappe er den standarddatamodel, der blev brugt til at oprette indholdet. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.
