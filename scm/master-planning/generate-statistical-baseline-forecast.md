---
title: Opret en statistisk oprindelige budget
description: Denne artikel indeholder oplysninger om de parametre og filtre, der bruges i beregningen af behovsprognoser.
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
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Opret en statistisk oprindelige budget

Denne artikel indeholder oplysninger om de parametre og filtre, der bruges i beregningen af behovsprognoser. 

Når du opretter en budgetplan, skal du først angive de parametre og filtre, der bruges i beregningen. Du kan f.eks. oprette budgetplan, der estimerer behovet for en bestemt virksomhed baseret på transaktionsdata fra sidste år, for den kommende måned og for en udvalgt gruppe af varer. 

Du kan oprette en efterspørgselsprognose ved at gå til **Master planning &gt;budgettering &gt;efterspørgsel prognoser &gt;Generer statistiske oprindelig budgetteret**. 

Prognosefilsættet kan vælges på tidspunktet for prognosegenereringen. De tilgængelige værdier er: Dag, Uge og Måned. 

Det antal filsæt, for hvilket der skal genereres en prognose, indstilles i feltet **Prognosehorisont**. 

Når prognosestrategien er indstillet til **Kopiér over historisk efterspørgsel**, ignoreres slutningen af den historiske horisont. Kopieres automatisk antallet filsæt, der er angivet i den **prognose horisonten** til forecastbehov, startende fra den dato, der er angivet i den **fra dato** felt under **historiske vandret**. Ved at kopiere historisk behov fra en bestemt dato frem kan produktionsplanlæggere lægge planen for næste kvartal på to måder:

-   Ved at kopiere behovet fra samme kvartal sidste år.
-   Ved at kopiere behovet fra forrige kvartal.

For at undgå forvirring i produktionsplanerne kan et bestemt antal prognosefilsæt fryses. Dette antal er angivet i feltet **Låsningstidshorisont**. På siden **Justeret behovsprognose** er cellerne for de frosne filsæt deaktiveret for at give en visuel indikation af, at disse værdier ikke bør ændres. 

Startdatoen for behovsprognosegrundlaget behøver ikke at være den aktuelle dato eller en dato i fremtiden. Hvis du vil angive en anden startdato, skal du bruge feltet **Startdato for prognosegrundlag – Fra-dato**. I juni kan brugere for eksempel oprette en prognose for næste år. Da prognosefilsættet mellem slutningen af det historiske behov og starten på grundlaget mangler, er forudsigelserne muligvis ikke nøjagtige. Hvis du bruger Microsoft Dynamics 365 for operationer efterspørgsel, prognoser service, er der fire måder, som du kan udfylde de huller, der mangler. Du kan vælge den metode, du vil ved at angive manglende\_værdi\_erstatning parameter på den **efterspørgsel, prognoser parametre** side. 

Den **oprindelige budget startdato for** - **fra dato** har felt er angivet til starten af en budgetteret filsæt, for eksempel i USA, en søndag, hvis forudsigelse bucket er uge. Systemet justerer automatisk den **oprindelige budget startdato for** - **fra dato** felt skal matche starten af en budgetteret filsæt. 

Den **oprindelige budget startdato for** - **fra dato** felt kan du vælge en dato i tidligere. Med andre ord er det muligt at generere en behovsprognose i fortiden. Dette er nyttigt, fordi brugerne får mulighed for at justere parametrene i prognosetjenesten, så den statistiske prognose, der er genereret i fortiden, svarer til det faktiske historiske behov. Brugere kan derefter fortsætte med at bruge disse parameterindstillingerne til at generere et statistisk prognosegrundlag for fremtiden. 

Manuelle justeringer, der er foretaget i tidligere gentagelser af behovsprognoser, kan automatisk anvendes på den grundlagsprognose, hvis afkrydsningsfeltet **Overfør manuelle justeringer til behovsprognosen**. Hvis afkrydsningsfeltet er markeret, føjes de manuelle justeringer ikke til grundlagsprognosen – men de slettes ikke. Manuelle justeringer, der er foretaget på prognose, kan kun slettes, når prognosen importeres. Det gøres ved at fjerne markeringen af **Importér de manuelle justeringer, der er foretaget af behovsprognosegrundlaget **. Manuelle justeringer gemmes på godkendelsestidspunktet. Derfor, hvis en bruger foretager manuelle justeringer i budgettet, men ikke godkende budgettet tilbage til Dynamics 365 for operationer, ændringerne går tabt. Yderligere oplysninger om manuelle justeringer, og hvordan de fungerer, se [godkendelse af den korrigerede budget](authorize-adjusted-forecast.md). 

Behovsprognosegenerering kan have et navn og kommentarer, så brugerne kan identificere den prognose, der er blevet genereret. Disse værdier er synlige i oversigten over prognosegenereringen på siden **Genereringshistorik for statistisk budgetgrundlag**. 

Den interne planlægningsgruppe i firmaet, varefordelingsnøgler og andre filtre kan anvendes på tidspunktet for prognosegenerering. Disse kan bruges til at forbedre ydeevnen eller opdele dataene i håndterbare stykker. Bemærk dog, at en behovsprognose ikke genereres for medlemmerne af en varefordelingsnøgle, der ikke er knyttet til en intern planlægningsgruppe i et firma, selvom den valgte varefordelingsnøgle er valgt i forespørgslen. 

**Tip**: Nogle gange kan brugere modtager fejl under generering af en behovsprognose, eller prognosegenerering færdiggøres uden sessionslogfil. Dette kan ske på grund af overskydende data i den forespørgsel, der tidligere blev brugt til oprettelse af prognose. Du kan løse dette problem ved at klikke på **Vælg** for at åbne siden **Forespørgsel**, klik på **Nulstil** og derefter generere grundlagsprognosen igen. 

Hvis budgettet ikke er oprettet for en stor række elementer, men, for eksempel for en vare eller en varefordelingsnøgle ad gangen og derefter for at opnå bedre ydeevne, skal du vælge den **bruger anmodning om svar tilstand** afkrydsningsfeltet under den **Master planlægning - Setup - Demand forecasting** - **efterspørgsel, prognoser parametre - Azure Machine Learning** under fanen.

<a name="see-also"></a>Se også
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


