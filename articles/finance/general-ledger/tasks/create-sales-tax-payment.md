---
title: Oprette en momsbetaling
description: Jobbet Afregn og bogfør momsprocedurer afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9523ef75953bdca36f509f596c51c08b12b3fdb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254457"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="e6e71-103">Oprette en momsbetaling</span><span class="sxs-lookup"><span data-stu-id="e6e71-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6e71-104">Jobbet Afregn og bogfør momsprocedurer afregner momssaldi i momskonti og udligner dem til momsafregningskontoen for en given periode.</span><span class="sxs-lookup"><span data-stu-id="e6e71-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="e6e71-105">Gå til **Moms > Opgørelser > Moms > Afregn og bogfør moms**.</span><span class="sxs-lookup"><span data-stu-id="e6e71-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="e6e71-106">Klik på rullelisten i feltet **Afregningsperiode** for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="e6e71-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e6e71-107">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e6e71-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e6e71-108">Indtast en dato i feltet **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="e6e71-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="e6e71-109">Hvis indstillingen **Medtag korrektioner** ikke er markeret på siden **Finansparametre**, kan afregningen behandles for forskellige versioner.</span><span class="sxs-lookup"><span data-stu-id="e6e71-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="e6e71-110">Oprindelig er den første afregning for et periodeinterval og kan kun behandles én gang for et periodeinterval.</span><span class="sxs-lookup"><span data-stu-id="e6e71-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="e6e71-111">De seneste rettelser udligner momsposteringer, der er bogført efter den oprindelige version er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="e6e71-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="e6e71-112">Angiv en dato i feltet **Transaktionsdato**.</span><span class="sxs-lookup"><span data-stu-id="e6e71-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="e6e71-113">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6e71-113">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]