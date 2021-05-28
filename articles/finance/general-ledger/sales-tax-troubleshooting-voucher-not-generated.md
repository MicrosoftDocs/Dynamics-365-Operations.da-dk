---
title: Bilag er ikke genereret
description: Dette emne indeholder fejlfindingsoplysninger, som kan hjælpe, når der skulle genereres et bilag, men det ikke sker.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba23b597b1d7d283b99638fb7d5d91da00afb09c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018751"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="6280e-103">Bilag er ikke genereret</span><span class="sxs-lookup"><span data-stu-id="6280e-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6280e-104">Hvis der skal genereres et bilag, men siden **Bilagsposteringer** ikke viser nogen bilag, skal du følge trinnene i følgende afsnit efter behov for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="6280e-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="6280e-105">[![Siden Bilagsposteringer, der ikke indeholder bilag](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6280e-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="6280e-106">Kontrollere anvendelse af moms</span><span class="sxs-lookup"><span data-stu-id="6280e-106">Check the tax applicability</span></span>

1. <span data-ttu-id="6280e-107">Gå til **Moms** \> **Periodiske opgaver** \> **Reskontrokladdeposteringer, der endnu ikke er overført**.</span><span class="sxs-lookup"><span data-stu-id="6280e-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="6280e-108">Hvis der er en kladdepost, skal du markere den og derefter vælge **Overfør nu**.</span><span class="sxs-lookup"><span data-stu-id="6280e-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="6280e-109">[![Knappen Overfør nu på siden Reskontrokladdeposteringer er endnu ikke overført](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6280e-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="6280e-110">Åbn siden **Bilagsposteringer** igen for at se, om bilaget er genereret.</span><span class="sxs-lookup"><span data-stu-id="6280e-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6280e-111">Afgøre, om der findes tilpasninger</span><span class="sxs-lookup"><span data-stu-id="6280e-111">Determine whether customization exists</span></span>

<span data-ttu-id="6280e-112">Hvis du har udført trinnene i forrige afsnit, men ikke har fundet nogen problemer, skal du afgøre, om der er foretaget tilpasninger.</span><span class="sxs-lookup"><span data-stu-id="6280e-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6280e-113">Hvis der ikke er foretaget tilpasninger, skal du oprette en Microsoft-serviceanmodning for at få yderligere support.</span><span class="sxs-lookup"><span data-stu-id="6280e-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
