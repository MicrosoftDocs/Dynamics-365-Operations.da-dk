---
title: Politikker for frynsegodeberettigelse
description: "Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 076b4f14a09698b6a0e2f5f3dd4f74ef5b673a8d
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="benefit-eligibility-policies"></a>Politikker for frynsegodeberettigelse

[!include[banner](includes/banner.md)]


Dette emne indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.

Når du opretter fordele, kan du beslutte, hvilke fordele der er tilgængelige for hvilke medarbejdere. I følgende tabel vises eksempler på fordele, som du kan gøre tilgængelige for bestemte medarbejdere.

| Frynsegode          | Hvem frynsegodet er tilgængeligt for |
|------------------|---------------------------------|
| Sygesikring | Alle medarbejdere                   |
| Mobiltelefon     | Salgsmedarbejdere, ledere         |
| Parkeringskort   | Ledere                      |

Følgende komponenter bruges til at oprette politikker for frynsegodeberettigelse:

-   Typer politikregler
-   Politikker for frynsegodeberettigelse

Politikregeltyper definerer de forespørgselsparametre, der bruges til udvikling af specifikke politikregler. Når du opretter politikregeltyper, kan du oprette politikker for frynsegodeberettigelse. Ved hjælp af politikkerne kan du oprette en samling regler, der gælder for en eller flere juridiske enheder. Inden for hver politik kan du se nogle af de politikregeltyper for frynsegodeberettigelse, som du oprettede tidligere. 

Du kan definere omfanget af reglen i politikken. For eksempel, hvis du opretter en politikregeltype for frynsegodeberettigelse, som hedder **Leder**, kan du angive, hvad reglen er inden for denne politik. I dette eksempel kan reglen angive, at enhver stilling, der indeholder ordet "leder", skal være omfattet af reglen. Når du har defineret parametrene for reglen eller regler, der er inkluderet i politikken, kan du tildele en bestemt regel for frynsegodet.

<a name="see-also"></a>Se også
--------

[Definition og administration af et frynsegodeprogram](manage-benefit-program.md)




