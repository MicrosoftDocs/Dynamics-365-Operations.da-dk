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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107346"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="a73d5-103">Oprette callcenter-ordrer</span><span class="sxs-lookup"><span data-stu-id="a73d5-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a73d5-104">Denne procedure gennemgår søgning efter en kunde, oprettelse af en ny ordre, søgning efter et produkt og opkrævning af betaling fra kunden.</span><span class="sxs-lookup"><span data-stu-id="a73d5-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="a73d5-105">Denne procedure bruger demodatafirmaet USRT og er beregnet til salgsassistenter.</span><span class="sxs-lookup"><span data-stu-id="a73d5-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="a73d5-106">Forudsætninger: Den bruger, der udfører proceduren, er konfigureret som call center-brugere, og Fabrikams halvårlige katalog udgives med mindst én kildekode i.</span><span class="sxs-lookup"><span data-stu-id="a73d5-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="a73d5-107">Gå til **Retail og Commerce \> Kunder \> Kundeservice**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="a73d5-108">Angiv søgekriterierne for at søge efter kunden i feltet **Søgetekst**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="a73d5-109">Til denne eksempelprocedure skal du skrive "Karen" og vælge **Tab**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="a73d5-110">Vælg Søg.</span><span class="sxs-lookup"><span data-stu-id="a73d5-110">Select Search.</span></span>
    * <span data-ttu-id="a73d5-111">Da der kun er én kunde med navnet "Karen" i demodataene, vælges resultatet automatisk.</span><span class="sxs-lookup"><span data-stu-id="a73d5-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="a73d5-112">Vælg **Ny salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="a73d5-113">Udvis eller skjul overskriftssektionen **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="a73d5-114">Vælg kildekoden til kataloget.</span><span class="sxs-lookup"><span data-stu-id="a73d5-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="a73d5-115">Hvis der ikke er nogen aktive kildekoder, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="a73d5-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="a73d5-116">Vælg **Tilføj linje**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-116">Select **Add line**.</span></span>
8. <span data-ttu-id="a73d5-117">Indtast søgeordet til varen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="a73d5-118">Til denne eksempelprocedure skal du angive en del af et varenummer, "8111" og trykke på tab. Denne handling åbner vinduet til varesøgning.</span><span class="sxs-lookup"><span data-stu-id="a73d5-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="a73d5-119">Vælg det produkt, der skal føjes til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a73d5-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="a73d5-120">Angiv salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="a73d5-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="a73d5-121">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-121">Select **Create**.</span></span>
12. <span data-ttu-id="a73d5-122">Vælg **Fuldført** for at hente kundebetalingen.</span><span class="sxs-lookup"><span data-stu-id="a73d5-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="a73d5-123">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-123">Select **Add**.</span></span>
    * <span data-ttu-id="a73d5-124">Linket Tilføj findes under fanen Betalinger. Udvid fanen Betalinger, hvis den er skjult.</span><span class="sxs-lookup"><span data-stu-id="a73d5-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="a73d5-125">Vælg betalingsmåden.</span><span class="sxs-lookup"><span data-stu-id="a73d5-125">Select the payment method.</span></span>
    * <span data-ttu-id="a73d5-126">Til denne procedure skal du vælge kontantbetalingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="a73d5-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="a73d5-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a73d5-127">Close the page.</span></span>
16. <span data-ttu-id="a73d5-128">Indtast beløbet.</span><span class="sxs-lookup"><span data-stu-id="a73d5-128">Enter the amount.</span></span>
    * <span data-ttu-id="a73d5-129">Til denne procedure skal du angive et beløb svarende til ordresaldoen, som kan ses på oversigtssiden Salgsordre til venstre for feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="a73d5-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="a73d5-130">Denne handling giver dig mulighed for at fuldføre ordren som fuldt ud betalt.</span><span class="sxs-lookup"><span data-stu-id="a73d5-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="a73d5-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-131">Select **OK**.</span></span>
18. <span data-ttu-id="a73d5-132">Vælg **Send**.</span><span class="sxs-lookup"><span data-stu-id="a73d5-132">Select **Submit**.</span></span>

