--- 
title: "Konfigurere indkøbspolitikker"
description: "Denne fremgangsmåde viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="create-purchasing-policies"></a><span data-ttu-id="8e82a-103">Konfigurere indkøbspolitikker</span><span class="sxs-lookup"><span data-stu-id="8e82a-103">Create purchasing policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e82a-104">Denne fremgangsmåde viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb.</span><span class="sxs-lookup"><span data-stu-id="8e82a-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="8e82a-105">Før du kan oprette indkøbspolitikker, skal du konfigurere parametrene for indkøbspolitikker.</span><span class="sxs-lookup"><span data-stu-id="8e82a-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="8e82a-106">Det er muligt at oprette, redigere og trække en indkøbspolitik tilbage, men du kan ikke slette en indkøbspolitik.</span><span class="sxs-lookup"><span data-stu-id="8e82a-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="8e82a-107">Denne procedure vil typisk blive udført af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="8e82a-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="8e82a-108">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="8e82a-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="8e82a-109">Konfigurere politikparametre</span><span class="sxs-lookup"><span data-stu-id="8e82a-109">Set up policy parameters</span></span>
1. <span data-ttu-id="8e82a-110">Gå til Indkøbspolitikker.</span><span class="sxs-lookup"><span data-stu-id="8e82a-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="8e82a-111">Klik på Parametre.</span><span class="sxs-lookup"><span data-stu-id="8e82a-111">Click Parameters.</span></span>
    * <span data-ttu-id="8e82a-112">Prioriteringsregler for politikker gælder for forskellige niveauer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="8e82a-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="8e82a-113">De organisatoriske enheder, der vises, afhænger af organisationshierarkiet, og på hvilke niveauer i hierarkiet der er tildelt formål med intern kontrol af indkøb.</span><span class="sxs-lookup"><span data-stu-id="8e82a-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="8e82a-114">Organisationen kan f.eks. have juridiske enheder, bærere, områder og afdelinger, men det kan være, at kun nogle af dem har et hierarkiformål for intern kontrol af indkøb.</span><span class="sxs-lookup"><span data-stu-id="8e82a-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="8e82a-115">Som standard er organisationen af typen Firma tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="8e82a-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="8e82a-116">Klik på fanen Parametre for regeltypen.</span><span class="sxs-lookup"><span data-stu-id="8e82a-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="8e82a-117">Vælg 'Indkøbspolitik\Regel for styring af indkøbsrekvisition' i træet.</span><span class="sxs-lookup"><span data-stu-id="8e82a-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="8e82a-118">Du kan angive prioriterede rækkefølge for løsning af politikker på politikniveau.</span><span class="sxs-lookup"><span data-stu-id="8e82a-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="8e82a-119">For nogle politiktyper kan du dog tilsidesætte den prioriterede rækkefølge for enkelte politikregeltyper.</span><span class="sxs-lookup"><span data-stu-id="8e82a-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="8e82a-120">Du kan f.eks. definere den prioriterede rækkefølge for indkøbspolitikker til at være: bærer, afdeling, firma.</span><span class="sxs-lookup"><span data-stu-id="8e82a-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="8e82a-121">For katalogpolitikreglen skal den prioriterede rækkefølge måske være følgende: afdeling, bærer, firma.</span><span class="sxs-lookup"><span data-stu-id="8e82a-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="8e82a-122">Du kan ændre den prioriterede rækkefølge for katalogpolitikreglen.</span><span class="sxs-lookup"><span data-stu-id="8e82a-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="8e82a-123">Når en arbejder opretter en rekvisition, bestemmes det viste katalog af de politikker, der er tilknyttet arbejderens afdeling, derefter bæreren og derefter firmaet.</span><span class="sxs-lookup"><span data-stu-id="8e82a-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="8e82a-124">Hvis der vises mere end ét organisationsniveau, kan du bruge op/ned-pilene til at angive den prioriterede rækkefølge for reglen for styring af indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="8e82a-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="8e82a-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8e82a-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="8e82a-126">Opret en ny politik</span><span class="sxs-lookup"><span data-stu-id="8e82a-126">Create a new policy</span></span>
1. <span data-ttu-id="8e82a-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8e82a-127">Click New.</span></span>
2. <span data-ttu-id="8e82a-128">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="8e82a-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="8e82a-129">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8e82a-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="8e82a-130">En enkelt indkøbspolitik kan kun anvendes til ét organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="8e82a-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="8e82a-131">Du kan f.eks. have ét hierarki, der kaldes "Geografisk", og et, der kaldes "Afdeling", og have en forskellige indkøbspolitik for hver af dem.</span><span class="sxs-lookup"><span data-stu-id="8e82a-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="8e82a-132">Vælg en organisation, som politikken skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="8e82a-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="8e82a-133">Klik på pilen for at tilføje den valgte organisation.</span><span class="sxs-lookup"><span data-stu-id="8e82a-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="8e82a-134">Du kan gentage denne proces for at føje flere organisationer.</span><span class="sxs-lookup"><span data-stu-id="8e82a-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="8e82a-135">Tilføj en politikregel</span><span class="sxs-lookup"><span data-stu-id="8e82a-135">Add a policy rule</span></span>
1. <span data-ttu-id="8e82a-136">Vælg Regel for rekvisitionsformål på listen Regeltype.</span><span class="sxs-lookup"><span data-stu-id="8e82a-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="8e82a-137">Du opretter en regel, der angiver formålet med standardrekvisitionen til typen Forbrug, men tillader, at typen Opfyldning vælges i stedet.</span><span class="sxs-lookup"><span data-stu-id="8e82a-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="8e82a-138">Klik på Opret politikregel.</span><span class="sxs-lookup"><span data-stu-id="8e82a-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="8e82a-139">Vælg Ja i feltet Tillad manuel tilsidesættelse.</span><span class="sxs-lookup"><span data-stu-id="8e82a-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="8e82a-140">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="8e82a-140">Click Close.</span></span>
    * <span data-ttu-id="8e82a-141">Du kan nu konfigurere andre politikregler for indkøbspolitikken.</span><span class="sxs-lookup"><span data-stu-id="8e82a-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="8e82a-142">Bemærk, at en politikregeltype ikke kan have overlappende regler, der er aktive på samme tid i en enkelt indkøbspolitik.</span><span class="sxs-lookup"><span data-stu-id="8e82a-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="8e82a-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8e82a-143">Close the page.</span></span>
6. <span data-ttu-id="8e82a-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8e82a-144">Close the page.</span></span>


