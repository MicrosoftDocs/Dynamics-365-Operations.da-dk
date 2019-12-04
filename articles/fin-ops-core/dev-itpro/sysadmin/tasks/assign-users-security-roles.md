---
title: Tildele brugere til sikkerhedsroller
description: For at få adgang til Finance and Operations-apps skal brugerne være tildelt sikkerhedsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807990"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="d2dfa-103">Tildele brugere til sikkerhedsroller</span><span class="sxs-lookup"><span data-stu-id="d2dfa-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2dfa-104">Brugerne skal være tildelt sikkerhedsroller for at kunne bruge andet end almindelige egenskaber.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="d2dfa-105">Denne procedure forklarer, hvordan systemadministratorer automatisk kan tildele roller til brugerne ud fra forretningsdataene.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="d2dfa-106">Tildele brugere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="d2dfa-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="d2dfa-107">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="d2dfa-108">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d2dfa-109">Vælg den rolle, du vil konfigurere reglen for.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="d2dfa-110">Vælg Regnskabsansvarlig i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="d2dfa-111">Klik på **Tilføj regel** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="d2dfa-112">Find og vælg den ønskede post på listen **Vælg en forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="d2dfa-113">Vælg den forespørgsel, du vil bruge for denne regel.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="d2dfa-114">Klik på linket i den valgte række på listen **Navn på medlemskabsregel**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d2dfa-115">Klik på **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-115">Click **Edit query**.</span></span> <span data-ttu-id="d2dfa-116">Rediger forespørgslen efter behov.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="d2dfa-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-117">Click **OK**.</span></span>
8. <span data-ttu-id="d2dfa-118">Klik på **Kør automatisk rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="d2dfa-119">Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere** (helst i en separat fane i browseren).</span><span class="sxs-lookup"><span data-stu-id="d2dfa-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="d2dfa-120">Gennemse de roller, der er tildelt de forskellige brugere, for at bekræfte, at forespørgslen om rolletildeling er korrekt.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="d2dfa-121">Tilpas, og kør den igen, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="d2dfa-122">Udelukke brugere fra automatisk rolletildeling</span><span class="sxs-lookup"><span data-stu-id="d2dfa-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="d2dfa-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-123">Close the page.</span></span>
2. <span data-ttu-id="d2dfa-124">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="d2dfa-125">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="d2dfa-126">Vælg en rolle.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-126">Select a role.</span></span> <span data-ttu-id="d2dfa-127">Vælg Regnskabsansvarlig for dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="d2dfa-128">Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="d2dfa-129">Markér den valgte række på listen **Tildel en rolle til brugere, eller udeluk brugere fra rollen**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="d2dfa-130">Vælg en bruger.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-130">Select a user.</span></span>  
6. <span data-ttu-id="d2dfa-131">Vælg **Udeluk fra rolle** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="d2dfa-132">Klik på **Udeluk fra rolle** for at udelukke de valgte brugere fra rollen.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="d2dfa-133">Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på **Nulstil status**.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="d2dfa-134">Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="d2dfa-135">Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="d2dfa-136">I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.</span><span class="sxs-lookup"><span data-stu-id="d2dfa-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
