---
title: Kontostyringssider og -moduler
description: Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885803"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="74f1e-103">Kontostyringssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="74f1e-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="74f1e-104">Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74f1e-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74f1e-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="74f1e-105">Overview</span></span>

<span data-ttu-id="74f1e-106">Kontostyring henviser til en gruppe sider, der bruges til at administrere brugerkontorelaterede oplysninger i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74f1e-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="74f1e-107">Kontostyringssider omfatter landingssiden til kontostyring, brugerprofilside, brugeradresseside, ordrehistorikside, ordreoplysningside, fordelskundeside og ønskelisteside.</span><span class="sxs-lookup"><span data-stu-id="74f1e-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="74f1e-108">Landingsside for kontostyring</span><span class="sxs-lookup"><span data-stu-id="74f1e-108">Account management landing page</span></span>

<span data-ttu-id="74f1e-109">Landingssiden til kontostyring bruger følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="74f1e-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="74f1e-110">**Indholdsplacering** – dette modul er et containermodul, der indeholder alle modulerne på landingssiden til kontostyring.</span><span class="sxs-lookup"><span data-stu-id="74f1e-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="74f1e-111">**Velkomstelement for konto** – dette modul bruges til at angive en velkomstmeddelelse på kontostyringssiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="74f1e-112">Det indeholder egenskaber for overskriften og feltstørrelsen.</span><span class="sxs-lookup"><span data-stu-id="74f1e-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="74f1e-113">Egenskaben **Feltstørrelse** definerer bredden af modulet i indholdsplaceringsmodulet.</span><span class="sxs-lookup"><span data-stu-id="74f1e-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="74f1e-114">Værdierne går fra **1** til **12**, hvor **12** repræsenterer den fulde bredde på containeren til indholdsplacering.</span><span class="sxs-lookup"><span data-stu-id="74f1e-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="74f1e-115">**Ordreafgivelseselement for konto** – dette modul bruges til at angive en oversigt over antallet af ordrer, der er afgivet af brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="74f1e-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="74f1e-116">Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="74f1e-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="74f1e-117">Linket "vis detaljer" skal konfigureres, så der omdirigeres til ordrehistoriksiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="74f1e-118">**Profilplaceringselement for konto** – dette modul bruges til at angive en oversigt over brugerprofilen.</span><span class="sxs-lookup"><span data-stu-id="74f1e-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="74f1e-119">Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="74f1e-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="74f1e-120">Linket "vis detaljer" skal konfigureres, så der omdirigeres til brugerprofilsiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="74f1e-121">**Ønskelisteelement for konto** – dette modul bruges til at angive en oversigt over varerne på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="74f1e-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="74f1e-122">Det kan f. eks. angive, at "Du har 10 varer på din ønskeliste".</span><span class="sxs-lookup"><span data-stu-id="74f1e-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="74f1e-123">Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="74f1e-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="74f1e-124">Linket "vis detaljer" skal konfigureres, så der omdirigeres til ønskelistesiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="74f1e-125">**Adresseelement for konto** – dette modul bruges til at angive en oversigt over brugerens adresser.</span><span class="sxs-lookup"><span data-stu-id="74f1e-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="74f1e-126">Det kan f. eks. angive, at "Du har føjet 2 adresser til din konto".</span><span class="sxs-lookup"><span data-stu-id="74f1e-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="74f1e-127">Det indeholder egenskaber for overskriften, feltstørrelsen og linket "vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="74f1e-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="74f1e-128">Linket "vis detaljer" skal konfigureres, så der omdirigeres til brugeradressesiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="74f1e-129">**Fordelskundeelement for konto** – dette modul bruges til at få vist og indsætte et link til oplysninger om fordelskundeprogrammet.</span><span class="sxs-lookup"><span data-stu-id="74f1e-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="74f1e-130">Det indeholder egenskaber for overskriften, feltstørrelsen, linket "vis detaljer" samt linket "bliv medlem".</span><span class="sxs-lookup"><span data-stu-id="74f1e-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="74f1e-131">Linket "vis detaljer" skal konfigureres, så der omdirigeres til fordelskundesiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="74f1e-132">Linket "bliv medlem" skal konfigureres, så det omdirigeres til en side, hvor brugerne kan komme med i fordelskundeprogrammet.</span><span class="sxs-lookup"><span data-stu-id="74f1e-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="74f1e-133">Ordrehistorikside</span><span class="sxs-lookup"><span data-stu-id="74f1e-133">Order history page</span></span>

<span data-ttu-id="74f1e-134">På ordrehistoriksiden bruges modulet for ordrehistorik til at vise alle de seneste ordrer, som brugeren har afgivet.</span><span class="sxs-lookup"><span data-stu-id="74f1e-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="74f1e-135">Ordredetaljeside</span><span class="sxs-lookup"><span data-stu-id="74f1e-135">Order details page</span></span>

<span data-ttu-id="74f1e-136">På ordredetaljesiden vises der detaljerede oplysninger om hver enkelt ordre, og du kan få adgang til den fra ordrehistoriksiden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="74f1e-137">Den bruger ordredetaljemodulet, som kræver salgs-id'et eller transaktions-id'et for at kunne hente ordreoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="74f1e-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="74f1e-138">Brugerprofilside</span><span class="sxs-lookup"><span data-stu-id="74f1e-138">User profile page</span></span>

<span data-ttu-id="74f1e-139">På brugerprofilsiden forevises detaljer om brugerkonti, f.eks. en brugers navn og mailadresse.</span><span class="sxs-lookup"><span data-stu-id="74f1e-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="74f1e-140">Den bruger brugerprofilmodulet.</span><span class="sxs-lookup"><span data-stu-id="74f1e-140">It uses the user profile module.</span></span> <span data-ttu-id="74f1e-141">Mailadressen kan ikke fjernes, men den kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="74f1e-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="74f1e-142">Brugerprofilsiden viser også brugerpræferencer, der giver en bruger mulighed for at tilmelde sig eller fravælge visse funktioner såsom personalisering af anbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="74f1e-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="74f1e-143">Brugeradresseside</span><span class="sxs-lookup"><span data-stu-id="74f1e-143">User address page</span></span>

<span data-ttu-id="74f1e-144">På siden brugeradresse vises listen over de adresser, der er knyttet til brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="74f1e-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="74f1e-145">Brugeren har enten angivet disse adresser under betalingen eller tilføjet dem direkte på denne side.</span><span class="sxs-lookup"><span data-stu-id="74f1e-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="74f1e-146">Brugeradressemodulet bruges til at tilføje og redigere adresser, angive den primære adresse og gengive eksisterende adresser på siden.</span><span class="sxs-lookup"><span data-stu-id="74f1e-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="74f1e-147">Ønskelisteside</span><span class="sxs-lookup"><span data-stu-id="74f1e-147">Wish list page</span></span>

<span data-ttu-id="74f1e-148">På ønskelistesiden vises de varer, som er føjet til kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="74f1e-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="74f1e-149">Den bruger ønskelistemodulet ønske til at gengive ønskelisteelementer.</span><span class="sxs-lookup"><span data-stu-id="74f1e-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="74f1e-150">Side for fordelskunde</span><span class="sxs-lookup"><span data-stu-id="74f1e-150">Loyalty page</span></span>

<span data-ttu-id="74f1e-151">På fordelskundesiden kan kunderne blive medlem af et fordelskundeprogram eller, hvis de allerede er medlem af fordelskundeprogrammet, få vist oplysninger om deres program.</span><span class="sxs-lookup"><span data-stu-id="74f1e-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="74f1e-152">De kan også få vist de point, de har optjent og indløst i seneste transaktioner.</span><span class="sxs-lookup"><span data-stu-id="74f1e-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74f1e-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="74f1e-153">Additional resources</span></span>

[<span data-ttu-id="74f1e-154">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="74f1e-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="74f1e-155">Modulet Container</span><span class="sxs-lookup"><span data-stu-id="74f1e-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="74f1e-156">Købefeltmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="74f1e-157">Indkøbsvognmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="74f1e-158">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="74f1e-159">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="74f1e-160">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="74f1e-161">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="74f1e-161">Footer module</span></span>](author-footer-module.md)
