---
title: Synkronisere med Dynamics 365 Supply Chain Management-prissætningsprogrammet efter anmodning
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173171"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="8cad5-103">Synkronisere med Dynamics 365 Supply Chain Management-prissætningsprogrammet efter anmodning</span><span class="sxs-lookup"><span data-stu-id="8cad5-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8cad5-104">Microsoft Dynamics 365 Supply Chain Management indeholder et prissætningsprogram, der håndterer samhandelsaftaler, prislister, fordelskundeprogrammer, kampagner og rabatter.</span><span class="sxs-lookup"><span data-stu-id="8cad5-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="8cad5-105">Prissætningsprogrammet bruger komplekse regler til at bestemme den bedste pris for et givet tilbud eller en given ordre.</span><span class="sxs-lookup"><span data-stu-id="8cad5-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="8cad5-106">Når du bruger dobbeltskrivning, skal du enten bruge statisk prissætning eller prissætningsprogrammet fra Dynamics 365 Supply Chain Management på tilbuds- og ordresiderne i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8cad5-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="8cad5-107">Brug prissætningsprogrammet fra Supply Chain Management i Sales</span><span class="sxs-lookup"><span data-stu-id="8cad5-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="8cad5-108">Gå til **Sales \> Ordrer** i Sales.</span><span class="sxs-lookup"><span data-stu-id="8cad5-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="8cad5-109">Vælg **Ny** for at oprette en ny ordre eller vælg en eksisterende ordre på listen **Mine ordrer**.</span><span class="sxs-lookup"><span data-stu-id="8cad5-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="8cad5-110">Tilføj en ny ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="8cad5-110">Add a new order line.</span></span>
4. <span data-ttu-id="8cad5-111">Hvis du opretter en ny ordre, skal du vælge **Prisordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8cad5-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="8cad5-112">Hvis du opdaterer en eksisterende ordre, skal du vælge **Omberegn** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8cad5-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="8cad5-113">Følgende felter udfyldes automatisk:</span><span class="sxs-lookup"><span data-stu-id="8cad5-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="8cad5-114">Detaljebeløb</span><span class="sxs-lookup"><span data-stu-id="8cad5-114">Detail Amount</span></span>
    + <span data-ttu-id="8cad5-115">Rabat %</span><span class="sxs-lookup"><span data-stu-id="8cad5-115">Discount %</span></span>
    + <span data-ttu-id="8cad5-116">Diskontering</span><span class="sxs-lookup"><span data-stu-id="8cad5-116">Discount</span></span>
    + <span data-ttu-id="8cad5-117">Beløb før fragt</span><span class="sxs-lookup"><span data-stu-id="8cad5-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="8cad5-118">Fragtbeløb</span><span class="sxs-lookup"><span data-stu-id="8cad5-118">Freight Amount</span></span>
    + <span data-ttu-id="8cad5-119">Moms i alt</span><span class="sxs-lookup"><span data-stu-id="8cad5-119">Total Tax</span></span>
    + <span data-ttu-id="8cad5-120">Samlet beløb</span><span class="sxs-lookup"><span data-stu-id="8cad5-120">Total Amount</span></span>

## <a name="how-it-works"></a><span data-ttu-id="8cad5-121">Sådan fungerer det</span><span class="sxs-lookup"><span data-stu-id="8cad5-121">How it works</span></span>

<span data-ttu-id="8cad5-122">Når du vælger **Prisordre** i Sales, kaldes funktionen **Totaler** under **Salgsordre \> fanen Visning** i Supply Chain Management for den tilknyttede salgsordre.</span><span class="sxs-lookup"><span data-stu-id="8cad5-122">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="8cad5-123">Værdierne i ordretotalen bruges i Sales til at udfylde de tilsvarende felter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8cad5-123">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="8cad5-124">Når salgsordretotalen beregnes i Supply Chain Management, evaluerer beregningen de eksisterende samhandelsaftaler og salgsaftaler for kunden og de produkter, der er angivet i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="8cad5-124">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="8cad5-125">Oplysningerne bruges til at beregne totalerne.</span><span class="sxs-lookup"><span data-stu-id="8cad5-125">This information is used to calculate the totals.</span></span> <span data-ttu-id="8cad5-126">Når du har valgt **Prisordre**, afspejler Sales automatisk alle de opsætninger, der er udført i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8cad5-126">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="8cad5-127">Begrænsninger</span><span class="sxs-lookup"><span data-stu-id="8cad5-127">Limitations</span></span>

<span data-ttu-id="8cad5-128">Når felterne i Sales er udfyldt, gælder følgende begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="8cad5-128">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="8cad5-129">Opsætningen af gebyrer og gebyrtildelinger i Supply Chain Management replikeres ikke i Sales.</span><span class="sxs-lookup"><span data-stu-id="8cad5-129">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="8cad5-130">Prissætningen tager ikke hensyn til den særlige detailpris, der er angivet i feltet **Detailkanal** på siden med salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8cad5-130">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="8cad5-131">Rabatter, der er defineret i sektionen **Administration af handelstilladelse** i Supply Chain Management, tages ikke i betragtning.</span><span class="sxs-lookup"><span data-stu-id="8cad5-131">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
