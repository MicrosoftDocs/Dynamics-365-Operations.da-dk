---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570515"
---
# <a name="create-new-users"></a><span data-ttu-id="2d7ba-103">Oprette nye brugere</span><span class="sxs-lookup"><span data-stu-id="2d7ba-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d7ba-104">Brugerne er interne medarbejdere i din organisation eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="2d7ba-105">Tilknyt en bruger til en licens (kun nye licenstyper)</span><span class="sxs-lookup"><span data-stu-id="2d7ba-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="2d7ba-106">For kunder, der er medlem af en af de nye licenstyper, som er tilføjet i oktober 2019, skal brugere være tilknyttet en licens.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="2d7ba-107">Brugere, der er tilknyttet en licens, tilføjes automatisk som systembrugere, der ikke har nogen roller, første gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="2d7ba-108">Brugere, der ikke er knyttet til et licens, får vist en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="2d7ba-109">Systemadministratorer kan [tildele licenser til brugere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [Microsoft 365 Administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="2d7ba-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="2d7ba-110">Tilføje en ny bruger</span><span class="sxs-lookup"><span data-stu-id="2d7ba-110">Add a new user</span></span>
1. <span data-ttu-id="2d7ba-111">Gå til **Systemadministration \> Brugere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="2d7ba-112">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="2d7ba-113">Angiv et entydigt id for brugeren i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="2d7ba-114">Du skal angive et bruger-id.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-114">A user ID is required.</span></span>  
4. <span data-ttu-id="2d7ba-115">Angiv brugerens navn i feltet **Brugernavn**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="2d7ba-116">I feltet **Domæne** skal du angive brugerens domæne.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="2d7ba-117">Angiv brugerens alias i feltet **Alias**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="2d7ba-118">I feltet **Firma** skal du vælge det ønskede firma.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="2d7ba-119">I oversigtspanelet **Brugerens roller** skal du vælge **Tildel roller** for at [tildele brugere til sikkerhedsroller](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="2d7ba-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="2d7ba-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-120">Select **OK**.</span></span>
10. <span data-ttu-id="2d7ba-121">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="2d7ba-122">Importér brugere</span><span class="sxs-lookup"><span data-stu-id="2d7ba-122">Import users</span></span>
1. <span data-ttu-id="2d7ba-123">Vælg **Importer brugere** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="2d7ba-124">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2d7ba-125">Vælg **Importer brugere**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-125">Select **Import users**.</span></span>
4. <span data-ttu-id="2d7ba-126">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="2d7ba-126">Select **Close**.</span></span>

