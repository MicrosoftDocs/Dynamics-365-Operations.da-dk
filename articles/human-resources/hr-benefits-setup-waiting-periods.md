---
title: Konfigurere venteperioder
description: I Microsoft Dynamics 365 Human Resources opretter ventedage en milepæl, der bruges til frynsegodeplaner.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 07ceed65a0346912d4be012a5cec502b0f0a6149
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111852"
---
# <a name="configure-waiting-periods"></a>Konfigurere venteperioder

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
