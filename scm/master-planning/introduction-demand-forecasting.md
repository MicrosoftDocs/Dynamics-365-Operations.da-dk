---
title: "Efterspørgsel, prognoser oversigt"
description: "Behovsprognoser bruges til at forudsige uafhængigt behov fra salgsordrer og afhængigt behov ved ethvert afkoblingspunkt for debitorordrer. Den forbedrede Efterspørgselsprognosebehov reduktion regler er den ideelle løsning til masse tilpasning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Efterspørgsel, prognoser oversigt

Behovsprognoser bruges til at forudsige uafhængigt behov fra salgsordrer og afhængigt behov ved ethvert afkoblingspunkt for debitorordrer. Den forbedrede Efterspørgselsprognosebehov reduktion regler er den ideelle løsning til masse tilpasning.

For at generere prognosegrundlaget overføres en oversigt over historiske transaktioner til en Microsoft Azure Machine Learning-tjeneste, der er placeret på Azure. Da denne tjeneste ikke er delt mellem brugere, kan den nemt tilpasses til branchespecifikke behov. Du kan bruge Dynamics 365 for operationer til at visualisere budgettet, justere budgettet og få vist nøgletal (KPI'er) om budgetterede nøjagtighed.

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

-   **Modularitet** – behovsprognoser er modulære og lette at konfigurere. Du kan slå funktionen til og fra ved at ændre configuration key til **handel**&gt;**lagerbudgettet**&gt;**efterspørgsel prognoser**.
-   **Genbrug af stakken Microsoft** – Microsoft lanceret Machine Learning platform i februar 2015. Machine Learning, som nu er en del af Microsoft Cortana Analytics Suite, kan du hurtigt og nemt oprette fremtidsanalyser forsøg, som efterspørgsel skøn eksperimenter ved hjælp af algoritmer R eller Python programmeringssprog og en enkel træk-og-slip grænseflade.
    -   Du kan hente den Dynamics 365 for operationer efterspørgsel, prognoser forsøg, ændre dem for at opfylde virksomhedens behov, udgive dem som en webtjeneste på Azure og bruge dem til at generere efterspørgselsprognoser. Forsøg kan downloades, hvis du har købt en Dynamics 365 operationer abonnement til en produktionsplanlægger som enterprise-niveau bruger.
    -   Du kan hente alle aktuelt tilgængelige forsøg med fremtidsanalyse af behov fra [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/). Der er automatisk integreret Dynamics-365 for operationer efterspørgsel, prognoser Eksperimenter med Dynamics 365 for operationer, kunder og partnere skal håndtere integrationen af forsøg, de henter fra den [Cortana Analytics galleri](https://gallery.cortanaanalytics.com/). Derfor forsøg fra den [Cortana Analytics galleri](https://gallery.cortanaanalytics.com/) ikke er så ligetil bruges som Dynamics-365 for operationer efterspørgsel, prognoser forsøg. Du skal ændre koden for forsøg, så de bruger Dynamics-365 for operationer programmeringsgrænseflade (API).
    -   Du kan oprette dine egne forsøg i Microsoft Azure Machine Learning Studio, udgive dem som tjenester på Azure og bruge dem til at generere behovsprognoser.
    -   Hvis du ikke har brug for høj ydeevne, eller hvis du ikke kræver, at en stor mængde data skal behandles, kan du bruge det gratis Machine Learning-niveau. Vi anbefaler, at du altid starter fra dette niveau, især under implementerings- og testfaserne. Hvis du kræver højere ydeevne og ekstra lagerplads, kan du bruge Machine Learning-standardniveauet. Dette niveau kræver et Azure-abonnement og indebærer ekstra omkostninger. Få oplysninger om priser på Machine Learning under <http://aka.ms/machine-learning-price-info>.
-   **Budgetteret reduktion når som helst decoupling** – efterspørgsel, prognoser i Dynamics 365 for builds af operationer på denne funktion, hvor du kan forudsige både afhængige og uafhængige behov når som helst decoupling.

## <a name="basic-flow-in-demand-forecasting"></a>Grundlæggende arbejdsgang ved behovsprognoser
Det følgende diagram viser den grundlæggende arbejdsgang ved behovsprognoser. 

[![efterspørgsel diagram for forudsigelse Introduktion](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Efterspørgselsprognosebehov generation starter i Dynamics 365 for operationer. Historiske transaktionsdata fra Dynamics-365 for operationer transaktionsdatabasen indsamles og udfylder en midlertidig tabel. Denne midlertidige tabel indføres senere en Machine Learning-tjeneste. Udfører minimal tilpasning, kan du slutte forskellige datakilder i den midlertidige tabel. Datakilder kan omfatte Microsoft Excel-filer, filer med kommaseparerede værdier (CSV) og data fra Microsoft Dynamics AX 2009 og Microsoft Dynamics AX 2012. Du kan derfor oprette efterspørgselsprognoser, anser historiske data, som er spredt mellem flere systemer. Masterdata som f.eks. varenavne og måleenhederne skal være de samme på tværs af de forskellige datakilder.

Hvis du bruger Dynamics-365 for operationer efterspørgsel, prognoser Machine Learning forsøg, de ser ud til den bedste tilpasning mellem fem gang serie forudsigelse metoder til at beregne en oprindelig prognose. Parametre til metoderne forudsigelse administreres i Dynamics 365 for operationer. 

Budgetterne, historiske data og de ændringer, der er foretaget efterspørgselsprognoser i tidligere gentagelser er derefter tilgængelige i Dynamics 365 for operationer. 

Du kan bruge Dynamics 365 for operationer til at visualisere og ændre de oprindelige overslag. Manuelle justeringer skal godkendes, før prognoserne kan bruges til planlægning.

## <a name="limitations"></a>Begrænsninger
Behov budgettering i Dynamics 365 for operationer er et værktøj, der hjælper kunderne i fremstillingsindustrien oprette forudsigelse processer. Det tilbyder den grundlæggende funktionalitet af en efterspørgsel, prognoser løsning og er udviklet, så den nemt kan udvides. Behov for budgettering, ikke kan være bedst egnet til kunder inden for brancher som Detail, varer, opbevaring, transport eller andre professionelle services.

<a name="see-also"></a>Se også
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


