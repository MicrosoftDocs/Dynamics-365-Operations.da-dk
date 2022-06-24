---
title: Tilslutte et eksperiment og redigere variationer
description: Denne artikel indeholder en beskrivelse af, hvordan du kan oprette forbindelse fra et eksperiment i en tredjepartstjeneste til Dynamics 365 Commerce, og hvordan du redigerer variationer til eksperimentet.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942816"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Tilslutte et eksperiment og redigere variationer

Denne artikel beskriver, hvordan du kan tilslutte dit eksperiment i Commerce og foretage ændringer i variationerne, så de stemmer overens med hypotesen. 

I følgende diagram vises alle de trin, der er nødvendige for at konfigurere og køre et eksperiment på et e-handelswebsted i Dynamics 365 Commerce. Yderligere trin behandles i separate artikler.

[ ![Eksperimenteringens brugerrejse - tilslutte og redigere.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Når du har [konfigureret dit eksperiment](experimentation-setup.md) i en tredjepartstjeneste, skal du tilslutte eksperimentet i Dynamics 365 Commerce og redigere eksperimentets variationer.

## <a name="connect-your-experiment"></a>Tilslutte dit eksperiment
Hvis du vil tilslutte dit eksperiment, skal du starte guiden **Tilslut eksperiment**. Guiden fører dig gennem de trin, der er nødvendige for at kunne tilslutte dit eksperiment. Når du har fuldført guiden, er dit eksperiment tilsluttet, og variationer er oprettet og klar til at blive redigeret.

Benyt følgende fremgangsmåde for at komme i gang med at forbinde dit eksperimenter i Commerce-webstedsgenerator.

1. Hvis du vil starte guiden **Tilslut eksperiment**, skal du vælge **Eksperimenter** i venstre navigationsrude og derefter vælge **Opret forbindelse**. Du kan også få adgang til guiden fra en side- eller fragmenteditor ved at redigere den og vælge **Tilslut eksperiment** på kommandolinjen.

    > [!NOTE]
    > - En side kan kun tilsluttes ét eksperiment ad gangen. Hvis du vil tilslutte en side i et andet eksperiment, skal du først slette det eksperiment, som siden er tilsluttet.
    > - Du kan kun eksperimentere på sider med brugerdefinerede layouts. Hvis siden har et foruddefineret layout, skal du først konvertere det til et brugerdefineret layout. Det kan du gøre ved at gå til siden og vælge **Konverter til brugerdefineret layout** på kommandolinjen. Yderligere oplysninger om layout finder du i [Foruddefinerede og brugerdefinerede layouts](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Hvis du opretter forbindelse til et forsøg fra fanen **Forsøg** i venstre navigationsrude, skal du vælge navnet på forsøg på den liste, der vises.
1. Vælg den side eller det fragment, du vil køre dit eksperiment på.
1. Vælg **Opret variationer, og afslut guiden** i det sidste trin af guiden. Der oprettes variationer til eksperimentet. 

> [!NOTE]
> Hvis du vil planlægge, hvornår dit eksperiment bliver publiceret på dit live websted, skal du sørge for, at det indhold, du vil knytte til eksperimentet, er tilgængeligt i en publiceringsgruppe, *før* du tilslutter forsøget. Du kan finde flere oplysninger om publiceringsgrupper under [Arbejde med publiceringsgrupper](publish-groups.md).

## <a name="edit-your-variations"></a>Redigere variationerne

Når du afslutter guiden **Connect-forsøg**, oprettes der variationer for dig. Følg disse trin herunder for at redigere variationerne, så de afspejler de valg, du skal bruge for at kunne kontrollere hypotesen i eksperimentet.

1. I editorvisning skal du bruge rullemenuen med variationer under kommandolinjen til at redigere de enkelte variationer baseret på din oprindelige hypotese. Det kan også være en god ide at oprette en kontrol- eller basisvariation ved at lade en af variationerne være uændret.
1. Vælg det modul, der skal eksperimenteres på, vælg ellipse (...), og vælg derefter **Føj til eksperiment**.

> [!NOTE]
> Overvej at etablere en kontrol- eller basisvariation ved at lade en af variationerne være uændret.

## <a name="previous-step"></a>Forrige trin
[Konfigurere et eksperiment](experimentation-setup.md) 


## <a name="next-step"></a>Næste trin
[Gennemse og publicere et eksperiment](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
