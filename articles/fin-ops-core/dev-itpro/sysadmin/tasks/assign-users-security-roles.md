---
title: Tildele brugere til sikkerhedsroller
description: For at få adgang til Finance and Operations-apps skal brugerne være tildelt sikkerhedsroller.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180961"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="3be85-103">Tildele brugere til sikkerhedsroller</span><span class="sxs-lookup"><span data-stu-id="3be85-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3be85-104">Brugerne skal være tildelt sikkerhedsroller for at kunne bruge andet end almindelige egenskaber.</span><span class="sxs-lookup"><span data-stu-id="3be85-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="3be85-105">Denne procedure forklarer, hvordan systemadministratorer automatisk kan tildele roller til brugerne ud fra forretningsdataene.</span><span class="sxs-lookup"><span data-stu-id="3be85-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="3be85-106">Tildele brugere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="3be85-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="3be85-107">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="3be85-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="3be85-108">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="3be85-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="3be85-109">Vælg den rolle, du vil konfigurere reglen for.</span><span class="sxs-lookup"><span data-stu-id="3be85-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="3be85-110">Vælg Regnskabsansvarlig i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="3be85-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="3be85-111">Klik på **Tilføj regel** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3be85-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="3be85-112">Find og vælg den ønskede post på listen **Vælg en forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="3be85-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="3be85-113">Vælg den forespørgsel, du vil bruge for denne regel.</span><span class="sxs-lookup"><span data-stu-id="3be85-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="3be85-114">Klik på linket i den valgte række på listen **Navn på medlemskabsregel**.</span><span class="sxs-lookup"><span data-stu-id="3be85-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3be85-115">Klik på **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="3be85-115">Click **Edit query**.</span></span> <span data-ttu-id="3be85-116">Rediger forespørgslen efter behov.</span><span class="sxs-lookup"><span data-stu-id="3be85-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="3be85-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="3be85-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="3be85-118">Udelukke brugere fra automatisk rolletildeling</span><span class="sxs-lookup"><span data-stu-id="3be85-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="3be85-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3be85-119">Close the page.</span></span>
2. <span data-ttu-id="3be85-120">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="3be85-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="3be85-121">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="3be85-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="3be85-122">Vælg en rolle.</span><span class="sxs-lookup"><span data-stu-id="3be85-122">Select a role.</span></span> <span data-ttu-id="3be85-123">Vælg Regnskabsansvarlig for dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="3be85-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="3be85-124">Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.</span><span class="sxs-lookup"><span data-stu-id="3be85-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="3be85-125">Markér den valgte række på listen **Tildel en rolle til brugere, eller udeluk brugere fra rollen**.</span><span class="sxs-lookup"><span data-stu-id="3be85-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="3be85-126">Vælg en bruger.</span><span class="sxs-lookup"><span data-stu-id="3be85-126">Select a user.</span></span>  
6. <span data-ttu-id="3be85-127">Vælg **Udeluk fra rolle** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="3be85-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="3be85-128">Klik på **Udeluk fra rolle** for at udelukke de valgte brugere fra rollen.</span><span class="sxs-lookup"><span data-stu-id="3be85-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="3be85-129">Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på **Nulstil status**.</span><span class="sxs-lookup"><span data-stu-id="3be85-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="3be85-130">Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk.</span><span class="sxs-lookup"><span data-stu-id="3be85-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="3be85-131">Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen.</span><span class="sxs-lookup"><span data-stu-id="3be85-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="3be85-132">I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.</span><span class="sxs-lookup"><span data-stu-id="3be85-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
