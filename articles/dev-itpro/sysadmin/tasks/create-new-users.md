---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "361952"
---
# <a name="create-new-users"></a><span data-ttu-id="c113a-103">Oprette nye brugere</span><span class="sxs-lookup"><span data-stu-id="c113a-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c113a-104">Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.</span><span class="sxs-lookup"><span data-stu-id="c113a-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="c113a-105">Systemadministratorer kan udføre denne procedure for at føje brugere til systemet.</span><span class="sxs-lookup"><span data-stu-id="c113a-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="c113a-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="c113a-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="c113a-107">Tilføje en ny bruger</span><span class="sxs-lookup"><span data-stu-id="c113a-107">Add a new user</span></span>
1. <span data-ttu-id="c113a-108">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="c113a-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="c113a-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c113a-109">Click New.</span></span>
3. <span data-ttu-id="c113a-110">Indtast en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="c113a-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="c113a-111">Angiv entydig identifikation for brugeren.</span><span class="sxs-lookup"><span data-stu-id="c113a-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="c113a-112">Du skal angive et bruger-id.</span><span class="sxs-lookup"><span data-stu-id="c113a-112">A user ID is required.</span></span>  
4. <span data-ttu-id="c113a-113">Indtast en værdi i feltet Brugernavn.</span><span class="sxs-lookup"><span data-stu-id="c113a-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="c113a-114">Angiv brugerens navn.</span><span class="sxs-lookup"><span data-stu-id="c113a-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="c113a-115">Indtast en værdi i feltet Domæne.</span><span class="sxs-lookup"><span data-stu-id="c113a-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="c113a-116">Angiv brugerens domæne.</span><span class="sxs-lookup"><span data-stu-id="c113a-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="c113a-117">Indtast en værdi i feltet Alias.</span><span class="sxs-lookup"><span data-stu-id="c113a-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="c113a-118">Angiv brugerens alias.</span><span class="sxs-lookup"><span data-stu-id="c113a-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="c113a-119">Klik på rullelisten i feltet Firma for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="c113a-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c113a-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c113a-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c113a-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c113a-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c113a-122">Vælg brugerens firma.</span><span class="sxs-lookup"><span data-stu-id="c113a-122">Select the user's company</span></span>  
10. <span data-ttu-id="c113a-123">Klik på Tildel roller.</span><span class="sxs-lookup"><span data-stu-id="c113a-123">Click Assign roles.</span></span>
11. <span data-ttu-id="c113a-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="c113a-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c113a-125">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c113a-125">Click OK.</span></span>
13. <span data-ttu-id="c113a-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c113a-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="c113a-127">Importér brugere</span><span class="sxs-lookup"><span data-stu-id="c113a-127">Import users</span></span>
1. <span data-ttu-id="c113a-128">Klik på Importér brugere.</span><span class="sxs-lookup"><span data-stu-id="c113a-128">Click Import users.</span></span>
2. <span data-ttu-id="c113a-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c113a-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c113a-130">Klik på Importér brugere.</span><span class="sxs-lookup"><span data-stu-id="c113a-130">Click Import users.</span></span>
4. <span data-ttu-id="c113a-131">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="c113a-131">Click Close.</span></span>

