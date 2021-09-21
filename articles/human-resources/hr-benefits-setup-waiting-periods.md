---
title: Konfigurere venteperioder
description: I Microsoft Dynamics 365 Human Resources opretter ventedage en milepæl, der bruges til frynsegodeplaner.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 537ca48e819f047f2095bd5d9337ac7d80e49c5f
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431059"
---
# <a name="configure-waiting-periods"></a>Konfigurere venteperioder

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I Microsoft Dynamics 365 Human Resources opretter ventedage en milepæl, der bruges til frynsegodeplaner. Det kan f.eks. være tre måneder fra ansættelsesdatoen, den første i hver måned eller seks måneder.   

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Venteperioder** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Karenskode** | Et entydigt id for venteperioden. |
   | **Beskrivelse** | En beskrivelse af venteperioden. |
   | **Karensmetode** | Vælg den relevante ventemetode på rullelisten med værdier. Indstillingerne er **Netto**, **Aktuel måned**, **Aktuelt kvartal**, **Aktuelt år** og **Aktuel uge**. |
   | **Måneder** | Angiv det antal måneder, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | **Dage** | Angiv det antal dage, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | **Karensdag** | Vælg den ventedato, der skal bruges til at beregne ventedatoen. |

4. Vælg **Gem**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
