---
title: Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål
description: Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae4a792e53127196aacdf659bb483867d5c17494
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794727"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål. For eksempel, hvis du spørger "Foretrækker du kaffe eller te", bestemmes et logisk opfølgende spørgsmål afhængigt af om svarpersonen vælger kaffe eller te som deres svar. Det demodatafirma, der bruges til at oprette denne procedure, er USMF.


## <a name="find-the-existing-questionnaire"></a>Find det eksisterende spørgeskema
1. Gå til Spørgeskema > Design > Spørgeskemaer.
2. Markér WorkFH-spørgeskemaet på listen.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Føj alle spørgsmål og underspørgsmål til spørgeskemaet
1. Klik på Spørgsmål.
2. Klik på Ny.
3. Vælg spørgsmålsnummer 00016 i feltet Spørgsmål.
4. Find og vælg den ønskede post på listen.
5. Klik op linket i den valgte række på listen.
6. Klik på Gem.
7. Luk siden.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Angive Spørgeskemasekvensen til Betinget, og gør spørgsmålet afhængigt af det relevante spørgsmål
1. Klik på Rediger.
2. Udvid sektionen Konfiguration.
3. Vælg "Betinget" i feltet Spørgsmålsrækkefølge.
4. Klik på Betinget spørgsmål.
5. Vælg "Questions\Explain hvorfor du besvarede det forrige spørgsmål som du gjorde?" i træet.
6. Vælg spørgsmål 00009 i feltet Overordnet spørgsmål.
7. Klik op linket i den valgte række på listen.
8. Angiv det svarsekvens-id for den svarmulighed, du vil gøre spørgsmålet afhængigt af, i feltet Svar. Angiv for eksempel 1 til den første Smart-indstilling.
9. Klik på Gem.
10. Vælg '"Spørgsmål\Jeg betales rimeligt for det arbejde, jeg udfører.".
    * Bemærk, at spørgsmålstræet opdateres for at vise afhængigheden.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]