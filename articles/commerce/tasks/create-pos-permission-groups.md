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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac03e1bfb7a2463b31feca0a4303c182a00ad259
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964814"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="08fc5-103">Oprette POS-rettighedsgrupper</span><span class="sxs-lookup"><span data-stu-id="08fc5-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08fc5-104">Dette emner beskriver, hvordan du opretter en POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="08fc5-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="08fc5-105">Det demodatafirma, der bruges til at oprette denne opgave, er USRT.</span><span class="sxs-lookup"><span data-stu-id="08fc5-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="08fc5-106">Denne opgave er tiltænkt rollen Commerce-driftschef.</span><span class="sxs-lookup"><span data-stu-id="08fc5-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="08fc5-107">Gå i navigationsruden til **Moduler > Retail og Commerce > Medarbejdere > Rettighedsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="08fc5-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-108">Select **New**.</span></span>
3. <span data-ttu-id="08fc5-109">Skriv en værdi i feltet **Id for POS-rettighedsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="08fc5-110">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="08fc5-111">Vælg **Ja** i feltet **Vis tidsursangivelser**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="08fc5-112">Du kan nu aktivere eller deaktivere forskellige rettigheder for din POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="08fc5-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="08fc5-113">For nogle rettigheder kan du angive en værdi, der skal bruges til at vurdere, om POS-brugeren kan udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="08fc5-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="08fc5-114">Denne opgaveguide muliggør nogle få rettigheder, der kan gives til en kasseassistent.</span><span class="sxs-lookup"><span data-stu-id="08fc5-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="08fc5-115">Vælg **Ja** i feltet **Tillad oprettelse af ordre**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="08fc5-116">Vælg **Ja** i feltet **Tillad redigering af ordre**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="08fc5-117">Vælg **Ja** i feltet **Tillad hentning af ordre**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="08fc5-118">Vælg **Ja** i feltet **Tillad ændring af adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="08fc5-119">Vælg **Ja** i feltet **Tillad lukning uden kontrol**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="08fc5-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-120">Select **Save**.</span></span> <span data-ttu-id="08fc5-121">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til handelskanalerne.</span><span class="sxs-lookup"><span data-stu-id="08fc5-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="08fc5-122">Gå i navigationsruden til **Moduler > Human resources > Job > Job**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="08fc5-123">Dernæst vil vi tildele POS-rettighedsgruppen til et Job.</span><span class="sxs-lookup"><span data-stu-id="08fc5-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="08fc5-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="08fc5-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="08fc5-125">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-125">Select **Edit**.</span></span>
15. <span data-ttu-id="08fc5-126">Udvid sektionen **Jobklassificering**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="08fc5-127">Indtast eller vælg en værdi i feltet POS-rettighedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="08fc5-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="08fc5-128">Alle arbejdere i positioner for dette job vil bruge indstillinger for denne POS-rettighedsgruppe, medmindre arbejdernes POS-rettigheder er blevet tilsidesat på deres positionsniveau.</span><span class="sxs-lookup"><span data-stu-id="08fc5-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="08fc5-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="08fc5-129">Select **Save**.</span></span> <span data-ttu-id="08fc5-130">Når dine ændringer er gemt, skal du køre planen til medarbejderdistribution for at overføre ændringerne til kanalerne.</span><span class="sxs-lookup"><span data-stu-id="08fc5-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

