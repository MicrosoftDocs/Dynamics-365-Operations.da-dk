---
title: Oprette vedligeholdelsesbudgetter
description: Dette emne forklarer, hvordan du opretter et vedligeholdelsesbudget i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2c748fd230796643f1ed6279743da532e7cb320
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874802"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="0e8be-103">Oprette vedligeholdelsesbudgetter</span><span class="sxs-lookup"><span data-stu-id="0e8be-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]



<span data-ttu-id="0e8be-104">Vedligeholdelsesbudgetter bruges til at give en oversigt over forventede omkostninger ved forebyggende vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="0e8be-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="0e8be-105">Budgetlinjer beregnes på basis af linjer i vedligeholdelsestidsplanen, der har en forventet startdato i budgetperioden.</span><span class="sxs-lookup"><span data-stu-id="0e8be-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="0e8be-106">Vedligeholdelsesbudgetter er baseret på de omkostningstyper, der bruges i aktivstyring: **Præventiv**, **Korrigerende** og **Investering**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="0e8be-107">Budgetomkostninger for investeringsvedligeholdelse medtages for aktive aktiver, der har en erstatningsdato i løbet af budgetperioden og en relateret erstatningsværdi.</span><span class="sxs-lookup"><span data-stu-id="0e8be-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="0e8be-108">Budgetomkostninger for korrigerende vedligeholdelse medtages, hvis en tidligere korrektionsdato er inkluderet i budgetberegningen.</span><span class="sxs-lookup"><span data-stu-id="0e8be-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="0e8be-109">I dette tilfælde beregnes korrigerende omkostninger fra en tidligere periode for den samme fremtidige periode, som du beregner vedligeholdelsesbudgettet for.</span><span class="sxs-lookup"><span data-stu-id="0e8be-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="0e8be-110">Oprette et vedligeholdelsesbudget</span><span class="sxs-lookup"><span data-stu-id="0e8be-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="0e8be-111">Vælg **Styring af aktiver** \> **Forespørgsler** \> **Vedligeholdelsesbudget** \> **Budget**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="0e8be-112">Vælg **Opret budget**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="0e8be-113">I feltet **Vedligeholdelsesbudget** skal du indtaste et budget-id.</span><span class="sxs-lookup"><span data-stu-id="0e8be-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="0e8be-114">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0e8be-115">Angiv start- og slutdatoerne for budgetperioden i felterne **Fra-dato** og **Til-dato** i oversigtspanelet **Periode**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="0e8be-116">Hvis du vil medtage korrigerende budgetomkostninger, der beregnes på grundlag af faktiske omkostninger fra en tidligere periode, skal du angive startdatoen for den periode, som disse omkostninger skal medtages fra, i feltet **Korrigerende fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="0e8be-117">Afhængigt af det detaljeringsniveau, der kræves i budgettet, skal du angive de relevante indstillinger i de fem oversigtspaneler **Gruppér efter**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="0e8be-118">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-118">Select **OK**.</span></span>
8. <span data-ttu-id="0e8be-119">Vælg **Budgetlinjer** for at åbne siden **Vedligeholdelsesbudgetlinjer**, hvor du kan få vist alle de budgetlinjer, der er oprettet for perioden.</span><span class="sxs-lookup"><span data-stu-id="0e8be-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="0e8be-120">Hvis du vil godkende budgettet, skal du vælge det på siden **Vedligeholdelsesbudgetter** og derefter vælge **Godkend**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="0e8be-121">Vælg derefter **OK** i dialogboksen **Godkend budget**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="0e8be-122">Dit navn angives i feltet **Godkendt af** på siden **Vedligeholdelse budgetter**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0e8be-123">Når du har godkendt et vedligeholdelsesbudget, kan du ikke genberegne eller regulere de relaterede linjer på siden **Vedligeholdelsesbudgetlinjer**, medmindre du først har fjernet godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="0e8be-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="0e8be-124">Hvis du vil fjerne godkendelsen af et vedligeholdelsesbudget, skal du vælge det på siden **Vedligeholdelsesbudgetter** og derefter vælge **Godkend**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="0e8be-125">Vælg derefter **OK** i dialogboksen **Godkend budget**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Figur 1](media/01-maintenance-budgets.png)

<span data-ttu-id="0e8be-127">Du kan også oprette et nyt vedligeholdelsesbudget ved at kopiere et eksisterende budget.</span><span class="sxs-lookup"><span data-stu-id="0e8be-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="0e8be-128">Vælg det budget, du vil kopiere, på siden **Vedligeholdelsesbudgetter**, og vælg derefter **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="0e8be-129">Denne fremgangsmåde er nyttig, hvis du f.eks. har oprettet et budget for én måned og vil kopiere det til andre måneder.</span><span class="sxs-lookup"><span data-stu-id="0e8be-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="0e8be-130">Vedligeholdelsesbudgettet beregner kun budgetomkostninger baseret på vedligeholdelsestidsplanslinjer.</span><span class="sxs-lookup"><span data-stu-id="0e8be-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="0e8be-131">Hvis du vil beregne faktiske omkostninger for den samme periode, kan du udføre denne beregning på siden **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="0e8be-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
