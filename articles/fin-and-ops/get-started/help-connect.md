---
title: Oprette forbindelse til Hjælp-systemet
description: I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Finance and Operations, og du får et overblik over, hvordan du tilslutter dem, og hvordan du opretter en brugerdefineret Hjælp.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
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
ms.openlocfilehash: 929e453987c6e2773d1886d03a4393a68033566b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850895"
---
# <a name="connect-the-help-system"></a>Oprette forbindelse til Hjælp-systemet

[!include [banner](../includes/banner.md)]

I dette emne beskrives komponenterne i hjælpesystemet til Microsoft Dynamics 365 for Finance and Operations. Det giver et overblik over, hvordan du forbinder disse komponenter, og en oversigt over, hvordan du opretter brugerdefinerede Hjælp.

## <a name="help-architecture"></a>Hjælp-arkitektur

I følgende illustration vises de dele, som Finance and Operations Hjælp-systemet består af. Hjælpesystemet i produkter trækker artikler fra Finance and Operations-webstedet på https://docs.microsoft.com samt opgaveguides, der er gemt i Forretningsmodeldesigner i Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> De funktioner, der vises i diagrammet med en stjerne (\*), er planlagt, men er endnu ikke tilgængelige.

[![Hjælp-arkitektur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Forbindelse til Hjælp-systemet

> [!NOTE]
> Fanen **Opgaveguider** er i øjeblikket ikke tilgængelig i Microsoft Dynamics 365 for Talent og Microsoft Dynamics 365 for Retail. Vi arbejder aktuelt på at aktivere denne funktion i en senere version. Opgaveguiderne i oplevelsen Introduktion i Talent forbliver tilgængelig og dækker de grundlæggende funktioner. Automatiseret hjælp er også tilgængelig på webstedet docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for både Retail og Talent.

På siden **Systemparametre** kan systemadministratorer stykke Hjælp-systemet sammen med henblik på implementering.

[![Formularen Systemparametre med hjælpeindstillinger](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

På siden **Systemparametre** skal du følge disse trin:

> [!IMPORTANT]
> Første gang du åbner fanen **Hjælp**, skal du oprette forbindelse til Lifecycle Services. Du skal klikke på linket i midten af formularen, vente på forbindelsen, lukke dialogboksen og derefter klikke på **OK** for at få adgang til siden **Systemparametre**.
>
> [![Oprette forbindelse til LCS](./media/connect-to-lcs-crop-1024x365.png "Oprette forbindelse til LCS")](./media/connect-to-lcs-crop.png)

1. Vælg det Lifecycle Services-projekt, der skal oprettes forbindelse til.
2. Vælg BPM-biblioteker (inden for det valgte projekt), hvor der skal hentes opgaveregistreringer fra.

    - For Microsoft-indhold i Finance and Operations skal du vælge APQC Unified-biblioteket til Finance and Operations.
    - For Retail frigiver vi et bibliotek i nærmeste fremtid.
    - Du behøver ikke at vælge et bibliotek til Talent. Der er oprettet forbindelse til det korrekte bibliotek for dig.

3. Angiv visningsrækkefølgen for BPM-bibliotekerne. Dette bestemmer den rækkefølge, som opgaveregistreringer fra bibliotekerne vises i på ruden **Hjælp**.

Når du har fuldført disse trin, kan du åbne ruden **Hjælp** og klikke på fanen **Opgaveguider**. Nu kan du se opgaveguiderne, der gælder for den aktuelle side i Finance and Operations. Hvis der ikke findes opgaveguider, kan du angive nøgleord for at indsnævre søgningen.

### <a name="showing-translated-task-guides"></a>Visning af oversatte opgaveguider

Oversatte opgaveguider blev introduceret i APQC Unified-biblioteket maj 2016, og introduktionsbiblioteket. Når du vil se den lokaliserede hjælp til opgaveguider i Finance and Operations, skal du sørge for, at der er forbindelse til maj-biblioteket. Det sprog, en opgaveguide vises på, styres for hver bruger af sprogindstillingerne under **Indstillinger** &gt; **Indstillinger**.

> [!NOTE]
> Selvom mange opgaveguider er blevet oversat, vises navnene på de oversatte opgaveguider ikke i Finance and Operations-klienten lige nu. Kun de opgaveguider, der blev udgivet i februar 2016, er tilgængelige i oversatte versioner i maj-biblioteket. Vi udsender et opdateret bibliotek med flere oversættelser.
>
> - Hvis en opgaveguide er blevet oversat, vises teksten i opgaveguiden på det valgte sprog, når du åbner denne opgaveguide.
> - Hvis en opgaveguide ikke er blevet oversat, er det kun noget af teksten (tekst i kontrolelementerne), der vises på det valgte sprog, når du åbner guiden.

## <a name="creating-custom-help"></a>Oprettelse af tilpasset hjælp

Du kan bruge opgaveguider til at oprette brugerdefineret hjælp eller oprette forbindelse til Hjælp-ruden på et websted.

### <a name="create-custom-help-with-task-guides"></a>Oprette tilpasset hjælp til opgaveguider

Du kan oprette en brugerdefineret hjælp til Finance and Operations og til Retail ved at oprette opgaveregistreringer, der afspejler din implementering, og gemme dem på et bibliotek i LCS Business Proces. Du kan ikke oprette brugerdefinerede opgaveguider til Talent.

Hvis du som partner fremmer et bibliotek til at være virksomhedens bibliotek og medtager det i en løsning, bliver det tilgængeligt for dine kunder. Du kan også oprette en kopi af det globale APQC Unified-bibliotek og derefter åbne kopien, åbne opgaveregistreringer fra det, redigere dem og gemme registreringerne med dine ændringer. Du kan finde flere oplysninger under [Sådan opretter du en opgaveregistrering, der skal bruges som dokumentation eller uddannelse](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Oprette forbindelse til et brugerdefineret websted

Microsoft har udgivet en hvidbog og eksempelkode, der beskriver, hvordan du opretter og tilknytte et brugerdefineret Hjælp-websted til Hjælp-ruden. Du kan finde flere oplysninger i:

- [Oprette brugerdefineret Hjælp til Finance and Operations (hvidbog)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Brugerdefineret GitHub-hjælpelager](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Hjælp](help-overview.md)

[Oversigt over Arbejdsrutineoptager](../../dev-itpro/user-interface/task-recorder.md)

[Sådan opretter du en opgaveregistrering, der kan bruges til dokumentation eller undervisning](../../dev-itpro/user-interface/task-recorder-training-docs.md)
