---
title: Konfigurere venteperioder
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec64343e0db8877e108d5fc665443ff017477ccf
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008542"
---
# <a name="configure-waiting-periods"></a>Konfigurere venteperioder

[!include [banner](includes/preview-feature.md)]

I Microsoft Dynamics 365 Human Resources opretter ventedage en milepæl, der bruges til frynsegodeplaner. Det kan f.eks. være tre måneder fra ansættelsesdatoen, den første i hver måned eller seks måneder.   

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Venteperioder** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | Karenskode | Et entydigt id for venteperioden. |
   | Beskrivelse | En beskrivelse af venteperioden. |
   | Karensmetode | Vælg den relevante ventemetode på rullelisten med værdier. Indstillingerne er Netto, Aktuel måned, Indeværende kvartal, Indeværende år og Aktuel uge. |
   | Måneder | Angiv det antal måneder, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | Days | Angiv det antal dage, der skal føjes til ventemetoden for at beregne ventedatoen. |
   | Karensdag | Vælg den ventedato, der skal bruges til at beregne ventedatoen. |

4. Vælg **Gem**.
