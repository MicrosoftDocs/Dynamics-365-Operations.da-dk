---
title: Konfigurere et godkendelsestrin i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer egenskaberne for et godkendelsestrin.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b403a6f01a6c7ba95c2dd1cfd3bae8e58f0c6879
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="configure-an-approval-step-in-a-workflow"></a>Konfigurere et godkendelsestrin i en arbejdsgang

[!include[banner](../includes/banner.md)]


I dette emne forklares det, hvordan du konfigurerer egenskaberne for et godkendelsestrin.

Hvis du vil konfigurere et godkendelsestrin i arbejdsgangseditoren, skal du højreklikke på godkendelsestrinnet og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**. Brug derefter nedenstående procedurer til at konfigurere egenskaberne for godkendelsestrinnet.

## <a name="name-the-step"></a>Angive et navn på trinnet
Udfør følgende trin for at angive et navn på godkendelsestrinnet.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Angiv et entydigt navn til godkendelsestrinnet i feltet **Navn**.

## <a name="enter-a-subject-line-and-instructions"></a>Angive en emnelinje og instruktioner
Du skal angive en emnelinje og instruktioner til brugere, som har fået godkendelsestrinnet tildelt. Hvis du f.eks. konfigurerer et godkendelsestrin for indkøbsrekvisitioner, kan den bruger, der har fået trinnet tildelt, se emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**. Emnelinjen vises i en meddelelseslinje på siden. Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist instruktionerne. Udfør følgende trin for at angive en emnelinje og instruktioner.

1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  I feltet **Emne for workflowopgave** skal du indtaste emnelinjen.
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

## <a name="assign-the-approval-step"></a>Tildele godkendelsestrinnet
Udfør følgende trin for at angive, hvem godkendelsestrinnet skal tildeles.

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
    <th>Brugere, som godkendelsestrinnet er tildelt til</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td><ol>
    <li>Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele trinnet til.</li>
    <li>Vælg den gruppe eller rolle, som trinnet skal tildeles til, på listen <strong>Deltager</strong>.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele trinnet til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som trinnet kan tildeles til. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter: <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol></li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet trinnet skal tildeles: <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Trinnet tildeles alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Trinnet tildeles kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Trinnet tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
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
    <td>Bestemte Microsoft Dynamics 365 for Finance and Operations-brugere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere. Vælg de brugere, der skal tildeles trinnet, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter, der når til godkendelsestrinnet. Vælg en af følgende indstillinger:
    -   **Timer** – Angiv det antal timer, som brugeren har til at reagere i. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Dage** – Angiv det antal dage, som brugeren har til at reagere i. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Uger** – Angiv det antal uger, som brugeren har til at reagere i.
    -   **Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret. Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.
    -   **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret. Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.

    Hvis brugeren ikke håndterer dokumentet inden for den tildelte tid, er dokumentet forsinket. Et forsinket dokument eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.
4.  Hvis du har tildelt godkendelsestrinnet til flere brugere eller en gruppe af brugere, skal du vælge følgende indstillinger på fanen **Afviklingspolitik**:
    -   **Enkelt godkender** – den handling, der udføres på dokumentet, bestemmes af den første person, der reagerer. Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000. Dokumentet er aktuelt tildelt Mette, Karina og Bjarne. Hvis Mette er den første person, der reagerer på dokumentet, vil den handling, hun udfører, blive anvendt på dokumentet. Hvis Mette afviser dokumentet, afvises det og sendes tilbage til Søren. Hvis Mette godkender dokumentet, sendes det til Dorthe til godkendelse. 
    
    ![Arbejdsgang, der har en godkendelsesproces](./media/workflow_multipleusersinstep.gif)
    
    -   **Flertal af godkendere** – den handling, der skal anvendes på dokumentet, bliver bestemt, når de fleste af godkenderne har reageret. Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000. Dokumentet er aktuelt tildelt Mette, Karina og Bjarne. Hvis Mette og Karina er de første personer, der reagerer på dokumentet, vil den handling, de udfører, blive anvendt på dokumentet.
        -   Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.
        -   Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.
    -   **Procent af godkendere** – den handling, der anvendes på dokumentet, bliver bestemt, når en bestemt procentdel af godkenderne svarer. Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000. Udgiftsrapporten er aktuelt tildelt Mette, Karina og Bjarne, og du har angivet procentdelen til **50**. Hvis Mette og Karina er de første to godkendere, der reagerer, vil den handling, de udfører, blive anvendt på dokumentet, fordi de opfylder kravet om at være 50 procent af godkendere.
        -   Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.
        -   Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.
    -   **Alle godkendere** – alle godkendere skal godkende dokumentet. Ellers kan arbejdsgangen ikke fortsætte. Antag f.eks. at Søren har sendt en udgiftsrapport på 15.000 kr. Dokumentet er aktuelt tildelt Mette, Karina og Bjarne. Hvis Mette og Karina godkender dokumentet, men Bjarne afviser det, vil dokumentet blive afvist og sendt tilbage til Søren. Hvis Mette, Karina og Bjarne godkender dokumentet, bliver det sendt til Dorthe til godkendelse.

## <a name="specify-when-the-approval-step-is-required"></a>Angive, hvornår godkendelsestrinnet skal bruges
Du kan angive, hvornår godkendelsestrinnet er påkrævet. Godkendelsestrinnet kan være påkrævet altid, eller det kan kun være påkrævet, hvis bestemte betingelser er opfyldt.

### <a name="the-approval-step-is-always-required"></a>Godkendelsestrinnet er altid påkrævet

Udfør følgende trin, hvis godkendelsestrinnet altid er påkrævet.

1.  Klik på **Betingelse** i venstre rude.
2.  Vælg indstillingen **Udfør altid dette trin**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Godkendelsestrinnet er påkrævet under bestemte betingelser.

Det godkendelsestrin, du er ved at konfigurere, er måske kun påkrævet, hvis bestemte betingelser er opfyldt. Hvis du f.eks. er ved at konfigurere et godkendelsestrin til en arbejdsgang for en indkøbsrekvisition, vil du måske have, at godkendelsestrinnet kun skal bruges, hvis indkøbsrekvisitionsbeløbet er større end 10.000 kr. Udfør følgende trin, når du skal angive, at godkendelsestrinnet er påkrævet.

1.  Klik på **Betingelse** i venstre rude.
2.  Vælg indstillingen **Kør kun dette trin, når følgende betingelse er opfyldt**.
3.  Angiv en betingelse.
4.  Angiv eventuelle supplerende betingelser, hvis det er påkrævede.
5.  Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du følge disse trin:
    1.  Klik på **Test**.
    2.  På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.
    3.  Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.
    4.  Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Angive, hvad der sker, når dokumentet er forfaldent
Hvis en bruger ikke håndterer et dokument inden for den tildelte tid, er dokumentet forfaldent. Et forfaldent dokument kan eskaleres eller tildeles automatisk til en anden bruger til godkendelse. Følg disse trin for at eskalere dokumentet, hvis det er forfaldent.

1.  Klik på **Eskalering** i venstre rude.
2.  Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti. De brugere, der er angivet i eskaleringsstien, tildeles automatisk dokumentet. Følgende tabel repræsenterer f.eks. en eskaleringssti.

    | Forløb | Eskaleringssti      |
    |----------|----------------------|
    | 1        | Knyt til: Anna     |
    | 2        | Knyt til: Erik      |
    | 3        | Sluthandling: Afvis |

    I dette eksempel tildeles det forfaldne dokument automatisk til Anna. Hvis Anna ikke reagerer inden for den tildelte tid, tildeles dokumentet automatisk til Erik. Hvis Erik ikke reagerer inden for den tildelte tid, afvises dokumentet automatisk.
3.  Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien. Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og følg derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Indstilling</th>
    <th>Brugere, som dokumentet eskaleres til</th>
    <th>Ekstra trin</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarki</td>
    <td>Brugere i et bestemt organisationshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere dokumentet til.</li>
    <li>Systemet skal hente et interval af brugernavne fra hierarkiet. Disse navne repræsenterer de brugere, som dokumentet kan eskaleres til. Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter: <ol>
    <li>Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</li>
    <li>Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet. Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</li>
    </ol></li>
    <li>På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet dokumentet skal eskaleres til: <ul>
    <li><strong>Tildel til alle hentede brugere</strong> – Dokumentet eskaleres til alle brugere i intervallet.</li>
    <li><strong>Tildel kun til den sidst hentede bruger</strong> – Dokumentet eskaleres kun til den sidste bruger i intervallet.</li>
    <li><strong>Udeluk brugere med følgende betingelse</strong> – Dokumentet eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse. Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</li>
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
    <td>Bestemte Finance and Operations-brugere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere. Vælg de brugere, dokumentet skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter. Vælg en af følgende indstillinger:
    -   **Timer** – Angiv det antal timer, som brugeren har til at reagere i. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Dage** – Angiv det antal dage, som brugeren har til at reagere i. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    -   **Uger** – Angiv det antal uger, som brugeren har til at reagere i.
    -   **Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret. Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.
    -   **År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret. Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.

5.  Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien. Du kan ændre brugernes rækkefølge.
6.  Hvis brugerne i eskaleringsstien ikke reagerer inden for den tildelte tid, håndteres dokumentet automatisk af systemet. Hvis du vil angive den handling, som systemet skal udføre, skal du vælge rækken **Handling** og derefter vælge en handling på fanen **Sluthandling**.





