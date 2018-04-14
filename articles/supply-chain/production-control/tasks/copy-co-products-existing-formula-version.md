--- 
title: Kopiere samprodukter fra en eksisterende formelversion
description: Denne procedure viser, hvordan du kopierer samprodukter fra en eksisterende formelversion til en anden formelversion for et frigivet produkt.
author: YuyuScheller
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e6ca0de2956e7e2b76f1286b0d01a3a2e3f3d53d
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="db351-103">Kopiere samprodukter fra en eksisterende formelversion</span><span class="sxs-lookup"><span data-stu-id="db351-103">Copy co-products from an existing formula version</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="db351-104">Denne procedure viser, hvordan du kopierer samprodukter fra en eksisterende formelversion til en anden formelversion for et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="db351-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="db351-105">Det er en forudsætning, at der er mindst én formelversion tilknyttet samprodukter.</span><span class="sxs-lookup"><span data-stu-id="db351-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="db351-106">Det demodatafirmaet USP2 bruges til at oprette denne procedure.</span><span class="sxs-lookup"><span data-stu-id="db351-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="db351-107">Finde et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="db351-107">Find a released product</span></span>
1. <span data-ttu-id="db351-108">Gå til Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="db351-108">Go to Released products.</span></span>
2. <span data-ttu-id="db351-109">Klik på Vis filtre.</span><span class="sxs-lookup"><span data-stu-id="db351-109">Click Show filters.</span></span>
    * <span data-ttu-id="db351-110">Du er ved at tilføje feltet Produktionstype i dialogboksen Filtrer.</span><span class="sxs-lookup"><span data-stu-id="db351-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="db351-111">Klik på Tilføj et filterfelt for at føje feltet Produktionstype.</span><span class="sxs-lookup"><span data-stu-id="db351-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="db351-112">I næste trin skal du angive Formel manuelt i feltet Produktionstype, før du vælger Anvend.</span><span class="sxs-lookup"><span data-stu-id="db351-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="db351-113">Dette angiver filteret på listen over frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="db351-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="db351-114">Angiv Formel manuelt i feltet Produktionstype.</span><span class="sxs-lookup"><span data-stu-id="db351-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="db351-115">Klik på Anvend.</span><span class="sxs-lookup"><span data-stu-id="db351-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="db351-116">Vælge et frigivet produkt</span><span class="sxs-lookup"><span data-stu-id="db351-116">Select a released product</span></span>
1. <span data-ttu-id="db351-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="db351-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="db351-118">Klik på Formelversioner.</span><span class="sxs-lookup"><span data-stu-id="db351-118">Click Formula versions.</span></span>
    * <span data-ttu-id="db351-119">Klik på Formelversioner i handlingsruden Teknikere.</span><span class="sxs-lookup"><span data-stu-id="db351-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="db351-120">Kopiere samprodukter</span><span class="sxs-lookup"><span data-stu-id="db351-120">Copy co-products</span></span>
1. <span data-ttu-id="db351-121">Klik på Formelversion i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="db351-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="db351-122">Klik på Ko-produkter.</span><span class="sxs-lookup"><span data-stu-id="db351-122">Click Co-products.</span></span>
3. <span data-ttu-id="db351-123">Klik på Kopiér.</span><span class="sxs-lookup"><span data-stu-id="db351-123">Click Copy.</span></span>
4. <span data-ttu-id="db351-124">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="db351-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="db351-125">Indtast eller vælg en værdi i feltet Formelversion.</span><span class="sxs-lookup"><span data-stu-id="db351-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="db351-126">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="db351-126">Click OK.</span></span>
7. <span data-ttu-id="db351-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="db351-127">Close the page.</span></span>


