---
title: Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål
description: Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11787aa0b32c0d7493e4528b00304e51f01a655f
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728899"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål. For eksempel, hvis du spørger "Foretrækker du kaffe eller te", bestemmes et logisk opfølgende spørgsmål afhængigt af om svarpersonen vælger kaffe eller te som deres svar. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="find-the-existing-questionnaire"></a>Find det eksisterende spørgeskema
1. Gå til **Spørgeskema** > **Design** > **Spørgeskemaer**.
2. Markér WorkFH-spørgeskemaet på listen.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Føj alle spørgsmål og underspørgsmål til spørgeskemaet
1. Klik på **Spørgsmål**.
2. Klik på **Ny**.
3. Vælg spørgsmålsnummer 00016 i feltet **Spørgsmål**.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på **Gem**.
7. Luk siden.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Angive Spørgeskemasekvensen til Betinget, og gør spørgsmålet afhængigt af det relevante spørgsmål
1. Klik på **Rediger**.
2. Udvid sektionen **Konfiguration**.
3. Vælg "Betinget" i feltet **Spørgsmålsrækkefølge**.
4. Klik på **Betinget** spørgsmål.
5. Vælg "Questions\Explain hvorfor du besvarede det forrige spørgsmål som du gjorde?" i træet.
6. Vælg spørgsmål 00009 i feltet **Overordnet spørgsmål**.
7. Klik op linket i den valgte række på listen.
8. Angiv svarsekvens-id for den svarmulighed, du vil gøre spørgsmålet afhængigt af, i feltet **Svar**. Angiv for eksempel 1 til den første Smart-indstilling.
9. Klik på **Gem**.
10. Vælg '"Spørgsmål\Jeg betales rimeligt for det arbejde, jeg udfører.".
    * Bemærk, at spørgsmålstræet opdateres for at vise afhængigheden.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
