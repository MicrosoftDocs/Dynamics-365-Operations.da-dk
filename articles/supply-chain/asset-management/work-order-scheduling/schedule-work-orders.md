---
title: Planlæg arbejdsordrer
description: Dette emne beskriver, hvordan du planlægger arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a594bacb1fcf53ae4a278dbb26f1de174e22288c
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275596"
---
# <a name="schedule-work-orders"></a>Planlæg arbejdsordrer

[!include [banner](../../includes/banner.md)]

 

Dette emne beskriver, hvordan du planlægger arbejdsordrer i Styring af aktiver. 

Det nødvendige antal timer for en arbejdsordre defineres af summen af budgetterede timer minus bogførte timer. Hvis der kræves mere tid, skal prognosen justeres tilsvarende. I **Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer** kan du se eller redigere prognoser på en arbejdsordre ved at vælge arbejdsordren og klikke på **Prognose** under fanen **Arbejdsordre**. Når der er oprettet og forkalkuleret arbejdsordrer, er næste trin at allokere de påkrævede vedligeholdelsesarbejdere og -værktøjer, der skal til for at fuldføre arbejdsordrerne.

Det er kun arbejdsordrer med en livscyklustilstand, der kan planlægges. Tillad planlægning er konfigureret i **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Livscyklustilstande** >  oversigtspanelet **Generelt** > til/fra-knappen **Tillad planlægning**.

1. Klik på **Styring af aktiver** > **Almindeligt** > **Arbejdsordrer** > **Alle arbejdsordrer**.

2. Vælg de arbejdsordrer, du vil planlægge, på listen. Du kan sortere listen f.eks. efter **Aktuel livscyklustilstand**.

3. Klik på **Tidsplan** under fanen **Generelt**.

4. I dialogboksen **Planlæg arbejdsordrer** kan du tilføje valg angående forventet startdato og serviceniveau, hvis det er nødvendigt. Hvis planlægningsprocessen skal overholde kapacitetsbegrænsningerne for ressourcer, der allerede er planlagt for andre job, skal du sørge for, at til/fra-knapperne **Aktiv**, **Værktøj** og **Arbejder** er indstillet til "Ja".

    [!NOTE]
    Hvis du indstiller knapperne **Aktiv**, **Værktøj** og **Arbejder** til "Nej", bliver eksisterende reservationer ignoreret. I infologgen vises en liste over overlappende tidsplaner for arbejdsordrer, og du kan klikke på meddelelserne for at åbne en arbejdsordre og omplanlægge, hvis det er nødvendigt.

5. Hvis du vil have vist detaljerede oplysninger om planlægningsprocessen, skal du vælge "Ja" på knappen **Detaljeret**. Det betyder, at der vises detaljerede oplysninger om de beregnede scorer for arbejdsordrerene og vedligeholdelsesarbejderne i infologgen.

6. Klik på **OK** for at starte planlægningsprocessen.

7. Når planlægningen er fuldført, viser en infolog antallet af planlagte arbejdsordrer samt mere detaljerede oplysninger, hvis til/fra-knappen **Detaljeret** er indstillet til "Ja".

>[!NOTE]
>Arbejdsordrer planlægges i én cyklus pr. arbejdsordre, ikke pr. arbejdsordrejob. Du kan også åbne dialogboksen **Planlæg arbejdsordrer** direkte i **Styring af aktiver** > **Periodisk** > **Arbejdsordrer** > **Planlæg arbejdsordrer**. Foretag de ønskede valg, og klik på **OK** for at starte arbejdsordreplanlægningen. Du kan oprette en arbejdsordreplanlægning som et batchjob i dialogboksen **Planlæg arbejdsordrer** > oversigtspanelet **Kør i baggrunden**.

*Eksempel:* I nedenstående figur genererer den formel, der er indsat i feltet **Forventet start**, arbejdsordreplanlægning for alle arbejdsordrer med en forventet startdato en uge fra det aktuelle tidspunkt og senere. Denne formel kan være nyttig, når du kører ordreplanlægning løbende, men vil sikre dig, at de arbejdsordrer, der er planlagt for de næste 5-6 dage, ikke omplanlægges.

![Figur 1](media/03-work-order-scheduling.png)

Den arbejdsordretype, der er knyttet til arbejdsordrer, kan f.eks. oprette planlægning for én vedligeholdelsesarbejder (**Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Arbejdsordretyper** > **Én vedligeholdelsesarbejder**-til/fra-knappen indstillet til "Ja"). Det betyder, at hvis arbejdsordretypen bruges på en arbejdsordre, er til/fra-knappen **Én vedligeholdelsesarbejder** automatisk indstillet til "Ja" på detaljesiden **Alle arbejdsordrer** > visningen **Hoved** > oversigtspanelet **Tidsplan**. Under planlægningen af arbejdsordrer planlægges alle arbejdsordrejob, der er oprettet på arbejdsordren, efterfølgende for den samme vedligeholdelsesarbejder. Hvis det er nødvendigt, kan du redigere valget på til/fra-knappen **Én vedligeholdelsesarbejder** i **Alle arbejdsordrer**, så der er mulighed for at planlægge flere arbejdere eller én arbejder på arbejdsordrejob.

Planlægningsprocessen i Styring af aktiver omfatter flere faktorer i planlægningsberegningen:

- Beregning af scorer for både arbejdsordrer og vedligeholdelsesarbejdere. Scorer for arbejdsordrer og vedligeholdelsesarbejdere konfigureres i **Parametre til aktivstyring**. 
- Kontrol af, om der er overensstemmende kompetencer, hvilket vil sige færdigheder og certifikater, der kræves for at udføre jobbet. Færdigheder og certifikater konfigureres for vedligeholdelsesarbejdere i modulet **Personale** (**Personale** > **Arbejdere** > **Arbejdere** > vælg arbejder på listen > fanen **Arbejder** > sektionen **Kompetencer** > knapperne **Færdigheder** og **Certifikater**). Det er også muligt at føje færdigheder og certifikater til vedligeholdelsesjobtyper og fag, der er relevante for vedligeholdelsesjob. Læs mere om kompetencer og vedligeholdelsesjobtyper under [Kategorier af vedligeholdelsesjobtyper og vedligeholdelsesjobtyper, varianter af vedligeholdelsesjobtyper, fag relateret til vedligeholdelsesjob og vedligeholdelsestjeklister](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Scorer, der bruges i planlægning af arbejdsordrer

Beregning af scorer for et job på en arbejdsordre er baseret på den forventede startdato og serviceniveauet i arbejdsordren.

Beregning af **startdato**: For hver fremtidig dato, der er beregnet ud fra den forventede startdato, fratrækkes scoren for startdatoen, og den ganges med scoren, som er "10" i nedenstående eksempler.

Beregning af **kritikalitet**: Kritikalitetsscoren ganget med en kritikaliteten på arbejdsordren.

Beregning af **serviceniveau**: Serviceniveauscoren divideret med serviceniveauet på arbejdsordren.

I eksemplerne nedenfor er kritikalitetsscoren "2", og serviceniveauscoren er "5" og "100".

**Eksempel 1:**

| Arbejdsordre-id | Forventet startdato | Arbejdsordrekritikalitet | Serviceniveau for arbejdsordre | Udregning               | Resultat      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| AO-00010816   | I morgen            | 2                      | 20              | (-1 \*10) + (2 \*2) + 5 / 20     | \- 5.75    |
| AO-00010817   | To dage fra nu   | 2                      | 20              | (-2 \*10) + (2 \*2) + 5 / 20     | \- 15.75   |
| AO-00010818   | To dage fra nu   | 3                      | 5               | (-2 \*10) + (2 \*3) + 5 / 5      | \- 13      |

Arbejdsordrerne planlægges i følgende rækkefølge: AO-000108**16**, AO-000108**18**, AO-000108**17**.

**Eksempel 2:**

| Arbejdsordre-id | Forventet startdato | Arbejdsordrekritikalitet | Serviceniveau for arbejdsordre | Udregning                 | Resultat    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| AO-00010816   | I morgen            | 2                      | 20                  | (-1 \*10) + (2 \*2) + 100 / 20 | \- 1     |
| AO-00010817   | To dage fra nu   | 2                      | 20                  | (-2 \*10) + (2 \*2) + 100 / 20 | \- 11    |
| AO-00010818   | To dage fra nu   | 3                      | 5                   | (-2 \*10) + (2 \*3) + 100 / 5  | 6        |

Hvis scoren på serviceniveau øges til '100' i stedet for '5', vil planlægningsrækkefølgen være: AO-000108**18**, AO-000108**16**, AO-000108**17**.

De rangeringsscorer, der vedrører beregning af, hvilke vedligeholdelsesarbejdere der skal arbejde på arbejdsordrerne, konfigureres alle som numre, der føjes til hver enkelt arbejderberegning under planlægningen af arbejdsordrer. Den vedligeholdelsesmedarbejder, der har den højeste score, vælges på arbejdsordren. Her er en kort beskrivelse af scorerne for vedligeholdelsesarbejdere:

| Vedligeholdelsesarbejderscore| Beskrivelse |
|---|---|
| Ansvarlig arbejder | Hvis vedligeholdelsesarbejderen er valgt som ansvarlig arbejder på arbejdsordren, tilføjes scoren. |
| Ansvarlig vedligeholdelsesarbejdergruppe | Hvis vedligeholdelsesarbejderen indgår i den ansvarlige vedligeholdelsesarbejdergruppe på arbejdsordren, tilføjes scoren. |
| Foretrukken vedligeholdelsesarbejder         | Hvis arbejderen er valgt som den foretrukne vedligeholdelsesarbejder på aktivet, tilføjes scoren. |
| Foretrukken vedligeholdelsesarbejdergruppe   | Hvis arbejderen indgår i den foretrukne vedligeholdelsesarbejdergruppe på aktivet, tilføjes scoren.  |
| Adresse  | Hvis din virksomhed bruger arbejdssteder, får vedligeholdelsesarbejderne fuld score, hvis de er på det arbejdssted, der er relateret til aktivet. Hvis aktivets arbejdssted har et overordnet sted, får vedligeholdelsesarbejdere på det pågældende arbejdssted 1/2 score. Hvis dette sted også har et overordnet sted, vil vedligeholdelsesarbejdere på dette sted få 1/3 score. Hvis dette sted også har et overordnet sted, vil vedligeholdelsesarbejderne på dette sted få 1/4 score osv. Hvis dit firma bruger aktivlokation, hvilket vi fraråder, bruges lokation, område og zone til at beregne lokationsscore. Arbejdere får fuld score, hvis de er placeret i lokationen og området og zonen, der er relateret til aktivet. Hvis arbejderens lokation kun svarer til lokation og område, er rangeringsscoren for vedligeholdelsesarbejderen 2/3 af den fulde score. Hvis vedligeholdelsesarbejderens lokation kun svarer til lokation, er rangeringsscoren for vedligeholdelsesarbejderen 1/3 af den fulde score. |
| Startdato for medarbejder  | For hver dato, som den planlagte startdato er senere end den forventede startdato, fratrækkes scoren.  |

>[!NOTE]
>Hvis en score er indstillet til "0", beregnes den ikke. Dette er nyttigt, hvis du f.eks. ikke vil inkludere en ansvarlig arbejder i din planlægning.

## <a name="competencies-used-in-work-order-scheduling"></a>Kompetencer, der bruges i planlægning af arbejdsordrer

Der kan oprettes krav til færdigheder og certifikater på vedligeholdelsesjobtyper (**Styring af aktiver** > **Opsætning** > **Job** > **Vedligeholdelsesjobtyper**) og fag med relevans for vedligeholdelsesjob (**Styring af aktiver** > **Opsætning** > **Job** > **Vedligeholdelsesjobfag**). 

Du kan vælge vedligeholdelsesjobtyper og vedligeholdelsesjobfag på arbejdsordrer. Hvis du har valgt færdigheder eller certifikater på en vedligeholdelsesjobtype eller vedligeholdelsesjobfag, og denne type eller dette fag bruges på et job i en arbejdsordre, er det kun vedligeholdelsesarbejdere med matchende færdigheder og certifikater, der planlægges til at arbejde på arbejdsordren.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Arbejde med planlagte arbejdsordrer ved hjælp af et Gantt-diagram

**Gantt-diagrammet Planlagte arbejdsordrer** udgør en grafisk brugergrænseflade, hvor du kan se og ændre planlægningen af dine arbejdsordrer.

Sådan kan du se og arbejde med Gantt-diagrammet:

1. Gå til **Styring af aktiver > Arbejdsordrer > Gantt-diagrammet Planlagte arbejdsordrer**.

1. Du kan bruge rullelisterne og felterne i sektionen **Indstillinger** til at definere det arbejdssted, det tidsinterval og den tidsskala, der skal vises i Gantt-diagrammet.

1. Vælg **Anvend**.

    - Gantt-diagrammet opdateres til at vise de planlagte arbejdsordrer, der svarer til dine indstillinger. Hver enkelt arbejdsordre repræsenteres af et blåt rektangel.
    - Hvis du vil ændre planlægningen af en vist arbejdsordre, skal du vælge og derefter trække den til den relevante nye dato og det ønskede klokkeslæt.

1. Hvis du har foretaget ændringer, skal du vælge **Gem** i handlingsruden for at gemme dem.
