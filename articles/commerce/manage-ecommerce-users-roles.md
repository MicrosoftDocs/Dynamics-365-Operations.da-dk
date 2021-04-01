---
title: Administrere e-handelsbrugere og -roller
description: I dette emne beskrives, hvordan du giver brugere adgang til oprettelsesmiljøet for dit Microsoft Dynamics 365 Commerce-websted.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255913"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="30a4d-103">Administrere e-handelsbrugere og -roller</span><span class="sxs-lookup"><span data-stu-id="30a4d-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="30a4d-104">I dette emne beskrives, hvordan du giver brugere adgang til oprettelsesmiljøet for dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="30a4d-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="30a4d-105">Som en hjælp til at styre brugeradgang og tildele brugerrettigheder til at udføre bestemte opgaver, bruger miljøet til webstedsoprettelse sikkerhedsgrupper, som du opretter i Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="30a4d-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="30a4d-106">Du skal først tildele en ny eller eksisterende sikkerhedsgruppe fra Azure AD til hver rolle i oprettelsesmiljøet.</span><span class="sxs-lookup"><span data-stu-id="30a4d-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="30a4d-107">Derefter kan du tildele eller tilbagekalde individuelle brugeres rettigheder ved enten at føje disse brugere til en relevant sikkerhedsgruppe eller ved at fjerne dem fra en sikkerhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="30a4d-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="30a4d-108">Oversigt over roller i oprettelsesmiljøet</span><span class="sxs-lookup"><span data-stu-id="30a4d-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="30a4d-109">Dynamics 365 for Commerce-oprettelsesmiljøet understøtter følgende roller.</span><span class="sxs-lookup"><span data-stu-id="30a4d-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="30a4d-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="30a4d-110">Role</span></span>                 | <span data-ttu-id="30a4d-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="30a4d-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="30a4d-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="30a4d-112">System Administrator</span></span> | <span data-ttu-id="30a4d-113">Brugere, der har denne rolle, har alle rettigheder til alle værktøjer og til alle vurderinger og anmeldelser.</span><span class="sxs-lookup"><span data-stu-id="30a4d-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="30a4d-114">De kan også oprette websteder.</span><span class="sxs-lookup"><span data-stu-id="30a4d-114">They can also create sites.</span></span> |
| <span data-ttu-id="30a4d-115">Administrator</span><span class="sxs-lookup"><span data-stu-id="30a4d-115">Administrator</span></span>   | <span data-ttu-id="30a4d-116">Brugere, der har denne rolle, har alle rettigheder til alle værktøjer og RnR i en bestemt webstedsstruktur.</span><span class="sxs-lookup"><span data-stu-id="30a4d-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="30a4d-117">Webproducent</span><span class="sxs-lookup"><span data-stu-id="30a4d-117">Web Producer</span></span>         | <span data-ttu-id="30a4d-118">Brugere, der har denne rolle, kan oprette sider, fragmenter og skabeloner, overføre og administrere aktiver og forbedre produkter og kategorier.</span><span class="sxs-lookup"><span data-stu-id="30a4d-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="30a4d-119">Læser</span><span class="sxs-lookup"><span data-stu-id="30a4d-119">Reader</span></span>               | <span data-ttu-id="30a4d-120">Brugere, der har denne rolle, kan få vist sider, skabeloner, aktiver, fragmenter, layout og indstillinger, men kan muligvis ikke foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="30a4d-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="30a4d-121">RnR-redaktør</span><span class="sxs-lookup"><span data-stu-id="30a4d-121">RnR Moderator</span></span>        | <span data-ttu-id="30a4d-122">Brugere, der har denne rolle, kan moderere produktanmeldelser.</span><span class="sxs-lookup"><span data-stu-id="30a4d-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="30a4d-123">Systemadministratorrolle</span><span class="sxs-lookup"><span data-stu-id="30a4d-123">System Administrator role</span></span>

<span data-ttu-id="30a4d-124">Når du klargør Dynamics 365 Commerce i Microsoft Dynamics Lifecycle Services-miljøet (LCS), bliver du bedt om at angive en sikkerhedsgruppe for rollen **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="30a4d-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="30a4d-125">Denne rolle anvendes derefter automatisk på alle de websteder, du opretter i det miljø, du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="30a4d-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="30a4d-126">Sikkerhedsgruppen for denne rolle kan kun opdateres i LCS.</span><span class="sxs-lookup"><span data-stu-id="30a4d-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="30a4d-127">På siden **Webstedsadministration** for alle websteder vises den som skrivebeskyttet og er kun til orientering.</span><span class="sxs-lookup"><span data-stu-id="30a4d-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="30a4d-128">Administratorrolle</span><span class="sxs-lookup"><span data-stu-id="30a4d-128">Administrator role</span></span>

<span data-ttu-id="30a4d-129">Når du opretter et nyt websted i Commerce, bliver du bedt om at angive en sikkerhedsgruppe for **Administrator**-rollen.</span><span class="sxs-lookup"><span data-stu-id="30a4d-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="30a4d-130">Se tabellen tidligere i dette emne for at få en oversigt over de rettigheder, som denne rolle giver.</span><span class="sxs-lookup"><span data-stu-id="30a4d-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="30a4d-131">Tilføje eller opdatere sikkerhedsgrupper</span><span class="sxs-lookup"><span data-stu-id="30a4d-131">Add or update security groups</span></span>

<span data-ttu-id="30a4d-132">Når webstedet er oprettet, er det kun brugere, der er i sikkerhedsgrupper, som er tilknyttet rollerne **Systemadministrator** og **Administrator**, der har adgang til oprettelsesmiljøet for det pågældende websted.</span><span class="sxs-lookup"><span data-stu-id="30a4d-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="30a4d-133">Hvis du vil tildele brugere rollerne **Webproducent**, **RnR-redaktør** og **Læser**, skal du tildele sikkerhedsgrupper til disse roller.</span><span class="sxs-lookup"><span data-stu-id="30a4d-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="30a4d-134">Hvis du vil føje en sikkerhedsgruppe til en rolle eller opdatere en sikkerhedsgruppe, der aktuelt er tildelt en rolle, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="30a4d-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="30a4d-135">Gå til det websted, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="30a4d-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="30a4d-136">Åbn siden **Sikkerhed** i **Administration af websted**.</span><span class="sxs-lookup"><span data-stu-id="30a4d-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="30a4d-137">Vælg den rolle, der skal redigeres.</span><span class="sxs-lookup"><span data-stu-id="30a4d-137">Select the role to modify.</span></span>
1. <span data-ttu-id="30a4d-138">Føj sikkerhedsgrupper til roller, eller fjern sikkerhedsgrupper fra roller.</span><span class="sxs-lookup"><span data-stu-id="30a4d-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30a4d-139">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="30a4d-139">Additional resources</span></span>

[<span data-ttu-id="30a4d-140">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="30a4d-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="30a4d-141">Overvejelser om optimering af søgeprogram (SEO) for webstedet</span><span class="sxs-lookup"><span data-stu-id="30a4d-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="30a4d-142">Administrere sikkerhedspolitik for indhold (CSP)</span><span class="sxs-lookup"><span data-stu-id="30a4d-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]