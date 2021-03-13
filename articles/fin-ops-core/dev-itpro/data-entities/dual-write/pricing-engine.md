---
title: Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov
description: Dette emne beskriver, hvordan du bruger prissætningsprogrammet i Dynamics 365 Supply Chain Management fra Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130647"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="cd83f-103">Synkronisere med Supply Chain Management-prissætningsprogrammet efter behov</span><span class="sxs-lookup"><span data-stu-id="cd83f-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cd83f-104">Microsoft Dynamics 365 Supply Chain Management indeholder et prissætningsprogram, der håndterer samhandelsaftaler, prislister, fordelskundeprogrammer, kampagner og rabatter.</span><span class="sxs-lookup"><span data-stu-id="cd83f-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="cd83f-105">Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre.</span><span class="sxs-lookup"><span data-stu-id="cd83f-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="cd83f-106">Når du bruger dobbeltskrivning, skal du enten bruge statisk prissætning eller prissætningsprogrammet fra Dynamics 365 Supply Chain Management på tilbuds- og ordresiderne i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="cd83f-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="cd83f-107">Brug prissætningsprogrammet fra Supply Chain Management i Sales</span><span class="sxs-lookup"><span data-stu-id="cd83f-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="cd83f-108">Gå til **Sales \> Ordrer** i Sales.</span><span class="sxs-lookup"><span data-stu-id="cd83f-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="cd83f-109">Vælg **Ny** for at oprette en ny ordre eller vælg en eksisterende ordre på listen **Mine ordrer**.</span><span class="sxs-lookup"><span data-stu-id="cd83f-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="cd83f-110">Tilføj en ny ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="cd83f-110">Add a new order line.</span></span>
4. <span data-ttu-id="cd83f-111">Hvis du opretter en ny ordre, skal du vælge **Prisordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cd83f-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="cd83f-112">Hvis du opdaterer en eksisterende ordre, skal du vælge **Omberegn** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cd83f-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="cd83f-113">Følgende kolonner udfyldes automatisk:</span><span class="sxs-lookup"><span data-stu-id="cd83f-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="cd83f-114">Detaljebeløb</span><span class="sxs-lookup"><span data-stu-id="cd83f-114">Detail Amount</span></span>
    + <span data-ttu-id="cd83f-115">Rabat %</span><span class="sxs-lookup"><span data-stu-id="cd83f-115">Discount %</span></span>
    + <span data-ttu-id="cd83f-116">Diskontering</span><span class="sxs-lookup"><span data-stu-id="cd83f-116">Discount</span></span>
    + <span data-ttu-id="cd83f-117">Beløb før fragt</span><span class="sxs-lookup"><span data-stu-id="cd83f-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="cd83f-118">Fragtbeløb</span><span class="sxs-lookup"><span data-stu-id="cd83f-118">Freight Amount</span></span>
    + <span data-ttu-id="cd83f-119">Moms i alt</span><span class="sxs-lookup"><span data-stu-id="cd83f-119">Total Tax</span></span>
    + <span data-ttu-id="cd83f-120">Samlet beløb</span><span class="sxs-lookup"><span data-stu-id="cd83f-120">Total Amount</span></span>
    
5. <span data-ttu-id="cd83f-121">For at sikre, at der tages hensyn til handels-og salgsaftaler i beregning af prisen:</span><span class="sxs-lookup"><span data-stu-id="cd83f-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="cd83f-122">Naviger til dit Supply Chain Management-miljø.</span><span class="sxs-lookup"><span data-stu-id="cd83f-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="cd83f-123">Naviger til **Debitor \> Opsætning \> Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="cd83f-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="cd83f-124">Vælg fanen **Priser** på sidens navigationslinje.</span><span class="sxs-lookup"><span data-stu-id="cd83f-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="cd83f-125">Fjern markeringen i afkrydsningsfeltet **Manuel indtastning** i oversigtspanelet **Evaluering af samhandelsaftale**.</span><span class="sxs-lookup"><span data-stu-id="cd83f-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="cd83f-126">Sådan fungerer det</span><span class="sxs-lookup"><span data-stu-id="cd83f-126">How it works</span></span>

<span data-ttu-id="cd83f-127">Når du vælger **Prisordre** i Sales, kaldes funktionen **Totaler** under **Salgsordre \> fanen Visning** i Supply Chain Management for den tilknyttede salgsordre.</span><span class="sxs-lookup"><span data-stu-id="cd83f-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="cd83f-128">Værdierne i ordretotalen bruges i Sales til at udfylde de tilsvarende kolonner i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cd83f-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="cd83f-129">Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende samhandelsaftaler og salgsaftaler for kunden og de produkter, der er angivet i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="cd83f-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="cd83f-130">Oplysningerne bruges til at beregne totalerne.</span><span class="sxs-lookup"><span data-stu-id="cd83f-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="cd83f-131">Når du har valgt **Prisordre**, afspejler Sales automatisk alle de opsætninger, der er udført i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cd83f-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="cd83f-132">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="cd83f-132">Limitations</span></span>

<span data-ttu-id="cd83f-133">Når kolonnerne i Sales er udfyldt, gælder følgende begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="cd83f-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="cd83f-134">Opsætningen af gebyrer og gebyrtildelinger i Supply Chain Management replikeres ikke i Sales.</span><span class="sxs-lookup"><span data-stu-id="cd83f-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="cd83f-135">Prissætningen tager ikke hensyn til den særlige detailpris, der er angivet i kolonnen **Detailkanal** på siden med salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cd83f-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="cd83f-136">Rabatter, der er defineret i sektionen **Administration af handelstilladelse** i Supply Chain Management, tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="cd83f-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
