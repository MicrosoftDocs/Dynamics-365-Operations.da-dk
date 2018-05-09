--- 
title: " Skubbe produkter fra distributionscenter til butik ved hjælp af centraliseret indkøb"
description: "Denne procedure gennemgår trin til oprettelse og behandling af et centraliseret indkøb med henblik på distribution af produkter fra én lokation til en eller mange butikker."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 393b12cf5486e3151f41f752f628ef6335c28e6e
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="7e201-103"> Skubbe produkter fra distributionscenter til butik ved hjælp af centraliseret indkøb</span><span class="sxs-lookup"><span data-stu-id="7e201-103">Push products from distribution center to store using buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7e201-104">Denne procedure gennemgår trin til oprettelse og behandling af et centraliseret indkøb med henblik på distribution af produkter fra én lokation til en eller mange butikker.</span><span class="sxs-lookup"><span data-stu-id="7e201-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="7e201-105">Brugeren kan definere flere konfigurationer og få systemet til at foreslå, hvordan produkter skal distribueres, eller manuelt angive, hvor produkterne skal distribueres til, og hvor meget der bliver distribueret til de enkelte butikker.</span><span class="sxs-lookup"><span data-stu-id="7e201-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="7e201-106">Denne procedure omfatter ikke opsætning af data, der kan bruges i centraliseret indkøb som f.eks. genopfyldningsregler, organisationshierarkier og vægten af butikken.</span><span class="sxs-lookup"><span data-stu-id="7e201-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="7e201-107">Denne procedure bruger demofirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="7e201-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="7e201-108">Gå til Bestilling efter ordre.</span><span class="sxs-lookup"><span data-stu-id="7e201-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="7e201-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7e201-109">Click New.</span></span>
3. <span data-ttu-id="7e201-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7e201-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="7e201-111">Indtast eller vælg en værdi i feltet Lokation.</span><span class="sxs-lookup"><span data-stu-id="7e201-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="7e201-112">Angiv eller vælg et lagersted, der har produkter med disponible antal, i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="7e201-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="7e201-113">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7e201-113">Click Add.</span></span>
7. <span data-ttu-id="7e201-114">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7e201-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7e201-115">Indtast eller vælg et produkt i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="7e201-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="7e201-116">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7e201-116">Click Add.</span></span>
10. <span data-ttu-id="7e201-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7e201-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="7e201-118">Indtast eller vælg et variant-produkt i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="7e201-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="7e201-119">Når du angiver et variantprodukt, oprettes der linjer for hver variant.</span><span class="sxs-lookup"><span data-stu-id="7e201-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="7e201-120">Markér en række på listen.</span><span class="sxs-lookup"><span data-stu-id="7e201-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="7e201-121">Skriv i feltet Udskudt antal, hvor mange af det valgte produkt, du vil fordele.</span><span class="sxs-lookup"><span data-stu-id="7e201-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="7e201-122">I feltet Tillægsantal til overførsel skal du angive antallet af produkter, der har tilgængeligt antal til fordeling.</span><span class="sxs-lookup"><span data-stu-id="7e201-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="7e201-123">Angiv "Lokationsvægt" i feltet Distribution.</span><span class="sxs-lookup"><span data-stu-id="7e201-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="7e201-124">Du kan vælge andre typer for at bruge andre regler for fordelingen.</span><span class="sxs-lookup"><span data-stu-id="7e201-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="7e201-125">Vælg en værdi i feltet Opfyldningshierarki.</span><span class="sxs-lookup"><span data-stu-id="7e201-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="7e201-126">Vælg Ja i feltet Respektér udvalg.</span><span class="sxs-lookup"><span data-stu-id="7e201-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="7e201-127">Klik på Beregn antal, og gennemgå de antal, der er føjet til rækkerne i sektionen Lagersted.</span><span class="sxs-lookup"><span data-stu-id="7e201-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="7e201-128">Klik på Opret ordre.</span><span class="sxs-lookup"><span data-stu-id="7e201-128">Click Create order.</span></span>
20. <span data-ttu-id="7e201-129">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="7e201-129">Click Yes.</span></span>


