---
title: Inspicere varers kvalitet
description: Dette emne forklarer, hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145611"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="a77c0-103">Inspicere varers kvalitet</span><span class="sxs-lookup"><span data-stu-id="a77c0-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a77c0-104">Dette emne forklarer, hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="a77c0-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="a77c0-105">Du kan køre denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="a77c0-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="a77c0-106">Inden du begynder denne eksempelprocedure, skal du bekræfte indkøbsordren "000016" og bogføre en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="a77c0-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="a77c0-107">Dette vil automatisk oprette en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="a77c0-107">This will automatically create a quality order.</span></span> <span data-ttu-id="a77c0-108">Kvalitetskontroller foretages normalt af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="a77c0-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a77c0-109">Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="a77c0-109">Select a quality order</span></span>
1. <span data-ttu-id="a77c0-110">I navigationsruden skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.**</span><span class="sxs-lookup"><span data-stu-id="a77c0-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="a77c0-111">Vælg den kvalitetsordre, der blev oprettet, før du startede denne procedure.</span><span class="sxs-lookup"><span data-stu-id="a77c0-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="a77c0-112">Registrere testresultater</span><span class="sxs-lookup"><span data-stu-id="a77c0-112">Record test results</span></span>
1. <span data-ttu-id="a77c0-113">Vælg **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-113">Select **Results**.</span></span>
2. <span data-ttu-id="a77c0-114">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-114">Select **Edit**.</span></span>
3. <span data-ttu-id="a77c0-115">I feltet **Antal resultater** skal du skrive et tal.</span><span class="sxs-lookup"><span data-stu-id="a77c0-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="a77c0-116">I feltet **Udfald** skal du vælge den ønskede post i rullemenuen.</span><span class="sxs-lookup"><span data-stu-id="a77c0-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="a77c0-117">I dette eksempel er resultatet baseret på et foruddefineret udfald.</span><span class="sxs-lookup"><span data-stu-id="a77c0-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="a77c0-118">Normalt ville du registrere et mere specifikt testresultat, for eksempel en størrelse eller anden dimension.</span><span class="sxs-lookup"><span data-stu-id="a77c0-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="a77c0-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-119">Select **Save**.</span></span>
6. <span data-ttu-id="a77c0-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a77c0-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="a77c0-121">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="a77c0-121">Validate the quality order</span></span>
1. <span data-ttu-id="a77c0-122">Vælg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-122">Select **Validate**.</span></span>
2. <span data-ttu-id="a77c0-123">I feltet **Valideret af** skal du i rullemenuen vælge den bruger, som udfører inspektionen.</span><span class="sxs-lookup"><span data-stu-id="a77c0-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="a77c0-124">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-124">Click **Select**.</span></span>
4. <span data-ttu-id="a77c0-125">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a77c0-125">Select **OK**.</span></span>
5. <span data-ttu-id="a77c0-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a77c0-126">Close the page.</span></span>

