---
title: Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål
description: Betingede spørgsmål, kan du angive, hvilken opfølgende spørgsmål vises til en svarperson, efter svar på det foregående spørgsmål.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e49ee4dd1f2d4a5af3112d27eaf8d697904d2487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177073"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Stille et spørgsmål afhængigt af svaret på det forrige spørgsmål

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
