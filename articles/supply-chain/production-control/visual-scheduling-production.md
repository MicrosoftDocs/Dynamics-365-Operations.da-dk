---
title: "Gantt-diagram til finplanlægning"
description: "Produktionsplanlæggere kan styre og optimere produktionsplaner ved hjælp af Gantt-diagrammer."
author: johanhoffmann
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5a4b0450cc76c8d9307b9b21b78a170afcc298e4
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="gantt-chart-for-job-scheduling"></a>Gantt-diagram til finplanlægning

[!include[banner](../includes/banner.md)]

Gantt-diagrammet er udviklet til at sætte produktionsplanlæggere i stand til at styre og optimere produktionsplanen. Gantt-diagrammet gør strømmen af operationer gennemskuelig og gør det let at justere produktionsplanen under hensyntagen til materiale- eller ressourceunderskud. Dette hjælper planlæggere med at udnytte de disponible ressourcer bedst muligt, minimere igangværende arbejde og optimere procestider for produktionsordrer.

Et Gantt-diagram er en visuel repræsentation af planlagte aktiviteter inden for et tidsinterval, der er defineret. Aktiviteterne, der er planlagt på ressourcer, der har en defineret kapacitet i en kapacitetskalender. Følgende typer aktiviteter kan vises i Gantt-diagrammet.

-   Planlagte job fra produktionsordrer.
-   Job fra planlagte produktionsordrer.
-   Finplanlagte projektaktiviteter af typen Timebudgetter.

Gantt-diagrammet kan åbnes i to forskellige visninger, **Ordrevisning** og **Ressourcevisning**[](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true). I **Ordrevisning** grupperes aktiviteter under produktionsordrer. Dette kan være nyttigt, hvis du f.eks. vil vedligeholde en oversigt over alle de job, der tilhører samme ordrer. I **Ressourcevisning** er alle job grupperet under individuelle ressourcer. Denne visning kan være nyttig, når du optimerer planen på ressourceniveau, f.eks. en maskine eller en gruppe af maskiner. Gantt-diagrammerne i illustrationerne nedenfor viser **Ordrevisning** og **Ressourcevisning** med følgende nøgleelementer:

1.  Gantt-diagramaktivitet
2.  Mangel på materialer-ikon
3.  Tilgængelighed af materiale-ikon
4.  Ordrens leveringsdato-ikon
5.  Kapacitetslinje

## <a name="order-view"></a>Ordrevisning

[![Ordrevisning](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Ressourcevisning
[![Ressourcevisning](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Aktiviteter
Aktiviteterne vises som søjler og er organiseret på en skala i tidsgitteret med planlagt start- og sluttidspunkt, så længden af søjlerne er proportional med den tid, der er nødvendig for at fuldføre aktiviteten. Aktiviteterne vises i henhold til en tidsskala. Du kan justere tidsskalaen i menuen, hvor du kan vælge en startdato og slutdato og en tidsenhed, f.eks., timer eller dage. Du kan angive fokus på et tidsinterval, hvor du vil administrere aktiviteter, ved at justere tidsskalaen. 

For at få et bedre overblik er der forskellige muligheder for at kontrollere farven på aktiviteter. Du kan konfigurere en enkelt farve for aktiviteter, bruge temafarven, der er det generelle farvetema til programmet, eller konfigurere farven, så den kontrolleres af farvekoden for produktionsordrer. 

Tidsintervallet for aktiviteter har en skygge i baggrunden. Perioder med en hvid skygge angiver et tidsinterval med defineret kapacitet på ressourcen for aktiviteten, mens perioder med en grå skygge angiver tidsintervaller uden defineret kapacitet. 

I venstre side af diagrammet er der flere oplysninger om aktiviteten, f.eks., ressourcen, som aktiviteten er planlagt på, og produktionsordrenummeret. Forbindelsen mellem job, der tilhører samme ordre, vises med en pil. 

Du kan få flere oplysninger om en aktivitet i dialogboksen Aktivitet. Dobbeltklik på aktiviteten for at åbne dialogboksen, eller vælg menuen **Oplysninger**. Du kan se den planlagte start- og slutdato og tidsoplysninger om, hvilke materialer aktiviteten er planlagt til at forbruge, i dialogboksen Aktivitet. 

Aktiviteterne kan grupperes i grupperingsniveauer. De viste grupperingsniveauer er hierarkiske og kan bruges til at foretage en logisk gruppering af aktiviteter. Hvis du f.eks. har et layout, hvor produktionsaktiviteter grupperes efter lokation, produktionsenheder, ressourcegrupper og ressourcer, kan du bruge de viste grupperingsniveauer til at gruppere aktiviteterne i overensstemmelse med dette layout. Grupperingsniveauerne kan udvides og skjules på enten individuelt grupperingsniveau eller for alle niveauer i diagrammet ved hjælp af knapperne **Udvid alle** og **Skjul alle** i menuen. Du kan også konfigurere grupperingsniveauer til at udvides eller skjules, når diagrammet åbnes.

### <a name="material-availability"></a>Materialers tilgængelighed

Gantt-diagrammet kan konfigureres til at give planlæggeren detaljerede oplysninger om materialestatus for de enkelte aktiviteter. Det kan f.eks. være nyttigt, hvis materiale er forsinket og påvirker produktionsplanen. I så fald fremhæves materialeproblemerne i Gantt-diagrammet for at hjælpe planlæggeren med at forstå konsekvenserne og foretage nødvendige justeringer. 

Et job vises med et ikon for mangel på materialer, hvis tidsplanens startdato for jobbet er senere end datoen for tilgængelighed af materialer, der forbruges af jobbet. Tilgængelighedsdatoen for materiale beregnes ud fra udligningsoplysninger i den dynamiske behovsplan. Mangel på materiale-ikonet vises for eksempel på et job, der forbruger materiale, der er udlignet mod en indkøbsordre, som har en tilgang, der er senere end den planlagte startdato for jobbet.

### <a name="indicator-of-material-availability-date"></a>Datoindikator for materialetilgængelighed

Når du opretter diagrammet til at få vist job med materialemangel, kan et ikon for visning af tilgængelighedsdatoen for materiale også vises for jobbet. Ikonet vises kun, hvis tilgængelighedsdatoen for materiale ligger inden for det definerede tidsinterval for diagrammet. Hvis tilgængelighedsdatoen for materiale ligger uden for det angivne tidsinterval, kan mere detaljerede oplysninger om tilgængelighed af materiale hentes på materialelisten i dialogboksen Job. På listen er der også et ikon, der viser forsinkede materialer til jobbet. Du kan omplanlægge et job med tilgængelighedsdatoen for materiale som startdato.

### <a name="indicator-of-order-delivery-date"></a>Indikator for ordreleveringsdato

Dette ikon angiver leveringsdatoen for en produktionsordre. Ikonet er kun synligt i ordrevisningen.

### <a name="capacity-bar"></a>Kapacitetslinje

Du kan konfigurere diagrammet til at vise en ressourcekapacitetslinje. Den indeholder en oversigt over ressourcekapacitet for en aktivitet i det angivne tidsinterval for diagrammet. Kapacitetslinjen vises ikke i de perioder, hvor ressourcen ikke er reserveret. I perioder, hvor ressourcen er reserveret, vises kapacitetslinjen som en optrukken streg. I perioder, hvor ressourcen er overbooket, er linjen tykkere og med en rød farve. Hvis to job f.eks. overlapper, vil kapacitetslinje angive en overbooking i tidsintervallet, hvor der er overlap. Kapacitetslinjen opdateres dynamisk, når du planlægger et job. Du kan aktivere kapacitetslinjen i menuen **Vis kapacitetslinje**. Den kan kun vises i **Ressourcevisning**. Hvis du vil have en mere detaljeret visning af kapacitetsbelastningen for en ressource, kan du bruge **Kapacitetsbelastning**-diagrammet, der kan åbnes i menuen eller genvejsmenuen for en valgt aktivitet.

## <a name="job-scheduling-in-the-gantt-chart"></a>Finplanlægning i Gantt-diagrammet
Gantt-diagrammet giver forskellige muligheder til at foretage reguleringer i produktionsplanen. I Gantt-diagrammet kan du omplanlægge aktiviteter som en interaktion med træk og slip eller fra en menu for tidsplanen. I planlægningsprocessen kan du tage ressourcekapacitet, ressourceegenskaber og materialebegrænsninger i betragtning.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Planlægge et job som en interaktion med træk og slip

Du kan omplanlægge job i tidsintervallet, der er defineret, som en interaktion med træk og slip. Du kan kun omplanlægge jobbet på den samme ressource, og du kan kun planlægge ét job ad gangen.

### <a name="schedule-a-job-from-the-menu"></a>Planlægge et job i menuen

I menuen **Finplanlægge** kan du planlægge et eller flere valgte job i diagrammet, der er baseret på en planlægningsretning og en planlagt datoangivelse. Der findes tre forskellige planlægningsretninger.

-   Fremad fra planlægningsdato
-   Bagud fra planlægningsdato
-   Fremad fra datoen for materialetilgængelighed

Det er ikke muligt at planlægge et job uden for det angivne tidsinterval i Gantt-diagrammet. Hvis du gør det, vil jobbet forblive ikke-planlagt, og du modtager fejlmeddelelsen "Jobbet kunne ikke planlægges inden for den indlæste tidsperiode".

### <a name="schedule-previous-jobs"></a>Planlæg foregående job

I et netværk af aktiviteter som f.eks. job, der tilhører samme produktionsordre, kan du bruge funktionen **Planlæg foregående job** til at planlægge de foregående job i forhold til et valgt job i netværket. I eksemplet nedenfor er den fremhævede aktivitet det valgte job. Diagrammet viser, før det foregående job er planlagt, og efter det foregående job er planlagt. 

[![Planlæg foregående job](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Planlæg efterfølgende job

Du kan bruge funktionen **Planlæg efterfølgende job** til at planlægge de næste job i forhold til et valgt job i et netværk af aktiviteter. I eksemplet nedenfor er den fremhævede aktivitet det valgte job. Diagrammet viser, før det næste job er planlagt, og efter det næste job er planlagt. 

[![Planlæg næste job](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Planlæg omkring job

Du kan bruge funktionen **Planlæg omkring job** til at planlægge det næste job og det foregående job i forhold til et valgt job i et netværk af aktiviteter. I eksemplet nedenfor er den fremhævede aktivitet det valgte job. Diagrammet viser, før et job er planlagt, og efter jobbet er planlagt. 

[![Planlæg omkring job](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Arranger job

Du kan bruge funktionen **Arranger** til at arrangere de valgte aktiviteter på samme ressource. Disse aktiviteter kan være i det samme netværk af aktiviteter, men de kan også tilhøre forskellige netværk. Når du bruger funktionen Arranger, vil tidsrum mellem de valgte aktiviteter blive elimineret. Du kan bruge denne funktion til at optimere kapacitetsudnyttelsen af ressourcerne. Diagrammet viser, før et job er planlagt, og efter jobbet er planlagt. 

[![Arranger job](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Gentildele aktiviteter fra én ressource til en anden

Du kan gentildele et job fra én ressource til en anden. Dette kan være nyttigt i situationer, hvor en maskine er defekt eller overbooket, og du vil finde en anden tilgængelig ressource, der kan udføre jobbet.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Gentildele en aktivitet som en interaktion med træk og slip

I visningen **Ressource** kan du gentildele en aktivitet til en anden ressource i Gantt-diagrammet som en interaktion med træk og slip. Det gør du ved at markere den række, hvor aktiviteten er planlagt. Når du har markeret rækken, kan du trække rækken til ressourcen i diagrammet under et andet ressourcegrupperingsniveau.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Gentildele en aktivitet i menuen Finplanlægge

Du kan gentildele et job i **Planlæg job**-dialogboksen ved at åbne den i **Planlæg job**-menuen. I denne menu kan du kun gentildele et job til en ressource, der allerede er indlæst i Gantt-diagrammet. Hvis du kun vælger ét job, sorteres rullemenuen for ressourcen efter relevante ressourcer. Hvis du vælger flere job, vil der ikke være nogen oplysninger om relevante ressourcer på ressourcelisten.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Indlæse yderligere ressourcer i Gantt-diagrammet
I **ressourcevisning** har du mulighed for at indlæse yderligere ressourcer i Gantt-diagrammet. Dette kan være nyttigt, hvis du vil søge efter en alternativ ressource til et job, der er planlagt på en maskine, der er overbooket eller defekt. På siden **Indlæs yderligere ressourcer** får du en liste over ressourcer, der har gyldighedsdato pr. den dato, hvor listen åbnes. Relevante ressourcer i forhold til et valgt job i Gantt-diagrammet vises først. Hvis du har flere job, der er markeret, før du åbner listen, vises ingen angivelse af relevante ressourcer. På siden **Indlæs yderligere ressourcer** kan du vælge en eller flere ressourcer, der skal indlæses i Gantt-diagrammet, når du bekræfter dit valg. Hvis der ikke er nogen planlagte job på den valgte ressource i tidsintervallet i Gantt-diagrammet, placeres ressourcen under et ressourcegrupperingsniveau i bunden af listen over aktiviteter i Gantt-diagrammet.

### <a name="access-the-gantt-chart"></a>Adgang til Gantt-diagrammet

Gantt-diagrammet kan åbnes fra følgende sider.

| **Side**                                                                                     | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Produktionsordreliste og -detaljer**                                                         | På siden **Produktionsordreliste og -detaljer** kan du åbne Gantt-diagrammet fra en eller flere af de valgte ordrer. Åbning af diagrammet fra **Gantt-diagram**-menupunktet indlæser alle job, der er relateret til de valgte produktionsordrer, men også job fra andre produktionsordrer, der er planlagt på de samme ressourcer. Åbning af diagrammet fra menupunktet **Gantt-diagram – hurtig visning** indlæser kun job, der er relateret til de valgte produktionsordrer. I denne visning er det ikke muligt at planlægge job. |
| **Ressource**                                                                                 | På siden **Ressource** kan du åbne Gantt-diagrammet fra menupunktet **Gantt-diagram**. Når det er valgt, indlæses alle de job, der er planlagt for ressourcen i et valgt tidsinterval, i diagrammet.                                                                                                                                                                                                                                                                                                   |
| **Ressourcegruppe**                                                                           | På siden **Ressourcegruppe** kan du åbne Gantt-diagrammet fra menupunktet **Gantt-diagram**. Når det er valgt, indlæses alle de job, der er planlagt for ressourcen i ressourcegruppen i et valgt tidsinterval.                                                                                                                                                                                                                                                                                    |
| **Gantt-diagrammer**                                                                             | På siden **Gantt-diagrammer** kan du konfigurere Gantt-diagrammer med ressourcer og ressourcegrupper. Hvis du f.eks. vil styre produktionsaktiviteter for bestemte sæt af ressourcer eller ressourcegrupper, kan du foretage individuelle konfigurationer af disse på siden **Gantt-diagrammer**. Du kan derefter åbne Gantt-diagrammet fra hver konfiguration.                                                                                                                                                    |
| **Timebudgetter** (projekt)                                                                 | Projektaktiviteter af typen **Timebudgetter** kan finplanlægges på ressourcer. På siden **Timebudget** i menuen **Planlægning** kan du åbne Gantt-diagrammet på en ordre for at se finplanlagte projektaktiviteter af typen timebudget.                                                                                                                                                                                                                                                             |
| **Job, der skal færdiggøres** (liste i arbejdsområdet **Administration af produktion**)                      | I arbejdsområdet **Job, der skal færdiggøres i Administration af produktion** vises job fra produktions og batchordrer, der er i gang på de valgte ressourcer til arbejdsområdet. På menupunktet **Gantt-diagram** kan du åbne Gantt-diagrammet, hvor alle de job, der er valgt på listen, indlæses i diagrammet.                                                                                                                                                                                |
| **Produktionsordrer, der skal frigives** (åbnes fra arbejdsområdet **Administration af produktion**) | Siden Produktionsordrer, der skal frigives, åbnes fra arbejdsområdet **Administration af produktion**. Denne side viser planlagte produktions- og batchordrer, der afventer frigivelse. På denne side kan du åbne Gantt-diagrammet for de valgte produktionsordrer.                                                                                                                                                                                                                                                        |
## <a name="see-also"></a>Se også  
[Visuel planlægning med Gantt-diagram for produktion og batchordrer (video)](https://youtu.be/BtbuShkGj4I)

[Visuel planlægning for produktionen (demoscript)](https://mbs.microsoft.com/customersource/northamerica/365Enterprise/learning/documentation/how-to-articles/365finoptvisschep)


