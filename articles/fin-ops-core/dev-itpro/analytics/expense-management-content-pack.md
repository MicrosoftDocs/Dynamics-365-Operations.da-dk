---
title: Power BI-indhold til udgiftsstyring
description: Dette emne beskriver, hvad der er omfattet af Power BI-indholdspakken til udgiftsstyring.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 9391676beea6aac831648d5fa55eae5eba3f6397
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682791"
---
# <a name="expense-management-power-bi-content"></a>Power BI-indhold til udgiftsstyring

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvad der er omfattet af Power BI-indholdet til udgiftsstyring. 

## <a name="overview"></a>Overblik
Der er to Power BI-indholdspakker tilgængelige, som kan anvendes sammen med udgiftsstyring i version 8.1 og nyere. 
- Der er et personligt dashboard, som er designet til medarbejdere, der indsender udgiftsrapporter. 

  Dashboardet er skræddersyet med henblik på at tilvejebringe centrale oplysninger til enkeltpersoner vedrørende ikke-sendte og sendte beløb samt historik for og indsigt i posteringshistorikken for udgifter. Det personlige dashboard er en enkelt side, som indeholder de vigtigste oplysninger for brugeren.

- Der er et administratordashboard, som er designet til kreditormedarbejdere og -ansvarlige. Dashboardet er skræddersyet til at spore og rapportere de samlede medarbejderudgifter. Det tilvejebringer centrale udgiftsværdier såsom ikke-sendte udgifter, kilometertal og de gennemsnitlige beløb i udgiftsrapporterne. Det anvender transaktionsdata og tilvejebringer samlede oversigter over udgiftsstyring på tværs af alle virksomheder. Det tilvejebringer endvidere en opdeling pr. medarbejder med mulighed for at tilføje data fra den økonomiske dimension. Indholdet i analyser af administratorudgifter omfatter: 
  - En overbliksside med centrale værdier vedrørende udgiftsbeløb og indsigt i kladder, processer og fuldførte udgiftsrapporter. 
  - En side med medarbejderstatistikker med henblik på en gennemgang af en medarbejders individuelle detaljer opdelt på tid, omkostningstype og statistikgruppe. 
  - En side med medarbejdersammenligning for at sammenligne flere medarbejdere over tid. 

Alle beløb vises i virksomhedens valuta. Data for alle virksomheder vises, men det er muligt at tilføje et virksomhedsfilter. 

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet
Du kan finde Power BI-indholdet "Expense Admin Dashboard.pbix" og "Expense Personal Dashboard.pbix" i biblioteket "Delte aktiver" i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Indholdet er tilgængeligt fra den udgiftsansvarliges arbejdsområde som en del af Power Bi-indholdet. Alle udgiftsejere kan tilgå deres egne personlige udgifter, hvorimod alene kreditormedarbejdere og -ansvarlige har adgang til administratorindholdet, hvor de kan se alle brugerens udgiftsdata.

## <a name="refreshing-the-power-bi-content"></a>Opdatering af Power BI-indholdet
Power BI-indholdet for udgiftsstyring kræver, at målingerne TrvBiExpenseMeasurement og BudgetActivityMeasure opdateres via enhedslagret. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrikker, der er inkluderet i Power BI-indholdet
Indholdet omfatter et sæt rapportsider. Hver side består af en række mål, som er visualiseret som diagrammer, felter og tabeller. I nedenstående tabel vises en oversigt over visualiseringerne i Power BI-indholdet.

**Analyse af personlige udgifter**

| Rapportside | Visualisering                             |
|-------------|-------------------------------------------|
| Mine udgifter | Beløb for kørsel                         |
|             | Udgiftsrapporter under behandling                |
|             | Nr. om ikke-sendte udgifter               |
|             | Skyldige personlige udgifter              |
|             | Ikke-sendt beløb                        |
|             | Sendt beløb                          |
|             | Afventende refusionsbeløb             |
|             | Udgiftsrapporter med beløb og status   |
|             | Indsendte, men ikke godkendte, udgiftsrapporter  |
|             | Udgifter fordelt på omkostningstype                     |
|             | Udgifter fordelt på forhandler                      |
|             | Udgifter fordelt på behandlede udgifter            |
|             | Udgifter fordelt på projekt                       |
|             | Det samlede transaktionsbeløb over tid        |

**Analyse af administratorudgifter**

| Rapportside         | Visualisering                           |           
|---------------------|-----------------------------------------|
| Udgiftsoversigt    | Kladde med udgiftsbeløb                   |
|                     | Antal udgiftslinjer i kladden           |
|                     | Udgiftslinjer i kladden                     |
|                     | Overtrædelser af politikken for udgiftsrapporter        |
|                     | Udestående beløb                      |
|                     | Indsendte, men ikke godkendte, udgifter       |
|                     | Godkendte udgifter                       |
|                     | Samlet udgiftsbeløb                    |
|                     | Sammendrag af udgiftsrapporter                |
|                     | Udgifter fordelt på omkostningstype                   |
|                     | Udgifter fordelt på forhandler                    |
|                     | Udgifter fordelt på medarbejdere                   |
|                     | Udgifter i forhold til projekt                     |
| Sammenligning af medarbejdere | Udgiftsbeløb                         |
|                     | Udgiftsbeløb over tid fordelt på medarbejdere   |
| Medarbejderstatistikker | Udgiftsrapporter fordelt på omkostningstype            |
|                     | Personlige udgifter                       |
|                     | Udgiftsrapporter fordelt på statistikgrupper     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]