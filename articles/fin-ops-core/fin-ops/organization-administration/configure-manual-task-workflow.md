---
title: Konfigurere manuelle opgave i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer egenskaberne for en manuel opgave.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f61e0f7ee16519767192fb379f20c1ed20b69caa
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798799"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Konfigurere manuelle opgave i en arbejdsgang

[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du konfigurerer egenskaberne for en manuel opgave.

Hvis du vil konfigurere en manuel opgave i arbejdsgangseditoren, skal du højreklikke på opgaven og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**. Brug derefter følgende procedurer for at konfigurere egenskaberne for den manuelle opgave.

## <a name="name-the-task"></a>Navngive opgaven

Udfør følgende trin for at angive et navn på den manuelle opgave.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Angiv et entydigt navn til opgaven i feltet **Navn**.

## <a name="enter-a-subject-line-and-instructions"></a>Angive en emnelinje og instruktioner

Du skal angive en emnelinje og instruktioner til brugere, som har fået opgaven tildelt. Hvis du f.eks. konfigurerer en opgave for indkøbsrekvisitioner, ser den bruger, der har fået opgaven tildelt, emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**. Emnelinjen vises i en meddelelseslinje på siden. Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist detaljerede instruktioner. Udfør følgende trin for at angive en emnelinje og instruktioner.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. I feltet **Emne for workflowopgave** skal du indtaste emnelinjen.
3. Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

4. Følg disse trin for at tilføje oversættelser af emnelinjen:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.
    6. Klik på **Luk**.

5. I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.
6. Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

7. Følg disse trin for at tilføje oversættelser af instruktionerne:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.
    6. Klik på **Luk**.

## <a name="assign-the-task"></a>Tildele opgaven

Udfør følgende trin for at angive, hvem den manuelle opgave skal tildeles til.

1. Klik på **Tildeling** i venstre rude.
2. Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.

    <table>
    <thead>
    <tr>
    <th>Indstilling</th>
    <th>Brugere, som opgaven er tildelt til</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele opgaven til.</li>
    <li>Vælg den gruppe eller rolle, som opgaven skal tildeles, på listen <strong>Deltager</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele opgaven til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som opgaven kan tildeles. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter: <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol>
    </li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet opgaven skal tildeles: <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Opgaven tildeles alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Opgaven tildeles kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Opgaven tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruger</td>
    <td>Specifikke brugere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere. Vælg de brugere, der skal tildeles opgaven, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kø</td>
    <td>En workflowopgavekø</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Kø</strong>, skal du klikke på fanen <strong>Købaseret</strong>.</li>
    <li>Udfør følgende trin for at tildele opgaven til en bestemt kø: <ol>
    <li>På listen <strong>Køtype</strong> skal du vælge <strong>Workflowopgavekøer</strong>.</li>
    <li>Vælg køen på listen <strong>Kønavn</strong>.</li>
    </ol>
    </li>
    <li>Hvis en bestemt betingelse skal være afgørende for, hvilken kø opgaven tildeles, skal du udføre følgende trin: <ol>
    <li>På listen <strong>Køtype</strong> skal du vælge <strong>Betingede workflowopgavekøer</strong>.</li>
    <li>På listen <strong>Kønavn</strong> skal du vælge <strong>Betinget kø</strong>.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Denne indstilling bruges kun til nogle få arbejdsgange som f.eks. Sagsstyring.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at færdiggøre opgaven. Vælg en af følgende indstillinger:

    - **Timer** – Angiv det antal timer, brugeren har til at færdiggøre opgaven. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Dage** – Angiv det antal dage, som brugeren har til at færdiggøre opgaven. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Uger** – Angiv det antal uger, som brugeren har til at færdiggøre opgaven.
    - **Måneder** – Vælg den dag og uge, hvor brugeren senest skal have færdiggjort opgaven. Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i måneden.
    - **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have færdiggjort opgaven. Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i december.

    Hvis brugeren ikke færdiggør opgaven inden for den tildelte tid, er opgaven forsinket. En opgave, der er forsinket, kan eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Angive, hvad der sker, når opgaven er forfalden

Hvis en bruger ikke færdiggør den manuelle opgave inden for den tildelte tid, er opgaven forsinket. En opgave, der er forfalden, kan eskaleres eller tildeles automatisk til en anden bruger. Udfør følgende trin for at eskalere opgaven, hvis den er forfalden.

1. Klik på **Eskalering** i venstre rude.
2. Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti. De brugere, der er angivet i eskaleringsstien, tildeles automatisk opgaven. Følgende tabel repræsenterer f.eks. en eskaleringssti.

    | Forløb | Eskaleringssti      |
    |----------|----------------------|
    | 1        | Knyt til: Anna     |
    | 2        | Knyt til: Erik      |
    | 3        | Sluthandling: Afvis |

    I dette eksempel tildeles den forfaldne opgave automatisk til Anna. Hvis Anna ikke færdiggør opgaven inden for den tildelte tid, tildeles opgaven automatisk til Erik. Hvis Erik ikke færdiggør opgaven inden for den tildelte tid, afvises det dokument, der blev sendt til behandling, af systemet.

3. Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien. Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og følg derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.

    <table>
    <thead>
    <tr>
    <th>Indstilling</th>
    <th>Brugere, som opgaven eskaleres til</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere opgaven til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som opgaven kan eskaleres til. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter: <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol>
    </li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet opgaven skal eskaleres til: <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Opgaven eskaleres til alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Opgaven eskaleres kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Opgaven eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruger</td>
    <td>Specifikke brugere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere. Vælg de brugere, som opgaven skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at færdiggøre opgaven. Vælg en af følgende indstillinger:

    - **Timer** – Angiv det antal timer, brugeren har til at færdiggøre opgaven. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Dage** – Angiv det antal dage, som brugeren har til at færdiggøre opgaven. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Uger** – Angiv det antal uger, som brugeren har til at færdiggøre opgaven.
    - **Måneder** – Vælg den dag og uge, hvor brugeren senest skal have færdiggjort opgaven. Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i måneden.
    - **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have færdiggjort opgaven. Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i december.

5. Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien. Du kan ændre brugernes rækkefølge.
6. Hvis brugerne i eskaleringsstien ikke færdiggør opgaven inden for den tildelte tid, håndteres opgaven af systemet. Hvis du vil angive den handling, som systemet skal udføre, skal du vælge rækken **Handling** og derefter vælge en handling på fanen **Sluthandling**.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Angive, hvornår systemet automatisk skal behandle opgaven

Du kan konfigurere systemet, så en manuel opgave håndteres, hvis bestemte betingelser er opfyldt. En opgave kræver f.eks., at et medlem af udgiftsrapportafdelingen gennemgår de kvitteringer, der fremlægges sammen med en udgiftsrapport. Ifølge firmaets politik skal denne opgave udføres, hvis det samlede beløb i udgiftsrapporten overstiger USD 100. I dette scenarie kan du konfigurere systemet, så opgaven automatisk markeres som **Fuldført**, når det samlede beløb er mindre end 100. Udfør disse trin for at angive, hvornår systemet skal håndtere den manuelle opgave.

1. Klik på **Automatiske handlinger** i venstre rude.
2. Marker afkrydsningsfeltet **Aktivér automatiske handlinger**.
3. Klik på **Tilføj betingelse**.
4. Angiv en betingelse.
5. Angiv eventuelle supplerende betingelser, hvis det er påkrævede.
6. Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du følge disse trin:

    1. Klik på **Test**.
    2. På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.
    3. Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.
    4. Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.

7. Vælg den handling, som systemet skal udføre på opgaven, på listen **Handling til automatisk udførelse**.

## <a name="specify-when-notifications-are-sent"></a>Angive, hvornår beskeder sendes

Du kan sende beskeder til personer, når en manuel opgave er delegeret videre, eskaleret, fuldført eller afvist, eller når der er anmodet om en ændring. Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.

1. Klik på **Beskeder** i ruden til venstre.
2. Markér afkrydsningsfeltet ud for de hændelser, som beskederne udsendes i forbindelse med.

    - **Deleger** – Opgaven er tildelt en anden bruger.
    - **Eskaler** – Den bruger, der har fået opgaven tildelt, har ikke fuldført den inden for den tildelte tid.
    - **Fuldført** – Den bruger, der har fået opgaven tildelt, har fuldført den.
    - **Afvis** – Den bruger, der har fået opgaven tildelt, har afvist det fremsendte dokument.
    - **Anmod om ændring** – Den bruger, der har fået opgaven tildelt, har anmodet om en ændring i det fremsendte dokument.

3. Vælg rækken for den hændelse, du har valgt i trin 2.
4. Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.
5. Hvis du vil personalisere beskeden, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante oplysninger, når beskeden vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

6. Følg disse trin for at tilføje oversættelser af beskeden:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.
    6. Klik på **Luk**.

7. På fanen **Modtager** skal du angive, hvem beskederne skal sendes til. Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.

    <table>
    <thead>
    <tr>
    <th>Indstilling</th>
    <th>Modtagere af besked</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</li>
    <li>Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbejdsgangsbruger</td>
    <td>Brugere i den aktuelle arbejdsgang</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruger</td>
    <td>Specifikke brugere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere. Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.

## <a name="set-a-time-limit"></a>Angive en tidsgrænse

Udfør følgende trin, hvis den manuelle opgave skal fuldføres inden en bestemt tidsgrænse.

> [!NOTE]
> De indstillinger, du vælger i denne procedure, overskriver de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** på siden.

1. Klik på **Avancerede indstillinger** i venstre rude.
2. Markér afkrydsningsfeltet **Angiv en tidsgrænse for arbejdsgangselementet**
3. Angiv, hvornår opgaven skal være fuldført, i feltet **Varighed**. Vælg en af følgende indstillinger:

    - **Timer** – Angiv det antal timer, som opgaven skal fuldføres på. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Dage** – Angiv det antal dage, som opgaven skal fuldføres på. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Uger** – Angiv det antal uger, inden for hvilke opgaven skal være fuldført.
    - **Måneder** – Vælg den dag og uge, hvor opgaven senest skal være fuldført. Det kan f.eks. være, at opgaven skal være fuldført f.eks. senest fredag i den tredje uge i måneden.
    - **År** – Vælg den dag, uge og måned, hvor opgaven senest skal være fuldført. Det kan f.eks. være, at opgaven skal være fuldført senest fredag i den tredje uge i december.

4. Hvis tidsfristen overskrides, håndteres opgaven af systemet. Vælg den handling, der skal udføres, på listen **Handling**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angiv, hvilke handlinger der er tilgængelige for brugeren

Når den manuelle opgave tildeles en bruger, skal vedkommende håndtere opgaven. Udfør disse trin for at angive, hvilke handlinger brugeren kan udføre på opgaven.

> [!NOTE]
> Det vil variere, hvilke handlinger der er tilgængelige, afhængigt af opgavens design.

1. Klik på **Avancerede indstillinger** i venstre rude.
2. Markér afkrydsningsfeltet **Fuldført**, hvis brugeren skal kunne markere opgaven som **Fuldført**.
3. Markér afkrydsningsfeltet **Afvis**, hvis brugeren skal kunne afvise det dokument, der blev fremsendt.
4. Markér afkrydsningsfeltet **Anmod om ændring**, hvis brugeren skal kunne anmode om ændringer i det fremsendte dokument.
5. Markér afkrydsningsfeltet **Deleger**, hvis brugeren skal kunne tildele denne opgave til en anden bruger.
6. Markér afkrydsningsfeltet **Tildel igen**, hvis brugeren skal kunne tildele denne opgave til en anden bruger i workflowopgavekøen.
7. Markér afkrydsningsfeltet **Frigiv**, hvis brugeren skal kunne tildele denne opgave til workflowopgavekøen. Derefter kan en anden bruger fuldføre opgaven.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]