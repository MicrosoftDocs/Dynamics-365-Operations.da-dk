---
title: Konfigurere en manuel beslutning i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ac4f520d17c721e249737b4ae95c10685f914497
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-manual-decision-in-a-workflow"></a>Konfigurere en manuel beslutning i en arbejdsgang

[!include[banner](../includes/banner.md)]


I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.

Hvis du vil konfigurere en manuel beslutning i arbejdsgangseditoren, skal du højreklikke på den manuelle beslutning og derefter klikke på **Egenskaber** for at åbne formularen **Egenskaber**. Brug derefter nedenstående procedure for at konfigurere egenskaberne for den manuelle beslutning.

## <a name="name-the-decision"></a>Navngive beslutningen
Udfør følgende trin for at angive et navn på den manuelle beslutning.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Angiv et entydigt navn på den manuelle beslutning i feltet **Navn**.

## <a name="enter-a-subject-line-and-instructions"></a>Angive en emnelinje og instruktioner
Du skal angive en emnelinje og instruktioner til brugere, som har fået den manuelle beslutning tildelt. Hvis du f.eks. konfigurerer en beslutning for indkøbsrekvisitioner, ser den bruger, der har fået beslutningen tildelt, emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**. Emnelinjen vises i en meddelelseslinje på siden. Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist detaljerede instruktioner. Udfør følgende trin for at angive en emnelinje og instruktioner.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  På fanen **Instruktioner** i feltet **Emne for workflowopgave** skal du indtaste emnelinjen.
3.  Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.
    1.  I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2.  Klik på **Indsæt pladsholder**.
    3.  Vælg den pladsholder, du vil indsætte, på den viste liste.
    4.  Klik på **Indsæt**.

4.  Følg disse trin for at tilføje oversættelser af emnelinjen:
    1.  Klik på **Oversættelser**.
    2.  Klik på **Tilføj** på den viste side.
    3.  På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4.  Indtast teksten i feltet **Oversat tekst**.
    5.  Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.
    6.  Klik på **Luk**.

5.  I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.
6.  Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.
    1.  I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2.  Klik på **Indsæt pladsholder**.
    3.  Vælg den pladsholder, du vil indsætte, på den viste liste.
    4.  Klik på **Indsæt**.

7.  Følg disse trin for at tilføje oversættelser af instruktionerne:
    1.  Klik på **Oversættelser**.
    2.  Klik på **Tilføj** på den viste side.
    3.  På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4.  Indtast teksten i feltet **Oversat tekst**.
    5.  Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.
    6.  Klik på **Luk**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Angive mulige udfald af en beslutning
Når et dokument tildeles en beslutningstager, får beslutningstageren typisk stillet et spørgsmål. Svaret på spørgsmålet er normalt **Ja**eller **Nej**, **Sand** eller **Falsk**. Udfør følgende trin for at angive det mulige udfald af den manuelle beslutning.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Indtast navnet på udfaldet eller indstillingen på fanen **Udfald** i feltet **Udfald 1**.
3.  Følg disse trin for at tilføje oversættelser af udfaldet:
    1.  Klik på **Oversættelser**.
    2.  Klik på **Tilføj** på den viste side.
    3.  På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4.  Indtast teksten i feltet **Oversat tekst**.
    5.  Klik på **Luk**.

4.  Indtast navnet på udfaldet eller indstillingen i feltet **Udfald 2**.
5.  Følg disse trin for at tilføje oversættelser af udfaldet:
    1.  Klik på **Oversættelser**.
    2.  Klik på **Tilføj** på den viste side.
    3.  På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4.  Indtast teksten i feltet **Oversat tekst**.
    5.  Klik på **Luk**.

## <a name="specify-when-notifications-are-sent"></a>Angive, hvornår beskeder sendes
Du kan sende beskeder til personer, når en beslutning er truffet, delegeret videre eller eskaleret. Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.

1.  Klik på **Beskeder** i ruden til venstre.
2.  Markér afkrydsningsfeltet ud for de hændelser, som beskederne udsendes i forbindelse med.
    -   **\[Valg 1\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 1\]**.
    -   **\[Valg 2\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 2\]**.
    -   **Deleger** – Den bruger, der er tildelt beslutningen, har tildelt den til en anden bruger.
    -   **Eskaler** – Den bruger, der har fået tildelt beslutningen, har ikke truffet beslutningen inden for den tildelte tid.

3.  Vælg rækken for den hændelse, du har valgt i trin 2.
4.  Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.
5.  Hvis du vil personalisere beskeden, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når beskeden vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.
    1.  I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2.  Klik på **Indsæt pladsholder**.
    3.  Vælg den pladsholder, du vil indsætte, på den viste liste.
    4.  Klik på **Indsæt**.

6.  Følg disse trin for at tilføje oversættelser af beskeden:
    1.  Klik på **Oversættelser**.
    2.  Klik på **Tilføj** på den viste side.
    3.  På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4.  Indtast teksten i feltet **Oversat tekst**.
    5.  Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.
    6.  Klik på **Luk**.

7.  På fanen **Modtager** skal du angive, hvem beskederne skal sendes til. Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Indstilling</th>
    <th>Modtagere af besked</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td><ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</li>
    <li>Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td><ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Bruger</td>
    <td>Bestemte Microsoft Dynamics 365 for Operations-brugere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere af Dynamics 365 for Operations. Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.

## <a name="assign-a-decision"></a>Tildele en beslutning
Udfør følgende trin for at angive, hvem en manuel beslutning skal tildeles til.

1.  Klik på **Tildeling** i venstre rude.
2.  Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Indstilling</th>
    <th>Brugere, som beslutningen tildeles</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td><ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele beslutningen til.</li>
    <li>Vælg den type gruppe eller rolle, som beslutningen skal tildeles til, på listen <strong>Deltager</strong>.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele beslutningen til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som beslutningen kan tildeles til. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:
    <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol></li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal tildeles:
    <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Beslutningen tildeles alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen tildeles kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td><ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Bruger</td>
    <td>Bestemte Dynamics 365 for Operations-brugere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere af Dynamics 365 for Operations. Vælg de brugere, der skal tildeles beslutningen, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Kø</td>
    <td>En workflowopgavekø</td>
    <td><ol>
    <li>Når du har valgt <strong>Kø</strong>, skal du klikke på fanen <strong>Købaseret</strong>.</li>
    <li>Udfør følgende trin for at tildele beslutningen til en bestemt kø:
    <ol>
    <li>På listen <strong>Køtype</strong> skal du vælge <strong>Workflowopgavekøer</strong>.</li>
    <li>Vælg køen på listen <strong>Kønavn</strong>.</li>
    </ol></li>
    <li>Hvis en bestemt betingelse skal være afgørende for, hvilken kø beslutningen tildeles til, skal du udføre følgende trin:
    <ol>
    <li>På listen <strong>Køtype</strong> skal du vælge <strong>Betingede workflowopgavekøer</strong>.</li>
    <li>På listen <strong>Kønavn</strong> skal du vælge <strong>Betinget kø</strong>.</li>
    </ol></li>
    </ol>
    <strong>Bemærk!</strong> Denne indstilling bruges kun til nogle få arbejdsgange såsom Sagsstyring.</td>
    </tr>
    </tbody>
    </table>

3.  På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen. Vælg en af følgende indstillinger:
    -   **Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.
    -   **Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen. Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.
    -   **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen. Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.

    Hvis brugeren ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket. En forsinket beslutning eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Angive, hvad der sker, når en beslutning er forsinket.
Hvis en bruger ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket. En beslutning, der er forfalden, kan eskaleres eller tildeles automatisk til en anden bruger. Udfør følgende trin for at eskalere beslutningen, hvis den er forsinket.

1.  Klik på **Eskalering** i venstre rude.
2.  Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti. De brugere, der er angivet i eskaleringsstien, tildeles automatisk beslutningen. Følgende tabel repræsenterer f.eks. en eskaleringssti.
    | Forløb | Eskaleringssti            |
    |----------|----------------------------|
    | 1        | Knyt til: Anna           |
    | 2        | Knyt til: Erik            |
    | 3        | Sluthandling: \[Valg 1\] |

    I dette eksempel tildeles den forsinkede beslutning automatisk til Anna. Hvis Anna ikke træffer beslutningen inden for den tildelte tid, tildeles beslutningen automatisk til Erik. Hvis Erik ikke træffer beslutningen inden for den tildelte tid, vælges **\[[Valg 1\]** automatisk som beslutning.
3.  Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien. Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Indstilling</th>
    <th>Brugere, som beslutningen eskaleres til</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere beslutningen til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som beslutningen kan eskaleres til. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:
    <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol></li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal eskaleres til:
    <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Beslutningen eskaleres til alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen eskaleres kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td><ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Bruger</td>
    <td>Bestemte Dynamics 365 for Operations-brugere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere af Dynamics 365 for Operations. Vælg de brugere, beslutningen skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen. Vælg en af følgende indstillinger:
    -   **Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.
    -   **Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen. Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.
    -   **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen. Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.

5.  Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien. Du kan ændre brugernes rækkefølge.
6.  Hvis brugerne i eskaleringsstien ikke træffer beslutningen inden for den tildelte tid, træffes beslutningen automatisk af systemet. Hvis du vil angive den indstilling, som systemet vælger, skal du vælge rækken **Handling** og derefter vælge en indstilling på fanen **Sluthandling**.

## <a name="set-a-time-limit"></a>Angive en tidsgrænse
Udfør følgende trin, hvis beslutningen skal træffes inden en bestemt tidsgrænse. **Bemærk!** De indstillinger, du vælger i denne procedure, overskriver de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** på siden.

1.  Klik på **Avancerede indstillinger** i venstre rude.
2.  Markér afkrydsningsfeltet **Angiv en tidsgrænse for arbejdsgangselementet**
3.  Angiv, hvornår beslutningen skal være truffet, i feltet **Varighed**. Vælg en af følgende indstillinger:
    -   **Timer** – Angiv antallet af timer. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Dage** – Angiv antallet af dage. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Uger** – Angiv antallet af uger.
    -   **Måneder** – Vælg den dag og uge, hvor beslutningen senest skal være truffet. Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i måneden.
    -   **År** – Vælg den dag, uge og måned, hvor beslutningen senest skal være truffet. Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i december.

4.  Hvis tidsfristen overskrides, træffes beslutningen automatisk af systemet. Vælg den indstilling, som systemet skal vælge, på listen **Handling**.





