---
title: Inspicere varers kvalitet
description: Denne procedure viser, hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: aeed7eab750c606ea0009fa7c51baf96e2f9de51
ms.contentlocale: da-dk
ms.lasthandoff: 09/12/2017

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="b6f5e-103">Inspicere varers kvalitet</span><span class="sxs-lookup"><span data-stu-id="b6f5e-103">Inspect the quality of goods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6f5e-104">Denne procedure viser, hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="b6f5e-105">Du kan køre denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="b6f5e-106">Inden du begynder denne eksempelprocedure, skal du bekræfte indkøbsordren "000016" og bogføre en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="b6f5e-107">Dette vil automatisk oprette en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-107">This will automatically create a quality order.</span></span> <span data-ttu-id="b6f5e-108">Kvalitetskontroller foretages normalt af en kvalitetsmedarbejder.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="b6f5e-109">Vælg en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="b6f5e-109">Select a quality order</span></span>
1. <span data-ttu-id="b6f5e-110">Gå til Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="b6f5e-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6f5e-112">Vælg den kvalitetsordre, der blev oprettet, før du startede denne procedure.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="b6f5e-113">Registrere testresultater</span><span class="sxs-lookup"><span data-stu-id="b6f5e-113">Record test results</span></span>
1. <span data-ttu-id="b6f5e-114">Klik på Resultater.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-114">Click Results.</span></span>
2. <span data-ttu-id="b6f5e-115">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-115">Click Edit.</span></span>
3. <span data-ttu-id="b6f5e-116">Skriv et tal i feltet Antalsresultat.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="b6f5e-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b6f5e-118">Klik på rullelisten i feltet Udfald for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b6f5e-119">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b6f5e-120">I dette eksempel er resultatet baseret på et foruddefineret udfald.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="b6f5e-121">Normalt ville du registrere et mere specifikt testresultat, for eksempel en størrelse eller anden dimension.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="b6f5e-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b6f5e-123">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-123">Click Save.</span></span>
9. <span data-ttu-id="b6f5e-124">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="b6f5e-125">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="b6f5e-125">Validate the quality order</span></span>
1. <span data-ttu-id="b6f5e-126">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-126">Click Validate.</span></span>
2. <span data-ttu-id="b6f5e-127">Klik på rullelisten i feltet Valideret af for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b6f5e-128">Vælg den bruger, der udfører kvalitetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="b6f5e-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b6f5e-130">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-130">Click Select.</span></span>
5. <span data-ttu-id="b6f5e-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-131">Click OK.</span></span>
6. <span data-ttu-id="b6f5e-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b6f5e-132">Close the page.</span></span>

