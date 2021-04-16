---
title: A-skat i indkøbstransaktioner
description: For kreditorer, der skal betale A-skat, kan du tildele standardgruppen for **A-skat** på siden **Alle kreditorer**.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816877"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="b49b9-103">A-skat i indkøbstransaktioner</span><span class="sxs-lookup"><span data-stu-id="b49b9-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="b49b9-104">For kreditorer, der skal betale A-skat, kan du tildele standardgruppen for **A-skat** på siden **Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="b49b9-105">Gå til **Navigationsruden > Moduler > Kreditor > Kreditorer > Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="b49b9-106">Klik på den pågældende kreditorkonto, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="b49b9-107">Angiv **Ja** i feltet **Beregn A-skat** på fanen **Faktura og levering**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b49b9-108">A-skat beregnes ikke, hvis **Beregn A-skat** ikke er aktiveret for denne leverandør i dataene.</span><span class="sxs-lookup"><span data-stu-id="b49b9-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="b49b9-109">Vælg en A-skattegruppe i **A-skattegruppen**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="b49b9-110">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-110">Click **Save**.</span></span>

<span data-ttu-id="b49b9-111">For varer/tjenester, der er ansvarlige for A-skat, kan du tildele standardgruppen for **Varer i A-skattegruppe** i **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="b49b9-112">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="b49b9-113">Klik på det pågældende elementnummer og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="b49b9-114">Klik på **Beregn A-skat** på fanen **Køb**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b49b9-115">A-skat beregnes ikke, hvis **Beregn A-skat** ikke er angivet til **Ja** for denne vare under fanen **Indkøb** på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="b49b9-116">Vælg et element i A-skattegruppe på listen **Element i A-skattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="b49b9-117">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-117">Click **Save**.</span></span>

<span data-ttu-id="b49b9-118">A-skattegrupper og A-skattegrupper for varer kan tildeles på sider:</span><span class="sxs-lookup"><span data-stu-id="b49b9-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="b49b9-119">**Indkøbsordre**</span><span class="sxs-lookup"><span data-stu-id="b49b9-119">**Purchase order**</span></span>
- <span data-ttu-id="b49b9-120">**Kreditorfaktura**</span><span class="sxs-lookup"><span data-stu-id="b49b9-120">**Vendor invoice**</span></span>
- <span data-ttu-id="b49b9-121">**Fakturajournal**</span><span class="sxs-lookup"><span data-stu-id="b49b9-121">**Invoice journal**</span></span>

<span data-ttu-id="b49b9-122">Standardgruppen for A-skattegruppe og A-skattegruppen for varer overføres til linjerne, når der oprettes **Indkøbsordrer** og/eller **Ventende kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="b49b9-123">I forbindelse med **Kreditorfakturakladde** kan du skifte til **Beregn A-skat** og vælge **Element i A-skattegruppe** på fanen **Generelt** i kladden.</span><span class="sxs-lookup"><span data-stu-id="b49b9-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="b49b9-124">Det midlertidige beløb for A-skat er tilgængeligt i feltet **Reguleret A-skat** på fanen **Totaler** på siden **Indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![A-skat medtages på indkøbsordren](media/withholding-tax-adjusted.png)

<span data-ttu-id="b49b9-126">A-skat beregnes på **leverandørbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="b49b9-127">Du kan manuelt justere de relevante koder for A-skat og de faktiske beløb for A-skat under fanen **A-skat** på siden **Afregn posteringer**.</span><span class="sxs-lookup"><span data-stu-id="b49b9-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![A-skat kan reguleres manuelt på siden Udlign posteringer](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="b49b9-129">Beløbet for den afledte A-skat trækkes fra kreditorbetalingen og bogføres på kontoen for **A-skattekonto** i et relateret bilag.</span><span class="sxs-lookup"><span data-stu-id="b49b9-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![A-skattekonto, der viser et relateret bilag](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]