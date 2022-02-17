---
title: Opret et nyt frynsegode
description: Denne opgave viser, hvordan du kan oprette frynsegodeelementer, der skal bruges, når du opretter et nyt frynsegode.
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 222bac97d461cd0a090c3e5d99594c07724818ff
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066970"
---
# <a name="create-a-new-benefit"></a>Opret et nyt frynsegode


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne opgave viser, hvordan du kan oprette frynsegodeelementer, der skal bruges, når du opretter et nyt frynsegode. Det demodatafirma, der bruges til at oprette denne opgave, er USMF. Opgaven er beregnet til en leder for kompensation og frynsegoder.


## <a name="create-benefit-elements"></a>Oprettet frynsegodeelementer

1. Gå til **Human Resources \> Personalegoder \> Konfiguration \> Personalegodeelementer**.
2. Vælg **Ny**.
3. Angiv navnet på den type frynsegode, du opretter, i feltet **Type**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Vælg en indstilling i feltet **Samtidig tilmelding**.

    Hvis du vil begrænse medarbejdernes mulighed for at tilmelde sig flere medicinske planer, skal du vælge **Én tilmelding pr. type**.

6. Vælg en indstilling i feltet **Lønart**.
7. Vælg **Ny** under fanen **Planer**.
8. Angiv en værdi i feltet **Plan**.
9. Indtast en værdi i feltet **Beskrivelse**.
10. Indtast eller vælg en værdi i feltet **Type**.
11. Vælg en indstilling i feltet **Løneffekt**.
12. Vælg **Gem**.

## <a name="create-a-benefit"></a>Oprette et personalegode

1. Gå til **Human resources \> Personalegoder \> Personalegoder**.
2. Vælg **Ny**.
3. I feltet **Plan** i rulledialogboksen skal du angive eller vælge en værdi.
4. Indtast eller vælg en værdi i feltet **Indstilling**.
5. Angiv en dato og et klokkeslæt i feltet **Gyldig**.
6. Vælg **Opret frynsegode**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
