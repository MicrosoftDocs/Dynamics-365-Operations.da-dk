--- 
title: Levere produkter direkte fra modtagende lagersteder til butikker
description: "Denne procedure gennemgår trin til oprettelse og behandling af en cross-dock med henblik på distribution af produkter fra modtagelokationen af en købsordre til en eller flere butikker."
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c8e25007cc4a204aeaf73a2e819c129fa8fa29d
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="f7cd4-103">Levere produkter direkte fra modtagende lagersteder til butikker</span><span class="sxs-lookup"><span data-stu-id="f7cd4-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7cd4-104">Denne procedure gennemgår trin til oprettelse og behandling af en cross-dock med henblik på distribution af produkter fra modtagelokationen af en købsordre til en eller flere butikker.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="f7cd4-105">Brugeren kan definere flere konfigurationer og få systemet til at foreslå, hvordan produkter skal distribueres, eller manuelt angive, hvor produkterne skal distribueres til, og hvor meget der bliver distribueret til de enkelte butikker.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="f7cd4-106">Proceduren omfatter ikke opsætning af data, der kan bruges i cross-dock'en som f.eks. genopfyldningsregler, organisationshierarkier og vægten af butikken.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="f7cd4-107">Proceduren bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f7cd4-108">Gå til Alle indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f7cd4-109">Vælg en indkøbsordre på listen, og klik på linket for at åbne ordren.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="f7cd4-110">Klik på Detail i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="f7cd4-111">Klik på Cross docking.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-111">Click Cross docking.</span></span>
5. <span data-ttu-id="f7cd4-112">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-112">Click Edit.</span></span>
    * <span data-ttu-id="f7cd4-113">Kategorien, der kan bruges til at filtrere varerne i sektionen Linjer.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="f7cd4-114">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f7cd4-115">Skriv en værdi i feltet Antal til direkte levering for at angive, hvor meget af den mængde, der købes af det valgte produkt, der skal fordeles.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="f7cd4-116">I feltet Yderligere antal til direkte levering skal du angive en værdi for at angive mængderne, der skal fordeles for de tilgængelige produkter, der købes</span><span class="sxs-lookup"><span data-stu-id="f7cd4-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="f7cd4-117">Angiv "Lokationsvægt" i feltet Distribution.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="f7cd4-118">Du kan vælge andre typer for at bruge forskellige regler for fordelingen.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="f7cd4-119">Vælg en værdi i feltet Opfyldningshierarki.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="f7cd4-120">Vælg Ja i feltet Respektér udvalg.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="f7cd4-121">Klik på Beregn antal.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="f7cd4-122">Klik på Opret ordre.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-122">Click Create order.</span></span>
14. <span data-ttu-id="f7cd4-123">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-123">Click Yes.</span></span>
15. <span data-ttu-id="f7cd4-124">På listen skal du finde og vælge et lagersted, der har modtaget produkter.</span><span class="sxs-lookup"><span data-stu-id="f7cd4-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="f7cd4-125">Klik på Bestil for at få vist de ordrer, der blev oprettet for det valgte lagersted</span><span class="sxs-lookup"><span data-stu-id="f7cd4-125">Click Order to view the orders that got created for the selected warehouse</span></span>


