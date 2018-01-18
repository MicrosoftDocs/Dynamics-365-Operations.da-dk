---
title: Callcenter-funktionalitet
description: Dette emne indeholder en oversigt over call center-salgsfunktioner i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 55bad891f9295eca6b0bf39847ede890b7294370
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="call-center-functionality"></a><span data-ttu-id="e7e88-103">Callcenter-funktionalitet</span><span class="sxs-lookup"><span data-stu-id="e7e88-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e7e88-104">Denne artikel indeholder en oversigt over call center-salgsfunktioner i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e7e88-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="e7e88-105">Dynamics 365 for Retail understøtter også callcentre som en slags detailkanal.</span><span class="sxs-lookup"><span data-stu-id="e7e88-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="e7e88-106">I et callcenter tager arbejdere ordrer fra kunder over telefonen og opretter salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="e7e88-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="e7e88-107">Callcenterfunktioner omfatter funktioner, der er beregnet til at gøre det nemmere at tage telefonordre og håndtere kundeservice i hele ordreopfyldelsesprocesen.</span><span class="sxs-lookup"><span data-stu-id="e7e88-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="e7e88-108">Eksempelvis kan call center-medarbejdere angive oplysninger om debitorbetalinger direkte til salgsordren og kan se en detaljeret oversigt over gebyrer og betalinger, før de kan sende ordren.</span><span class="sxs-lookup"><span data-stu-id="e7e88-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="e7e88-109">Arbejdere har også mulighed for at styre prisen og få adgang til forskellige data om debitorer, produkter og priser fra siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="e7e88-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="e7e88-110">Desuden har callcentre har forbedret funktionalitet til sporing af debitorers historik og ordrestatus.</span><span class="sxs-lookup"><span data-stu-id="e7e88-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="e7e88-111">Hvert callcenter kan have sine egne brugere, betalingsmetoder, prisgrupper, økonomiske dimensioner og leveringsmåder.</span><span class="sxs-lookup"><span data-stu-id="e7e88-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="e7e88-112">Du kan konfigurere disse indstillinger, når du opretter callcenteret.</span><span class="sxs-lookup"><span data-stu-id="e7e88-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="e7e88-113">Du kan også bruge siden **Callcenter** til at aktivere eller deaktivere følgende grupper af funktioner, der er unikke for callcentre:</span><span class="sxs-lookup"><span data-stu-id="e7e88-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="e7e88-114">**Ordrefuldførelse** – Denne gruppe omfatter funktioner, der er knyttet til betalinger og færdiggørelse på siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="e7e88-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="e7e88-115">**Dirigeret salg** – Denne gruppe indeholder funktioner, der er relateret til kildekoder, scripts og kataloganmodninger.</span><span class="sxs-lookup"><span data-stu-id="e7e88-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="e7e88-116">Når du aktiverer disse funktioner i indstillingerne for callcenteret, er de tilgængelige på siden **Salgsordre** for brugere, der er knyttet til callcenteret.</span><span class="sxs-lookup"><span data-stu-id="e7e88-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="e7e88-117">De fleste af disse funktioner kræver yderligere opsætning, før de kan bruges.</span><span class="sxs-lookup"><span data-stu-id="e7e88-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="e7e88-118">Før brugere kan oprette callcenter-ordrer, skal du føje brugere til callcentret som callcenter-brugere.</span><span class="sxs-lookup"><span data-stu-id="e7e88-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="e7e88-119">Dette trin aktiverer kanalspecifikke konfiguration og funktionalitet for callcenter.</span><span class="sxs-lookup"><span data-stu-id="e7e88-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="e7e88-120">Her er nogle eksempler på funktioner, der bliver tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="e7e88-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="e7e88-121">Vejledt salg indeholder konfigurationsindstillinger for telefonsalgsscripts og produktbilleder for at hjælpe og vejlede salgsassistenter, når de tager ordrer.</span><span class="sxs-lookup"><span data-stu-id="e7e88-121">Guided selling provides configuration options for tele-sales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="e7e88-122">Ordrer kan ikke fuldføres, før salgsassistenten har hentet mindst én betalingsmetode.</span><span class="sxs-lookup"><span data-stu-id="e7e88-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="e7e88-123">Regler for mersalg og krydssalg kan konfigureres til at bede salgsassistenten om at reklamere for specifikke produkter til debitoren.</span><span class="sxs-lookup"><span data-stu-id="e7e88-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="e7e88-124">Salgsassistenten kan hente koden til det katalog, som en debitor bestiller fra.</span><span class="sxs-lookup"><span data-stu-id="e7e88-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="e7e88-125">Salgsassistenten kan føje en detailhandlers kuponer til ordren.</span><span class="sxs-lookup"><span data-stu-id="e7e88-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="e7e88-126">Salgsassistenten kan sælge kontinuitetsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="e7e88-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="e7e88-127">Ordrer kan sættes på hold manuelt eller automatisk for at angive, at yderligere undersøgelse er påkrævet, før ordren kan behandles.</span><span class="sxs-lookup"><span data-stu-id="e7e88-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





