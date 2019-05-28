---
title: Generere et statistisk budgetgrundlag
description: Denne artikel indeholder oplysninger om de parametre og filtre, der bruges i beregningen af behovsprognoser.
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
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f2ccb8c0b4d7c4755e0b8dc66539e165265090
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546311"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Generere et statistisk budgetgrundlag

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om de parametre og filtre, der bruges i beregningen af behovsprognoser. 

Når du opretter en budgetplan, skal du først angive de parametre og filtre, der bruges i beregningen. Du kan f.eks. oprette budgetplan, der estimerer behovet for en bestemt virksomhed baseret på transaktionsdata fra sidste år, for den kommende måned og for en udvalgt gruppe af varer. 

Hvis du vil generere en behovsprognose, skal du gå til **Overordnet planlægning &gt; Prognose &gt; Behovsprognose &gt; Generér statistisk budgetgrundlag**. 

Prognosefilsættet kan vælges på tidspunktet for prognosegenereringen. De tilgængelige værdier er: Dag, Uge og Måned. 

Det antal filsæt, for hvilket der skal genereres en prognose, indstilles i feltet **Prognosehorisont**. 

Når prognosestrategien er indstillet til **Kopiér over historisk efterspørgsel**, ignoreres slutningen af den historiske horisont. Systemet kopierer antallet af filsæt, der er angivet i feltet **Prognosehorisont**, til prognosebehovet, hvor der startes fra den dato, der er indstillet i feltet **Fra dato** under **Historisk horisont**. Ved at kopiere historisk behov fra en bestemt dato frem kan produktionsplanlæggere lægge planen for næste kvartal på to måder:

-   Ved at kopiere behovet fra samme kvartal sidste år.
-   Ved at kopiere behovet fra forrige kvartal.

For at undgå forvirring i produktionsplanerne kan et bestemt antal prognosefilsæt fryses. Dette antal er angivet i feltet **Låsningstidshorisont**. På siden **Justeret behovsprognose** er cellerne for de frosne filsæt deaktiveret for at give en visuel indikation af, at disse værdier ikke bør ændres. 

Startdatoen for behovsprognosegrundlaget behøver ikke at være den aktuelle dato eller en dato i fremtiden. Hvis du vil angive en anden startdato, skal du bruge feltet **Startdato for prognosegrundlag – Fra-dato**. I juni kan brugere for eksempel oprette en prognose for næste år. Da prognosefilsættet mellem slutningen af det historiske behov og starten på grundlaget mangler, er forudsigelserne muligvis ikke nøjagtige. Hvis du bruger den tjeneste til behovsprognoser i Microsoft Dynamics 365 for Finance and Operations, er der fire måder, hvorpå du kan udfylde hullerne. Du kan vælge den ønskede metode ved at indstille parameteren MISSING\_VALUE\_SUBSTITUTION på siden **Parametre til behovsprognoser**. 

Feltet **Startdato for prognosegrundlag** - **Fra-dato** skal være indstillet til begyndelsen på filsættet, f.eks. i USA, en søndag, hvis prognosefilsættet er ugen. Systemet justerer automatisk feltet **Startdato for prognosegrundlag** - **Fra-dato**, så den matcher begyndelsen på prognosefilsættet. 

Feltet **Startdato for prognosegrundlag** - **Fra-dato** kan indstilles til en dato i fortiden. Med andre ord er det muligt at generere en behovsprognose i fortiden. Dette er nyttigt, fordi brugerne får mulighed for at justere parametrene i prognosetjenesten, så den statistiske prognose, der er genereret i fortiden, svarer til det faktiske historiske behov. Brugere kan derefter fortsætte med at bruge disse parameterindstillingerne til at generere et statistisk prognosegrundlag for fremtiden. 

Manuelle justeringer, der er foretaget i tidligere gentagelser af behovsprognoser, kan automatisk anvendes på den grundlagsprognose, hvis afkrydsningsfeltet **Overfør manuelle justeringer til behovsprognosen**. Hvis afkrydsningsfeltet er markeret, føjes de manuelle justeringer ikke til grundlagsprognosen – men de slettes ikke. Manuelle justeringer, der er foretaget på prognose, kan kun slettes, når prognosen importeres. Det gøres ved at fjerne markeringen af **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget**. Manuelle justeringer gemmes på godkendelsestidspunktet. Hvis en bruger derfor foretager manuelle justeringer i prognosen, men ikke godkender prognosen tilbage til Dynamics 365 for Finance and Operations, går ændringerne tabt. Få flere oplysninger om manuelle justeringer, og hvordan de fungerer, under [Godkendelse af den justerede prognose](authorize-adjusted-forecast.md). 

Behovsprognosegenerering kan have et navn og kommentarer, så brugerne kan identificere den prognose, der er blevet genereret. Disse værdier er synlige i oversigten over prognosegenereringen på siden **Genereringshistorik for statistisk budgetgrundlag**. 

Den interne planlægningsgruppe i firmaet, varefordelingsnøgler og andre filtre kan anvendes på tidspunktet for prognosegenerering. Disse kan bruges til at forbedre ydeevnen eller opdele dataene i håndterbare stykker. Bemærk dog, at en behovsprognose ikke genereres for medlemmerne af en varefordelingsnøgle, der ikke er knyttet til en intern planlægningsgruppe i et firma, selvom den valgte varefordelingsnøgle er valgt i forespørgslen. 

**Tip**: Nogle gange kan brugere modtager fejl under generering af en behovsprognose, eller prognosegenerering færdiggøres uden sessionslogfil. Dette kan ske på grund af overskydende data i den forespørgsel, der tidligere blev brugt til oprettelse af prognose. Du kan løse dette problem ved at klikke på **Vælg** for at åbne siden **Forespørgsel**, klik på **Nulstil** og derefter generere grundlagsprognosen igen. 

Hvis prognosen ikke er oprettet for en lang række varer, men for eksempel for én vare eller én varefordelingsnøgle ad gangen, kan du opnå bedre ydeevne ved derefter at vælge afkrydsningsfeltet **Brug svartilstand for anmodning** under fanen **Overordnet planlægning – Opsætning – Behovsprognose** - **Parametre til behovsprognoser – Azure Machine Learning**.

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Konfigurere behovsprognoser](demand-forecasting-setup.md)

[Foretage manuelle reguleringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)

[Godkende den justerede prognose](authorize-adjusted-forecast.md)



