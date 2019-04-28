---
title: Registrer varer til en grundlæggende lagerstedsaktiveret vare ved hjælp af en varemodtagelseskladde
description: Denne fremgangsmåde viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger "grundlæggende lagerstedsfunktioner" i Lagerstyringsmodulet.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3e8ffa6cee7742de1cd98c9c83d134b6d5e4a89
ms.sourcegitcommit: 529763612e8af315d588e85ba807a5c849df57bf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/25/2019
ms.locfileid: "894672"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="fc776-103">Registrer varer til en grundlæggende lagerstedsaktiveret vare ved hjælp af en varemodtagelseskladde</span><span class="sxs-lookup"><span data-stu-id="fc776-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc776-104">Denne fremgangsmåde viser, hvordan du registrerer varer ved hjælp af varemodtagelseskladden, når du bruger "grundlæggende lagerstedsfunktioner" i Lagerstyringsmodulet.</span><span class="sxs-lookup"><span data-stu-id="fc776-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="fc776-105">Dette vil normalt blive udført af en modtagende medarbejder.</span><span class="sxs-lookup"><span data-stu-id="fc776-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="fc776-106">Du kan køre denne procedure i USMF-demodatafirmaet ved hjælp af eksempelværdierne, der vises.</span><span class="sxs-lookup"><span data-stu-id="fc776-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="fc776-107">Hvis du ikke bruger USMF, skal du have en bekræftet indkøbsordre med en åben indkøbsordrelinje, før du starter denne guide.</span><span class="sxs-lookup"><span data-stu-id="fc776-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="fc776-108">Varen på linjen skal være på lager.</span><span class="sxs-lookup"><span data-stu-id="fc776-108">The item on the line must be stocked.</span></span> <span data-ttu-id="fc776-109">Og varen skal tilknyttes en lagringsdimensionsgruppe, hvor sted og lagersted er aktive.</span><span class="sxs-lookup"><span data-stu-id="fc776-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="fc776-110">Opret en overskrift til varemodtagelseskladden</span><span class="sxs-lookup"><span data-stu-id="fc776-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="fc776-111">Gå til Lagerstyring > Kladdeposteringer > Varemodtagelse > Varemodtagelse.</span><span class="sxs-lookup"><span data-stu-id="fc776-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="fc776-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="fc776-112">Click New.</span></span>
3. <span data-ttu-id="fc776-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="fc776-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fc776-114">Hvis du bruger USMF, kan du skrive WHS.</span><span class="sxs-lookup"><span data-stu-id="fc776-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="fc776-115">Hvis du bruger andre data, skal kladden, hvis navn du vælger, have følgende egenskaber: Undersøg plukplads skal angives til Nej, og Karantænestyring skal angives til Nej.</span><span class="sxs-lookup"><span data-stu-id="fc776-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="fc776-116">Skriv en værdi i feltet Følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="fc776-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="fc776-117">Dette er følgeseddel-id'et fra følgesedlen, der er udstedt af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="fc776-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="fc776-118">Tilføj et entydigt tal.</span><span class="sxs-lookup"><span data-stu-id="fc776-118">Add a unique number.</span></span>  
5. <span data-ttu-id="fc776-119">Vælg indkøbsordren i feltet Tal.</span><span class="sxs-lookup"><span data-stu-id="fc776-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="fc776-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fc776-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="fc776-121">Føj linjer til varemodtagelseskladden</span><span class="sxs-lookup"><span data-stu-id="fc776-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="fc776-122">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="fc776-122">Click Functions.</span></span>
2. <span data-ttu-id="fc776-123">Klik på Opret linjer.</span><span class="sxs-lookup"><span data-stu-id="fc776-123">Click Create lines.</span></span>
    * <span data-ttu-id="fc776-124">Linjerne kan indtastes manuelt i denne kladde eller oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="fc776-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="fc776-125">Dette viser, hvordan du oprette dette automatisk.</span><span class="sxs-lookup"><span data-stu-id="fc776-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="fc776-126">Markér eller fjern markeringen af afkrydsningsfeltet Initialiser antal.</span><span class="sxs-lookup"><span data-stu-id="fc776-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="fc776-127">Dette initialiserer mængden på kladdelinjerne med den mængde, der ikke er registreret fra indkøbsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="fc776-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="fc776-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fc776-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="fc776-129">Bogfør kladden</span><span class="sxs-lookup"><span data-stu-id="fc776-129">Post the journal</span></span>
1. <span data-ttu-id="fc776-130">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="fc776-130">Click Post.</span></span>
2. <span data-ttu-id="fc776-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fc776-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="fc776-132">Generer produktkvitteringen</span><span class="sxs-lookup"><span data-stu-id="fc776-132">Generate the product receipt</span></span>
1. <span data-ttu-id="fc776-133">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="fc776-133">Click Functions.</span></span>
2. <span data-ttu-id="fc776-134">Klik på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="fc776-134">Click Product receipt.</span></span>
3. <span data-ttu-id="fc776-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fc776-135">Click OK.</span></span>

