---
title: Politikker for frynsegodeberettigelse
description: Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: fd4def17bf60ae2812927221c45547c5ac379f2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417726"
---
# <a name="benefit-eligibility-policies"></a>Politikker for berettigelse til frynsegoder

Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.

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






[!INCLUDE[footer-include](../includes/footer-banner.md)]