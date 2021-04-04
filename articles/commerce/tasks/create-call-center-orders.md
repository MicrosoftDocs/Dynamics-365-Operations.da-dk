---
title: Oprette callcenter-ordrer
description: Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecf6fe97287fcfb3c070215b563542878175789c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264278"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="96c40-103">Oprette callcenter-ordrer</span><span class="sxs-lookup"><span data-stu-id="96c40-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96c40-104">Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden.</span><span class="sxs-lookup"><span data-stu-id="96c40-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="96c40-105">Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter.</span><span class="sxs-lookup"><span data-stu-id="96c40-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="96c40-106">Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.</span><span class="sxs-lookup"><span data-stu-id="96c40-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="96c40-107">Gå til **Retail og Commerce \> Kunder \> Kundeservice**.</span><span class="sxs-lookup"><span data-stu-id="96c40-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="96c40-108">Angiv søgekriterierne for at søge efter kunden i feltet **Søgetekst**.</span><span class="sxs-lookup"><span data-stu-id="96c40-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="96c40-109">Til denne eksempelprocedure skal du skrive "Karen" og vælge **Tab**.</span><span class="sxs-lookup"><span data-stu-id="96c40-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="96c40-110">Vælg Søg.</span><span class="sxs-lookup"><span data-stu-id="96c40-110">Select Search.</span></span>
    * <span data-ttu-id="96c40-111">Da der kun er én kunde med navnet "Karen" i demodataene, vælges resultatet automatisk.</span><span class="sxs-lookup"><span data-stu-id="96c40-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="96c40-112">Vælg **Ny salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="96c40-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="96c40-113">Udvis eller skjul overskriftssektionen **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="96c40-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="96c40-114">Vælg kildekoden til kataloget.</span><span class="sxs-lookup"><span data-stu-id="96c40-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="96c40-115">Hvis der ikke er nogen aktive kildekoder, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="96c40-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="96c40-116">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="96c40-116">Select **Add line**.</span></span>
8. <span data-ttu-id="96c40-117">Indtast søgeordet til varen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="96c40-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="96c40-118">Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab. Denne handling åbner vinduet til varesøgning.</span><span class="sxs-lookup"><span data-stu-id="96c40-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="96c40-119">Vælg det produkt, der skal føjes til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="96c40-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="96c40-120">Angiv salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="96c40-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="96c40-121">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="96c40-121">Select **Create**.</span></span>
12. <span data-ttu-id="96c40-122">Vælg **Fuldført** for at hente kundebetalingen.</span><span class="sxs-lookup"><span data-stu-id="96c40-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="96c40-123">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="96c40-123">Select **Add**.</span></span>
    * <span data-ttu-id="96c40-124">Linket Tilføj findes under fanen Betalinger. Udvid fanen Betalinger, hvis den er skjult.</span><span class="sxs-lookup"><span data-stu-id="96c40-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="96c40-125">Vælg betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="96c40-125">Select the payment method.</span></span>
    * <span data-ttu-id="96c40-126">Til denne procedure skal du vælge kontantbetalingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="96c40-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="96c40-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96c40-127">Close the page.</span></span>
16. <span data-ttu-id="96c40-128">Indtast beløbet.</span><span class="sxs-lookup"><span data-stu-id="96c40-128">Enter the amount.</span></span>
    * <span data-ttu-id="96c40-129">Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="96c40-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="96c40-130">Denne handling giver dig mulighed for at fuldføre ordren som fuldt ud betalt.</span><span class="sxs-lookup"><span data-stu-id="96c40-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="96c40-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="96c40-131">Select **OK**.</span></span>
18. <span data-ttu-id="96c40-132">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="96c40-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96c40-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="96c40-133">Additional resources</span></span>

[<span data-ttu-id="96c40-134">Tilpasse transaktionsmails efter leveringsmåde</span><span class="sxs-lookup"><span data-stu-id="96c40-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="96c40-135">Skifte leveringsmåde til i POS</span><span class="sxs-lookup"><span data-stu-id="96c40-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]