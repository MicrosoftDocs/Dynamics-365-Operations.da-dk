---
title: Oprette indkøbspolitikker
description: Dette emne viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb.
author: mkirknel
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8416f9a869b9144a63a6fb08c667cc32dec9854
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149705"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="c8673-103">Oprette indkøbspolitikker</span><span class="sxs-lookup"><span data-stu-id="c8673-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8673-104">Dette emne viser, hvordan du opretter indkøbspolitikker, der skal justeres med dine forretningsprocesser til indkøb.</span><span class="sxs-lookup"><span data-stu-id="c8673-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="c8673-105">Før du kan oprette indkøbspolitikker, skal du konfigurere parametrene for indkøbspolitikker.</span><span class="sxs-lookup"><span data-stu-id="c8673-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="c8673-106">Det er muligt at oprette, redigere og trække en indkøbspolitik tilbage, men du kan ikke slette en indkøbspolitik.</span><span class="sxs-lookup"><span data-stu-id="c8673-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="c8673-107">Denne procedure vil typisk blive udført af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="c8673-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="c8673-108">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="c8673-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="c8673-109">Konfigurere politikparametre</span><span class="sxs-lookup"><span data-stu-id="c8673-109">Set up policy parameters</span></span>
1. <span data-ttu-id="c8673-110">I navigationsruden skal du gå til **Moduler > Indkøb og forsyning > Opsætning > Politikker > Indkøbspolitikker**.</span><span class="sxs-lookup"><span data-stu-id="c8673-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="c8673-111">Gå til handlingsruden, og vælg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="c8673-111">In the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="c8673-112">Prioriteringsregler for politikker gælder for forskellige niveauer i organisationen.</span><span class="sxs-lookup"><span data-stu-id="c8673-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="c8673-113">De organisatoriske enheder, der vises, afhænger af organisationshierarkiet, og på hvilke niveauer i hierarkiet der er tildelt formål med intern kontrol af indkøb.</span><span class="sxs-lookup"><span data-stu-id="c8673-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="c8673-114">Organisationen kan f.eks. have juridiske enheder, bærere, områder og afdelinger, men det kan være, at kun nogle af dem har et hierarkiformål for intern kontrol af indkøb.</span><span class="sxs-lookup"><span data-stu-id="c8673-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="c8673-115">Som standard er organisationen af typen Firma tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c8673-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="c8673-116">Vælg fanen **Parametre for regeltypen**.</span><span class="sxs-lookup"><span data-stu-id="c8673-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="c8673-117">Gå til **Indkøbspolitik > Regel for styring af indkøbsrekvisition** i træet.</span><span class="sxs-lookup"><span data-stu-id="c8673-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="c8673-118">Du kan angive prioriterede rækkefølge for løsning af politikker på politikniveau.</span><span class="sxs-lookup"><span data-stu-id="c8673-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="c8673-119">For nogle politiktyper kan du dog tilsidesætte den prioriterede rækkefølge for enkelte politikregeltyper.</span><span class="sxs-lookup"><span data-stu-id="c8673-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="c8673-120">Du kan f.eks. definere den prioriterede rækkefølge for indkøbspolitikker til at være: bærer, afdeling, firma.</span><span class="sxs-lookup"><span data-stu-id="c8673-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="c8673-121">For katalogpolitikreglen skal den prioriterede rækkefølge måske være følgende: afdeling, bærer, firma.</span><span class="sxs-lookup"><span data-stu-id="c8673-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="c8673-122">Du kan ændre den prioriterede rækkefølge for katalogpolitikreglen.</span><span class="sxs-lookup"><span data-stu-id="c8673-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="c8673-123">Når en arbejder opretter en rekvisition, bestemmes det viste katalog af de politikker, der er tilknyttet arbejderens afdeling, derefter bæreren og derefter firmaet.</span><span class="sxs-lookup"><span data-stu-id="c8673-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="c8673-124">Hvis der vises mere end ét organisationsniveau, kan du bruge op/ned-pilene til at angive den prioriterede rækkefølge for reglen for styring af indkøbsrekvisition.</span><span class="sxs-lookup"><span data-stu-id="c8673-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="c8673-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c8673-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="c8673-126">Opret en ny politik</span><span class="sxs-lookup"><span data-stu-id="c8673-126">Create a new policy</span></span>
1. <span data-ttu-id="c8673-127">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c8673-127">Select **New**.</span></span>
2. <span data-ttu-id="c8673-128">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c8673-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="c8673-129">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c8673-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="c8673-130">En enkelt indkøbspolitik kan kun anvendes til ét organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="c8673-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="c8673-131">Du kan f.eks. have ét hierarki, der kaldes "Geografisk", og et, der kaldes "Afdeling", og have en forskellige indkøbspolitik for hver af dem.</span><span class="sxs-lookup"><span data-stu-id="c8673-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="c8673-132">Vælg en organisation, som politikken skal gælde for.</span><span class="sxs-lookup"><span data-stu-id="c8673-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="c8673-133">Vælg pilen for at tilføje den valgte organisation.</span><span class="sxs-lookup"><span data-stu-id="c8673-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="c8673-134">Du kan gentage denne proces for at føje flere organisationer.</span><span class="sxs-lookup"><span data-stu-id="c8673-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="c8673-135">Tilføj en politikregel</span><span class="sxs-lookup"><span data-stu-id="c8673-135">Add a policy rule</span></span>
1. <span data-ttu-id="c8673-136">Vælg **Regel for rekvisitionsformål** på listen **Regeltype**.</span><span class="sxs-lookup"><span data-stu-id="c8673-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="c8673-137">Du opretter en regel, der angiver formålet med standardrekvisitionen til typen Forbrug, men tillader, at typen Opfyldning vælges i stedet.</span><span class="sxs-lookup"><span data-stu-id="c8673-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="c8673-138">Vælg **Opret politikregel**.</span><span class="sxs-lookup"><span data-stu-id="c8673-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="c8673-139">Vælg **Ja** i feltet **Tillad manuel tilsidesættelse**.</span><span class="sxs-lookup"><span data-stu-id="c8673-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="c8673-140">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="c8673-140">Select **Close**.</span></span>
- <span data-ttu-id="c8673-141">Du kan nu konfigurere andre politikregler for indkøbspolitikken.</span><span class="sxs-lookup"><span data-stu-id="c8673-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="c8673-142">Bemærk, at en politikregeltype ikke kan have overlappende regler, der er aktive på samme tid i en enkelt indkøbspolitik.</span><span class="sxs-lookup"><span data-stu-id="c8673-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

