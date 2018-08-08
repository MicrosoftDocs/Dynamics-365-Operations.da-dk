---
title: "Spore en vare eller råmateriale"
description: "Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: bc68fe6e6b87075c5406b5b6a8e89f4da8bd1166
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="f1106-103">Spore en vare eller råmateriale</span><span class="sxs-lookup"><span data-stu-id="f1106-103">Trace an item or raw material</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1106-104">Denne procedure viser, hvordan du bruger varesporing til at identificere, hvor varer eller råvarer er blevet brugt eller bruges.</span><span class="sxs-lookup"><span data-stu-id="f1106-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="f1106-105">Med denne procedure kan du identificere en vare, spore den tilbage til kilden og derefter spore den fremad gennem produktionen og salget af det færdige produkt.</span><span class="sxs-lookup"><span data-stu-id="f1106-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="f1106-106">Processen kan bruges til at undersøge de kunder og de salgsordrer, der berøres, m.m.</span><span class="sxs-lookup"><span data-stu-id="f1106-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="f1106-107">Proceduren bruger demodatafirmaet USP2.</span><span class="sxs-lookup"><span data-stu-id="f1106-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="f1106-108">Spore et element bagud ved hjælp af et kendt batchnummer</span><span class="sxs-lookup"><span data-stu-id="f1106-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="f1106-109">Gå til Lagerstyring > Forespørgsler og rapporter > Sporingsdimensioner > Varesporing.</span><span class="sxs-lookup"><span data-stu-id="f1106-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="f1106-110">I feltet Varenummer skal du vælge P9100.</span><span class="sxs-lookup"><span data-stu-id="f1106-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="f1106-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f1106-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f1106-112">Vælg 'Bagud' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="f1106-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="f1106-113">Vælg as-12-344-01' i feltet Batchnummer.</span><span class="sxs-lookup"><span data-stu-id="f1106-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="f1106-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f1106-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f1106-115">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f1106-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="f1106-116">Identificere en vare, spore den fremad og foretage en analyse</span><span class="sxs-lookup"><span data-stu-id="f1106-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="f1106-117">Den øverste node i træet repræsenterer det disponible antal af den valgte vare og batch.</span><span class="sxs-lookup"><span data-stu-id="f1106-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="f1106-118">Du skal udvide noderne i træet for at finde den vare, som den fremadrettede sporing skal udføres for.</span><span class="sxs-lookup"><span data-stu-id="f1106-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="f1106-119">I træet skal du udvide de noder, der er beskrevet nedenfor og derefter vælge den sidste node.</span><span class="sxs-lookup"><span data-stu-id="f1106-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="f1106-120">Udvid: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7,00 gal \P9100 ● Plukket ● Salgsordre 000072 ● 12/22/2015 ● -1 keg ● -4,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 \P9100 ● Produktion B-000050 ● 12/9/2015● 7 keg ● 27,00 gal ● Sted=1, Lagersted=10, Batchnumber=as-12-344-01 ● Samprodukter: P9101', og vælg derefter denne node.</span><span class="sxs-lookup"><span data-stu-id="f1106-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="f1106-121">I træet skal du udvide den node, der er beskrevet nedenfor og derefter vælge denne node.</span><span class="sxs-lookup"><span data-stu-id="f1106-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="f1106-122">Start fra den node, du lige har valgt, udvid ' M9103 ● Produktionslinje B-000050 ● 12/9/2015 ●-160,00 lb ● Størrelse=70, Farve=OK, Sted=1, Lagersted=10, Batchnummer=App01', og vælg derefter denne node.</span><span class="sxs-lookup"><span data-stu-id="f1106-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="f1106-123">Klik på Spor fra node.</span><span class="sxs-lookup"><span data-stu-id="f1106-123">Click Trace from node.</span></span>
4. <span data-ttu-id="f1106-124">Klik på Fremad.</span><span class="sxs-lookup"><span data-stu-id="f1106-124">Click Forward.</span></span>
5. <span data-ttu-id="f1106-125">Klik på Sporing i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f1106-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="f1106-126">Der er flere vektoriseringsindstillinger, der indeholder oplysninger om de debitorer, der er påvirket af den vare, du sporer, og de salgsordrer, der relaterer til den vare, der er eller ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="f1106-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="f1106-127">Klik på Debitorer.</span><span class="sxs-lookup"><span data-stu-id="f1106-127">Click Customers.</span></span>
7. <span data-ttu-id="f1106-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1106-128">Close the page.</span></span>
8. <span data-ttu-id="f1106-129">Klik på Sporing i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f1106-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="f1106-130">Klik på Afsendte salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="f1106-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="f1106-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f1106-131">Close the page.</span></span>

