--- 
title: Definere regler og politikker for frynsegodeberettigelse
description: Denne registrering viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c570574d15bbc55b4d0d79b8e62d74adcc15b387
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere regler og politikker for frynsegodeberettigelse

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne registrering viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.  

Det demodatafirma, der bruges til at oprette denne post, er USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Opret politikregeltyper for frynsegodeberettigelse
1. Gå til Personale > Frynsegoder > Berettigelse > Politikregeltyper for frynsegodeberettigelse.
2. Klik på Ny.
3. Skriv en værdi i feltet Regelnavn.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Forespørgselsnavn for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
7. Klik på Gem.
8. Luk siden.

## <a name="benefit-eligibility-policy"></a>Politik for frynsegodeberettigelse
1. Gå til Personale > Frynsegoder > Berettigelse > Politikker for frynsegodeberettigelse.
2. Vælg en eksisterende frynsegodepolitik.
3. Klik op linket i den valgte række på listen.
4. Slå udvidelsen af sektionerne Politikorganisationer til/fra.  Her kan du tilføje eller fjerne de organisationer, du vil medtage i politikken.
5. Udvid eller skjul sektionen Politikregler.
6. Find den politikregel, som blev oprettet tidligere, på listen.
7. Klik på Opret politikregel.
8. Angiv den dato, hvor politikken skal træde i kraft, i feltet ikrafttrædelsesdato.
    * Angivelse af ikrafttrædelses- og slutdatoer gør det muligt at foretage fremtidige ændringer i politikregler og fjerner behovet for at vende tilbage til politikken, når disse ændringer skal træde i kraft.  
9. 
    * Hvis du f.eks. ønsker, at reglen kun gælder for salgschefer, kan du oprette en Where-sætning for at sige: hvor stillingsbeskrivelsen er lig med salgschef.  Du kan bruge And eller Or i flere Where-sætninger sammen i reglen.  
10. Klik på OK.
11. Luk siden.
12. Luk siden.

## <a name="assign-rule-to-benefit"></a>Tildel reglen til frynsegodet
1. Gå til Personale > Frynsegoder > Frynsegoder.
2. Find og vælg den ønskede post på listen.
3. Klik op linket i den valgte række på listen.
4. Udvid eller skjul sektionen Berettigelsesregler.
5. Klik på Rediger.
6. Vælg Regelbaseret på listen i feltet Berettigelse.
7. Klik på rullelisten i feltet Regeltype for at åbne opslaget.
8. Find og vælg den regel, som blev oprettet tidligere, på listen.
9. Klik op linket i den valgte række på listen.
10. Klik på Gem.
11. Luk formularen.


