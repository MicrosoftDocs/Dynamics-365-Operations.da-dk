---
title: Tildele brugere til sikkerhedsroller
description: Brugerne skal være tildelt sikkerhedsroller for at få adgang til Microsoft Dynamics 365 for Finance and Operations Enterprise edition.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851353"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="0b51d-103">Tildele brugere til sikkerhedsroller</span><span class="sxs-lookup"><span data-stu-id="0b51d-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b51d-104">Brugerne skal være tildelt sikkerhedsroller for at få adgang til Microsoft Dynamics 365 for Finance and Operations Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="0b51d-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="0b51d-105">Denne procedure forklarer, hvordan systemadministratorer kan tildele roller automatisk til brugerne ud fra forretningsdataene.</span><span class="sxs-lookup"><span data-stu-id="0b51d-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="0b51d-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="0b51d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="0b51d-107">Tildele brugere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="0b51d-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="0b51d-108">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="0b51d-109">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b51d-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0b51d-110">Vælg den rolle, du vil konfigurere reglen for.</span><span class="sxs-lookup"><span data-stu-id="0b51d-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="0b51d-111">Vælg Regnskabsansvarlig i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0b51d-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="0b51d-112">Klik på **Tilføj regel** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0b51d-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="0b51d-113">Find og vælg den ønskede post på listen **Vælg en forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="0b51d-114">Vælg den forespørgsel, du vil bruge for denne regel.</span><span class="sxs-lookup"><span data-stu-id="0b51d-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="0b51d-115">Klik på linket i den valgte række på listen **Navn på medlemskabsregel**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0b51d-116">Klik på **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-116">Click **Edit query**.</span></span> <span data-ttu-id="0b51d-117">Rediger forespørgslen efter behov.</span><span class="sxs-lookup"><span data-stu-id="0b51d-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="0b51d-118">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="0b51d-119">Udelukke brugere fra automatisk rolletildeling</span><span class="sxs-lookup"><span data-stu-id="0b51d-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="0b51d-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0b51d-120">Close the page.</span></span>
2. <span data-ttu-id="0b51d-121">Gå til **Navigationsrude > Moduler > Systemadministration > Sikkerhed > Tildel brugere roller**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="0b51d-122">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="0b51d-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0b51d-123">Vælg en rolle.</span><span class="sxs-lookup"><span data-stu-id="0b51d-123">Select a role.</span></span> <span data-ttu-id="0b51d-124">Vælg Regnskabsansvarlig for dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="0b51d-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="0b51d-125">Vælg **Tildel brugere roller/udeluk brugere fra roller manuelt** i menuen **Brugere, der er tildelt til rollen**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="0b51d-126">Markér den valgte række på listen **Tildel en rolle til brugere, eller udeluk brugere fra rollen**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="0b51d-127">Vælg en bruger.</span><span class="sxs-lookup"><span data-stu-id="0b51d-127">Select a user.</span></span>  
6. <span data-ttu-id="0b51d-128">Vælg **Udeluk fra rolle** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="0b51d-129">Klik på **Udeluk fra rolle** for at udelukke de valgte brugere fra rollen.</span><span class="sxs-lookup"><span data-stu-id="0b51d-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="0b51d-130">Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på **Nulstil status**.</span><span class="sxs-lookup"><span data-stu-id="0b51d-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="0b51d-131">Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk.</span><span class="sxs-lookup"><span data-stu-id="0b51d-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="0b51d-132">Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen.</span><span class="sxs-lookup"><span data-stu-id="0b51d-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="0b51d-133">I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.</span><span class="sxs-lookup"><span data-stu-id="0b51d-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
