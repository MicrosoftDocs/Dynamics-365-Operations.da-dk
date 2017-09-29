---
title: "Bogføringsdefinitioner"
description: "Denne artikel indeholder oplysninger om bogføringsdefinitioner, og hvordan du definerer og kæder dem sammen. Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e1865a695a89ed0501f97189b542b3915a96bf08
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="posting-definitions"></a>Bogføringsdefinitioner

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om bogføringsdefinitioner, og hvordan du definerer og kæder dem sammen. Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter.

Til understøttede bogføringstyper og -dokumenter kan du bruge bogføringsdefinitioner i stedet for posteringsprofiler til at klassificere hovedkonti og økonomiske dimensioner på regnskabsposter. Du kan se de understøttede dokumenter og bogføringstyper på siden **Definitioner af posteringsbogføring**. 

Hvis du vil bruge bogføringsdefinitioner, skal du vælge indstillingen**Brug bogføringsdefinitioner** på siden **Finansparametre**. Selv når du bruger bogføringsdefinitioner, skal du stadig definere posteringsprofiler for de oprindelige poster og de ikke-understøttede bogføringsprofiler og -dokumenter. 

Du skal bruge bogføringsdefinitioner for at kunne aktivere indeholder bogføring af behæftelser for indkøbsordrer og bogføring af budgetreservationer for indkøbsrekvisitioner.

## <a name="defining-posting-definitions"></a>Definition af bogføringsdefinitioner
Brug siden**Bogføringsdefinitioner** til at angive søgekriterier og definere de poster, der skal genereres, når der opstår et match. Søgekriterierne evalueres som regnskabsfordelinger for de oprindelige poster. 

På siden **Bogføringsdefinitioner** kan du også tildele prioritetsnumre til posteringslinjer for at styre den rækkefølge, linjerne evalueres i. De linjer, der har det laveste prioritetsnummer, evalueres først. For eksempel evalueres alle linjer, der har prioritet 1, og derefter linjer, der har en prioritet 2, osv. Når der er overensstemmelse, ignoreres de andre søgekriterier. Desuden er det kun de kriterier i gruppen, der matcher den oprindelige transaktion, der opretter genererede poster. 

Du kan validere dine bogføringsdefinitioner ved hjælp af guiden **Test bogføringsdefinition**. Når du definerer et eksempel på en oprindelig postering for en bogføringsdefinition, kan du se de genererede poster. 

Du kan bruge bogføringsdefinitionsversioner sammen med ikrafttrædelsesdatoer. Du kan f.eks. oprette en fremtidig version af en bogføringsdefinition til bogføring på en anden finanskonti i et nyt regnskabsår. 

Brug siden **Definitioner af posteringsbogføring** til at tildele bogføringsdefinitioner til transaktionstyper.

## <a name="linking-posting-definitions"></a>Tilknytning af bogføringsdefinitioner
Du kan sammenkæde én bogføringsdefinition med en anden, når du opretter dem. Kriterierne for den definition, du har sammenkædet til, tages derefter i betragtning sammen med kriterierne for den aktuelle bogføringsdefinition. Denne funktion hjælper dig med at spare tid, fordi du ikke behøver at indtaste kriterierne igen på oversigtspanelet **Poster** på siden **Bogføringsdefinitioner** for den aktuelle bogføringsdefinition, hvis du allerede har angivet linjerne for en anden definition. 

I diagrammerne eller tabellerne kan du alle de sammenkædninger, du kan komme til at bruge. For at undgå konflikter med den aktuelle bogføringsdefinition bør du sikre dig, at linjerne i alle bogføringsdefinitioner, som du sammenkæder til, er entydige. 

Der er følgende begrænsninger, når du opretter sammenkædninger i bogføringsdefinitioner:

-   En given bogføringsdefinition kan enten sammenkædes med en anden bogføringsdefinition, eller der kan oprettes en sammenkædning til den fra en anden bogføringsdefinition, men ikke begge dele. Men en bogføringsdefinition kan blive kædet samme med flere bogføringsdefinitioner.
-   Du kan oprette sammenkædninger blandt bogføringsdefinitioner i samme modul.
-   Du kan tildele en bogføringsdefinition til alle posteringstyper, men posteringstypen skal være i samme modul som bogføringsdefinitionen. Brug siden **Definitioner af posteringsbogføring** for at se, hvilket modul en transaktionstype er i.


Yderligere oplysninger finder du i afsnittet [Eksempler på posteringsdefinitioner](example-posting-definitions.md). 


