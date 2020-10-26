---
title: Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt
description: Denne procedure gennemgår trinnene for brug af variantvægte til automatisk udfyldning af indkøbsordrelinjer for hver variant af et produkt.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c099daf888cb2a1740dda3e860b37f88089c5ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986449"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="a899e-103">Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt</span><span class="sxs-lookup"><span data-stu-id="a899e-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a899e-104">Denne procedure gennemgår trinnene for brug af variantvægte til automatisk udfyldning af indkøbsordrelinjer for hver variant af et produkt.</span><span class="sxs-lookup"><span data-stu-id="a899e-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="a899e-105">Når du vælger mængden af produktet, du vil købe, oprettes der indkøbsordrelinjer for alle varianter af produktet med foreslåede mængder, der er baseret på de vægte, der er konfigureret i produktvarianterne.</span><span class="sxs-lookup"><span data-stu-id="a899e-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="a899e-106">Denne procedure omfatter ikke trin til at konfigurere vægtværdier for produktdimensioner og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="a899e-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="a899e-107">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="a899e-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a899e-108">Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="a899e-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a899e-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a899e-109">Click New.</span></span>
3. <span data-ttu-id="a899e-110">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a899e-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a899e-111">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a899e-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a899e-112">Slå udvidelsen af sektionen Generelt til/fra.</span><span class="sxs-lookup"><span data-stu-id="a899e-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="a899e-113">Klik på rullelisten i feltet Sted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a899e-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a899e-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a899e-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a899e-115">Klik på rullelisten i feltet Lagersted for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="a899e-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a899e-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a899e-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a899e-117">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a899e-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a899e-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a899e-118">Click OK.</span></span>
12. <span data-ttu-id="a899e-119">Slå udvidelsen af sektionen Linjedetaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="a899e-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="a899e-120">Klik på fanen Varianter.</span><span class="sxs-lookup"><span data-stu-id="a899e-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="a899e-121">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="a899e-121">Click Add line.</span></span>
15. <span data-ttu-id="a899e-122">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a899e-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="a899e-123">I feltet Varenummer skal du skrive "0140".</span><span class="sxs-lookup"><span data-stu-id="a899e-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="a899e-124">Angiv antallet til '1000'.</span><span class="sxs-lookup"><span data-stu-id="a899e-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="a899e-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a899e-125">Click Save.</span></span>

