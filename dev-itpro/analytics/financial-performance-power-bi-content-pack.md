---
title: "Økonomisk ydeevne strøm BI-indhold"
description: "Dette emne beskriver Microsoft Dynamics 365 for operationer økonomisk Performance indhold pack til Microsoft Power BI. Den beskriver dashboard og rapporter, der er inkluderet i pakken med indhold og giver oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack."
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Økonomisk ydeevne strøm BI-indhold

Dette emne beskriver Microsoft Dynamics 365 for operationer økonomisk Performance indhold pack til Microsoft Power BI. Den beskriver dashboard og rapporter, der er inkluderet i pakken med indhold og giver oplysninger om datamodel og enheder, der blev brugt til at opbygge indhold pack.

<a name="accessing-the-content-pack"></a>Adgang til indhold pack
--------------------------

Der findes to versioner af økonomisk Performance indhold pack. En version er tilgængelig fra Microsoft Dynamics livscyklus Services (LCS), og den anden er tilgængelig fra PowerBI.com.

-   **Version, der er tilgængelige fra LCS:** indhold pack til de økonomiske resultater, der er tilgængelig fra LCS understøtter Microsoft Dynamics 365 af operationer version 1611 opdager. Du kan finde indhold pack i aktivbiblioteket delt i Remburser. Finde flere oplysninger om, hvordan du henter indhold pack og forbinde den til din Microsoft Dynamics-365 for operationer data [Power BI indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).
-   **Version, der er tilgængelig fra PowerBI.com:** indhold pack til de økonomiske resultater, der er tilgængelig fra PowerBI.com understøtter Microsoft Dynamics AX-version 7.0 og 7.0.1. Finde flere oplysninger om at oprette forbindelse og indlæse din Dynamics 365 for operationer data [Access strøm BI indhold fra PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Konfigurationen af hovedkontoen
Da organisationer vil passiver og omsætningsbeløb skal vises som positive beløb i rapporter, er opsætningen af hovedkonti i Dynamics 365 for operationer er vigtigt. For disse hovedkonti, der skal vises som positive beløb, der skal angives hovedkontotypen til **ansvar** eller **indtægter**. Når der bruges disse kontotyper, vil rapportering via Microsoft Power BI omvendt fortegn og vises som positive beløb.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard og rapporter, der er inkluderet i pakken med indhold
Når du har knyttet indholdspakken til dine Dynamics 365 for Operations-data, viser dashboardet og rapporterne de finansielle data. Hvis du aldrig har brugt strøm BI før, kan du lære mere om det på den [automatiseret Learning side for strøm BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Dashboardet indeholder opsummerende datafelter, der er baseret på underliggende rapporter. Hvert felt indeholder opsummerende oplysninger for det indeværende år på tværs af alle virksomheder i en organisation. Her er nogle af fliserne:

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

Hver flise er understøttet af en supplerende rapport. Disse rapporter indeholder både diagrammer og tabeller, der indeholder flere oplysninger. Rapporterne er beskrevet i følgende tabel.

| Rapport                      | Rapportens oplysninger omfatter:                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pengestrømsanalyse               | Kontant ved juridisk enhed cash pr. kvartal, samlede kontante og kontant efter firma **Bemærk:** de **kontant pr. kvartal** rapport ikke indeholder primosaldi i det samlede beløb for første kvartal. Det viser samlet nye posteringer, der bogføres i hvert kvartal.                                                                                |
| Analyse af aktuel dækningsgrad      | Aktuel dækningsgrad efter juridisk enhed, aktuel dækningsgrad pr. kvartal og saldi for omsætningsaktiver og kortfristet gæld                                                                                                                                                                                                                              |
| Analyse af likviditetsgrad på kort sigt        | Hurtig forholdet efter juridisk enhed, hurtig forholdet kvartal og saldi til kontanter, konti, tilgodehavender og aktuelle passiver                                                                                                                                                                                                                      |
| Analyse af vareforbrug | Vareforbrug (COGS) efter juridisk enhed, vareforbrug i år og sidste år pr. kvartal, vareforbrug i forhold til salg efter juridisk enhed, samlet vareforbrug og vareforbrug i forhold til salg i procent                                                                                                                                                                                   |
| Analyse af arbejdskapital    | Arbejdskapital efter juridisk enhed, arbejdskapital pr. kvartal, omsætningsaktiver, kortfristet gæld og samlet arbejdskapital                                                                                                                                                                                                                   |
| Analyse af aktiver og gæld     | Afkast af samlede aktiver og gæld i forhold til de samlede aktiver efter juridisk enhed, gæld i forhold til samlede aktiver og afkast for samlede aktiver pr. kvartal i forhold til dato, aktiver og passiver                                                                                                                                                                                     |
| Analyse af overskudsgrad      | Faktisk og budgetteret overskudsgrad efter juridisk enhed, overskudsmarkering pr. kvartal, overskudsgrad i procent og overskudsgrad                                                                                                                                                                                                                       |
| Analyse af nettoresultat         | Faktisk og budgetteret nettoresultat efter juridisk enhed, nettoresultat i år og sidste år og udgifter i forhold til nettoresultat i procent                                                                                                                                                                                                                       |
| Analyse af indtjening           | Faktisk og budgetteret overskud før renter og skat (EBIT) efter juridisk enhed, EBIT i år og sidste år, udgifter i forhold til omsætning i procent og faktiske og budgetterede udgifter i forhold til indtægter                                                                                                                                                          |
| Analyse af omsætning            | Samlet omsætning, samlede faktiske og budgetterede omsætning efter juridisk enhed, samledt omsætning i år og sidste år, afvigelse i omsætningsbudget efter juridisk enhed og samlet af omsætning i indeværende og sidste periode                                                                                                                                                 |
| Udgiftsanalyse            | Samlede udgifter, faktiske i forhold til budgetterede samlede udgifter efter juridisk enhed, samlede faktiske og budgetterede samlede udgifter pr. kvartal, samlede udgifter efter kontokategori og driftsudgiftsgrad                                                                                                                                                                 |
| Analyse af faktureret omsætning     | Sum af debitorer, samlede tilgodehavender efter juridisk enhed, samlede tilgodehavender pr. kvartal og saldi for konti tilgodehavender **Bemærk:** rapporterne, der ikke medtager primosaldi for finanskonti konti tilgodehavender. De viser totalen for nye transaktioner, der er bogført til konti, debitorer. |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Hvis du vil finde flere oplysninger om filtrering og fastgørelse i Power BI, skal du se [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder
De data, der udfylder dashboard og rapporter i driftsregnskabet indhold pack er Dynamics 365 til data af handlinger. Følgende enheder blev brugt som grundlag for pakken med indhold: **sammenlægge data-enheder**

-   **GeneralLedgerActivities** – denne enhed samler finanssaldi af kontoarten.
-   **BudgetActivities** – denne enhed samler budgetsaldi af kontoarten.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Finans
-   ChartofAccounts

Disse enheder blev brugt til at oprette beregnede målpunkter i datamodellen. De beregnede målpunkter, der bruges til at beregne nøgletal (KPI'er) og rapporter, der bruges i indhold pack. Som standard omfatter indholdspakken data for de sidste tre år og et år frem. Hvis du vil medtage yderligere beregninger i rapporter og dashboard, kan du redigere [Microsoft Excel-projektmappen](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). Denne projektmappe er den standarddatamodel, der blev brugt til at oprette indholdspakken. Når du har foretaget ændringerne, kan du oprette en indholdspakke og et dashboard for organisationen, som indeholder de oplysninger, du har tilføjet.

## <a name="additional-resources"></a>Yderligere ressourcer
Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

-   [Dataenheder](..\data-entities\data-entities.md)
-   [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Tilføjelse af Power BI-felter til arbejdsområder](configure-power-bi-integration.md)



