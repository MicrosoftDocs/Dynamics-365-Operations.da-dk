---
title: Øjeblikkelig genopfyldning
description: Dette emne beskriver, hvordan du kan bruge øjeblikkelig genopfyldning til genopfyldning af lageret, når en lokationsvejledning ikke kan fordele lageret.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ab1f06951d5daceaf002b2cc23236dd818457985
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "348589"
---
# <a name="immediate-replenishment"></a>Øjeblikkelig genopfyldning

[!include [banner](../includes/banner.md)]

Øjeblikkelig genopfyldning gør det muligt at genopfylde lageret, så snart en lokationsvejledning ikke kan fordele lageret. Genopfyldningen er baseret på en enkelt linje i opsætningen af lokationsvejledningen. Hvis lageret ikke er disponibelt i den måleenhed, der er angivet af den pågældende linje, udføres der straks genopfyldning med den pågældende måleenhed.

Øjeblikkelig genopfyldning er et alternativ til den metode, hvor fordelingen af lager er baseret på flere linjer i lokationsvejledningen, og efterspørgslen opsummeres i slutningen af tildelingen og genopfyldes i den måleenhed, der er angivet i den sidste linje i lokationsvejledningen.

Fordelene ved at bruge øjeblikkelig opfyldning er, at genopfyldningen kan begrænses af bestemte enheder, og antallet kan sendes til bestemte lokationer.

## <a name="business-scenario"></a>Forretningsscenarie

Du har f.eks., et lagersted med separate plukområder for "kassen" og "hver" måleenhed. Du vil optimere plukprocessen ved at plukke så mange kasser som muligt og derefter plukke eventuelle restantal, der er mindre end en kasse fra området "hver".

I så fald kan du bruge øjeblikkelig genopfyldning. I lokationsvejledningen kan du konfigurere øjeblikkelig genopfyldning for kasser, så genopfyldning efter behov bruges, så snart der er mangel på kasser til plukning af behovsantallet. På denne måde kan du optimere plukprocessen, så plukningen omfatter så mange kasser som muligt. Øjeblikkelig genopfyldning genererer genopfyldning af kasserne, og behovet overføres ikke, så antallet plukkes i måleenheden for "hver". Med andre ord vil kun de antal, der skal plukkes i måleenheden for "hver" (dvs. antal, der er mindre end en boks), blive plukket fra området "hver". Hvis der opstår mangel i området "kasse", kan du plukke så mange kasser som muligt ud af det samlede behov. De resterende antal plukkes derefter fra området "hver".

## <a name="where-it-applies"></a>Hvor det er relevant

Øjeblikkelig genopfyldning anvendes under bølgeudførelse, hvis allokeringen mislykkes for en lokationsvejledningslinje, hvor der er angivet en genopfyldningsskabelon.

## <a name="set-up-immediate-replenishment"></a>Konfigurere øjeblikkelig genopfyldning

- Gå til **Lokationsstyring** \> **Opsætning** \> **Lokationsvejledning**, og klik derefter på fanen **Linjer** på listen **Skabelon for øjeblikkelig genopfyldning**, og vælg en genopfyldningsskabelon for bølgebehov.

Genopfyldningsskabelonen anvendes, hvis lokationsvejledningslinjen ikke kan tildele en dedikeret måleenhed.

## <a name="troubleshooting"></a>Fejlfinding

Hvis øjeblikkelig genopfyldning er valgt for en lokationsvejledningslinje, men intet genopfyldningsarbejde genereres, når du kan bruger skabeloner for genopfyldning efter behov for den pågældende lokationsvejledningslinje, skal to hovedårsager undersøges:

- Kontroller, at den skabelon for genopfyldning efter behov, der anvendes, er konfigureret til at bruge de rette lokationsskabeloner og arbejdsskabeloner af typen **Genopfyldning**.
- Sørg for, at der er tilstrækkelig disponibel lagerbeholdning på de lokationer, hvor skabelonen for genopfyldning efter behov søger efter den disponible lagerbeholdning med henblik på genopfyldning.
