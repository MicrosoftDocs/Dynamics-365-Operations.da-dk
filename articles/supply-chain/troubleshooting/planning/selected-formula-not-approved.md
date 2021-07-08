---
title: Det markerede formelnummer er ikke godkendt til en batchordre
description: Når du forsøger at autorisere et ordreforslag, modtager du en fejlmeddelelse om, at det valgte formelnummer ikke er godkendt til en batchordre.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294034"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="30553-103">Det markerede formelnummer er ikke godkendt til en batchordre</span><span class="sxs-lookup"><span data-stu-id="30553-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="30553-104">Fejlkode: PRO2614</span><span class="sxs-lookup"><span data-stu-id="30553-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="30553-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="30553-105">Symptoms</span></span>

<span data-ttu-id="30553-106">Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="30553-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="30553-107">Det valgte formelnummer er ikke godkendt for en batchordre.</span><span class="sxs-lookup"><span data-stu-id="30553-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="30553-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="30553-108">Cause</span></span>

<span data-ttu-id="30553-109">Systemet validerer den autoriserede handling for at sikre, at der findes en godkendt formel til den aktive vare.</span><span class="sxs-lookup"><span data-stu-id="30553-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="30553-110">Du skal sandsynligvis godkende formlen.</span><span class="sxs-lookup"><span data-stu-id="30553-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="30553-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="30553-111">Resolution</span></span>

<span data-ttu-id="30553-112">Benyt følgende fremgangsmåde for at godkende en formel.</span><span class="sxs-lookup"><span data-stu-id="30553-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="30553-113">Gå til **Administration af produktoplysninger \> Styklister og formler \> Formler**.</span><span class="sxs-lookup"><span data-stu-id="30553-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="30553-114">Vælg den relevante formel.</span><span class="sxs-lookup"><span data-stu-id="30553-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="30553-115">Vælg **Godkend formel** i gruppen **Vedligehold** under fanen **Formel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="30553-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="30553-116">Vælg en godkender i dialogboksen **Godkend stykliste eller formel**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="30553-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
