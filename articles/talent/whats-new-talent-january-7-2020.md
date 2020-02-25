---
title: Nyheder eller ændringer i Dynamics 365 Talent (7. januar 2020)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974424"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Nyheder eller ændringer i Dynamics 365 Talent (7. januar 2020)

I denne artikel beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2697. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Kan ikke slette arbejdere, der ikke har ansættelsesposter - (386157)

Denne ændring tilføjer en sletteindstilling i formen **Arbejdere uden ansættelse**. Arbejdere vises i denne form, når der ikke findes fremtidige, aktive eller historiske ansættelser for arbejderen. I denne version er sletning kun aktiveret for systemadministratorer. I næste uges udgivelse vil sikkerheden dog blive opdateret, så alle brugere med rollen som personaleassistent kan fjerne medarbejdere uden ansættelser. Du kan også foretage disse ændringer manuelt ved at følge nedenstående trin.

1. Gå til **Sikkerhedskonfiguration**.
2. Filtrer listen **Rettigheder** under fanen **Rettigheder** til **Vedligehold medarbejdere**.
3. Vælg **Vis menupunkter** i kolonnen **Referencer**.
4. Vælg **HcmWOrkersWithoutEmployment** i **Vis menupunkter**.
5. Angiv rettigheden **Slet** til Tildel.
6. Vælg fanen **Ikke-publicerede objekter**.
7. Vælg **Publicer alle**.
