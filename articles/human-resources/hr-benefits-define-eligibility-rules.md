---
title: Definere regler og politikker for frynsegodeberettigelse
description: Denne artikel viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805940"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Definere regler og politikker for frynsegodeberettigelse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emne viser dig, hvordan du kan oprette regler og politikker for frynsegodeberettigelse og derefter tildele regler til frynsegoderne.  

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