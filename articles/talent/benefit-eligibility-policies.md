---
title: Politikker for frynsegodeberettigelse
description: Denne artikel indeholder oplysninger om politikker for frynsegodeberettigelse, som gør det lettere at definere, hvem der er berettiget til særlige frynsegoder.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: b44287bf22f0b6c4e33a29b4b86aaae934505a43
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814686"
---
# <a name="benefit-eligibility-policies"></a>Politikker for frynsegodeberettigelse

[!include [banner](includes/banner.md)]

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

<a name="additional-resources"></a>Yderligere ressourcer
--------

[Definere og administrere et frynsegodeprogram](manage-benefit-program.md)



