---
title: Konfigurere og behandle en udveksling på en returordre
description: Dette emne forklarer, hvordan du konfigurerer en udveksling på en returnering i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458691"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="3a46a-103">Konfigurere og behandle en udveksling på en returordre</span><span class="sxs-lookup"><span data-stu-id="3a46a-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a46a-104">I tidligere versioner af Dynamics 365 Commerce, blev returneringer ud fra kundeordrer behandlet ved hjælp af returordredokumentet i Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3a46a-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="3a46a-105">Returordredokumentet kan dog kun bruges til at behandle produkter, der returneres.</span><span class="sxs-lookup"><span data-stu-id="3a46a-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="3a46a-106">De returnerede produkter er angivet med et negativt antal på returordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="3a46a-107">Salg er derimod angivet med et positivt antal.</span><span class="sxs-lookup"><span data-stu-id="3a46a-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="3a46a-108">Returordredokumentet understøtter dog ikke positive antal.</span><span class="sxs-lookup"><span data-stu-id="3a46a-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="3a46a-109">På grund af denne begrænsning understøttede tidligere versioner af appen ikke scenarier, hvor produktudvekslinger udføres ved hjælp af returordredokumentet.</span><span class="sxs-lookup"><span data-stu-id="3a46a-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="3a46a-110">Der er imidlertid blevet tilføjet funktionalitet til understøttelse af scenarier, hvor udveksling udføres på returordrer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="3a46a-111">Commerce anvender nu salgsordredokumentet i stedet for returordredokumentet til behandling af disse typer transaktioner.</span><span class="sxs-lookup"><span data-stu-id="3a46a-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="3a46a-112">Konfigurere Commerce til at understøtte udvekslinger på returordrer</span><span class="sxs-lookup"><span data-stu-id="3a46a-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="3a46a-113">Følg disse trin for at konfigurere systemet til at understøtte udvekslinger på returordrer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="3a46a-114">Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre**.</span><span class="sxs-lookup"><span data-stu-id="3a46a-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="3a46a-115">På oversigtspanelet **Kundeordrer** skal du angive indstillingen **Behandl returordrer som salgsordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3a46a-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="3a46a-116">Kør jobbet **Global konfiguration distributionsplan** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="3a46a-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="3a46a-117">Foretag en udveksling.</span><span class="sxs-lookup"><span data-stu-id="3a46a-117">Make an exchange</span></span>

<span data-ttu-id="3a46a-118">Når systemet er konfigureret som beskrevet i den forrige sektion, vælger POS-brugeren stadig en salgsordre eller salgsfaktura for at behandle en returnering, som i tidligere versioner af appen.</span><span class="sxs-lookup"><span data-stu-id="3a46a-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="3a46a-119">Men når returvarerne er føjet til indkøbsvognen, kan brugeren tilføje nye salgslinjer til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="3a46a-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="3a46a-120">For disse nye salgslinjer skal brugeren angive alle de attributter, der er nødvendige for at behandle en kundeordrelinje.</span><span class="sxs-lookup"><span data-stu-id="3a46a-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="3a46a-121">Disse attributter omfatter leveringsmetode og opfyldelseslokation.</span><span class="sxs-lookup"><span data-stu-id="3a46a-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="3a46a-122">Den betaling, der er forfalden for transaktionen, bliver en nettoværdi af returordrelinjer og salgsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="3a46a-123">Når betalingen udføres for transaktionen, bogføres returordren som et salgsordredokument i Headquarters, og systemet fakturerer med det samme returneringslinjerne.</span><span class="sxs-lookup"><span data-stu-id="3a46a-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="3a46a-124">For at give bedre indsigt i de forskellige beløb for indkøbsvognen er der blevet tilføjet tre nye beløbsfelter til indkøbsvognen.</span><span class="sxs-lookup"><span data-stu-id="3a46a-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="3a46a-125">Du kan bruge skærmdesigneren for at gøre disse nye felter tilgængelige i POS-brugergrænsefladen (UI).</span><span class="sxs-lookup"><span data-stu-id="3a46a-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="3a46a-126">**Anvendt depositum** – Det indbetalingsbeløb, der anvendes på en transaktion, når brugeren udfører en kundeordreafhentning.</span><span class="sxs-lookup"><span data-stu-id="3a46a-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="3a46a-127">Hvis der ikke er nogen tilsidesættelse af indbetalt beløb, og et depositum på 10 procent er konfigureret, er beløbet i dette felt 90 procent af det samlede beløb for kundeordren.</span><span class="sxs-lookup"><span data-stu-id="3a46a-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="3a46a-128">**Udførelsesbeløb** – Det samlede beløb for linjer, hvor leveringsmåden blev angivet til **Udfør**, da ordren blev oprettet eller redigeret, eller under en kundeordreudveksling.</span><span class="sxs-lookup"><span data-stu-id="3a46a-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="3a46a-129">Beløbet i dette felt omfatter moms og gebyrer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="3a46a-130">**Returbeløb** – Det samlede beløb for linjer med negative antal under kundeordreudvekslingen.</span><span class="sxs-lookup"><span data-stu-id="3a46a-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="3a46a-131">Beløbet i dette felt omfatter moms og gebyrer.</span><span class="sxs-lookup"><span data-stu-id="3a46a-131">The amount in this field includes taxes and charges.</span></span>
