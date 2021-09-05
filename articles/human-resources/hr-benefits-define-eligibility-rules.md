---
title: Definere regler og politikker for frynsegodeberettigelse
description: Dette emne forklarer, hvordan du opretter regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoder.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 59a0ee2f8a1411e921da1d348b87038f9aafccd3
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416851"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere regler og politikker for frynsegodeberettigelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne forklarer, hvordan du opretter regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoder.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Opret politikregeltyper for frynsegodeberettigelse

1. Gå til **Human Resources > Frynsegoder > Berettigelse > Politikregeltyper for frynsegodeberettigelse**.
2. Vælg **Ny**.
3. Angiv en værdi i feltet **Regelnavn**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Klik på rullelisten i feltet **Forespørgselsnavn** for at åbne opslaget.
6. Vælg linket i den valgte række på listen.
7. Vælg **Gem**.
8. Luk siden.

## <a name="benefit-eligibility-policy"></a>Politik for personalegodeberettigelse

1. Gå til **Human Resources > Frynsegoder > Berettigelse > Politikker for frynsegodeberettigelse**.
2. Vælg en eksisterende frynsegodepolitik.
3. Vælg linket i den valgte række på listen.
4. Slå udvidelsen af sektionerne **Politikorganisationer** til/fra. Du kan tilføje eller fjerne de organisationer, du vil medtage i politikken.
5. Udvid eller skjul sektionen **Politikregler**.
6. Find den politikregel, som blev oprettet tidligere, på listen.
7. Vælg **Opret politikregel**.
8. Angiv den dato, hvor politikken skal træde i kraft, i feltet **Ikrafttrædelsesdato**.
    * Angivelse af gældende slutdatoer gør det muligt at foretage fremtidige ændringer i politikregler, så det ikke er nødvendigt at vende tilbage til politikken, når disse ændringer skal træde i kraft.  
9. Tilføj om nødvendigt en where-sætning i feltet **Tilføj betingelse**.
    * Hvis du f.eks. ønsker, at reglen kun gælder for salgschefer, kan du oprette en Where-sætning for at sige: hvor stillingsbeskrivelsen er lig med salgschef. Du kan tilføje flere Where-sætninger sammen i reglen.  
10. Vælg **OK**.
11. Luk siden.

## <a name="assign-rule-to-benefit"></a>Tildel reglen til frynsegodet

1. Gå til **Human resources > Frynsegoder > Frynsegoder**.
2. Find og vælg den ønskede post på listen.
3. Vælg linket i den valgte række på listen.
4. Udvid eller skjul sektionen **Berettigelsesregler**.
5. Vælg **Rediger**.
6. Vælg Regel i feltet **Berettigelse**.
7. Vælg den regel, som du oprettede tidligere, i feltet **Regeltype**.
9. Vælg linket i den valgte række på listen.
10. Vælg **Gem**.
11. Luk formularen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
