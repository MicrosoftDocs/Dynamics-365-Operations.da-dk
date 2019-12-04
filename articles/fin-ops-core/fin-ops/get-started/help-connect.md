---
title: Oprette forbindelse til Hjælp-systemet
description: I dette emne beskrives komponenterne i Hjælp-systemet til Finance and Operations-apps, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter brugerdefineret Hjælp.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812574"
---
# <a name="connect-the-help-system"></a>Oprette forbindelse til Hjælp-systemet

[!include [banner](../includes/banner.md)]

Dette emne beskriver komponenterne i Hjælp-systemet til Finance and Operations-apps, f.eks. Dynamics 365 Finance Supply Chain Management, Retail og Talent. Det giver et overblik over, hvordan du forbinder disse komponenter, og en oversigt over, hvordan du opretter brugerdefinerede Hjælp.

## <a name="help-architecture"></a>Hjælp-arkitektur

I følgende illustration vises delene i Hjælp-systemet. Hjælp-systemet i produkter henter artikler fra https://docs.microsoft.com samt opgaveguides, der er gemt i Forretningsmodeldesigner i LCS (Lifecycle Services).

> [!NOTE]
> De funktioner, der vises i diagrammet med en stjerne (\*), er planlagt, men er endnu ikke tilgængelige.

[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Forbindelse til Hjælp-systemet

> [!NOTE]
> Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Dynamics 365 Talent eller Retail. Vi arbejder aktuelt på at aktivere denne funktion i en senere version. Opgaveguiderne i oplevelsen Introduktion i Talent forbliver tilgængelig og dækker de grundlæggende funktioner. Automatiseret hjælp er også tilgængelig på docs.microsoft.com-webstedet for både Retail og Talent.

På siden **Systemparametre** kan systemadministratorer stykke Hjælp-systemet sammen med henblik på implementering.

[![Formularen Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

På siden **Systemparametre** skal du følge disse trin:

> [!IMPORTANT]
> Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services. Du skal klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på **OK** for at få adgang til siden **Systemparametre**.
>
> [![Opret forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Opret forbindelse til LCS")](./media/connect-to-lcs-crop.png)

1. Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
2. Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.
3. Angiv visningsrækkefølgen for BPM-bibliotekerne. Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.

Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se de opgaveguider, der gælder for den aktuelle side i Finance and Operations. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.

### <a name="showing-translated-task-guides"></a>Visning af oversatte opgaveguider

Oversatte opgaveguider blev introduceret i APQC Unified-biblioteket maj 2016, og introduktionsbiblioteket. Når du vil se den lokaliserede hjælp til opgaveguider i Finance and Operations-apps, skal du sørge for, at der er forbindelse til maj-biblioteket. Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.

> [!NOTE]
> Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i klienten lige nu. Kun de opgaveguider, der blev udgivet i februar 2016, er tilgængelige i oversatte versioner i maj-biblioteket. Vi udsender et opdateret bibliotek med flere oversættelser.
>
> - Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
> - Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.

## <a name="creating-custom-help"></a>Oprettelse af tilpasset hjælp

Du kan bruge opgaveguider til at oprette brugerdefineret hjælp eller oprette forbindelse til Hjælp-ruden på et websted.

### <a name="create-custom-help-with-task-guides"></a>Oprette tilpasset hjælp til opgaveguider

Du kan oprette en brugerdefineret hjælp til Finance, Supply Chain Management og til Retail ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem i et bibliotek i en LCS-forretningsproces. Du kan ikke oprette brugerdefinerede opgaveguider til Talent.

Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder. Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer. Du kan finde flere oplysninger under [Arbejdsrutineoptagerressourcer](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Oprette forbindelse til et brugerdefineret websted

Microsoft har udgivet en hvidbog og eksempelkode, der beskriver, hvordan du opretter og tilknytte et brugerdefineret Hjælp-websted til Hjælp-ruden. Du kan finde flere oplysninger i:

- [Oprette brugerdefineret Hjælp til Finance and Operations-apps (hvidbog)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Brugerdefineret GitHub-hjælpelager](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Yderligere ressourcer

[Hjælp-system](help-overview.md)

[Ressourcer til arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder.md)

[Oprette dokumentation eller kursusmateriale ved hjælp af Arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder-training-docs.md)
