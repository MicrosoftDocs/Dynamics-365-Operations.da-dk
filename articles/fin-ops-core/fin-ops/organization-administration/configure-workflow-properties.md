---
title: Konfigurere egenskaber for arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190114"
---
# <a name="configure-workflow-properties"></a>Konfigurere egenskaber for arbejdsgang

[!include [banner](../includes/banner.md)]

I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.

Du kan konfigurere egenskaberne for en arbejdsgang ved at åbne arbejdsgangen i arbejdsgangseditoren. Klik på lærredet i arbejdsgangseditoren, og klik derefter på **Egenskaber** for at åbne siden **Egenskaber**. Du kan derefter bruge følgende procedurer til at konfigurere forskellige egenskaber for arbejdsgangen.

## <a name="name-the-workflow"></a>Navngive arbejdsgangen

Udfør følgende trin for at angive et navn på arbejdsgangen.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Angiv et entydigt navn til arbejdsgangen i feltet **Navn**. Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, du opererer i, kan du navngive arbejdsgangen for indkøbsrekvisitioner **Indkøbsrekvisitioner Danmark** eller **Indkøbsrekvisitioner Spanien**.

## <a name="specify-the-workflow-owner"></a>Angive ejer af arbejdsgang

Ejeren af arbejdsgangen er den person, der administrerer og vedligeholder arbejdsgangen. Udfør følgende trin for at angive ejeren af arbejdsgangen.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Vælg navnet på den person, der skal administrere arbejdsgangen, på listen **Ejer**.

## <a name="select-an-email-template"></a>Vælge en e-mail-skabelon

Udfør følgende trin for at vælge den mailskabelon, der skal bruges til at generere beskeder om arbejdsgangen.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. På listen **E-mail-skabelon til arbejdsgangsbeskeder** skal du vælge skabelonen.

## <a name="enter-instructions-for-users"></a>Angive instruktioner til brugere

Du kan angive instruktioner til brugere, der sender dokumenter til behandling og godkendelse. Disse brugere kaldes også *igangsættere*. Antag f.eks., at du opretter en arbejdsgang for indkøbsrekvisitioner, og du angiver instruktioner. Disse instruktioner kan derefter ses af brugere, der angiver indkøbsrekvisitioner på siden **Indkøbsrekvisitioner**. Igangsætteren klikker på ikonet på arbejdsgangens meddelelseslinje for at få vist instruktioner. Udfør følgende trin for at angive instruktioner til brugerne.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. I feltet **Afsendelsesinstruktioner** skal du indtaste instruktionerne.
3. Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere. Pladsholdere erstattes med de relevante data, når instruktionerne vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. Klik et sted i feltet **Afsendelsesinstruktioner** for at angive, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.

4. Følg disse trin for at tilføje oversættelser af instruktionerne:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil personalisere teksten, kan du indsætte pladsholdere. I trin 3 kan du se anvisninger i, hvordan du angiver en pladsholder.
    6. Klik på **Luk**.

## <a name="specify-when-this-workflow-is-used"></a>Angive, hvornår denne arbejdsgang bruges

Du kan oprette flere arbejdsgange, der er baseret på samme type. Du kan f.eks. oprette en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, som du opererer i, f.eks. Indkøbsrekvisitioner Danmark eller Indkøbsrekvisitioner Spanien. Når der findes flere arbejdsgange, der er baseret på samme type, skal du angive, hvornår den enkelte arbejdsgang bruges. I det foregående eksempel skal du angive følgende betingelser:

- Indkøbsrekvisitioner Danmark bruges når: land/område = DK
- Indkøbsrekvisitioner Spanien bruges når: land/område = ES

Udfør følgende trin for at angive, hvornår den arbejdsgang, du konfigurerer, skal bruges.

1. Klik på **Aktivering** i venstre rude.
2. Markér afkrydsningsfeltet **Angiv betingelserne for at køre denne arbejdsgang**
3. Klik på **Tilføj betingelse**.
4. Angiv en betingelse.
5. Angiv eventuelle supplerende betingelser, hvis det er påkrævede.
6. Hvis du vil kontrollere, at de angivne betingelser er konfigureret korrekt, skal du følge disse trin:

    1. Klik på **Test**.
    2. På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.
    3. Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har angivet. Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner til Spanien, vises en liste over indkøbsrekvisitioner i området **Valider betingelse** på siden. Når du klikker på **Test**, evaluerer systemet den markerede indkøbsrekvisition for at finde ud af, om land/område er ES.
    4. Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.

## <a name="specify-when-notifications-are-sent"></a>Angive, hvornår beskeder sendes

Når et dokument sendes til behandling, oprettes en arbejdsgangsforekomst. Du kan sende beskeder til brugerne, når forekomster, som er baseret på arbejdsgangen, startes, fuldføres, afsluttes eller stoppes på grund af en fejl. Udfør følgende trin til at angive, hvornår der sendes beskeder.

1. Klik på **Beskeder** i ruden til venstre.
2. Markér afkrydsningsfeltet for hver hændelse, som skal udløse beskeder:

    - **Startet** – Send beskeder, når en arbejdsgangsforekomst er startet.
    - **Stoppet** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en fejl.
    - **Fuldført** – Send beskeder, når en arbejdsgangsforekomst er fuldført.
    - **Uoprettelig** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en uoprettelig fejl.
    - **Afsluttet** – Send beskeder, når en arbejdsgangsforekomst er afsluttet.

3. Vælg rækken for den hændelse, du har valgt i trin 2.
4. Indtast teksten til beskeden på fanen **Beskedtekst**.
5. Hvis du vil personalisere teksten, kan du indsætte pladsholdere. Pladsholderne erstattes med de relevante data, når teksten vises for brugerne. Udfør følgende trin for at indsætte en pladsholder.

    1. Klik i feltet for at angive, hvor pladsholderen skal vises.
    2. Klik på **Indsæt pladsholder**.
    3. Vælg den pladsholder, du vil indsætte, på den viste liste.
    4. Klik på **Indsæt**.
    5. En fælles pladsholder for **Beskedtekst**, der skal medtages, er "Seneste noter: %Workflow.Last note%", som viser alle kommentarer fra det forrige trin.

6. Følg disse trin for at tilføje oversættelser af teksten:

    1. Klik på **Oversættelser**.
    2. Klik på **Tilføj** på den viste side.
    3. På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.
    4. Indtast teksten i feltet **Oversat tekst**.
    5. Hvis du vil personalisere teksten, kan du indsætte pladsholdere. I trin 5 kan du se anvisninger i, hvordan du angiver en pladsholder.
    6. Klik på **Luk**.

7. På fanen **Modtager** skal du bruge følgende indstillinger til at angive, hvem der skal modtage beskeder.

    <table>
    <thead>
    <tr>
    <th>Indstilling</th>
    <th>Beskederne sendes til disse brugere.</th>
    <th>Hvis du vil sende beskeder, skal du følge disse trin</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltager</td>
    <td>Brugere, som er tildelt til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>På fanen <strong>Modtager</strong> skal du klikke på <strong>Deltager</strong>.</li>
    <li>På fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong> skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</li>
    <li>Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbejdsgangsbruger</td>
    <td>Brugere, som deltager i denne arbejdsgang</td>
    <td>
    <ol>
    <li>På fanen <strong>Modtager</strong> skal du klikke på <strong>Arbejdsgangsbruger</strong>.</li>
    <li>På fanen <strong>Arbejdsgangsbruger</strong> på listen <strong>Arbejdsgangsbruger</strong> skal du vælge en deltager i denne arbejdsgang.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Bruger</td>
    <td>Specifikke brugere</td>
    <td>
    <ol>
    <li>På fanen <strong>Modtager</strong> skal du klikke på <strong>Bruger</strong>.</li>
    <li>På fanen <strong>Bruger</strong> indeholder listen <strong>Tilgængelige brugere</strong> alle brugere. Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen.

Hvis du vil angive kommentarer om de ændringer, du har foretaget i arbejdsgangen, skal du udføre følgende trin.

1. Klik på **Noter** i ruden til venstre.
2. I feltet **Angiv kommentarer om arbejdsgangen** skal du angive dine kommentarer.
3. Gennemse kommentarer. Når du har tilføjet kommentarer, kan du ikke ændre dem.
4. Klik på **Tilføj** til at tilføje dine kommentarer til området **Kommentarhistorik**.