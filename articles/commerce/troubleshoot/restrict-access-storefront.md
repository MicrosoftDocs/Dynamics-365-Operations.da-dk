---
title: Begrænse adgangen til en butikspromenade under test eller udvikling
description: Dette emne indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018332"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="e0486-103">Begrænse adgangen til en butikspromenade under test eller udvikling</span><span class="sxs-lookup"><span data-stu-id="e0486-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0486-104">Dette emne indeholder en forklaring på, hvordan du kan begrænse adgangen til en Microsoft Dynamics 365 Commerce-butikspromenade, mens der udføres intern test eller udvikling.</span><span class="sxs-lookup"><span data-stu-id="e0486-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="e0486-105">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="e0486-105">Description</span></span>

<span data-ttu-id="e0486-106">Under interne test eller aktive udvikling kan du begrænse adgangen til dit websted for at forhindre, at eksterne brugere åbner de publicerede butikspromenadesider.</span><span class="sxs-lookup"><span data-stu-id="e0486-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="e0486-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="e0486-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="e0486-108">Oprette Azure AD B2C ved hjælp af standardbrugerflow</span><span class="sxs-lookup"><span data-stu-id="e0486-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="e0486-109">Du kan finde flere oplysninger om, hvordan du konfigurerer Azure Active Directory B2C (Azure AD B2C) til dit e-handelswebsted, i [Oprette en B2C-lejer i Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="e0486-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="e0486-110">Begrænse brugeradgang til butikspromenadesider og blokere oprettelsen af nye brugere</span><span class="sxs-lookup"><span data-stu-id="e0486-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="e0486-111">Hvis du vil begrænse brugeradgang til butikspromenadesider i Commerce Site Builder, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e0486-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e0486-112">Gå til dit websted.</span><span class="sxs-lookup"><span data-stu-id="e0486-112">Go to your site.</span></span>
1. <span data-ttu-id="e0486-113">Vælg **Sider**, og vælg derefter den side, der skal begrænses brugeradgang for.</span><span class="sxs-lookup"><span data-stu-id="e0486-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="e0486-114">Vælg modulet eller fragmentplads, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e0486-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="e0486-115">Vælg **Kræver logon?** i egenskabsruden, og vælg derefter **Udfør redigering**.</span><span class="sxs-lookup"><span data-stu-id="e0486-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e0486-116">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e0486-116">Select **Publish**.</span></span>

<span data-ttu-id="e0486-117">Hvis du vil spærre for oprettelse af nye brugere i Azure AD, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="e0486-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="e0486-118">Gå til [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e0486-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="e0486-119">Vælg det Azure AD B2C-program, du har oprettet til adgangen til dit websted.</span><span class="sxs-lookup"><span data-stu-id="e0486-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="e0486-120">Vælg **Brugerflows** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="e0486-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="e0486-121">Vælg **Brugerflows** øverst på siden og vælg **Nyt brugerflow**.</span><span class="sxs-lookup"><span data-stu-id="e0486-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="e0486-122">Vælg **Forhåndsvisning** på siden **Vælg en brugerflowtype**.</span><span class="sxs-lookup"><span data-stu-id="e0486-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="e0486-123">Midt på siden skal du vælge **log på v2**.</span><span class="sxs-lookup"><span data-stu-id="e0486-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="e0486-124">Følg derefter trinnene i [Opsætning af en B2C-lejer i Commerce](../set-up-b2c-tenant.md) for at konfigurere flowet som webstedets standardbrugerflow for Azure AD B2C under test eller udvikling.</span><span class="sxs-lookup"><span data-stu-id="e0486-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0486-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e0486-125">Additional resources</span></span>

[<span data-ttu-id="e0486-126">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="e0486-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="e0486-127">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="e0486-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
