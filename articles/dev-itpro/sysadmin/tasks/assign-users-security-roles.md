--- 
title: Tildele brugere til sikkerhedsroller
description: "For at få adgang til Microsoft Dynamics 365 for Finance and Operations skal brugerne være tildelt sikkerhedsroller."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0ab51a56c33a84dea9cf945e808fa7bc42d3727c
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="c94db-103">Tildele brugere til sikkerhedsroller</span><span class="sxs-lookup"><span data-stu-id="c94db-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c94db-104">For at få adgang til Microsoft Dynamics 365 for Finance and Operations skal brugerne være tildelt sikkerhedsroller.</span><span class="sxs-lookup"><span data-stu-id="c94db-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="c94db-105">Denne procedure forklarer, hvordan systemadministratorer kan tildele roller automatisk til brugerne ud fra forretningsdataene.</span><span class="sxs-lookup"><span data-stu-id="c94db-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="c94db-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c94db-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="c94db-107">Tildele brugere automatisk til roller</span><span class="sxs-lookup"><span data-stu-id="c94db-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="c94db-108">Gå til Systemadministration > Sikkerhed > Tildel brugere roller.</span><span class="sxs-lookup"><span data-stu-id="c94db-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="c94db-109">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="c94db-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c94db-110">Vælg den rolle, du vil konfigurere reglen for.</span><span class="sxs-lookup"><span data-stu-id="c94db-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="c94db-111">Vælg Regnskabsansvarlig i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c94db-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="c94db-112">Klik på Tilføj regel for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c94db-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="c94db-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c94db-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c94db-114">Vælg den forespørgsel, du vil bruge for denne regel.</span><span class="sxs-lookup"><span data-stu-id="c94db-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="c94db-115">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c94db-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c94db-116">Klik på Rediger forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="c94db-116">Click Edit query.</span></span>
    * <span data-ttu-id="c94db-117">Rediger forespørgslen efter behov.</span><span class="sxs-lookup"><span data-stu-id="c94db-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="c94db-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c94db-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="c94db-119">Udelukke brugere fra automatisk rolletildeling</span><span class="sxs-lookup"><span data-stu-id="c94db-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="c94db-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c94db-120">Close the page.</span></span>
2. <span data-ttu-id="c94db-121">Gå til Systemadministration > Sikkerhed > Tildel brugere roller.</span><span class="sxs-lookup"><span data-stu-id="c94db-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="c94db-122">Vælg 'Regnskabsansvarlig' i træet.</span><span class="sxs-lookup"><span data-stu-id="c94db-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="c94db-123">Vælg en rolle.</span><span class="sxs-lookup"><span data-stu-id="c94db-123">Select a role.</span></span> <span data-ttu-id="c94db-124">Vælg Regnskabsansvarlig for dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="c94db-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="c94db-125">Klik på Tildel brugere roller/udeluk brugere fra roller manuelt.</span><span class="sxs-lookup"><span data-stu-id="c94db-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="c94db-126">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c94db-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c94db-127">Vælg en bruger.</span><span class="sxs-lookup"><span data-stu-id="c94db-127">Select a user.</span></span>  
6. <span data-ttu-id="c94db-128">Klik på Udeluk fra rolle.</span><span class="sxs-lookup"><span data-stu-id="c94db-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="c94db-129">Klik på Udeluk fra rolle for at udelukke de valgte brugere fra rollen.</span><span class="sxs-lookup"><span data-stu-id="c94db-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="c94db-130">Hvis du vil fjerne udelukkelser, skal du markere de brugere, hvor du vil fjerne udelukkelser, og derefter klikke på Nulstil status.</span><span class="sxs-lookup"><span data-stu-id="c94db-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="c94db-131">Når du fjerner en udelukkelse ved at nulstille brugerens status, tildeles brugerens rolle igen automatisk.</span><span class="sxs-lookup"><span data-stu-id="c94db-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="c94db-132">Brugeren bliver dog ikke tildelt eller udelukket fra rollen med det samme, når du nulstiller statussen.</span><span class="sxs-lookup"><span data-stu-id="c94db-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="c94db-133">I stedet bliver brugeren enten tildelt eller fjernet fra rollen, næste gang reglerne for automatisk rolletildeling bliver kørt.</span><span class="sxs-lookup"><span data-stu-id="c94db-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


