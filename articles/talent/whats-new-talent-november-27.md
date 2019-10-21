---
title: Nyheder eller ændringer i Dynamics 365 Talent - Core HR (27. november 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9ff375ca97444d060c701e27c8fdcfecab4df186
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010170"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-november-27-2018"></a>Nyheder eller ændringer i Dynamics 365 Talent: Core HR (27. november 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2064**

Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.


## <a name="changes"></a>Ændringer

### <a name="unable-to-create-a-note-in-case-management"></a>Der kan ikke oprettes en note i Sagsstyring

Der er foretaget en ændring på grund af et problem under forsøg på at redigere eller oprette en note i sagsloggen i Sagsstyring.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Forkert stavet ord under fanen analyser i arbejdsområdet kompensation 

Er der foretaget en ændring for at rette stavningen af 'etnisk oprindelse' i kompensationsanalysediagrammet i arbejdsområdet kompensation.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Medarbejderes selvbetjeningsarbejdsområde vises ikke, når en bruger ikke er tildelt til en arbejder 

Der er foretaget en ændring, når arbejdsområdet **Medarbejderselvbetjening** vælges som den første side ved start for en bruger, der ikke er tildelt til en arbejder. Når dette er tilfældet, vises standarddashboardet.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Orlov og fravær-fejl: Objektreference er ikke indstillet til en forekomst af et objekt

Der er foretaget ændringer af Orlov og fravær, så fejlen rettes efter godkendelse af orlov- og fraværsposter på listen **Workflowopgaver, der er tildelt til mig**.

### <a name="unable-to-recall-an-image-workflow"></a>Et billede af en arbejdsgang kan ikke tilbagekaldes

Når et billede på en arbejdsgang tilbagekaldes, indstilles arbejdsgangen til "Annulleret", og den eksisterende anmodning kan slettes i selvbetjeningsarbejdsområdet for medarbejdere.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Genansatte medarbejdere eller kontrahenter vises flere gange efter afslutning 

Med denne opdatering vises fratrådte medarbejdere, der er genansat, kun én gang på listen over afsluttede. 

## <a name="known-issue"></a>Kendt problem

- **Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet. 
- **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket. Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret. (Dette problem vil blive løst i den næste platformsopdatering).
