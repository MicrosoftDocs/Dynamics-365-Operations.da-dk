---
title: Batchattributter
description: Dette emne indeholder oplysninger om batchattributter. Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches. I dette emne forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424978"
---
# <a name="batch-attributes"></a><span data-ttu-id="6ca33-105">Batchattributter</span><span class="sxs-lookup"><span data-stu-id="6ca33-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ca33-106">Dette emne indeholder oplysninger om batchattributter.</span><span class="sxs-lookup"><span data-stu-id="6ca33-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="6ca33-107">Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches.</span><span class="sxs-lookup"><span data-stu-id="6ca33-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="6ca33-108">I dette emne forklares også, hvordan du tildeler batchattributter, og hvordan du kan søge efter dem, når du reserverer batchnumre.</span><span class="sxs-lookup"><span data-stu-id="6ca33-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="6ca33-109">Batchattributter er karakteristika for de råvarer og færdigvarer, der udgør lagerbatches.</span><span class="sxs-lookup"><span data-stu-id="6ca33-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="6ca33-110">Batchattributter kan være forskellige, afhængigt af faktorer, som f.eks. miljømæssige forhold eller kvaliteten af de råvarer, der bruges til batchfremstillingen, eller udfaldet at færdigvarer.</span><span class="sxs-lookup"><span data-stu-id="6ca33-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="6ca33-111">Antallet og typerne af batchattributter, der bruges, kan variere meget fra branche til branche.</span><span class="sxs-lookup"><span data-stu-id="6ca33-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="6ca33-112">Her er to eksempler på, hvordan du kan bruge batchattributter:</span><span class="sxs-lookup"><span data-stu-id="6ca33-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="6ca33-113">Inden for osteindustrien, hvor mælk, der er en af de råvarer, der bruges til fremstillingen af ost, kan have attributter som f.eks. fedtindhold og vægtet procent.</span><span class="sxs-lookup"><span data-stu-id="6ca33-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="6ca33-114">Den ost, der fremstilles af mælken, kan have andre attributter, som fugtighed og alder.</span><span class="sxs-lookup"><span data-stu-id="6ca33-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="6ca33-115">Inden for stålindustrien kan det jern, der fremstilles, have attributter som f.eks. procentvis indhold af magnesium, indhold af sølv og indhold af zink.</span><span class="sxs-lookup"><span data-stu-id="6ca33-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="6ca33-116">For bedre at administrere antallet og typerne af attributter kan du bruge batchattributgrupper.</span><span class="sxs-lookup"><span data-stu-id="6ca33-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="6ca33-117">På denne måde kan du ikke tilføje attributterne enkeltvist.</span><span class="sxs-lookup"><span data-stu-id="6ca33-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="6ca33-118">Tilknyt batchattributter</span><span class="sxs-lookup"><span data-stu-id="6ca33-118">Assign batch attributes</span></span>
<span data-ttu-id="6ca33-119">Du kan knytte batchattributter til de enkelte produkter, der opbevares i lagerbatches, eller du kan tildele dem til produkter, der er knyttet til bestemte debitorer.</span><span class="sxs-lookup"><span data-stu-id="6ca33-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="6ca33-120">Før du kan tildele en batchattribut på debitorniveau, skal du først tildele den på produktniveau.</span><span class="sxs-lookup"><span data-stu-id="6ca33-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="6ca33-121">Batchdimensionen for produktet skal være angivet til **Aktiv** i sporingsdimensionsgruppen.</span><span class="sxs-lookup"><span data-stu-id="6ca33-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="6ca33-122">Hvis du vil tildele en batchattribut til et enkelt produkt, skal du bruge den produktspecifikke side.</span><span class="sxs-lookup"><span data-stu-id="6ca33-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="6ca33-123">Hvis attributten er specifik for et produkt til en debitor, skal du bruge den debitorspecifikke side.</span><span class="sxs-lookup"><span data-stu-id="6ca33-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="6ca33-124">Når du føjer en attribut til et produkt, skal du også definere andre parametre.</span><span class="sxs-lookup"><span data-stu-id="6ca33-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="6ca33-125">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="6ca33-125">Here are some examples:</span></span>

-   <span data-ttu-id="6ca33-126">Minimum- og maksimumintervallerne for attributten **Heltal** eller **Del**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="6ca33-127">Tolerancehandlingerne for en attribut af typen **Heltal** eller **Del**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="6ca33-128">Hvis attributten falder uden for minimum- og maksimumintervallet, kan handlingen være enten en advarsel eller en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="6ca33-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="6ca33-129">Destinationsværdien for attributten.</span><span class="sxs-lookup"><span data-stu-id="6ca33-129">The target value for the attribute.</span></span> <span data-ttu-id="6ca33-130">Denne værdi er den valgfri værdi for attributten, og den gælder for alle attributtyper.</span><span class="sxs-lookup"><span data-stu-id="6ca33-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="6ca33-131">Du kan åbne siderne for produkter, du vælger på siden **Frigivne produkter** i Administration af produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="6ca33-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="6ca33-132">Når du har føjet batchattributter til et produkt, kan du føje specifikke værdier til attributterne på siden **Lagerbatchattributter**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="6ca33-133">Reservere batches</span><span class="sxs-lookup"><span data-stu-id="6ca33-133">Reserve batches</span></span>
<span data-ttu-id="6ca33-134">Du kan søge efter batchattributter, når du foretager batchreservationer for en salgsordre for at opfylde en kundeordre, eller når du plukker og reserverer batches til en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="6ca33-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="6ca33-135">Du kan bruge søgningen til at finde en lagerbatch, der indeholder produktet med den ønskede batchattribut.</span><span class="sxs-lookup"><span data-stu-id="6ca33-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="6ca33-136">Når du har fundet den eller de ønskede batches, kan du reservere produktet til den oprindelige lagertransaktionslinje.</span><span class="sxs-lookup"><span data-stu-id="6ca33-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



