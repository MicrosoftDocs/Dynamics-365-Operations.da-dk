---
title: Konfigurere individuelle nummerserier
description: Dette emne beskriver, hvordan du konfigurerer nummerserier på individuel basis.
author: sericks007
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83ebcf96aa6a5b5c757285be1c5602ac4e8f50fc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890852"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Konfigurere individuelle nummerserier

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer nummerserier på individuel basis. Nummerserier bruges til generering af læselige, entydige id'er for masterdataposter og transaktionsposter, der kræver id'er. En masterdata- eller transaktionspost, der kræver et id, kaldes en reference. Før du kan oprette nye poster til en reference, skal du konfigurere en nummerserie og knytte den til referencen. Du kan oprette alle nødvendige nummerserier på én gang ved at bruge guiden **Opret nummerserier**, eller du kan oprette eller redigere enkelte nummerserier ved hjælp af siden **Nummerserier**.

1. Gå til **Navigationsrude > Moduler > Organisationsadministration > Nummerserier > Nummerserier**.
2. Vælge **Nummerserier**.
3. Skriv en værdi i feltet **Nummerseriekode**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg et område til nummerserien i oversigtspanelet **Områdeparametre**, og vælg områdeværdier fra rullelisten. Området definerer, hvilke organisationer der bruger nummerserien. Nummerserier med et andet område end **Delt** kan desuden have segmenter, der passer til deres område. En nummerserie med området **Juridisk enhed** kan f.eks. have et segment, der udgøres af en juridisk enhed. Du kan finde flere oplysninger om områder i [Oversigt over nummerserier](../number-sequence-overview.md). 
6. Udvid sektionen **Segmenter**.
    - Definer formatet til nummerserien ved at tilføje, fjerne eller flytte rundt på segmenter.  
    - Nummerserier for alle områder kan indeholde *Konstante segmenter* og *Alfanumeriske segmenter*. Konstante segmenter indeholder et sæt alfanumeriske tegn, der ikke kan ændres. Brug denne segmenttype til at tilføje en bindestreg eller andre separatorer mellem nummerseriesegmenter. Alfanumeriske segmenter indeholder en kombination af nummertegn (#) og &-tegn (&). Disse tegn repræsenterer bogstaver og tal, der øges trinvist, hver gang der bruges et nummer fra serien. Brug et nummertegn (#) for at angive stigende tal, og &-tegnet til stigende bogstaver. Formatet `#####_2014` opretter eksempelvis serien `00001_2014`, `00002_2014` osv. Der skal være mindst ét alfanumerisk segment. Områdesegmenter som f.eks. firma eller juridisk enhed er ikke påkrævede. Hvis du ikke medtager områdesegmenter i formatet, genereres der stadig numre pr. område for den valgte reference.  
7. Udvid sektionen **Referencer**. Vælg den dokumenttype eller postering, som denne nummerserie skal knyttes til, i oversigtspanelet. Dette trin er obligatorisk, hvis der er defineret serier til brugsmønstre til specielle formål. I disse tilfælde genereres der et nyt tal på basis af værdien af en nummerseriekode eller et nummerserie-id, uden at der bruges en reference. Et eksempel på et brugsmønster til specielle formål er en bilagsserie, der bruges til bestemte kladdenavn. Det anbefales dog, at du undlader at bruge mønstre af denne type.  
8. Udvid sektionen **Generelt**. Angiv, om nummerserien er manuel, og om den er fortløbende eller ej, i oversigtspanelet Generelt. Angiv dernæst det laveste og det højeste nummer, der kan bruges i nummerserien. Det anbefales, at man ikke ændrer en ikke-fortløbende nummerserie til en fortløbende nummerserie. Nummerserien vil ikke blive reelt kontinuerlig. Denne ændring kan også medføre fejl med dubletnøgler i databasen. Fortløbende nummerserier har desuden en større effekt på ydeevnen.   
9. Klik på **Gem**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
