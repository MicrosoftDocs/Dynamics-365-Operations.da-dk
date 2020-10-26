---
title: Tildele en status for produktlivscyklus til en frigivet produktmaster
description: Denne fremgangsmåde viser, hvordan du tildeler en status for produktlivscyklus til en frigivet produktmaster og dens varianter.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981128"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="0c032-103">Tildele en status for produktlivscyklus til en frigivet produktmaster</span><span class="sxs-lookup"><span data-stu-id="0c032-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c032-104">Denne fremgangsmåde viser, hvordan du tildeler en status for produktlivscyklus til en frigivet produktmaster og dens varianter.</span><span class="sxs-lookup"><span data-stu-id="0c032-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="0c032-105">Forudsætning: Du skal afspille opgaveguiden "Opret en ny status for produktlivscyklus" først for at sikre, at du har oprettet mindst én status for produktlivscyklus, før du kan afspille denne opgaveguide.</span><span class="sxs-lookup"><span data-stu-id="0c032-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="0c032-106">Find en frigiven produktmaster.</span><span class="sxs-lookup"><span data-stu-id="0c032-106">Find a released product master</span></span>
1. <span data-ttu-id="0c032-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="0c032-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0c032-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0c032-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="0c032-109">En produktmaster har produktundertypen Produktmaster.</span><span class="sxs-lookup"><span data-stu-id="0c032-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="0c032-110">Opdatere livscyklussen</span><span class="sxs-lookup"><span data-stu-id="0c032-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="0c032-111">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0c032-111">Click Edit.</span></span>
2. <span data-ttu-id="0c032-112">Indtast eller vælg en værdi i feltet Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="0c032-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="0c032-113">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0c032-113">Click Save.</span></span>
4. <span data-ttu-id="0c032-114">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="0c032-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="0c032-115">Hvis Ja er markeret, opdateres alle de relaterede frigivne produktvarianter, der har samme oprindelige status som den frigivne produktmaster, også til den nye status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="0c032-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="0c032-116">Hvis Nej er markeret, bevarer alle varianter deres aktuelle tilstand.</span><span class="sxs-lookup"><span data-stu-id="0c032-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="0c032-117">Varianter, der har en anden status for produktlivscyklus end den frigivet produktmaster, opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="0c032-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="0c032-118">Kontroller livscyklussen for varianterne</span><span class="sxs-lookup"><span data-stu-id="0c032-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="0c032-119">Klik på Frigivne produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="0c032-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="0c032-120">Bemærk, at alle varianter har arvet den valgte status for produktlivscyklus fra den frigivne produktmaster.</span><span class="sxs-lookup"><span data-stu-id="0c032-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="0c032-121">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0c032-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0c032-122">Indtast eller vælg en værdi i feltet Status for produktlivscyklus.</span><span class="sxs-lookup"><span data-stu-id="0c032-122">In the Product lifecycle state field, enter or select a value.</span></span>

