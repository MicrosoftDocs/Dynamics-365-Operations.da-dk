---
title: Konfigurere godkendelsesprocesser i en arbejdsgang
description: Brug nedenstående procedure til at konfigurere egenskaberne for godkendelsesprocessen.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "325635"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Konfigurere godkendelsesprocesser i en arbejdsgang

[!include [banner](../includes/banner.md)]

Brug nedenstående procedure til at konfigurere egenskaberne for godkendelsesprocessen.

Hvis du vil konfigurere en godkendelsesproces i arbejdsgangseditoren, skal du højreklikke på godkendelsesprocessen og derefter klikke på **Egenskaber** for at åbne formularen **Egenskaber**.

## <a name="name-the-approval-process"></a>Navngive godkendelsesprocessen

Udfør følgende trin for at angive et navn til godkendelsesprocessen.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Skriv et entydigt navn til godkendelsesprocessen i feltet **Navn**.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Angive, hvornår systemet automatisk skal behandle dokumentet

Du kan konfigurere systemet, så et dokument behandles automatisk, hvis bestemte betingelser er opfyldt. Systemet kan f.eks. godkende udgiftsrapporter med totalbeløb på mindre end 100 kr. Udfør disse trin for at angive, hvornår systemet skal behandle dokumentet automatisk.

1. Klik på **Automatiske handlinger** i venstre rude.
2. Marker afkrydsningsfeltet **Aktivér automatiske handlinger**.
3. Klik på **Tilføj betingelse**.
4. Angiv en betingelse.
5. Angive yderligere betingelser, hvis det er nødvendigt.
6. Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du udføre følgende trin:

    1. Klik på **Test** for at åbne formen **Test betingelse for arbejdsgang**.
    2. Vælg en post i området **Valider betingelse** i formen.
    3. Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.
    4. Klik på **OK** eller **Annuller** for at vende tilbage til formen **Egenskaber**.

7. Vælg den handling, som systemet skal udføre på dokumentet, på listen **Handling til automatisk udførelse**.

## <a name="specify-when-notifications-are-sent"></a>Angive, hvornår beskeder sendes

Du kan sende beskeder til personer, når et dokument er godkendt, afvist, delegeret videre eller eskaleret - eller når der er anmodet om en ændring. Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.

1. Klik på **Beskeder** i ruden til venstre.
2. Markér afkrydsningsfeltet ud for de hændelser, der skal sendes beskeder i forbindelse med.

    - **Deleger** – når et dokument er tildelt til en anden bruger til godkendelse.
    - **Eskaler** – når den tildelte bruger ikke har udført nogen handling i forbindelse med dokumentet inden for den tildelte tid.
    - **Godkend** – når et dokument er blevet godkendt.
    - **Afvis** – når et dokument er blevet afvist.
    - **Anmod om ændring** – når den bruger, der har fået opgaven tildelt, har anmodet om en ændring i et fremsendt dokument.

3. Vælg rækken for den hændelse, du har valgt i trin 2.
4. Klik på fanen **Beskedtekst**.
5. Angiv beskedteksten i tekstboksen.
6. Hvis du vil personalisere teksten, kan du indsætte pladsholdere, som erstattes af de korrekte data, når de vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. Klik i tekstboksen på det sted, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

7. Klik på **Oversættelser** for at tilføje oversættelser af beskeden. Udfør følgende trin i den form, der vises:

    1. Klik på **Tilføj**.
    2. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    3. Indtast teksten i tekstfeltet **Oversat tekst**.
    4. Hvis du vil personalisere teksten, kan du indsætte pladsholdere.
    5. Klik på **Luk**.

8. Klik på fanen **Modtager**.
9. Angiv, hvem beskederne sendes til. Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin i forbindelse med indstillingen, før du går videre til trin 10.

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
    <td><strong>Deltager</strong></td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltager</strong>, skal du klikke på fanen <strong>Rollebaseret</strong>.</li>
    <li>Vælg den type gruppe eller rolle, du vil have sendt beskeder til, på listen <strong>Deltagertype</strong>.</li>
    <li>Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Arbejdsgangsbruger</strong></td>
    <td>Brugere, som deltager i den aktuelle arbejdsgang</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Arbejdsgangsbruger</strong>, skal du klikke på fanen <strong>Arbejdsgangsbruger</strong>.</li>
    <li>På listen <strong>Arbejdsgangsbruger</strong> skal du vælge en bruger, som deltager i arbejdsgangen.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Brugere</strong></td>
    <td>Specifikke Microsoft Dynamics 365 for Finance and Operations-brugere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</li>
    <li>Listen <strong>Tilgængelige brugere</strong>: indeholder alle Microsoft Dynamics 365 for Finance and Operations-brugere. Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Gentag trin 3 til 9 for hvert af de hændelser, du har valgt i trin 2.

## <a name="specify-a-final-approver"></a>Angive en endelig godkender

Det kan være en god ide at udpege en endelig godkender for scenarier, hvor godkenderen er den person, der har sendt dokumentet til godkendelse. Udfør følgende trin for at angive en endelig godkender.

1. Klik på **Avancerede indstillinger** i venstre rude.
2. Markér afkrydsningsfeltet **Brug endelig godkender**.
3. Vælg den bruger på listen, der skal være endelig godkender.

## <a name="set-a-time-limit"></a>Angive en tidsgrænse

Udfør følgende trin, hvis godkendelsesprocessen skal fuldføres inden en bestemt tidsgrænse.

> [!NOTE]
> De indstillinger, du vælger under udførelsen af disse trin, tilsidesætter de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** for hvert godkendelsestrin.

1. Klik på **Avancerede indstillinger** i venstre rude.
2. Markér afkrydsningsfeltet **Angiv en tidsgrænse for** **arbejdsgangselementet**.
3. Angiv, hvornår godkendelsesprocessen skal fuldføres, i feltet **Varighed**. Vælg en af følgende indstillinger:

    - **Timer** – angiv det antal timer, inden for hvilke godkendelsesprocessen skal være fuldført. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Dage** – angiv det antal dage, inden for hvilke godkendelsesprocessen skal være fuldført. Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.
    - **Uger** – angiv det antal uger, inden for hvilke godkendelsesprocessen skal være fuldført.
    - **Måneder** – vælg den dag og uge, hvor godkendelsesprocessen senest skal være fuldført. Måske ønsker du godkendelsesprocessen fuldført f.eks. senest fredag i den tredje uge i måneden.
    - **År** – vælg den dag, uge og måned, hvor godkendelsesprocessen senest skal være fuldført. Måske ønsker du godkendelsesprocessen fuldført f.eks. senest fredag i den tredje uge i december.

4. Hvis tidsfristen overskrides, behandles dokumentet af systemet. Vælg den handling, der skal udføres, på listen **Handling**.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angiv, hvilke handlinger der er tilgængelige for brugeren

Når en bruger tildeles et dokument, som skal godkendes, skal han eller hun behandle dokumentet som angivet. Udfør følgende trin for at angive, hvilke handlinger brugeren kan udføre med det dokument, der er sendt.

1. Klik på **Avancerede indstillinger** i venstre rude.
2. Markér afkrydsningsfeltet **Godkend**, hvis brugeren kan godkende dokumentet.
3. Markér afkrydsningsfeltet **Afvis**, hvis brugeren kan afvise dokumentet.
4. Markér afkrydsningsfeltet **Anmod om ændring**, hvis brugeren kan anmode om ændringer af dokumentet.
5. Marker afkrydsningsfeltet **Deleger**, hvis brugeren kan tildele dokumentet til en anden bruger til godkendelse.

> [!NOTE]
> Afkrydsningsfeltet **Aktivér handlinger fra opgavelisten i Enterprise Portal** er blevet udfaset.

## <a name="configure-the-approval-steps"></a>Konfigurere godkendelsestrinene

En godkendelsesproces består af godkendelsestrin. Fuldfør følgende procedure for at tilføje trin til godkendelsesprocessen og konfigurere trinene.

1. Dobbeltklik på godkendelsesprocessen i arbejdsgangseditoren. I arbejdsgangseditoren vises trinene i godkendelsesprocessen.
2. Du kan tilføje et godkendelsestrin ved at trække trinnet fra området **Arbejdsgangselementer** til lærredet.
3. Hvis du vil konfigurere et godkendelsestrin, skal du se [Konfigurere et godkendelsestrin](configure-approval-step-workflow.md).
