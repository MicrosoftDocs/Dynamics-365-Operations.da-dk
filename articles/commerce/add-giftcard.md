---
title: Gavekortmodul
description: I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962757"
---
# <a name="gift-card-module"></a><span data-ttu-id="e6b63-103">Gavekortsmodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6b63-104">I dette emne dækkes gavekortmoduler, og det beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6b63-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e6b63-105">Gavekortmoduler kan bruges i betalingsmoduler til at acceptere gavekort og er en almindelig betalingsform i e-handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="e6b63-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="e6b63-106">Gavekortmodulet understøtter Dynamics 365-, SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="e6b63-107">SVS- og Givex-gavekort indløses via betalingsudbyderen Adyen.</span><span class="sxs-lookup"><span data-stu-id="e6b63-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="e6b63-108">Du kan se flere oplysninger om understøttelse af eksterne gavekort som f.eks. SVS og Givex i emnet [Understøttelse af eksterne gavekort](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="e6b63-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e6b63-109">Understøttelse til indløsning af SVS- og Givex-gavekort i betalingsprocessen er tilgængelig i Dynamics 365 Commerce version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="e6b63-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="e6b63-110">Der er to tilgængelige gavekortmoduler:</span><span class="sxs-lookup"><span data-stu-id="e6b63-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="e6b63-111">**Gavekort** – Dette modul kan bruges på en betalingsside til at indløse et gavekort som betalingsmiddel.</span><span class="sxs-lookup"><span data-stu-id="e6b63-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="e6b63-112">**Saldokontrol for gavekort** – Dette modul kan bruges på enhver side til at kontrollere saldoen for et gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="e6b63-113">Dette modul er tilgængeligt i Commerce version 10.0.14 og nyere.</span><span class="sxs-lookup"><span data-stu-id="e6b63-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="e6b63-114">Understøttelse af saldokontrolmodulet til gavekort er tilgængelig i Dynamics 365 Commerce version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="e6b63-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="e6b63-115">Det følgende billede viser et eksempel på et gavekortmodul på en betalingsside.</span><span class="sxs-lookup"><span data-stu-id="e6b63-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Eksempel på et gavekortmodul](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="e6b63-117">Modulegenskaber</span><span class="sxs-lookup"><span data-stu-id="e6b63-117">Module properties</span></span>

- <span data-ttu-id="e6b63-118">**Vis yderligere felter** – Denne egenskab definerer, hvilke felter der skal vises for gavekort ud over gavekortnummeret, der altid vises som standard.</span><span class="sxs-lookup"><span data-stu-id="e6b63-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="e6b63-119">Nogle gavekort understøtter f.eks. visning af en pinkode, og andre understøtter visning af en pinkode og udløbsdato.</span><span class="sxs-lookup"><span data-stu-id="e6b63-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="e6b63-120">Denne egenskab kan også angives til "Ingen", hvilket kun viser gavekortnummeret og ingen yderligere felter.</span><span class="sxs-lookup"><span data-stu-id="e6b63-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="e6b63-121">Understøttede værdier:</span><span class="sxs-lookup"><span data-stu-id="e6b63-121">Supported values:</span></span>
-   <span data-ttu-id="e6b63-122">Pinkode</span><span class="sxs-lookup"><span data-stu-id="e6b63-122">PIN</span></span>
-   <span data-ttu-id="e6b63-123">Udløbsdato</span><span class="sxs-lookup"><span data-stu-id="e6b63-123">Expiration date</span></span>
-   <span data-ttu-id="e6b63-124">Pinkode og udløbsdato</span><span class="sxs-lookup"><span data-stu-id="e6b63-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="e6b63-125">None</span><span class="sxs-lookup"><span data-stu-id="e6b63-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="e6b63-126">Indstillinger for websted for gavekortmoduler</span><span class="sxs-lookup"><span data-stu-id="e6b63-126">Site settings for gift card modules</span></span>

<span data-ttu-id="e6b63-127">I Commerce-webstedsgenerator under **Indstillinger for websted \> Udvidelser** er der en indstilling for gavekortmodulet, der kaldes **Understøttet gavekorttype**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="e6b63-128">Denne indstilling understøtter tre værdier:</span><span class="sxs-lookup"><span data-stu-id="e6b63-128">This setting supports three values:</span></span>
- <span data-ttu-id="e6b63-129">**Dynamics 365-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsning af Dynamics 365-gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="e6b63-130">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="e6b63-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="e6b63-131">**SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet kun indløsning af SVS- og Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="e6b63-132">Denne indstilling understøttes for anonyme brugere og brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="e6b63-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="e6b63-133">**Dynamics 365-, SVS- og Givex-gavekort** – Når denne indstilling er valgt, tillader gavekortmodulet indløsning af Dynamics 365-, Givex- og SVS-gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="e6b63-134">Denne indstilling understøttes kun for brugere, der er logget på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="e6b63-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6b63-135">Disse indstillinger er tilgængelige i Dynamics 365 Commerce version 10.0.11 og er kun nødvendige, hvis du har brug for understøttelse af SVS- eller Givex-gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="e6b63-136">Hvis du opdaterer fra en ældre version af Dynamics 365 Commerce, skal du opdatere filen appsettings.json manuelt.</span><span class="sxs-lookup"><span data-stu-id="e6b63-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="e6b63-137">Oplysninger om opdatering af filen appsettings.json finder du under [Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="e6b63-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="e6b63-138">Udvide interne gavekort til brug i udstillingsvinduer for e-handel</span><span class="sxs-lookup"><span data-stu-id="e6b63-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="e6b63-139">Interne gavekort er som standard ikke optimeret til brug i udstillingsvinduer for e-handel.</span><span class="sxs-lookup"><span data-stu-id="e6b63-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="e6b63-140">Før du tillader brug af interne gavekort til betaling, skal du konfigurere dem med udvidelser, der gør dem mere sikre.</span><span class="sxs-lookup"><span data-stu-id="e6b63-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="e6b63-141">Her er de gavekortområder, som du skal udvide, før du tillader, at interne gavekort bruges i produktionen:</span><span class="sxs-lookup"><span data-stu-id="e6b63-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="e6b63-142">**Gavekortnummer** – Nummerserier bruges til generering af gavekortnumre til interne gavekort.</span><span class="sxs-lookup"><span data-stu-id="e6b63-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="e6b63-143">Da nummerserier er forudsigelige, skal du udvide genereringen af gavekortnumre, så der anvendes tilfældige og kryptografisk sikre strenge til de gavekortnumre, der udstedes.</span><span class="sxs-lookup"><span data-stu-id="e6b63-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="e6b63-144">**GetBalance** – API'en for **GetBalance** bruges til at få vist gavekortsaldi.</span><span class="sxs-lookup"><span data-stu-id="e6b63-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="e6b63-145">Denne API er som standard offentlig.</span><span class="sxs-lookup"><span data-stu-id="e6b63-145">By default, this API public.</span></span> <span data-ttu-id="e6b63-146">Hvis der ikke kræves en PIN-kode for at få vist gavekortsaldi, er der risiko for, at brute force-angreb kan bruge API'en for **GetBalance** til at forsøge at få vist gavekortnumre med saldi.</span><span class="sxs-lookup"><span data-stu-id="e6b63-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="e6b63-147">Når du implementerer både PIN-krav for interne gavekort og API-begrænsning, kan du reducere risikoen.</span><span class="sxs-lookup"><span data-stu-id="e6b63-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="e6b63-148">**PIN-kode** – Interne gavekort understøtter som standard ikke PIN-koder.</span><span class="sxs-lookup"><span data-stu-id="e6b63-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="e6b63-149">Du skal udvide interne gavekort, så der kræves en PIN-kode for at få vist saldi.</span><span class="sxs-lookup"><span data-stu-id="e6b63-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="e6b63-150">Denne funktionalitet kan også bruges til at låse gavekort efter flere forkerte forsøg på at indtaste PIN-koden.</span><span class="sxs-lookup"><span data-stu-id="e6b63-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="e6b63-151">Aktivere gavekortbetalinger for gæsters betaling</span><span class="sxs-lookup"><span data-stu-id="e6b63-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="e6b63-152">Som standard er gavekortbetalinger ikke aktiveret for gæsters (anonyme) betaling.</span><span class="sxs-lookup"><span data-stu-id="e6b63-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="e6b63-153">Hvis du vil aktivere denne funktion, skal du benytte denne fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="e6b63-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="e6b63-154">I Commerce-hovedkvarteret skal du gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="e6b63-155">Vælg og hold (eller højreklik på) gitterhovedet, og vælg derefter **Indsæt kolonner**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="e6b63-156">Markér afkrydsningsfeltet **AllowChecknymousAccess** i dialogboksen **Indsæt kolonner**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="e6b63-157">Vælg **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-157">Select **Update**.</span></span>
1. <span data-ttu-id="e6b63-158">For handlingerne **520** (gavekortsaldo) og **214** skal du angive værdien for **AllowSynonymousAccess** til **1**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="e6b63-159">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e6b63-159">Select **Save**.</span></span>
1. <span data-ttu-id="e6b63-160">Kør planlægningsjobbet **1090** for at synkronisere ændringerne med kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="e6b63-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="e6b63-161">Føje et gavekortmodul til en side</span><span class="sxs-lookup"><span data-stu-id="e6b63-161">Add a gift card module to a page</span></span>

<span data-ttu-id="e6b63-162">Du kan få flere oplysninger om, hvordan du føjer et gavekortmodul til en betalingsside og angiver de påkrævede egenskaber, i [Betalingsmodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e6b63-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6b63-163">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e6b63-163">Additional resources</span></span>

[<span data-ttu-id="e6b63-164">Indkøbskurvsmodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e6b63-165">Ikonmodul for indkøbskurv</span><span class="sxs-lookup"><span data-stu-id="e6b63-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e6b63-166">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e6b63-167">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e6b63-168">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e6b63-169">Leveringsindstillingsmodul</span><span class="sxs-lookup"><span data-stu-id="e6b63-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e6b63-170">Modul med afhentningsoplysninger</span><span class="sxs-lookup"><span data-stu-id="e6b63-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e6b63-171">Ordredetaljer-modul</span><span class="sxs-lookup"><span data-stu-id="e6b63-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e6b63-172">Understøttelse af eksterne gavekort</span><span class="sxs-lookup"><span data-stu-id="e6b63-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="e6b63-173">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="e6b63-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
