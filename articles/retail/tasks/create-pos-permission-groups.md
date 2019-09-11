---
title: Oprette POS-rettighedsgrupper
description: Dette emner beskriver, hvordan du opretter en POS-rettighedsgruppe.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
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
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914780"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="9aa04-103">Oprette POS-rettighedsgrupper</span><span class="sxs-lookup"><span data-stu-id="9aa04-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9aa04-104">Dette emner beskriver, hvordan du opretter en POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9aa04-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="9aa04-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="9aa04-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="9aa04-106">Denne opgave er tiltænkt rollen Retail driftschef.</span><span class="sxs-lookup"><span data-stu-id="9aa04-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="9aa04-107">Gå i navigationsruden til **Moduler > Detail > Medarbejdere > Rettighedsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="9aa04-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-108">Select **New**.</span></span>
3. <span data-ttu-id="9aa04-109">Skriv en værdi i feltet **Id for POS-rettighedsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="9aa04-110">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="9aa04-111">Vælg **Ja** i feltet **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="9aa04-112">Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9aa04-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="9aa04-113">For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="9aa04-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="9aa04-114">Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.</span><span class="sxs-lookup"><span data-stu-id="9aa04-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="9aa04-115">Vælg **Ja** i feltet **Tillad oprettelse af ordre**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="9aa04-116">Vælg **Ja** i feltet **Tillad redigering af ordre**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="9aa04-117">Vælg **Ja** i feltet **Tillad hentning af ordre**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="9aa04-118">Vælg **Ja** i feltet **Tillad ændring af adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="9aa04-119">Vælg **Ja** i feltet **Tillad lukning uden kontrol**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="9aa04-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-120">Select **Save**.</span></span> <span data-ttu-id="9aa04-121">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="9aa04-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="9aa04-122">Gå i navigationsruden til **Moduler > Personale > Job > Job**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="9aa04-123">Dernæst vil vi tildele POS-rettighedsgruppen til et Job.</span><span class="sxs-lookup"><span data-stu-id="9aa04-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="9aa04-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="9aa04-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9aa04-125">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-125">Select **Edit**.</span></span>
15. <span data-ttu-id="9aa04-126">Udvid sektionen **Jobklassificering**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="9aa04-127">Indtast eller vælg en værdi i feltet POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9aa04-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="9aa04-128">Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.</span><span class="sxs-lookup"><span data-stu-id="9aa04-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="9aa04-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9aa04-129">Select **Save**.</span></span> <span data-ttu-id="9aa04-130">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til detailkanaler.</span><span class="sxs-lookup"><span data-stu-id="9aa04-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

