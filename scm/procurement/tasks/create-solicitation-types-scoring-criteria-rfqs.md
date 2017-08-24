--- 
title: Oprette anmodningstyper og scorekriterier for tilbudsanmodninger
description: Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 04f8cb1a6375be9371bca2af7e4044392ce7322b
ms.openlocfilehash: c77173c5dd9f0513de5d794f7453715ceff550da
ms.contentlocale: da-dk
ms.lasthandoff: 08/02/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Oprette anmodningstyper og scorekriterier for tilbudsanmodninger

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode. Den viser også, hvordan du bruger anmodningstypen på en tilbudsanmodninger, som derefter angiver standardscoremetoden. Disse opgaver udføres normalt af en indkøbschef. Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data. Du skal have en scoremetode tilgængelig, før du starter.


## <a name="create-a-solicitation-type"></a>Oprette en anmodningstype.
1. Gå til Indkøb og forsyning > Opsætning > Tilbudsanmodning > Anmodningstype.
2. Klik på Ny.
3. Skriv en værdi i feltet Navn.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg i feltet Scoremetode den scoremetode, du vil bruge for denne anmodningstype.
6. Klik på Gem.
7. Luk siden.

## <a name="use-the-solicitation-type"></a>Brug anmodningstypen
1. Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.
2. Klik på Ny.
3. I feltet Anmodningstype skal du vælge den anmodningstype, som du lige har oprettet. 
4. Klik på OK.
5. Klik på Scorekriterier.
    * De scorekriterier, der vises, er dem fra scoremetoden, som du har knyttet til anmodningstypen. Du kan vælge at tilføje eller slette kriterierne på denne side. Det er også muligt at tilføje nye kriterier ved at kopiere dem fra andre scoremetoder.  
6. Klik på Kopiér kriterier.
7. Indtast eller vælg en værdi i feltet Scoremetode.
8. Klik på OK.
9. Luk siden.


