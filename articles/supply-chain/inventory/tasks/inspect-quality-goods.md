---
title: Inspicere varers kvalitet
description: Dette emne beskriver, hvordan du behandler kvalitetsordrer.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb5547b6c1d4c44e53faba0d6e2c1f0368fb95768a2520ecc39066ff73a03d2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755352"
---
# <a name="inspect-the-quality-of-goods"></a>Inspicere varers kvalitet

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du behandler kvalitetsordrer. Kvalitetskontroller er udføres typisk af en kvalitetsmedarbejder.

Hvis standarddemodataene er installeret, kan du bruge dem til at gennemføre procedurerne i dette emne. Hvis du vil bruge demodataene, skal du vælge den juridiske enhed *USMF*, før du starter. Du skal derefter bekræfte indkøbsordre *000016* og bogføre en produktmodtagelse. En kvalitetsordre genereres automatisk.

## <a name="step-1-select-a-quality-order"></a>Trin 1: Vælg en kvalitetsordre

Benyt denne fremgangsmåde for at vælge en kvalitetsordre.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg den kvalitetsordre, der blev genereret, før du startede denne procedure.

## <a name="step-2-record-test-results"></a>Trin 2: Registrere testresultater

Benyt følgende fremgangsmåde for at registrere testresultater.

1. Vælg **Resultater**.
1. Vælg **Rediger**.
1. I feltet **Antal resultater** skal du skrive et tal.
1. I feltet **Udfald** skal du vælge det ønskede post. I dette eksempel er resultatet baseret på et foruddefineret udfald. Normalt vil du registrere et mere specifikt testresultat som f.eks. en størrelse eller anden dimension.
1. Vælg **Gem**.
1. Luk siden.

## <a name="step-3-validate-the-quality-order"></a>Trin 3: Validere kvalitetsordren

Benyt denne fremgangsmåde for at validere kvalitetsordren.

1. Vælg **Valider**.
1. Vælg den bruger, der skal udføre inspektionen, i feltet **Valideret af**.
1. Vælg **Vælg**.
1. Vælg **OK**.
1. Luk siden.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
