---
title: Konfigurere tilladelser til bestilling af produkter på vegne af en anden person
description: I dette emne beskrives, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere.
author: mkirknel
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 145d8a0e341857bf238fc934cd668ff12b8505b8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207548"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="a706a-103">Konfigurere tilladelser til bestilling af produkter på vegne af en anden person</span><span class="sxs-lookup"><span data-stu-id="a706a-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a706a-104">I dette emne beskrives, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere.</span><span class="sxs-lookup"><span data-stu-id="a706a-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="a706a-105">Med andre ord kan "klargøreren" af en indkøbsrekvisition oprette en rekvisition for en anden "anmoder."</span><span class="sxs-lookup"><span data-stu-id="a706a-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="a706a-106">Proceduren viser også, hvordan du kan tildele en arbejder rettigheder til at bestille varer og tjenester i forskellige juridiske enheder eller driftsenheder.</span><span class="sxs-lookup"><span data-stu-id="a706a-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="a706a-107">Disse opgaver udføres typisk af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="a706a-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="a706a-108">Du kan enten bruge denne procedure dataene i USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a706a-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="a706a-109">Tildel tilladelse til at indtaste indkøbsrekvisitioner på vegne af en anden arbejder</span><span class="sxs-lookup"><span data-stu-id="a706a-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="a706a-110">I navigationsruden skal du gå til **Moduler > Indkøb og forsyning > Opsætning > Politikker > Tilladelser til indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="a706a-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="a706a-111">Sørg for, at feltet **Aktuel visning** er indstillet til **Efter klargører**.</span><span class="sxs-lookup"><span data-stu-id="a706a-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="a706a-112">På listen i venstre rude vises de personer, der kan gives tilladelse til at oprette indkøbsrekvisitioner på vegne af andre personer.</span><span class="sxs-lookup"><span data-stu-id="a706a-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="a706a-113">Vælg den person, du vil give tilladelse til (klargøreren).</span><span class="sxs-lookup"><span data-stu-id="a706a-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="a706a-114">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a706a-114">Select **Add**.</span></span>
4. <span data-ttu-id="a706a-115">Find og vælg den person, der skal tilføjes som anmoder.</span><span class="sxs-lookup"><span data-stu-id="a706a-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="a706a-116">Anmoderen er den person, der klargøreren kan oprette indkøbsrekvisitioner på vegne af.</span><span class="sxs-lookup"><span data-stu-id="a706a-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="a706a-117">Vælg **Specifik** i feltet **Godkendelse**, hvis klargøreren skal være i stand til at oprette indkøbsrekvisitioner på vegne af den valgte arbejder.</span><span class="sxs-lookup"><span data-stu-id="a706a-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="a706a-118">Vælg **Rapportering**, hvis klargøreren også skal være i stand til at oprette indkøbsrekvisitioner på vegne af alle arbejdere, der rapporterer til denne arbejder.</span><span class="sxs-lookup"><span data-stu-id="a706a-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="a706a-119">Angiv en dato i feltet **Gældende**.</span><span class="sxs-lookup"><span data-stu-id="a706a-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="a706a-120">Angiv en dato i feltet **Udløb**.</span><span class="sxs-lookup"><span data-stu-id="a706a-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="a706a-121">Vis klargørere, der har tilladelse til at oprette indkøbsrekvisitioner for en valgt arbejder</span><span class="sxs-lookup"><span data-stu-id="a706a-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="a706a-122">Vælg **Efter anmoder** i feltet **Aktuel visning**.</span><span class="sxs-lookup"><span data-stu-id="a706a-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="a706a-123">I denne visning kan du få vist en liste over klargørere, der har fået tilladelse til at oprette indkøbsrekvisitioner på vegne af en valgt arbejder.</span><span class="sxs-lookup"><span data-stu-id="a706a-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="a706a-124">Brug Quick Filter til at finde den medarbejder, som du netop har tilføjet, som anmoder.</span><span class="sxs-lookup"><span data-stu-id="a706a-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="a706a-125">Vælg anmoderen.</span><span class="sxs-lookup"><span data-stu-id="a706a-125">Select the requester.</span></span> <span data-ttu-id="a706a-126">Listen Klargører viser de personer, der har tilladelse til at bestille varer på vegne af den anmoder, der er valgt i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="a706a-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="a706a-127">Du kan tilføje yderligere klargørere her.</span><span class="sxs-lookup"><span data-stu-id="a706a-127">You can add additional preparers here.</span></span> <span data-ttu-id="a706a-128">I denne visning kan du også give anmoderen tilladelse til at oprette indkøbsrekvisitioner i juridiske enheder og driftsenheder, der ikke er den pågældende persons primære juridiske enhed eller driftsenhed.</span><span class="sxs-lookup"><span data-stu-id="a706a-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

