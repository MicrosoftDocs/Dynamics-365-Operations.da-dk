---
title: Konfigurere venteperioder
description: I Microsoft Dynamics 365 Human Resources opretter ventedage en milepæl, der bruges til frynsegodeplaner.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3621580e0db3ca5b041ddac0ec882a1e42e429b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791407"
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
   | **Karensmetode** | Vælg den relevante ventemetode på rullelisten med værdier. Indstillingerne er Netto, Aktuel måned, Indeværende kvartal, Indeværende år og Aktuel uge. |
   | **Måneder** | Angiv det antal måneder, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | **Dage** | Angiv det antal dage, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | **Karensdag** | Vælg den ventedato, der skal bruges til at beregne ventedatoen. |

4. Vælg **Gem**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]