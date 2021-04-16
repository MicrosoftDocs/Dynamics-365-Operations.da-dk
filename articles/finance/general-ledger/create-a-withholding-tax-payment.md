---
title: Oprette en betaling af A-skat
description: Jobproceduren betaling af A-skat afregner A-skatsaldi fra Kreditor på A-skatkonti og forskyder A-skat for en given periode. Dette emne indeholder en oversigt over trinene til opsætning af en betaling for A-skat.
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
ms.openlocfilehash: 72d80fbb3b2448f4b89fa7d7fa580387e1a3621c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832940"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="e0852-104">Oprette en betaling af A-skat</span><span class="sxs-lookup"><span data-stu-id="e0852-104">Create a withholding tax payment</span></span>

<span data-ttu-id="e0852-105">Jobproceduren betaling af A-skat afregner A-skatsaldi fra Kreditor på A-skatkonti og forskyder A-skat for en given periode.</span><span class="sxs-lookup"><span data-stu-id="e0852-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="e0852-106">Dette emne indeholder en oversigt over trinene til opsætning af en betaling for A-skat.</span><span class="sxs-lookup"><span data-stu-id="e0852-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="e0852-107">Der skal ikke tages højde for A-skat (fra debitorer), når der beregnes A-skat.</span><span class="sxs-lookup"><span data-stu-id="e0852-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="e0852-108">Gå til **Navigationsrude > Moduler > Skat > erklæringer > A-skat > Betaling til A-skat**.</span><span class="sxs-lookup"><span data-stu-id="e0852-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="e0852-109">Klik på rullelisten i feltet **Afregningsperiode** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e0852-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e0852-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e0852-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e0852-111">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="e0852-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="e0852-112">Angiv en dato i feltet **Transaktionsdato**.</span><span class="sxs-lookup"><span data-stu-id="e0852-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="e0852-113">Vælg **Opdater** for at bogføre betalingsbilaget for A-skat på afregningskontoen for A-skat.</span><span class="sxs-lookup"><span data-stu-id="e0852-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="e0852-114">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0852-114">Click **OK**.</span></span>

![Parametre for betaling af A-skat](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]