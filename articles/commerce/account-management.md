---
title: Kontostyringssider og -moduler
description: Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817152"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="b355b-103">Kontostyringssider og -moduler</span><span class="sxs-lookup"><span data-stu-id="b355b-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b355b-104">Dette emne omfatter sider og moduler til kontostyring i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b355b-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b355b-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b355b-105">Overview</span></span>

<span data-ttu-id="b355b-106">Kontostyring henviser til en gruppe sider, der bruges til at administrere brugerkontorelaterede oplysninger i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b355b-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b355b-107">Kontostyringssider omfatter landingssiden til kontostyring, brugerprofilside, brugeradresseside, ordrehistorikside, ordreoplysningside, fordelskundeside og ønskelisteside.</span><span class="sxs-lookup"><span data-stu-id="b355b-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="b355b-108">Landingsside for kontostyring</span><span class="sxs-lookup"><span data-stu-id="b355b-108">Account management landing page</span></span>

<span data-ttu-id="b355b-109">Landingssiden til kontostyring bruger følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="b355b-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="b355b-110">**Container** - Alle sidemoduler for kontoadministration skal placeres i en container.</span><span class="sxs-lookup"><span data-stu-id="b355b-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="b355b-111">**Velkomsttitel for konto** – Dette modul bruges til at angive en velkomstmeddelelse på kontostyringssiden.</span><span class="sxs-lookup"><span data-stu-id="b355b-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="b355b-112">Den indeholder egenskaber for overskriften.</span><span class="sxs-lookup"><span data-stu-id="b355b-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="b355b-113">**Generisk kontotitel** – Dette modul kan bruges til at angive overskrifter og links til kontostyringssider, f.eks. siderne "Ordreoversigt" eller "Min profil".</span><span class="sxs-lookup"><span data-stu-id="b355b-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="b355b-114">Det generiske flisemodul kan bruges til at konfigurere en flise for en side.</span><span class="sxs-lookup"><span data-stu-id="b355b-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="b355b-115">I Fabrikam bruges dette modul til sidelinkene "Ordreoversigt" og "Min profil" på siden til start af kontostyring.</span><span class="sxs-lookup"><span data-stu-id="b355b-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="b355b-116">**Ønskelisteflise for konto** – Dette modul bruges til at angive en oversigt over varerne på kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="b355b-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="b355b-117">Det kan f. eks. angive, at "Du har 10 varer på din ønskeliste".</span><span class="sxs-lookup"><span data-stu-id="b355b-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="b355b-118">Det indeholder egenskaber for overskriften og linket "Vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="b355b-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b355b-119">Linket "Vis detaljer" skal konfigureres, så der omdirigeres til ønskelistesiden.</span><span class="sxs-lookup"><span data-stu-id="b355b-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="b355b-120">**Adresseflise for konto** – Dette modul bruges til at angive en oversigt over brugerens adresser.</span><span class="sxs-lookup"><span data-stu-id="b355b-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="b355b-121">Det kan f. eks. angive, at "Du har føjet 2 adresser til din konto".</span><span class="sxs-lookup"><span data-stu-id="b355b-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="b355b-122">Det indeholder egenskaber for overskriften og linket "Vis detaljer".</span><span class="sxs-lookup"><span data-stu-id="b355b-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b355b-123">Linket "Vis detaljer" skal konfigureres, så der omdirigeres til brugeradressesiden.</span><span class="sxs-lookup"><span data-stu-id="b355b-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="b355b-124">**Fordelskundeflise for konto** – Dette modul bruges til at få vist og indsætte et link til oplysninger om fordelskundeprogrammet.</span><span class="sxs-lookup"><span data-stu-id="b355b-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="b355b-125">Dette felt indeholder to tilstande: en tilstand viser link til at deltage i et fordelskundeprogam, hvis brugeren ikke allerede er medlem.</span><span class="sxs-lookup"><span data-stu-id="b355b-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="b355b-126">I den anden tilstand vises links til visning af siden Fordelskundeoplysninger, når brugeren allerede er medlem.</span><span class="sxs-lookup"><span data-stu-id="b355b-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="b355b-127">Egenskaber omfatter overskriften, linket "Tilmeld" og linket "Vis fordelskunde".</span><span class="sxs-lookup"><span data-stu-id="b355b-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="b355b-128">Linket "Vis fordelskunde" skal konfigureres, så der omdirigeres til fordelskundesiden.</span><span class="sxs-lookup"><span data-stu-id="b355b-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="b355b-129">Linket "Tilmeld" skal konfigureres, så det omdirigeres til en side, hvor brugerne kan komme med i fordelskundeprogrammet.</span><span class="sxs-lookup"><span data-stu-id="b355b-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="b355b-130">Ordrehistorikside</span><span class="sxs-lookup"><span data-stu-id="b355b-130">Order history page</span></span>

<span data-ttu-id="b355b-131">På ordrehistoriksiden bruges modulet for ordrehistorik til at vise alle de seneste ordrer, som brugeren har afgivet.</span><span class="sxs-lookup"><span data-stu-id="b355b-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="b355b-132">Ordredetaljeside</span><span class="sxs-lookup"><span data-stu-id="b355b-132">Order details page</span></span>

<span data-ttu-id="b355b-133">På ordredetaljesiden vises der detaljerede oplysninger om hver enkelt ordre, og du kan få adgang til den fra ordrehistoriksiden.</span><span class="sxs-lookup"><span data-stu-id="b355b-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="b355b-134">Den bruger ordredetaljemodulet, som kræver salgs-id'et eller transaktions-id'et for at kunne hente ordreoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="b355b-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="b355b-135">Brugerprofilside</span><span class="sxs-lookup"><span data-stu-id="b355b-135">User profile page</span></span>

<span data-ttu-id="b355b-136">På brugerprofilsiden forevises detaljer om brugerkonti, f.eks. en brugers navn og mailadresse.</span><span class="sxs-lookup"><span data-stu-id="b355b-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="b355b-137">Den bruger brugerprofilen og redigeringsmodulerne til brugerprofiler.</span><span class="sxs-lookup"><span data-stu-id="b355b-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="b355b-138">Mailadressen kan ikke fjernes, men den kan redigeres.</span><span class="sxs-lookup"><span data-stu-id="b355b-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="b355b-139">Brugerprofilsiden viser også brugerpræferencer, der giver en bruger mulighed for at tilmelde sig eller fravælge visse funktioner som f.eks. personalisering af anbefalingslister.</span><span class="sxs-lookup"><span data-stu-id="b355b-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="b355b-140">Brugeradresseside</span><span class="sxs-lookup"><span data-stu-id="b355b-140">User address page</span></span>

<span data-ttu-id="b355b-141">På siden brugeradresse vises listen over de adresser, der er knyttet til brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="b355b-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="b355b-142">Brugeren har enten angivet disse adresser under betalingen eller tilføjet dem direkte på denne side.</span><span class="sxs-lookup"><span data-stu-id="b355b-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="b355b-143">Brugeradressemodulet bruges til at tilføje og redigere adresser, angive den primære adresse og gengive eksisterende adresser på siden.</span><span class="sxs-lookup"><span data-stu-id="b355b-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="b355b-144">Ønskelisteside</span><span class="sxs-lookup"><span data-stu-id="b355b-144">Wish list page</span></span>

<span data-ttu-id="b355b-145">På ønskelistesiden vises de varer, som er føjet til kundens ønskeliste.</span><span class="sxs-lookup"><span data-stu-id="b355b-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="b355b-146">Den bruger ønskelistemodulet ønske til at gengive ønskelisteelementer.</span><span class="sxs-lookup"><span data-stu-id="b355b-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="b355b-147">Side for fordelskunde</span><span class="sxs-lookup"><span data-stu-id="b355b-147">Loyalty page</span></span>

<span data-ttu-id="b355b-148">På fordelskundesiden kan kunderne få vist deres fordelskundedetaljer, hvis de allerede er medlem af fordelskundeprogrammet.</span><span class="sxs-lookup"><span data-stu-id="b355b-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="b355b-149">De kan også få vist de point, de har optjent og indløst i seneste transaktioner.</span><span class="sxs-lookup"><span data-stu-id="b355b-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="b355b-150">På denne side bruges modulet fordelskundeoplysninger til at vise fordelskundeoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="b355b-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="b355b-151">Hvis du vil deltage i fordelskundesprogrammet, kan der oprettes en marketingside med modulerne til fordelskundetilmelding og fordelskundebetingelserne.</span><span class="sxs-lookup"><span data-stu-id="b355b-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="b355b-152">Hvis brugeren ikke er medlem af et fordelskundeprogram, vil disse moduler give brugeren mulighed for at tilmelde sig.</span><span class="sxs-lookup"><span data-stu-id="b355b-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b355b-153">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b355b-153">Additional resources</span></span>

[<span data-ttu-id="b355b-154">Oversigt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="b355b-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b355b-155">Container-modul</span><span class="sxs-lookup"><span data-stu-id="b355b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b355b-156">Boksmodul til køb</span><span class="sxs-lookup"><span data-stu-id="b355b-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b355b-157">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="b355b-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b355b-158">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="b355b-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b355b-159">Ordrebekræftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="b355b-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b355b-160">Sidehovedmodul</span><span class="sxs-lookup"><span data-stu-id="b355b-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b355b-161">Sidefodsmodul</span><span class="sxs-lookup"><span data-stu-id="b355b-161">Footer module</span></span>](author-footer-module.md)
