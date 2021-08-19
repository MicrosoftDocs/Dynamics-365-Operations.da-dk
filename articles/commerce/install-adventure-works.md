---
title: Installere Adventure Works-temaet
description: Dette emne beskriver, hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655842"
---
# <a name="install-the-adventure-works-theme"></a>Installere Adventure Works-temaet

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du installerer Adventure Works-temaet i Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> Adventure Works-temaet og -modulerne er tilgængelige fra og med Dynamics 365 Commerce version 10.0.20. De er tilgængelige fra Microsoft AppSource.

## <a name="prerequisites"></a>Forudsætninger

Før du installerer Adventure Works-temaet, skal du have et Dynamics 365 Commerce-miljø (Commerce version 10.0.20 eller senere), der omfatter Retail Cloud Scale Unit (RCSU), online Commerce-softwareudviklingssæt (SDK) og Commerce-modulbiblioteket. Du kan finde oplysninger om installation af Commerce SDK og modulbiblioteket i [SDK og modulbiblioteksopdateringer](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Installationstrin

### <a name="install-the-adventure-works-theme-in-your-application"></a>Installere Adventure Works-temaet i programmet

Adventure Works-temapakken er tilgængelig i feedet for **dynamics365-commerce** som **@msdyn365-commerce-theme/adventureworks-theme-kit**. Selvom Adventure Works-temapakken er en del af dette feed, er den placeret under et andet navneområde. Derfor skal du følge disse trin for at tilføje registreringsdatabaseposter for navneområdet.

1. Opdater filen **.npmrc**, så den indeholder følgende registreringsdatabasepost (hvis posten ikke allerede er inkluderet):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Opdater filen **.yarnrc**, så den indeholder følgende registreringsdatabasepost (hvis posten ikke allerede er inkluderet):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Hvis du vil installere pakken i dit lokale miljø, skal du køre følgende kommando fra kommandoprompten. Denne kommando opdaterer automatisk filen package.json, så den omfatter afhængigheden.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

I filen **package.json** skal du opdatere den aktuelle temaversion til en bestemt version.

> [!IMPORTANT]
> - Temaversionen skal passe til versionen af modulbiblioteket for at sikre, at alle funktioner fungerer som forventet. 
> - Minimumsversionen for Commerce-modulbiblioteket og SDK skal være 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Tilføje skrifttypefiler til Adventure Works-temaet

Når Adventure Works-temaet er installeret i appen, skal du tilføje de skriftfiler, der kræves til den. For at fuldføre dette trin skal du kopiere alle skrifttypefiler fra **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** til stien for partnerprogrammets offentlige mappe **\public\webfonts**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Konfigurere ressourcerne for Adventure Works-temaet

Næste trin er at opdatere den krævede standardressource for temaet. For at fuldføre dette trin skal du kopiere indholdet fra filen globale.json under **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** til partnerprogrammets fil global.json under **\src\resources\modules**. Hvis målmappen **\src\resources** ikke findes, kan den kopieres i sin helhed fra kildemappen **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** til målmappen **\src**.

### <a name="pull-updates-and-validate-the-theme"></a>Trække opdateringer og validere temaet

Yderligere oplysninger om, hvordan du trækker det seneste SDK, modulbiblioteket og andre opdateringer af afhængighed, finder du i afsnittet "Trække opdateringer" i [Opdateringer af SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#pull-updates).

Når de seneste afhængigheder er trukket ned, kan du køre kommandoen **yarn start** for at starte Node-serveren i udviklingsmiljøet, og teste det nye Adventure Works-tema. Gennemse programmet lokalt ved hjælp af parameteren for forespørgselsstrengen `?theme=adventureworks` (f.eks. `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Yderligere ressourcer

[Adventure Works-tema](adventure-works-theme.md)

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]