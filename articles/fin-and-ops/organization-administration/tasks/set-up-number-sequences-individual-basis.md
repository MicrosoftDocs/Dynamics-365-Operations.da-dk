---
title: Konfigurere nummerserier på individuel basis
description: Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6734d66a06f8a8dc90a48bd68b7b4e22177b4672
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560584"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Konfigurere nummerserier på individuel basis

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er. En masterdata- eller transaktionspost, der kræver et id, kaldes en reference. Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen. Du kan oprette alle nødvendige nummerserier på én gang ved at bruge guiden Oprette nummerserier, eller du kan oprette eller redigere enkelte nummerserier ved hjælp af siden Nummerserier.

1. Gå til Virksomhedsadministration > Nummerserier > Nummerserier.
2. Klik på Nummerserie.
3. Skriv en værdi i feltet Nummerseriekode.
4. Skriv en værdi i feltet Navn.
5. Udvid sektionen Intervalparametre.
    * Vælg et område til nummerserien i oversigtspanelet Intervalparametre, og vælg områdeværdier.     Området definerer, hvilke organisationer der bruger nummerserien. Nummerserier med et andet område end Delt kan desuden have segmenter, der passer til deres område. En nummerserie med området Juridisk enhed kan f.eks. have et segment, der udgøres af en juridisk enhed. Du kan finde flere oplysninger om områder i hjælpeemnet "Oversigt over nummerserier".  
6. Udvid sektionen Segmenter.
    * Definer formatet til nummerserien i oversigtspanelet Segmenter ved at tilføje, fjerne eller flytte rundt på segmenter.  
    * Nummerserier for alle områder kan indeholde konstante og alfanumeriske segmenter. Konstante segmenter indeholder et sæt alfanumeriske tegn, der ikke kan ændres. Brug denne segmenttype til at tilføje en bindestreg eller andre separatorer mellem nummerseriesegmenter. Alfanumeriske segmenter indeholder en kombination af nummertegn (#) og &-tegn (&). Disse tegn repræsenterer bogstaver og tal, der øges trinvist, hver gang der bruges et nummer fra serien. Brug et nummertegn (#) for at angive stigende tal, og &-tegnet til stigende bogstaver. Formatet #####_2014 giver f.eks. serien 00001_2014, 00002_2014 osv.     Der skal være mindst ét alfanumerisk segment. Områdesegmenter som f.eks. firma eller juridisk enhed er ikke påkrævede. Hvis du ikke medtager områdesegmenter i formatet, genereres der stadig numre pr. område for den valgte reference.  
7. Udvid sektionen Referencer.
    * Vælg den dokumenttype eller -post, som denne nummerserie skal knyttes til, i oversigtspanelet Referencer.     Dette trin er obligatorisk, hvis der er defineret serier til brugsmønstre til specielle formål. I disse tilfælde genereres der et nyt tal på basis af værdien af en nummerseriekode eller et nummerserie-id, uden at der bruges en reference. Et eksempel på et brugsmønster til specielle formål er en bilagsserie, der bruges til bestemte kladdenavn. Det anbefales dog, at du undlader at bruge mønstre af denne type.  
8. Udvid sektionen Generelt.
    * Angiv, om nummerserien er manuel, og om den er fortløbende eller ej, i oversigtspanelet Generelt. Angiv dernæst det laveste og det højeste nummer, der kan bruges i nummerserien.     Det anbefales, at man ikke ændrer en ikke-fortløbende nummerserie til en fortløbende nummerserie. Nummerserien vil ikke blive reelt kontinuerlig. Denne ændring kan også medføre fejl med dubletnøgler i databasen. Fortløbende nummerserier har desuden en større effekt på ydeevnen.   
9. Klik på Gem.

