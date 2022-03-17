---
title: Anvende en betalingsplan på fakturakladden
description: Dette emne beskriver, hvordan du føjer en betaling til kreditorfakturakladden.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f6481c3fc033acf4bb563bf1716789216646b60b
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358333"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Anvende en betalingsplan på fakturakladden

[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Finance release 10.0.25 understøttes en betalingsplan nu i **kreditorfakturakladden**.

Hvis du vil bruge denne funktion, skal du aktivere funktionen **Anvend betalingsplan til fakturakladde** i Funktionsstyring.

Når funktionen er aktiveret, føjes der et nyt felt til **Betalingsplan** til siden **Fakturakladde**. Når du opretter en fakturakladdelinje, og hvis betalingsbetingelserne vedligeholdes for kreditoren, og betalingsbetingelserne er valgt i betalingsplanen, opdateres feltet **Betalingsplan** på siden **Fakturakladde**.

Du kan ændre den betalingsplan, der bruges, i overensstemmelse med dit forretningsbehov. Under bogføring af kreditorfakturakladden oprettes åbne kreditorposteringer i overensstemmelse med betalingsplanen.

 - Hvis du vil have vist flere åbne kreditorposteringer, der er oprettet fra betalingsplanen, skal du gå til **Kreditor \> Fakturaer \> Åbne kreditorfakturaer** og angive fakturanummeret eller kreditorkontoen.
 - Du kan gennemse eller konfigurere betalingsplanen ved at gå til **Kreditor \> Opsætning af betaling \> Betalingsplan**.
 - Hvis du vil konfigurere betalingsbetingelserne og tildele en betalingsplan, skal du gå til **Kreditor \> Opsætning af betaling \> Betalingsbetingelser**.
 - Hvis du vil vedligeholde betalingsbetingelserne for en kreditor, skal du gå til **Kreditor \> Alle kreditorer**, vælge kreditorkontoen og derefter angive feltet **Betalingsbetingelser** under fanen **Betaling**.

Funktionen til betalingsplan er også tilgængelig i processen **Kreditorfakturaregistrering**. Hvis der er valgt en betalingsplan i fakturaregisterkladden, genereres der **ikke** flere kreditorbetalingslinjer, når fakturaregisteret bogføres. Kreditorbetalingslinjerne genereres, når fakturaen godkendes.

## <a name="limitation"></a>Begrænsning

Hvis betalingsplanen for en ventende kreditorfaktura findes i fakturahovedet, er der en avanceret side, hvor brugerne kan redigere betalingslinjerne. (Brugere kan f.eks. redigere forfaldsdatoen og værdien for hver betalingslinje). Betalingslinjer, der oprettes ud fra fakturakladden, har værdien fra betalingsplanen.

Denne funktion er tilgængelig for **kreditorfakturakladden** og **ventende fakturaer** i en fremtidig version.
