---
title: Oversigt over behovsprognose
description: Behovsprognoser bruges til at forudsige uafhængigt behov fra salgsordrer og afhængigt behov ved ethvert afkoblingspunkt for debitorordrer. De forbedrede reduceringsregler for behovsprognoser i er en ideel løsning til massetilpasning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27c9bf32a88858ec2d2214f18ff96138c29e59bc
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815151"
---
# <a name="demand-forecasting-overview"></a>Oversigt over behovsprognose

[!include [banner](../includes/banner.md)]

Behovsprognoser bruges til at forudsige uafhængigt behov fra salgsordrer og afhængigt behov ved ethvert afkoblingspunkt for debitorordrer. De forbedrede reduceringsregler for behovsprognoser i er en ideel løsning til massetilpasning.

For at generere prognosegrundlaget overføres en oversigt over historiske transaktioner til en Microsoft Azure Machine Learning-tjeneste, der er placeret på Azure. Da denne tjeneste ikke er delt mellem brugere, kan den nemt tilpasses til branchespecifikke behov. Du kan bruge Supply Chain Management til at visualisere prognosen, justere prognosen og få vist nøgletal (KPI'er) om prognosenøjagtigheden.

## <a name="key-features-of-demand-forecasting"></a>Nøglefunktioner i behovsprognoser
Her er nogle af de vigtigste funktioner i behovsprognoser:

-   Generere statistisk budgetgrundlag, der er baseret på historiske data.
-   Bruge et dynamisk sæt prognosedimensioner.
-   Visualisere behovstendenser, konfidensintervaller og justeringer af prognosen.
-   Tillade, at den justerede prognose bruges i planlægningsprocesser.
-   Fjerne afvigelser.
-   Oprette målinger af prognosenøjagtighed.

## <a name="major-themes-in-demand-forecasting"></a>Overordnede temaer i behovsprognoser
Tre overordnede temaer er implementeret i behovsprognoser:

-   **Modularitet** – behovsprognoser er modulære og lette at konfigurere. Du kan slå funktionen til og fra ved at ændre konfigurationsnøglen under **Handel** &gt; **Lagerbudget** &gt; **Behovsprognoser**.
-   **Genbrug af Microsoft-stakken** – Microsoft lancerede Machine Learning platformen i februar 2015. Med Machine Learning, som nu er en del af Microsoft Cortana Analytics Suite, kan du hurtigt og nemt lave forsøg med fremtidsanalyser, f.eks. forsøg med behovsestimeringer, ved at bruge algoritmerne R eller Python-programmeringssprogene og en enkel grænseflade med træk og slip.
    -   Du kan downloade forsøg med behovsprognoser, ændre dem, så de svarer til dine forretningsmæssige behov, udgive dem som en webtjeneste på Azure og bruge dem til at generere behovsprognoser. Forsøgene kan downloades, hvis du har købt et abonnement på Supply Chain Management til en produktionsplanlægger som bruger på enterprise-niveau.
    -   Du kan hente alle aktuelt tilgængelige forsøg med fremtidsanalyse af behov fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Hvor forsøg med behovsprognoser automatisk integreres i Supply Chain Management, skal kunder og partnere kunne håndtere integrationen af de forsøg, de downloader fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Forsøg fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) er derfor ikke ligetil at bruge som forsøg med behovsprognoser i Finance and Operations. Du skal ændre koden for forsøg, så de bruger Finance and Operations' API (application programming interface).
    -   Du kan oprette dine egne forsøg i Microsoft Azure Machine Learning Studio, udgive dem som tjenester på Azure og bruge dem til at generere behovsprognoser.
    -   Hvis du ikke har brug for høj ydeevne, eller hvis du ikke kræver, at en stor mængde data skal behandles, kan du bruge det gratis Machine Learning-niveau. Vi anbefaler, at du altid starter fra dette niveau, især under implementerings- og testfaserne. Hvis du kræver højere ydeevne og ekstra lagerplads, kan du bruge Machine Learning-standardniveauet. Dette niveau kræver et Azure-abonnement og indebærer ekstra omkostninger. Få oplysninger om priser på Machine Learning under [Machine Learning Studio-prisssætning](https://aka.ms/machine-learning-price-info).
-   **Prognosereduktion ved ethvert afkoblingspunkt** – Behovsprognoser bygger på denne funktion, hvor du kan forudsige både afhængigt og uafhængigt behov ved et hvilket som helst afkoblingspunkt.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlæggende arbejdsgang ved behovsprognoser
Det følgende diagram viser den grundlæggende arbejdsgang ved behovsprognoser. 

[![Introduktion til behovsprognoser](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Oprettelse af behovsprognose starter i Supply Chain Management. Historiske transaktionsdata fra Supply Chain Management-transaktionsdatabasen indsamles og udfylder en midlertidig tabel. Denne midlertidige tabel indføres senere en Machine Learning-tjeneste. Ved at foretage minimal tilpasning kan du slutte forskellige datakilder i den midlertidige tabel. Datakilder kan indeholde Microsoft Excel-filer, filer med kommaseparerede værdier (CSV) og data fra Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Du kan derfor generere behovsprognoser, der tager højde for historiske data, som er spredt mellem flere systemer. Masterdata som f.eks. varenavne og måleenhederne skal være de samme på tværs af de forskellige datakilder.

Hvis du bruger behovsprognose i forsøg med Machine Learning, prøver de at finde det bedste match mellem fem tidsserieprognosemetoder for at beregne et prognosegrundlag. Parametre for disse prognosemetoder administreres i Supply Chain Management. 

Prognoserne, de historiske data og de ændringer, der er foretaget i behovsprognoserne i tidligere gentagelser, er derefter tilgængelige i Supply Chain Management. 

Du kan bruge Supply Chain Management til at visualisere og ændre prognosegrundlaget. Manuelle justeringer skal godkendes, før prognoserne kan bruges til planlægning.

## <a name="limitations"></a>Begrænsninger
Behovsprognoser er et værktøj, der hjælper kunderne i produktionsbranchen med at generere prognoseprocesser. Det tilbyder den grundlæggende funktionalitet i en løsning til behovsprognoser og er designet, så den nemt kan udvides. Behovsprognoser er måske ikke den bedste valgmulighed for kunder inden for brancher som detailhandel, grossister, lagersteder, transport eller andre professionelle tjenester.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Konfigurere behovsprognoser](demand-forecasting-setup.md)

[Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)

[Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)

[Autorisere en justeret prognose](authorize-adjusted-forecast.md)

[Overvåge prognosenøjagtighed](monitor-forecast-accuracy.md)

[Fjerne afvigende fra historiktransaktionsdata, når du beregner en efterspørgselsprognose](remove-historical-outliers-calculating-demand-forecast.md)

[Udvide behovsprognosefunktionen](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



