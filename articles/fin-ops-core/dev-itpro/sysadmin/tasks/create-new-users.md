---
title: Oprette nye brugere
description: Brugerne er interne medarbejdere i din organisation, eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e84130ff2b1cf83b7d2b95eefc72175dc57743c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982496"
---
# <a name="create-new-users"></a><span data-ttu-id="f55f8-103">Oprette nye brugere</span><span class="sxs-lookup"><span data-stu-id="f55f8-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f55f8-104">Brugerne er interne medarbejdere i din organisation eller eksterne debitorer og kreditorer, der kræver adgang til systemet for at udføre deres job.</span><span class="sxs-lookup"><span data-stu-id="f55f8-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f55f8-105">Tilknyt en bruger til en licens (kun nye licenstyper)</span><span class="sxs-lookup"><span data-stu-id="f55f8-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="f55f8-106">For kunder, der er medlem af en af de nye licenstyper, som er tilføjet i oktober 2019, skal brugere være tilknyttet en licens.</span><span class="sxs-lookup"><span data-stu-id="f55f8-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="f55f8-107">Brugere, der er tilknyttet en licens, tilføjes automatisk som systembrugere, der ikke har nogen roller, første gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="f55f8-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="f55f8-108">Systemadministratorer kan [tildele licenser til brugere](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) i [Microsoft 365 Administration](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="f55f8-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f55f8-109">Tilknytte en ekstern bruger til en licens (kun nye licenstyper)</span><span class="sxs-lookup"><span data-stu-id="f55f8-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="f55f8-110">Brugere uden for den lejer, som miljøet blev implementeret i, skal repræsenteres i værtslejebiblioteket (Azure Active Directory (Azure AD)), så de kan tildeles licenser.</span><span class="sxs-lookup"><span data-stu-id="f55f8-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="f55f8-111">Disse eksterne brugere skal føjes til lejeren i Azure AD som gæstebrugere og derefter tildeles de relevante licenser.</span><span class="sxs-lookup"><span data-stu-id="f55f8-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="f55f8-112">Du kan finde flere oplysninger under [Tilføje Azure Active Directory B2B-samarbejdsbrugere i Azure-portalen](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="f55f8-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="f55f8-113">Tilføje en ny bruger</span><span class="sxs-lookup"><span data-stu-id="f55f8-113">Add a new user</span></span>
1. <span data-ttu-id="f55f8-114">Gå til **Systemadministration \> Brugere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f55f8-115">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f55f8-116">Angiv et entydigt id for brugeren i feltet **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="f55f8-117">Du skal angive et bruger-id.</span><span class="sxs-lookup"><span data-stu-id="f55f8-117">A user ID is required.</span></span>  
4. <span data-ttu-id="f55f8-118">Angiv brugerens navn i feltet **Brugernavn**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="f55f8-119">I feltet **Domæne** skal du angive brugerens domæne.</span><span class="sxs-lookup"><span data-stu-id="f55f8-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="f55f8-120">Angiv brugerens alias i feltet **Alias**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="f55f8-121">I feltet **Firma** skal du vælge det ønskede firma.</span><span class="sxs-lookup"><span data-stu-id="f55f8-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="f55f8-122">I oversigtspanelet **Brugerens roller** skal du vælge **Tildel roller** for at tildele brugere til sikkerhedsroller.</span><span class="sxs-lookup"><span data-stu-id="f55f8-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="f55f8-123">Du kan finde flere oplysninger under [Tildele brugere til sikkerhedsroller](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f55f8-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="f55f8-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-124">Select **OK**.</span></span>
10. <span data-ttu-id="f55f8-125">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="f55f8-126">Importér brugere</span><span class="sxs-lookup"><span data-stu-id="f55f8-126">Import users</span></span>
1. <span data-ttu-id="f55f8-127">Gå til **Systemadministration \> Brugere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f55f8-128">Vælg **Importer brugere** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="f55f8-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="f55f8-129">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f55f8-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f55f8-130">Vælg **Importer brugere**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-130">Select **Import users**.</span></span>
5. <span data-ttu-id="f55f8-131">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="f55f8-131">Select **Close**.</span></span>

