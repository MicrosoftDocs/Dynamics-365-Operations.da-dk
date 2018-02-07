--- 
title: " Oprette POS-rettighedsgrupper"
description: Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="6953d-103"> Oprette POS-rettighedsgrupper</span><span class="sxs-lookup"><span data-stu-id="6953d-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6953d-104">Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6953d-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="6953d-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="6953d-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="6953d-106">Denne opgave er tiltænkt rollen Retail driftschef.</span><span class="sxs-lookup"><span data-stu-id="6953d-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="6953d-107">Gå til Rettighedsgrupper.</span><span class="sxs-lookup"><span data-stu-id="6953d-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="6953d-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6953d-108">Click New.</span></span>
3. <span data-ttu-id="6953d-109">Skriv en værdi i feltet Id for POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6953d-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="6953d-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6953d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6953d-111">Vælg Ja i feltet Vis tidsursangivelser.</span><span class="sxs-lookup"><span data-stu-id="6953d-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="6953d-112">Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6953d-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="6953d-113">For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="6953d-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="6953d-114">Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.</span><span class="sxs-lookup"><span data-stu-id="6953d-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="6953d-115">Vælg Ja i feltet Tillad oprettelse af ordre.</span><span class="sxs-lookup"><span data-stu-id="6953d-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="6953d-116">Vælg Ja i feltet Tillad redigering af ordre.</span><span class="sxs-lookup"><span data-stu-id="6953d-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="6953d-117">Vælg Ja i feltet Tillad hentning af ordre.</span><span class="sxs-lookup"><span data-stu-id="6953d-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="6953d-118">Vælg Ja i feltet Tillad ændring af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="6953d-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="6953d-119">Vælg Ja i feltet Tillad lukning uden kontrol.</span><span class="sxs-lookup"><span data-stu-id="6953d-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="6953d-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6953d-120">Click Save.</span></span>
    * <span data-ttu-id="6953d-121">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="6953d-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="6953d-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6953d-122">Close the page.</span></span>
13. <span data-ttu-id="6953d-123">Gå til job.</span><span class="sxs-lookup"><span data-stu-id="6953d-123">Go to Jobs.</span></span>
    * <span data-ttu-id="6953d-124">Dernæst vil vi tildele POS-rettighedsgruppen til et Job.</span><span class="sxs-lookup"><span data-stu-id="6953d-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="6953d-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6953d-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6953d-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6953d-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6953d-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="6953d-127">Click Edit.</span></span>
17. <span data-ttu-id="6953d-128">Udvid sektionen Jobklassificering.</span><span class="sxs-lookup"><span data-stu-id="6953d-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="6953d-129">Indtast eller vælg en værdi i feltet POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6953d-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="6953d-130">Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.</span><span class="sxs-lookup"><span data-stu-id="6953d-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="6953d-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6953d-131">Click Save.</span></span>
    * <span data-ttu-id="6953d-132">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="6953d-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


