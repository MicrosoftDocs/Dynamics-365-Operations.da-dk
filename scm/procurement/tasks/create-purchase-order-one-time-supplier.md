--- 
title: "Oprette en indkøbsordre til en engangsleverandør"
description: "Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="9a4ee-103">Oprette en indkøbsordre til en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="9a4ee-103">Create a purchase order for a one-time supplier</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a4ee-104">Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="9a4ee-105">Leverandøren oprettes automatisk sammen med indkøbsordren, så du skal ikke oprette kreditorkontoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="9a4ee-106">Indkøbsordrer oprettes typisk af en indkøbsagent.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="9a4ee-107">Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9a4ee-108">Det er en forudsætning, at der er konfigureret en engangsleverandør på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="9a4ee-109">Oprette en indkøbsordre til en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="9a4ee-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="9a4ee-110">Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9a4ee-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-111">Click New.</span></span>
3. <span data-ttu-id="9a4ee-112">Vælg Ja i feltet Engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="9a4ee-113">Der oprettes automatisk en kreditorkonto, som og tildeles til købsordren.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="9a4ee-114">Kreditorkontoen oprettes ud fra den skabelon, der er angivet under fanen Generelt på siden Kreditorparametre.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="9a4ee-115">Skriv et navn til leverandørne i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="9a4ee-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-116">Click OK.</span></span>
    * <span data-ttu-id="9a4ee-117">Indkøbsordren kan nu udfyldes og behandles som enhver anden ordre.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="9a4ee-118">Der er ingen særlige kendetegn for, hvordan dette gøres.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="9a4ee-119">Fakturaen medregner en transaktion på den kreditorkonto, der blev oprettet til ordren, og betalingen vil derefter blive behandlet.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="9a4ee-120">Når dette er udført, kan kreditorkontoen slettes.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="9a4ee-121">Dette gøres typisk i kreditorafdelingen.</span><span class="sxs-lookup"><span data-stu-id="9a4ee-121">This is typically done by the accounts payable department.</span></span>  


