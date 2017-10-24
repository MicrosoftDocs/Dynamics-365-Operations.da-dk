--- 
title: Oprette en momsbetaling
description: "Jobbet Afregn og bogfør moms afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ee84da7fd055c8b0b50c43f134c0fc048ecfaeb
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="de4a6-103">Oprette en momsbetaling</span><span class="sxs-lookup"><span data-stu-id="de4a6-103">Create a sales tax payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de4a6-104">Jobbet Afregn og bogfør moms afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode.</span><span class="sxs-lookup"><span data-stu-id="de4a6-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="de4a6-105">Gå til Moms > Opgørelser > Moms > Afregn og bogfør moms.</span><span class="sxs-lookup"><span data-stu-id="de4a6-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="de4a6-106">Klik på rullelisten i feltet Afregningsperiode for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="de4a6-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="de4a6-107">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="de4a6-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="de4a6-108">Indtast en dato i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="de4a6-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="de4a6-109">Hvis indstillingen Medtag korrektioner ikke er markeret på siden Finansparametre, kan afregningen behandles for forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="de4a6-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="de4a6-110">Oprindelig er den første afregning for et periodeinterval og kan kun behandles én gang for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="de4a6-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="de4a6-111">Seneste rettelser udligner momsposteringer, der er bogført efter den oprindelige version er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="de4a6-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="de4a6-112">Angiv en dato i feltet Transaktionsdato.</span><span class="sxs-lookup"><span data-stu-id="de4a6-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="de4a6-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="de4a6-113">Click OK.</span></span>


