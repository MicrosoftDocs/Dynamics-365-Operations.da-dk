---
title: " Oprette POS-rettighedsgrupper"
description: Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "354454"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="f7d09-103"> Oprette POS-rettighedsgrupper</span><span class="sxs-lookup"><span data-stu-id="f7d09-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f7d09-104">Denne procedure viser, hvordan du opretter en POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f7d09-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="f7d09-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="f7d09-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="f7d09-106">Denne opgave er tiltænkt rollen Retail driftschef.</span><span class="sxs-lookup"><span data-stu-id="f7d09-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="f7d09-107">Gå til Rettighedsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f7d09-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="f7d09-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f7d09-108">Click New.</span></span>
3. <span data-ttu-id="f7d09-109">Skriv en værdi i feltet Id for POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f7d09-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="f7d09-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f7d09-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d09-111">Vælg Ja i feltet Vis tidsursangivelser.</span><span class="sxs-lookup"><span data-stu-id="f7d09-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="f7d09-112">Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f7d09-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="f7d09-113">For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="f7d09-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="f7d09-114">Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.</span><span class="sxs-lookup"><span data-stu-id="f7d09-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="f7d09-115">Vælg Ja i feltet Tillad oprettelse af ordre.</span><span class="sxs-lookup"><span data-stu-id="f7d09-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="f7d09-116">Vælg Ja i feltet Tillad redigering af ordre.</span><span class="sxs-lookup"><span data-stu-id="f7d09-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="f7d09-117">Vælg Ja i feltet Tillad hentning af ordre.</span><span class="sxs-lookup"><span data-stu-id="f7d09-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="f7d09-118">Vælg Ja i feltet Tillad ændring af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="f7d09-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="f7d09-119">Vælg Ja i feltet Tillad lukning uden kontrol.</span><span class="sxs-lookup"><span data-stu-id="f7d09-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="f7d09-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f7d09-120">Click Save.</span></span>
    * <span data-ttu-id="f7d09-121">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="f7d09-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="f7d09-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f7d09-122">Close the page.</span></span>
13. <span data-ttu-id="f7d09-123">Gå til job.</span><span class="sxs-lookup"><span data-stu-id="f7d09-123">Go to Jobs.</span></span>
    * <span data-ttu-id="f7d09-124">Dernæst vil vi tildele POS-rettighedsgruppen til et Job.</span><span class="sxs-lookup"><span data-stu-id="f7d09-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="f7d09-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="f7d09-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f7d09-126">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f7d09-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f7d09-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="f7d09-127">Click Edit.</span></span>
17. <span data-ttu-id="f7d09-128">Udvid sektionen Jobklassificering.</span><span class="sxs-lookup"><span data-stu-id="f7d09-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="f7d09-129">Indtast eller vælg en værdi i feltet POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f7d09-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d09-130">Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.</span><span class="sxs-lookup"><span data-stu-id="f7d09-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="f7d09-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f7d09-131">Click Save.</span></span>
    * <span data-ttu-id="f7d09-132">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="f7d09-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

