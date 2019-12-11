---
title: Oversigt over sider til indkøbsvogn og betaling ved kassen
description: Dette emne indeholder en oversigt over sider til indkøbsvogn og betaling ved kassen i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 347db3af36521e11dc70d5188dcc54b07efa1fbe
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697836"
---
# <a name="overview-of-cart-and-checkout-pages"></a><span data-ttu-id="dbf03-103">Oversigt over sider til indkøbsvogn og betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="dbf03-103">Overview of cart and checkout pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dbf03-104">Dette emne indeholder en oversigt over sider til indkøbsvogn og betaling ved kassen i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbf03-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbf03-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="dbf03-105">Overview</span></span>

<span data-ttu-id="dbf03-106">På indkøbsvognssiden på et e-handels-websted vises alle de varer, som en kunde har lagt i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="dbf03-107">Siden med indkøbsvognen opbygges ved hjælp af indkøbsvognsmodulet.</span><span class="sxs-lookup"><span data-stu-id="dbf03-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="dbf03-108">Indkøbsvognsmodulet er en container, der agerer vært for alle de moduler, der kræves for at fremvise varerne i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="dbf03-109">Modulet til indkøbsvognen kan også bruge andre moduler til at vise ordreoversigten og eventuelle kampagnekoder, der er anvendt på kundeordren.</span><span class="sxs-lookup"><span data-stu-id="dbf03-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="dbf03-110">Betalingssiden på et e-handels-websted indeholder en trinvis proces, som kunderne følger for at angive alle de oplysninger, der kræves for at afgive en ordre.</span><span class="sxs-lookup"><span data-stu-id="dbf03-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="dbf03-111">Et betalingsmodul kan omfatte moduler, der håndterer leveringsadressen, leveringsmetoderne, faktureringsoplysningerne, ordreoversigten og andre oplysninger, der er relateret til kundeordrer.</span><span class="sxs-lookup"><span data-stu-id="dbf03-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="dbf03-112">Siden med indkøbsvogn</span><span class="sxs-lookup"><span data-stu-id="dbf03-112">Cart page</span></span>

<span data-ttu-id="dbf03-113">Indkøbsvognens side fungerer som indkøbspose og indeholder alle de varer, der er lag i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="dbf03-114">I følgende illustration vises et eksempel på en indkøbsvognside, der er oprettet ved hjælp af startsættet og temaet "Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="dbf03-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![Eksempel på en indkøbsvognside](./media/cart2.PNG)

<span data-ttu-id="dbf03-116">Hovedindholdet af indkøbsvognens side viser alle de varer, som kunden har lagt i indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="dbf03-117">Alle relevante rabatter fremvises.</span><span class="sxs-lookup"><span data-stu-id="dbf03-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="dbf03-118">Disse rabatter omfatter komplekse rabatter.</span><span class="sxs-lookup"><span data-stu-id="dbf03-118">These discounts include complex discounts.</span></span> <span data-ttu-id="dbf03-119">Eksemplerne omfatter "Køb 3 varer, og få 10 % rabat" eller "Køb en flaske og en rygsæk, så du får 10 % rabat".</span><span class="sxs-lookup"><span data-stu-id="dbf03-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="dbf03-120">Modulet Ordreoversigt viser det beløb, der skal betales efter fradrag af rabat, forsendelse, moms og andet, der er anvendt.</span><span class="sxs-lookup"><span data-stu-id="dbf03-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="dbf03-121">Der findes også et kampagnekodemodul, hvor kunden kan anvende eller fjerne kampagnekoder.</span><span class="sxs-lookup"><span data-stu-id="dbf03-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="dbf03-122">En kunde kan købe anonymt eller som en bruger, der er logget på.</span><span class="sxs-lookup"><span data-stu-id="dbf03-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="dbf03-123">Hvis en kunde er logget på, bevares varer i indkøbsvognen mellem sessioner.</span><span class="sxs-lookup"><span data-stu-id="dbf03-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="dbf03-124">På denne måde kan kunden fortsætte med at handle fra flere enheder.</span><span class="sxs-lookup"><span data-stu-id="dbf03-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="dbf03-125">Fra indkøbsvognen kan kunden fortsætte til kassen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="dbf03-126">En kunde kan starte betaling som gæstebruger eller som en bruger, der er logget på.</span><span class="sxs-lookup"><span data-stu-id="dbf03-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="dbf03-127">Du kan finde oplysninger om, hvordan du opretter en indkøbsvognside, under [Føje et indkøbsvognmodul til en side](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="dbf03-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="dbf03-128">Siden Betaling ved kassen</span><span class="sxs-lookup"><span data-stu-id="dbf03-128">Checkout page</span></span>

<span data-ttu-id="dbf03-129">Siden med betaling ved kassen er det sted, hvor kunderne angiver de oplysninger, der skal bruges til afgivelsen af ordren.</span><span class="sxs-lookup"><span data-stu-id="dbf03-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="dbf03-130">I følgende illustration vises et eksempel på en betalingsside, der er oprettet ved hjælp af online startsættet.</span><span class="sxs-lookup"><span data-stu-id="dbf03-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![Eksempel på en betalingsside](./media/Checkout.PNG)

<span data-ttu-id="dbf03-132">Hovedindholdet af betalingssiden er det sted, hvor alle ordreoplysningerne indsamles.</span><span class="sxs-lookup"><span data-stu-id="dbf03-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="dbf03-133">Disse oplysninger omfatter leveringsadresse, leveringsindstillinger og betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="dbf03-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="dbf03-134">Betalingen er en trinvis proces, da oplysningerne skal angives i en bestemt rækkefølge for at blive behandlet.</span><span class="sxs-lookup"><span data-stu-id="dbf03-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="dbf03-135">Leveringsadressen skal f.eks. angives, før der kan beregnes forsendelsesomkostninger, og betalingen kan godkendes.</span><span class="sxs-lookup"><span data-stu-id="dbf03-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="dbf03-136">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="dbf03-136">Shipping address</span></span>

<span data-ttu-id="dbf03-137">Der skal angives en leveringsadresse, hvis der skal leveres varer.</span><span class="sxs-lookup"><span data-stu-id="dbf03-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="dbf03-138">Formatet for forsendelsesadresser for hver landestandard kan konfigureres i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="dbf03-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="dbf03-139">Hvis varerne f.eks. skal sendes til USA, skal leveringsadressen indeholde en gadeadresse, stat og postnummer.</span><span class="sxs-lookup"><span data-stu-id="dbf03-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="dbf03-140">Der udføres grundlæggende validering af leveringsadresser, f.eks. validering af alfanumeriske tegn, maksimumlængde og tal.</span><span class="sxs-lookup"><span data-stu-id="dbf03-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="dbf03-141">Selvom gyldigheden af selve adressen ikke bekræftes, kan denne kontrol udføres ved hjælp af tilpassede tredjepartstjenester.</span><span class="sxs-lookup"><span data-stu-id="dbf03-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="dbf03-142">Leveringsadressen anvendes på alle de varer i indkøbsvognen, som indstillingen "afsendelse" er valgt for.</span><span class="sxs-lookup"><span data-stu-id="dbf03-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="dbf03-143">Hvis du bruger flowet for betaling, der findes i online startersættet, kan individuelle varer i indkøbsvognen ikke leveres til forskellige adresser.</span><span class="sxs-lookup"><span data-stu-id="dbf03-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="dbf03-144">Hvis du har brug for denne egenskab, kan den implementeres ved at tilpasse betalingsmodulerne.</span><span class="sxs-lookup"><span data-stu-id="dbf03-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="dbf03-145">Når leveringsadressen er angivet, vises de leveringsmetoder, der er tilgængelige fra Dynamics 365 Commerce-onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="dbf03-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="dbf03-146">De leveringsmetoder og de adresser, de understøtter, kan konfigureres i Retail.</span><span class="sxs-lookup"><span data-stu-id="dbf03-146">The shipping methods and the addresses that they support can be configured in Retail.</span></span>

### <a name="payment"></a><span data-ttu-id="dbf03-147">Betaling</span><span class="sxs-lookup"><span data-stu-id="dbf03-147">Payment</span></span>

<span data-ttu-id="dbf03-148">Det næste trin i kasseprocessen er betalingen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="dbf03-149">I e-handel kan flere betalingsmåder bruges til at afgive ordrer, f.eks. kreditkort, gavekort og fordelskundepoint.</span><span class="sxs-lookup"><span data-stu-id="dbf03-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="dbf03-150">Der kan også bruges en kombination af disse betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="dbf03-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="dbf03-151">Afhængigt af de anvendte betalingsmetoder kan der være brug for flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="dbf03-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="dbf03-152">En kreditkortbetaling kræver f.eks. en faktureringsadresse.</span><span class="sxs-lookup"><span data-stu-id="dbf03-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="dbf03-153">Kreditkortbetalinger behandles ved hjælp af Adyen-betalingsconnectoren.</span><span class="sxs-lookup"><span data-stu-id="dbf03-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="dbf03-154">Fordelskundepoint</span><span class="sxs-lookup"><span data-stu-id="dbf03-154">Loyalty points</span></span>

<span data-ttu-id="dbf03-155">Under processen til betaling ved kassen kan en kunde, der er medlem af et fordelskundeprogram, og som har periodiserede fordelingskundepoint, indløse disse fordelskundepoint for en ordre.</span><span class="sxs-lookup"><span data-stu-id="dbf03-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="dbf03-156">Modulet til kundefordelspoint vises kun, hvis kunden har et eksisterende fordelskundemedlemskab.</span><span class="sxs-lookup"><span data-stu-id="dbf03-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="dbf03-157">Dette modul er skjult for ikke-medlemmer og gæstebrugere.</span><span class="sxs-lookup"><span data-stu-id="dbf03-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="dbf03-158">Gavekort</span><span class="sxs-lookup"><span data-stu-id="dbf03-158">Gift cards</span></span>

<span data-ttu-id="dbf03-159">Med online startsættet kan interne gavekort indløses for en ordre.</span><span class="sxs-lookup"><span data-stu-id="dbf03-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="dbf03-160">For at anvende et internt gavekort skal kunden være logget på.</span><span class="sxs-lookup"><span data-stu-id="dbf03-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="dbf03-161">Af hensyn til øget sikkerhed anbefales det, at du tilpasser processen ved at bruge et personligt identifikationsnummer (PIN) til interne gavekort.</span><span class="sxs-lookup"><span data-stu-id="dbf03-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="dbf03-162">Brugere, der er logget på, og gæstebrugere</span><span class="sxs-lookup"><span data-stu-id="dbf03-162">Signed-in and guest users</span></span>

<span data-ttu-id="dbf03-163">Kunden kan gennemføre betalingsprocessen som gæstebruger eller som en bruger, der er logget på.</span><span class="sxs-lookup"><span data-stu-id="dbf03-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="dbf03-164">Hvis kunden logger på, hentes der automatisk kontooplysninger som f.eks. gemte leveringsadresser og gemte oplysninger om kreditkort.</span><span class="sxs-lookup"><span data-stu-id="dbf03-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="dbf03-165">Ordreoversigt</span><span class="sxs-lookup"><span data-stu-id="dbf03-165">Order summary</span></span>

<span data-ttu-id="dbf03-166">Ved kassen vises en oversigt over linjevarerne i indkøbsvognen, så kunden kan bekræfte ordren, før den afgives.</span><span class="sxs-lookup"><span data-stu-id="dbf03-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="dbf03-167">Linjevarerne kan ikke redigeres i betalingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="dbf03-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="dbf03-168">Men der findes et link til indkøbsvognen, hvis brugeren vil gå tilbage og redigere linjevarer.</span><span class="sxs-lookup"><span data-stu-id="dbf03-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="dbf03-169">Når kunden har angivet forsendelses- og faktureringsoplysninger, afspejler ordreoversigten det beløb, der skal betales, når fordelskundepoint, gavekort og andre betalinger er anvendt.</span><span class="sxs-lookup"><span data-stu-id="dbf03-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="dbf03-170">Mail med ordrebekræftelse</span><span class="sxs-lookup"><span data-stu-id="dbf03-170">Order confirmation and email</span></span>

<span data-ttu-id="dbf03-171">Når kunden afgiver en ordre, udstedes et bekræftelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="dbf03-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="dbf03-172">På dette tidspunkt er betalingen godkendt, men ikke opkrævet.</span><span class="sxs-lookup"><span data-stu-id="dbf03-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="dbf03-173">Betalingen opkræves kun, når ordren er opfyldt (dvs. når den enten er leveret eller afhentet).</span><span class="sxs-lookup"><span data-stu-id="dbf03-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="dbf03-174">Når en ordre er oprettet, sendes der en ordrebekræftelse via mail til kunden.</span><span class="sxs-lookup"><span data-stu-id="dbf03-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="dbf03-175">Du kan finde flere oplysninger om, hvordan du opretter en betalingsside, under [Føje et betalingsmodul til en side](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="dbf03-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbf03-176">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dbf03-176">Additional resources</span></span>

[<span data-ttu-id="dbf03-177">Oversigt over startsiden</span><span class="sxs-lookup"><span data-stu-id="dbf03-177">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="dbf03-178">Oversigt over standardlandingsside for kategori og side for søgeresultater</span><span class="sxs-lookup"><span data-stu-id="dbf03-178">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="dbf03-179">Oversigt over sider med produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="dbf03-179">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="dbf03-180">Oversigt over sider til kontostyring</span><span class="sxs-lookup"><span data-stu-id="dbf03-180">Overview of account management pages</span></span>](quick-tour-account-management.md)
