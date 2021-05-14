---
title: Bilag er ikke genereret
description: Dette emne indeholder fejlfindingsoplysninger, som kan hjælpe, når der skulle genereres et bilag, men det ikke sker.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947616"
---
# <a name="voucher-isnt-generated"></a>Bilag er ikke genereret

[!include [banner](../includes/banner.md)]

Hvis der skal genereres et bilag, men siden **Bilagsposteringer** ikke viser nogen bilag, skal du følge trinnene i følgende afsnit efter behov for at løse dette problem.

[![Siden Bilagsposteringer, der ikke indeholder bilag](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Kontrollere anvendelse af moms

1. Gå til **Moms** \> **Periodiske opgaver** \> **Reskontrokladdeposteringer, der endnu ikke er overført**.
2. Hvis der er en kladdepost, skal du markere den og derefter vælge **Overfør nu**.

    [![Knappen Overfør nu på siden Reskontrokladdeposteringer er endnu ikke overført](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Åbn siden **Bilagsposteringer** igen for at se, om bilaget er genereret.

## <a name="determine-whether-customization-exists"></a>Afgøre, om der findes tilpasninger

Hvis du har udført trinnene i forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger. Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
