---
title: Omkostningskategorier, der bruges i produktionsruteplanlægning
description: Denne artikel indeholder oplysninger om omkostningsarter, der anvendes i produktionsmiljøer, og som bruger ruteplanlægning.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca4c0c9cecb79366cdd41069cb6c96f01b44a2094f4caf57077c391beb6ac106
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779680"
---
# <a name="cost-categories-used-in-production-routing"></a>Omkostningskategorier, der bruges i produktionsruteplanlægning

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om omkostningsarter, der anvendes i produktionsmiljøer, og som bruger ruteplanlægning.

Omkostningskategorier gælder for produktionsmiljøer, hvor der anvendes ruteplanlægning. De tildeles til operationsressourcer og ruteoperationer for at definere timeomkostninger og for at segmentere kostbidrag i beregnede omkostninger til en produceret vare. De kostgrupper, der er tildelt til omkostningskategorier, klassificerer bidrag til produktionsomkostninger baseret på operationsressourcerne og aktivitetstypen, f.eks. opsætnings- og procestid. Specificiteten af tildelinger af omkostningsgrupper, gør det muligt at beregne indirekte produktionsomkostninger baseret på ruteplanlægningsoplysninger. 

**Bemærk!** I produktionsmiljøer har omkostningskategorier også andre navne, f.eks. satskoder for arbejdsløn eller satskoder for maskiner. 

Hver enkelt omkostningskategori har tilknyttede omkostningsposter og en tildelt omkostningsgruppe. Flere omkostningskategorier er nødvendige for forskellige produktionsformål.

-   Tildel forskellige timeomkostninger, afhængigt af operationsressourcen. For eksempel kan omkostninger være forskellige for forskellige typer arbejdskompetencer, maskiner eller produktionsceller.
-   Tildel forskellige timeomkostninger for opstillingstid eller procestid, der er knyttet til en ruteoperation.
-   Tildel operationsressourceomkostninger baseret på udlagringsantal i stedet for timeomkostninger, f.eks. stykpriser for betalt arbejdskraft.
-   Angiv segmentering af omkostningsgrupper for kostbidrag til den beregnede kostpris for en produceret vare. Du kan eksempelvis segmentere omkostninger til arbejdskraft og maskiner.
-   Angiv basis for omkostningsgrupper for beregningsformler til indirekte omkostninger, f.eks. indirekte omkostning for arbejdskraft og indirekte omkostning for maskiner, der vedrører opstilling og procestid.

En omkostningskategori kan tildeles opstillingstid, procestiden og antal for en ruteoperation. Når f.eks. segmentering af omkostninger eller kostgrupper er forskellig i opsætnings- og procestiden, skal der defineres forskellige omkostningskategorier og tildeles opsætnings- og procestiden. Den særlige brug af omkostningskategorier til opstillingstid, procestid og antal bestemmes af den rutegruppe, der er tildelt en operation. Tildelingen af omkostningskategorier til tid og antal kan være godkendt af de politikker, der gælder for hele firmaet, og som defineres på siden **Produktionsstyringsparametre**. 

Hver enkelt omkostningskategori har tilknyttede omkostninger, der er baseret på definitionen af omkostningsposter i en efterkalkulationsversion. Du kan bruge siden **Pris for omkostningsart** til at definere omkostningsposter til en angivet efterkalkulationsversion og et angivet sted. Når omkostningsposten til en omkostningskategori angives første gang, har den statussen **Venter** og en ønsket ikrafttrædelsesdato. Når du aktiverer omkostningsposten, opdateres statussen til **Aktuelt aktiv**, og ikrafttrædelsesdatoen opdateres til aktiveringsdatoen. Forskellige omkostningsposter kan afspejle forskellige lokationer, ikrafttrædelsesdato eller statusser. I styklisteberegninger for en fremtidig eller historisk data anvendes der omkostningsposter, der har den relevante ikrafttrædelsesdato. Den aktuelle aktive omkostningspost bruges til at beregne omkostninger på en produktionsordre og til at estimere rapporteret tid i forhold til en produktionsordre. 

Omkostningsposten for en omkostningskategori kan være lokationsspecifik eller for hele firmaet. Hvis du vil gøre en omkostningspost lokationsspecifik, skal du knytte en lokation til den. Ellers angiver en tom værdi, at omkostningsposten gælder for alle lokationer i firmaet. Fordi omkostninger kan variere mellem lokationer, f.eks. skal omkostningsposter være defineret som lokationsspecifikke. 

En ruteoperation nedarver generelt de omkostningskategorier, der er tilknyttet operationsressourcen eller den overordnede operation. Når der oprettes en produktionsordre, afspejler ruteoperationerne i produktionsruten den valgte ruteversion. Du kan overstyre de omkostningskategorier, der er knyttet til operationerne i produktionsruten. 

Nogle typer produktionsarbejde kan gælde for projekttidsestimater og rapportering. Hvis det er tilfældet, en der også angives en omkostningsart til produktions- og projektformål. Du skal definere yderligere projektrelaterede oplysninger, når en omkostningskategori er markeret til brug i projekter.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]