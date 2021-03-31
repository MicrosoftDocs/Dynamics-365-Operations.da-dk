---
title: Oprette et budget ud fra posteringskonti og totalkonti
description: Denne artikel indeholder en oversigt over processen til at oprette budgetter baseret på totalkonti. Der beskrives også, hvordan du aktiverer budgetstyring for totalkonti, hvis budgetstyring er påkrævet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 085bc12433616d2da2bda40a8412fb88e40db3b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210187"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="519f5-104">Oprette et budget ud fra posteringskonti og totalkonti</span><span class="sxs-lookup"><span data-stu-id="519f5-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="519f5-105">Denne artikel indeholder en oversigt over processen til at oprette budgetter baseret på totalkonti.</span><span class="sxs-lookup"><span data-stu-id="519f5-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="519f5-106">Der beskrives også, hvordan du aktiverer budgetstyring for totalkonti, hvis budgetstyring er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="519f5-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="519f5-107">Både budgetplanen og dokumenter med budgetregisterposter giver mulighed for budgettering på hovedkonti, som har hovedkontotypen **Total**.</span><span class="sxs-lookup"><span data-stu-id="519f5-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="519f5-108">Faktiske kan kun bogføres til hovedkonti med transaktioner.</span><span class="sxs-lookup"><span data-stu-id="519f5-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="519f5-109">For den periodiske proces **Generér budgetplan fra finanskonto** under fanen **Kilde** kan du angive hovedkontotypen **Total** som et kriterium.</span><span class="sxs-lookup"><span data-stu-id="519f5-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="519f5-110">I så fald medtages hver totalhovedkonto i målbudgetplanen, og beløbet vil være lig med det samlede beløb for intervallet af de markerede hovedkonti.</span><span class="sxs-lookup"><span data-stu-id="519f5-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="519f5-111">Du kan aktivere budgetstyring for hovedkonti af typen **Total**.</span><span class="sxs-lookup"><span data-stu-id="519f5-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="519f5-112">Denne funktionalitet understøttes ved hjælp af budgetgrupper.</span><span class="sxs-lookup"><span data-stu-id="519f5-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="519f5-113">For hver totalhovedkonto skal det budget, der skal kontrolleres for en budgetgruppe, være oprettet på siden **Konfiguration af budgetstyring**.</span><span class="sxs-lookup"><span data-stu-id="519f5-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="519f5-114">De kriterier, du angiver, skal omfatte totalhovedkontoen og intervallet af konti.</span><span class="sxs-lookup"><span data-stu-id="519f5-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="519f5-115">For at fremskynde oprettelsen af budgetgrupper kan du udnytte fordelen ved budgetkontrolgruppernes dataenhed.</span><span class="sxs-lookup"><span data-stu-id="519f5-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="519f5-116">Når et budget bruges til rapportering, f.eks. i et regnskab, består budgetsummen for totalkontoen af følgende beløb:</span><span class="sxs-lookup"><span data-stu-id="519f5-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="519f5-117">De budgetter, der er oprettet ud fra de enkelte posteringsfinanskonti i totalkontoens interval.</span><span class="sxs-lookup"><span data-stu-id="519f5-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="519f5-118">Det budgetbeløb, der direkte er angivet på totalkontoen.</span><span class="sxs-lookup"><span data-stu-id="519f5-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="519f5-119">Derfor kan du oprette separate budgetter for de væsentligste posteringskonti i totalkontoens interval og derefter føje det tilgængelige budgetbeløb til totalkontoen.</span><span class="sxs-lookup"><span data-stu-id="519f5-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]