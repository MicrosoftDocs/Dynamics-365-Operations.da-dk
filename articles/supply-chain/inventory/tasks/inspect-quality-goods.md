---
title: Inspicere varers kvalitet
description: Dette emne forklarer, hvordan du behandler en kvalitetsordre.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244417"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="7b7ec-103">Inspicere varers kvalitet</span><span class="sxs-lookup"><span data-stu-id="7b7ec-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b7ec-104">Dette emne forklarer, hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="7b7ec-105">Du kan køre denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="7b7ec-106">Inden du begynder denne eksempelprocedure, skal du bekræfte indkøbsordren "000016" og bogføre en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="7b7ec-107">Dette vil automatisk oprette en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-107">This will automatically create a quality order.</span></span> <span data-ttu-id="7b7ec-108">Kvalitetskontroller foretages normalt af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="7b7ec-109">Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="7b7ec-109">Select a quality order</span></span>
1. <span data-ttu-id="7b7ec-110">I navigationsruden skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.**</span><span class="sxs-lookup"><span data-stu-id="7b7ec-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="7b7ec-111">Vælg den kvalitetsordre, der blev oprettet, før du startede denne procedure.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="7b7ec-112">Registrere testresultater</span><span class="sxs-lookup"><span data-stu-id="7b7ec-112">Record test results</span></span>
1. <span data-ttu-id="7b7ec-113">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-113">Select **Results**.</span></span>
2. <span data-ttu-id="7b7ec-114">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-114">Select **Edit**.</span></span>
3. <span data-ttu-id="7b7ec-115">I feltet **Antal resultater** skal du skrive et tal.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="7b7ec-116">I feltet **Udfald** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="7b7ec-117">I dette eksempel er resultatet baseret på et foruddefineret udfald.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="7b7ec-118">Normalt ville du registrere et mere specifikt testresultat, for eksempel en størrelse eller anden dimension.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="7b7ec-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-119">Select **Save**.</span></span>
6. <span data-ttu-id="7b7ec-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="7b7ec-121">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="7b7ec-121">Validate the quality order</span></span>
1. <span data-ttu-id="7b7ec-122">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-122">Select **Validate**.</span></span>
2. <span data-ttu-id="7b7ec-123">I feltet **Valideret af** skal du i rullemenuen vælge den bruger, som udfører inspektionen.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="7b7ec-124">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-124">Click **Select**.</span></span>
4. <span data-ttu-id="7b7ec-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-125">Select **OK**.</span></span>
5. <span data-ttu-id="7b7ec-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7b7ec-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]