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
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956128"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="860d8-103">Inspicere varers kvalitet</span><span class="sxs-lookup"><span data-stu-id="860d8-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="860d8-104">Dette emne beskriver, hvordan du behandler kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="860d8-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="860d8-105">Kvalitetskontroller er udføres typisk af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="860d8-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="860d8-106">Hvis standarddemodataene er installeret, kan du bruge dem til at gennemføre procedurerne i dette emne.</span><span class="sxs-lookup"><span data-stu-id="860d8-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="860d8-107">Hvis du vil bruge demodataene, skal du vælge den juridiske enhed *USMF*, før du starter.</span><span class="sxs-lookup"><span data-stu-id="860d8-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="860d8-108">Du skal derefter bekræfte indkøbsordre *000016* og bogføre en produktmodtagelse.</span><span class="sxs-lookup"><span data-stu-id="860d8-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="860d8-109">En kvalitetsordre genereres automatisk.</span><span class="sxs-lookup"><span data-stu-id="860d8-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="860d8-110">Trin 1: Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="860d8-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="860d8-111">Benyt denne fremgangsmåde for at vælge en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="860d8-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="860d8-112">Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.</span><span class="sxs-lookup"><span data-stu-id="860d8-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="860d8-113">Vælg den kvalitetsordre, der blev genereret, før du startede denne procedure.</span><span class="sxs-lookup"><span data-stu-id="860d8-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="860d8-114">Trin 2: Registrere testresultater</span><span class="sxs-lookup"><span data-stu-id="860d8-114">Step 2: Record test results</span></span>

<span data-ttu-id="860d8-115">Benyt følgende fremgangsmåde for at registrere testresultater.</span><span class="sxs-lookup"><span data-stu-id="860d8-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="860d8-116">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="860d8-116">Select **Results**.</span></span>
1. <span data-ttu-id="860d8-117">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="860d8-117">Select **Edit**.</span></span>
1. <span data-ttu-id="860d8-118">I feltet **Antal resultater** skal du skrive et tal.</span><span class="sxs-lookup"><span data-stu-id="860d8-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="860d8-119">I feltet **Udfald** skal du vælge det ønskede post.</span><span class="sxs-lookup"><span data-stu-id="860d8-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="860d8-120">I dette eksempel er resultatet baseret på et foruddefineret udfald.</span><span class="sxs-lookup"><span data-stu-id="860d8-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="860d8-121">Normalt vil du registrere et mere specifikt testresultat som f.eks. en størrelse eller anden dimension.</span><span class="sxs-lookup"><span data-stu-id="860d8-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="860d8-122">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="860d8-122">Select **Save**.</span></span>
1. <span data-ttu-id="860d8-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="860d8-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="860d8-124">Trin 3: Validere kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="860d8-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="860d8-125">Benyt denne fremgangsmåde for at validere kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="860d8-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="860d8-126">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="860d8-126">Select **Validate**.</span></span>
1. <span data-ttu-id="860d8-127">Vælg den bruger, der skal udføre inspektionen, i feltet **Valideret af**.</span><span class="sxs-lookup"><span data-stu-id="860d8-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="860d8-128">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="860d8-128">Select **Select**.</span></span>
1. <span data-ttu-id="860d8-129">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="860d8-129">Select **OK**.</span></span>
1. <span data-ttu-id="860d8-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="860d8-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
