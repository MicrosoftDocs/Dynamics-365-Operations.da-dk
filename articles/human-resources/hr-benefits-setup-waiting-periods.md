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
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6dd231ef43cfac3188af23289190c6e9e4fad453
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323862"
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
