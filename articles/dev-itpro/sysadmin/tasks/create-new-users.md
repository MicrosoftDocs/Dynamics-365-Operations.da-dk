--- 
title: Oprette nye brugere
description: "Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 295c355286b3d2df39cf1144ba7bfecdca25f9cb
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="create-new-users"></a><span data-ttu-id="adfd5-103">Oprette nye brugere</span><span class="sxs-lookup"><span data-stu-id="adfd5-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="adfd5-104">Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.</span><span class="sxs-lookup"><span data-stu-id="adfd5-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="adfd5-105">Systemadministratorer kan udføre denne procedure for at føje brugere til systemet.</span><span class="sxs-lookup"><span data-stu-id="adfd5-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="adfd5-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="adfd5-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="adfd5-107">Tilføje en ny bruger</span><span class="sxs-lookup"><span data-stu-id="adfd5-107">Add a new user</span></span>
1. <span data-ttu-id="adfd5-108">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="adfd5-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="adfd5-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="adfd5-109">Click New.</span></span>
3. <span data-ttu-id="adfd5-110">Indtast en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="adfd5-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="adfd5-111">Angiv entydig identifikation for brugeren.</span><span class="sxs-lookup"><span data-stu-id="adfd5-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="adfd5-112">Du skal angive et bruger-id.</span><span class="sxs-lookup"><span data-stu-id="adfd5-112">A user ID is required.</span></span>  
4. <span data-ttu-id="adfd5-113">Indtast en værdi i feltet Brugernavn.</span><span class="sxs-lookup"><span data-stu-id="adfd5-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="adfd5-114">Angiv brugerens navn.</span><span class="sxs-lookup"><span data-stu-id="adfd5-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="adfd5-115">Indtast en værdi i feltet Domæne.</span><span class="sxs-lookup"><span data-stu-id="adfd5-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="adfd5-116">Angiv brugerens domæne.</span><span class="sxs-lookup"><span data-stu-id="adfd5-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="adfd5-117">Indtast en værdi i feltet Alias.</span><span class="sxs-lookup"><span data-stu-id="adfd5-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="adfd5-118">Angiv brugerens alias.</span><span class="sxs-lookup"><span data-stu-id="adfd5-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="adfd5-119">Klik på rullelisten i feltet Firma for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="adfd5-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="adfd5-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="adfd5-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="adfd5-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="adfd5-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="adfd5-122">Vælg brugerens firma.</span><span class="sxs-lookup"><span data-stu-id="adfd5-122">Select the user's company</span></span>  
10. <span data-ttu-id="adfd5-123">Klik på Tildel roller.</span><span class="sxs-lookup"><span data-stu-id="adfd5-123">Click Assign roles.</span></span>
11. <span data-ttu-id="adfd5-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="adfd5-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="adfd5-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="adfd5-125">Click OK.</span></span>
13. <span data-ttu-id="adfd5-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="adfd5-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="adfd5-127">Importér brugere</span><span class="sxs-lookup"><span data-stu-id="adfd5-127">Import users</span></span>
1. <span data-ttu-id="adfd5-128">Klik på Importér brugere.</span><span class="sxs-lookup"><span data-stu-id="adfd5-128">Click Import users.</span></span>
2. <span data-ttu-id="adfd5-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="adfd5-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="adfd5-130">Klik på Importér brugere.</span><span class="sxs-lookup"><span data-stu-id="adfd5-130">Click Import users.</span></span>
4. <span data-ttu-id="adfd5-131">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="adfd5-131">Click Close.</span></span>


