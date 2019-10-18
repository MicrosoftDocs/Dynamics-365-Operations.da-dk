---
title: Beregne og justere moms på en kreditorfaktura
description: Dette emne forklarer, hvordan du justerer moms på en kreditorfaktura i Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186273"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="65582-103">Beregne og justere moms på en kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="65582-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65582-104">Dette emne forklarer, hvordan du justerer moms på en kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="65582-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="65582-105">Hvis det oprindelige kildedokument viser forskellige momsbeløb som beregnet, kan du justere beløbene, før der bogføres.</span><span class="sxs-lookup"><span data-stu-id="65582-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="65582-106">Denne opgave bruger demofirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="65582-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="65582-107">Gå til **Moduler > Kreditorer > Fakturaer > Fakturajournal** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="65582-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="65582-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="65582-108">Select **New**.</span></span>
3. <span data-ttu-id="65582-109">Vælg en indstilling i rullemenuen i feltet **Navn** i den nye række.</span><span class="sxs-lookup"><span data-stu-id="65582-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="65582-110">Gå til handlingsruden, og vælg **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="65582-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="65582-111">I feltet **Konto** skal du angive de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="65582-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="65582-112">Skriv en værdi i feltet **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="65582-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="65582-113">Angiv et tal i feltet **Kredit**.</span><span class="sxs-lookup"><span data-stu-id="65582-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="65582-114">I feltet **Modkonto** skal du specificere de ønskede værdier.</span><span class="sxs-lookup"><span data-stu-id="65582-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="65582-115">Vælg **Moms**.</span><span class="sxs-lookup"><span data-stu-id="65582-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="65582-116">Indtast et tal i feltet **Samlede faktiske momsbeløb**.</span><span class="sxs-lookup"><span data-stu-id="65582-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="65582-117">Under fanen **Regulering** kan momsbeløbene justeres pr. momskode</span><span class="sxs-lookup"><span data-stu-id="65582-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="65582-118">Vælg **Nulstil faktiske beløb fra til beregnede beløb**.</span><span class="sxs-lookup"><span data-stu-id="65582-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="65582-119">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65582-119">Select **OK**.</span></span>
14. <span data-ttu-id="65582-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="65582-120">Select **Save**.</span></span>

