---
title: A-skat i salgstransaktioner
description: I dette emne kan du se, hvordan du undgår at beregne A-skat for udvalgte kunder. For kunder, der angiver A-skat i deres betalinger til dig, kan du tildele standardgruppen for A-skat.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c839df1b54cdb60beefa6dc6c3fc6e945a6eac85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256637"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="c07a3-104">A-skat i salgstransaktioner</span><span class="sxs-lookup"><span data-stu-id="c07a3-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="c07a3-105">I dette emne kan du se, hvordan du undgår at beregne A-skat for udvalgte kunder.</span><span class="sxs-lookup"><span data-stu-id="c07a3-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="c07a3-106">For kunder, der angiver A-skat i deres betalinger til dig, kan du tildele standardgruppen for **A-skattegruppe** på siden **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="c07a3-107">Gå til **Navigationsrude > Moduler > Debitor > Kunder > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="c07a3-108">Klik på den pågældende debitorkonto, og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="c07a3-109">Angiv **Ja** i feltet **Beregn A-skat** på fanen **Faktura og levering**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="c07a3-110">A-skat beregnes ikke, hvis **Beregn A-skat** ikke er aktiveret for denne kunde i leverandør i masterdata.</span><span class="sxs-lookup"><span data-stu-id="c07a3-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="c07a3-111">Vælg en A-skattegruppe i **A-skattegruppen**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="c07a3-112">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-112">Click **Save**.</span></span>

<span data-ttu-id="c07a3-113">For varer/tjenester, der er ansvarlige for A-skat, kan du tildele standardgruppen for **Varer i A-skattegruppe** i **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="c07a3-114">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Produkter > Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="c07a3-115">Klik på det pågældende elementnummer og klik på **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="c07a3-116">Klik på **Beregn A-skat** på fanen **Sælg**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="c07a3-117">A-skat beregnes ikke, hvis **Beregn A-skat** ikke er angivet til **Ja** for denne vare under fanen **Sælg** på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="c07a3-118">Vælg et element i A-skattegruppe på listen **Element i A-skattegruppe**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="c07a3-119">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-119">Click **Save**.</span></span>

<span data-ttu-id="c07a3-120">A-skattegrupper og A-skattegrupper for varer kan tildeles ved hjælp af siden **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="c07a3-121">Standardgruppen for A-skat og A-skattegruppen for varer bruges som standardposter på salgsordrelinjer, når du opretter en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="c07a3-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="c07a3-122">A-skat beregnes og bogføres sammen med **Debitorbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="c07a3-123">Du kan manuelt justere den relevante kode for A-skat og det faktiske beløb for A-skat under fanen **A-skat** på siden **Afregn posteringer**.</span><span class="sxs-lookup"><span data-stu-id="c07a3-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="c07a3-124">Beløbet for den beregnede A-skat trækkes fra kundebetalingen og bogføres på kontoen for **A-skatteforskydning** i et relateret bilag.</span><span class="sxs-lookup"><span data-stu-id="c07a3-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]