---
title: Tilslutte et eksperiment og redigere variationer
description: Dette emne indeholder en beskrivelse af, hvordan du kan oprette forbindelse fra et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variationer til eksperimentet.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2020
ms.locfileid: "4411220"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Tilslutte et eksperiment og redigere variationer

Dette emne beskriver, hvordan du kan tilslutte dit eksperiment i Commerce og foretage ændringer i variationerne, så de stemmer overens med hypotesen. 

I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate emner.

[ ![Eksperimenteringens brugerrejse - tilslutte og redigere](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Når du har [konfigureret dit eksperiment](experimentation-setup.md) i en tredjepartstjeneste, skal du tilslutte eksperimentet i Dynamics 365 Commerce og redigere eksperimentets variationer.

## <a name="planning-considerations"></a>Overvejelser om planlægning

Før du tilslutter dit eksperiment i Commerce, skal du træffe nogle beslutninger, der påvirker den måde, som Commerce administrerer dit indhold på.

### <a name="determine-the-scope-of-your-experiment"></a>Fastlægge omfanget af dit eksperiment
Når du tilslutter et eksperiment, bliver du bedt om at definere omfanget af eksperimentet. Eksperimenter defineres som et **delvist** omfang eller **helt** omfang.
- Vælg **delvis**, hvis du vil gennemføre et eksperiment på en bestemt del af en side. Hvis du vælger denne indstilling, skal du identificere, hvilke moduler der er inkluderet i eksperimentet. Ændringer, der foretages af dele af standardsiden eller-fragmentet, som ikke er relateret til eksperimentet, synkroniseres automatisk på tværs af variationer.
- Vælg **hel**, hvis du vil gennemføre et eksperiment på en hel side eller et helt fragment. Der oprettes separate kopier af standardsiden eller -fragmentet. Du behøver ikke vælge, hvilke moduler der skal medtages i eksperimentet, fordi hele redigeringsoverfladen kan ændres. Du kan tilføje, slette eller omarrangere moduler efter behov. Hvis der foretages ændringer af den standardside eller det fragment, som eksperimentet er knyttet til, skal disse ændringer dog synkroniseres manuelt på tværs af alle variationer.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Hvis du knytter dit eksperiment til en side, der bruger et layout, kan du kun give eksperimentet et **helt** omfang.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Beslutte, om du vil planlægge, hvornår dit eksperiment skal publiceres
Hvis du vil planlægge, hvornår dit eksperiment bliver publiceret på dit live websted, skal du sørge for, at det indhold, du vil knytte til eksperimentet, er tilgængeligt i en publiceringsgruppe, *før* du tilslutter forsøget. 

Du kan finde flere oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).


## <a name="connect-your-experiment"></a>Tilslutte dit eksperiment
Hvis du vil tilslutte dit eksperiment, skal du starte guiden **Tilslut eksperiment**. Guiden fører dig gennem de trin, der er nødvendige for at kunne tilslutte dit eksperiment. Når du har fuldført guiden, er dit eksperiment tilsluttet, og variationer er oprettet og klar til at blive redigeret.

Benyt følgende fremgangsmåde for at komme i gang med at forbinde dit eksperimenter i Commerce-webstedsgenerator.

1. Hvis du vil starte guiden **Tilslut eksperiment**, skal du vælge **Eksperimenter** i venstre navigationsrude og derefter vælge **Opret forbindelse**. Du kan også få adgang til guiden fra en side- eller fragmenteditor ved at redigere den og vælge **Tilslut eksperiment** på kommandolinjen.

    > [!NOTE]
    > En side kan kun tilsluttes ét eksperiment ad gangen. Hvis du vil tilslutte en side i et andet eksperiment, skal du først slette det eksperiment, som siden er tilsluttet.

1. Vælg den side eller det fragment, du vil køre dit eksperiment på.
1. Indstil eksperimenterens omfang til **delvist** eller **helt**, afhængigt af hvad du har valgt i afsnittet [Fastlægge omfanget af dit eksperiment](#determine-the-scope-of-your-experiment) ovenfor.
    > [!NOTE]
    > Funktionsflaget **Eksperiment på sider eller fragmenter** skal være aktiveret, hvis du vil eksperimentere på en hel side eller et helt fragment. Se [Eksperimenteren i Dynamics 365 Commerce](experimentation-overview.md) for at få flere oplysninger.
    
1. Vælg **Opret variationer, og afslut guiden** i det sidste trin af guiden. Der oprettes variationer til eksperimentet. 

## <a name="edit-your-variations"></a>Redigere variationerne
Når du afslutter guiden, oprettes der variationer for dig. 

Derefter skal du redigere variationerne, så de afspejler de valg, du skal bruge for at kunne kontrollere hypotesen i eksperimentet. Vælg en af følgende procedurer, der svarer til det omfang, du valgte til eksperimentet, i afsnittet [Fastlægge omfanget af dit eksperiment](#determine-the-scope-of-your-experiment) ovenfor.

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Redigere variationer for eksperimenter med delvist omfang
Følg disse trin, hvis du har defineret omfanget af dit eksperimenter som **delvist** i guiden **Tilslut eksperiment**.

1. I editorvisning skal du bruge rullemenuen med variationer under kommandolinjen til at redigere de enkelte variationer baseret på din oprindelige hypotese. Det kan også være en god ide at oprette en kontrol- eller basisvariation ved at lade en af variationerne være uændret.
1. Vælg det modul, der skal eksperimenteres på, vælg ellipse (...), og vælg derefter **Føj til eksperiment**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Redigere variationer for eksperimenter med helt omfang
Hvis du har defineret eksperimentets omfang som **helt** i guiden **Tilslut eksperiment**, mens du er i editorvisning, skal du bruge rullemenuen med variationer under kommandolinjen til at redigere de enkelte variationer baseret på din oprindelige hypotese. 

> [!NOTE]
> Det kan i begge tilfælde være en god ide at oprette en kontrol- eller basisvariation ved at lade en af variationerne være uændret.

## <a name="previous-step"></a>Forrige trin
[Konfigurere et eksperiment](experimentation-setup.md) 


## <a name="next-step"></a>Næste trin
[Gennemse og publicere et eksperiment](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]