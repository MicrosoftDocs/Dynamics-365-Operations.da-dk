---
title: Konfigurere betalingsplaner med skatteallokering
description: Dette emne forklarer, hvordan du konfigurerer betalingsplaner med fordeling af kildeskat (TDS – Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023126"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="9e830-103">Konfigurere betalingsplaner med skatteallokering</span><span class="sxs-lookup"><span data-stu-id="9e830-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e830-104">Dette emne forklarer, hvordan du konfigurerer betalingsplaner med fordeling af kildeskat (TDS – Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="9e830-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="9e830-105">Gå til **Kreditor \> Betalingsopsætning \> Betalingsplaner**.</span><span class="sxs-lookup"><span data-stu-id="9e830-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="9e830-106">[![Siden Betalingsplaner](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="9e830-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="9e830-107">Vælg **Ny** i handlingsruden for at oprette en betalingsplan, og angiv de krævede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="9e830-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="9e830-108">Vælg den metode, der skal bruges til at fordele betalingen for betalingsplanen, i feltet **Fordeling**:</span><span class="sxs-lookup"><span data-stu-id="9e830-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="9e830-109">Sum</span><span class="sxs-lookup"><span data-stu-id="9e830-109">Total</span></span>
    - <span data-ttu-id="9e830-110">Fast beløb</span><span class="sxs-lookup"><span data-stu-id="9e830-110">Fixed amount</span></span>
    - <span data-ttu-id="9e830-111">Fast antal</span><span class="sxs-lookup"><span data-stu-id="9e830-111">Fixed quantity</span></span>
    - <span data-ttu-id="9e830-112">Specificeret</span><span class="sxs-lookup"><span data-stu-id="9e830-112">Specified</span></span>

    <span data-ttu-id="9e830-113">Feltet **Fordeling af A-skat** viser skattefordelingsmetoden for betalingsplanen.</span><span class="sxs-lookup"><span data-stu-id="9e830-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="9e830-114">Hvis du vælger **Total** i feltet **Fordeling**, angives feltet **Fordeling af A-skat** automatisk til **Total**.</span><span class="sxs-lookup"><span data-stu-id="9e830-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="9e830-115">Hvis du vælger **Fast beløb**, **Fast antal** eller **Angivet** i feltet **Fordeling**, angives feltet **Fordeling af A-skat** automatisk til **Proportionalt**.</span><span class="sxs-lookup"><span data-stu-id="9e830-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e830-116">Hvis feltet **Fordeling af A-skat** er angivet til **Total**, beregnes betalingsraterne baseret på det bruttobeløb, som omfatter skattebeløbet.</span><span class="sxs-lookup"><span data-stu-id="9e830-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="9e830-117">Hvis feltet **Fordeling af A-skat** er angivet til **Proportionalt**, beregnes betalingsraterne baseret på nettofakturabeløbet, efter skattebeløbet er fratrukket.</span><span class="sxs-lookup"><span data-stu-id="9e830-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="9e830-118">Angiv de øvrige krævede oplysninger, og luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="9e830-118">Enter the other required details, and then close the page.</span></span>
