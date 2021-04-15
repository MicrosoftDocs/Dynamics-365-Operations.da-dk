---
title: Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder
description: Dette emne beskriver, hvordan du kan konfigurere debitorkontobetalingsmåden for business-to-business (B2B)-e-handelswebsteder.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799799"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="00e13-103">Konfigurere betalingsmåden for debitorkonti for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="00e13-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00e13-104">Dette emne beskriver, hvordan du kan konfigurere debitorkontobetalingsmåden for business-to-business (B2B)-e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="00e13-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="00e13-105">Detailhandlende kan acceptere forskellige former for betalinger for de produkter og tjenester, de sælger i en e-handelskanal.</span><span class="sxs-lookup"><span data-stu-id="00e13-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="00e13-106">De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres i Microsoft Dynamics 365 Commerce, når systemet konfigureres.</span><span class="sxs-lookup"><span data-stu-id="00e13-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="00e13-107">Betalingsmåden for debitorkontoen (eller "akonti") skal understøttes på B2B-e-handelswebsteder.</span><span class="sxs-lookup"><span data-stu-id="00e13-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="00e13-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="00e13-108">Prerequisites</span></span>

1. <span data-ttu-id="00e13-109">Tilføj debitorkontobetalingsmåden i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="00e13-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="00e13-110">Tilknyt betalingsmåden for debitorkontoen til e-handelskanalen.</span><span class="sxs-lookup"><span data-stu-id="00e13-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="00e13-111">Sørg for, at **Tillad på konto** er aktiveret for kunden i **Retail og Commerce \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="00e13-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="00e13-112">Sørg også for, at parametrene for **kreditmaksimum** er angivet korrekt for kunden i **Retail og Commerce \> Kunder \> Alle kunder \> Kredit og rykkere** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="00e13-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="00e13-113">Aktivere betalingsmåden for debitorkonti i Commerce-webstedsgenerator</span><span class="sxs-lookup"><span data-stu-id="00e13-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="00e13-114">Følg disse trin for at aktivere betalingsmåden for debitorkonti i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="00e13-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="00e13-115">Gå til **Webstedsindstillinger \> Udvidelser**.</span><span class="sxs-lookup"><span data-stu-id="00e13-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="00e13-116">Angiv egenskaben **Aktiver debitorkontobetalinger** til **Aktiveret for B2B-debitorer**.</span><span class="sxs-lookup"><span data-stu-id="00e13-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="00e13-117">Vælg **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="00e13-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="00e13-118">De nye indstillinger for webstedet træder først i kraft, når app.settings.json-filen er opdateret.</span><span class="sxs-lookup"><span data-stu-id="00e13-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="00e13-119">Yderligere oplysninger finder du i [SDK- og modulbiblioteksopdateringer](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="00e13-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="00e13-120">Aktivere betalingsmetoden for debitorkontoen på siden til betaling ved kassen for E-handelswebstedet for B2B</span><span class="sxs-lookup"><span data-stu-id="00e13-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="00e13-121">Følg disse trin for at aktivere betalingsmetoden for debitorkontoen på siden til betaling ved kassen for E-handelswebstedet for B2B.</span><span class="sxs-lookup"><span data-stu-id="00e13-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="00e13-122">I Commerce site builder skal du finde og redigere den side eller det system til betaling ved kassen, som indeholder modulet til betaling ved kassen for webstedet B2B-e-handel.</span><span class="sxs-lookup"><span data-stu-id="00e13-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="00e13-123">I **Container til betalingssektion**-kassen skal du vælge **Tilføj modul** og derefter tilføje et **Debitorkontobetaling**-modul.</span><span class="sxs-lookup"><span data-stu-id="00e13-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="00e13-124">Placer **Debitorkontobetaling**-modulet ved at vælge ellipsen (**...**) og derefter vælge **Flyt op** eller **Flyt ned** efter behov.</span><span class="sxs-lookup"><span data-stu-id="00e13-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="00e13-125">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="00e13-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="00e13-126">Bekræft, at betalingsmetoden for debitorkonti er aktiveret og udgivet</span><span class="sxs-lookup"><span data-stu-id="00e13-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="00e13-127">Følg disse trin for at bekræfte, at betalingsmetoden for debitorkonti er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="00e13-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="00e13-128">Log på e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="00e13-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="00e13-129">Tilføjet produkt til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="00e13-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="00e13-130">Gå til betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="00e13-130">Go to the checkout page.</span></span> <span data-ttu-id="00e13-131">Du bør se den nye betalingsmåde for **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="00e13-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00e13-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="00e13-132">Additional resources</span></span>

[<span data-ttu-id="00e13-133">Konfigurere et B2B-e-handelswebsted</span><span class="sxs-lookup"><span data-stu-id="00e13-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="00e13-134">Oprette organisationsmodelhierarkier for B2B-organisationer</span><span class="sxs-lookup"><span data-stu-id="00e13-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="00e13-135">Administrere forretningspartnerbrugere på B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="00e13-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="00e13-136">Angive produktantalsgrænser for B2B-e-handelswebsteder</span><span class="sxs-lookup"><span data-stu-id="00e13-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="00e13-137">Opdateringer til SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="00e13-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]