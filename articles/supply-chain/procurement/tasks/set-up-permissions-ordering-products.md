--- 
title: "Konfigurere tilladelser til bestilling af produkter på vegne af en anden person"
description: "Denne fremgangsmåde viser, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere."
author: mkirknel
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
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="dd6df-103">Konfigurere tilladelser til bestilling af produkter på vegne af en anden person</span><span class="sxs-lookup"><span data-stu-id="dd6df-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd6df-104">Denne fremgangsmåde viser, hvordan du kan give arbejdere tilladelse til at oprette indkøbsrekvisitioner på vegne af andre arbejdere.</span><span class="sxs-lookup"><span data-stu-id="dd6df-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="dd6df-105">Med andre ord kan "klargøreren" af en indkøbsrekvisition oprette en rekvisition for en anden "anmoder."</span><span class="sxs-lookup"><span data-stu-id="dd6df-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="dd6df-106">Proceduren viser også, hvordan du kan tildele en arbejder rettigheder til at bestille varer og tjenester i forskellige juridiske enheder eller driftsenheder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="dd6df-107">Disse opgaver udføres typisk af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="dd6df-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="dd6df-108">Du kan enten bruge denne procedure dataene i USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="dd6df-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="dd6df-109">Tildel tilladelse til at indtaste indkøbsrekvisitioner på vegne af en anden arbejder</span><span class="sxs-lookup"><span data-stu-id="dd6df-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="dd6df-110">Gå til Indkøb og forsyning > Konfiguration > Politikker > Tilladelser til indkøbsrekvisitioner.</span><span class="sxs-lookup"><span data-stu-id="dd6df-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="dd6df-111">Sørg for, at feltet Aktuel visning er angivet til Efter klargører.</span><span class="sxs-lookup"><span data-stu-id="dd6df-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="dd6df-112">På listen i venstre rude vises de personer, der kan gives tilladelse til at oprette indkøbsrekvisitioner på vegne af andre personer.</span><span class="sxs-lookup"><span data-stu-id="dd6df-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="dd6df-113">Vælg den person, du vil give tilladelse til (klargøreren).</span><span class="sxs-lookup"><span data-stu-id="dd6df-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="dd6df-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="dd6df-114">Click Add.</span></span>
4. <span data-ttu-id="dd6df-115">Find og vælg den person, der skal tilføjes som anmoder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="dd6df-116">Anmoderen er den person, der klargøreren kan oprette indkøbsrekvisitioner på vegne af.</span><span class="sxs-lookup"><span data-stu-id="dd6df-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="dd6df-117">Vælg Specifik i feltet Godkendelse, hvis klargøreren skal være i stand til at oprette indkøbsrekvisitioner på vegne af den valgte arbejder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="dd6df-118">Vælg Rapportering, hvis klargøreren også skal være i stand til at oprette indkøbsrekvisitioner på vegne af alle arbejdere, der rapporterer til denne arbejder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="dd6df-119">Angiv en dato i feltet Gældende.</span><span class="sxs-lookup"><span data-stu-id="dd6df-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="dd6df-120">Angiv en dato i feltet Udløb.</span><span class="sxs-lookup"><span data-stu-id="dd6df-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="dd6df-121">Vis klargørere, der har tilladelse til at oprette indkøbsrekvisitioner for en valgt arbejder</span><span class="sxs-lookup"><span data-stu-id="dd6df-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="dd6df-122">Vælg 'Efter anmoder' i feltet Aktuel visning.</span><span class="sxs-lookup"><span data-stu-id="dd6df-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="dd6df-123">I denne visning kan du få vist en liste over klargørere, der har fået tilladelse til at oprette indkøbsrekvisitioner på vegne af en valgt arbejder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="dd6df-124">Brug Quick Filter til at finde den medarbejder, som du netop har tilføjet, som anmoder.</span><span class="sxs-lookup"><span data-stu-id="dd6df-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="dd6df-125">Vælg anmoderen.</span><span class="sxs-lookup"><span data-stu-id="dd6df-125">Select the requester.</span></span>
    * <span data-ttu-id="dd6df-126">Listen Klargører viser de personer, der har tilladelse til at bestille varer på vegne af den anmoder, der er valgt i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="dd6df-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="dd6df-127">Du kan tilføje yderligere klargørere her.</span><span class="sxs-lookup"><span data-stu-id="dd6df-127">You can add additional preparers here.</span></span>   <span data-ttu-id="dd6df-128">I denne visning kan du også give anmoderen tilladelse til at oprette indkøbsrekvisitioner i juridiske enheder og driftsenheder, der ikke er den pågældende persons primære juridiske enhed eller driftsenhed.</span><span class="sxs-lookup"><span data-stu-id="dd6df-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


