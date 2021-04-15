---
title: Opdatere vedligeholdelsesbudgetter
description: Dette emne forklarer, hvordan du opdaterer et vedligeholdelsesbudget i Styring af aktiver.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 01620e1cca17d3c2b08b3abcdf9a4482693f0409
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809824"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="44a62-103">Opdatere vedligeholdelsesbudgetter</span><span class="sxs-lookup"><span data-stu-id="44a62-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="44a62-104">Siden **Vedligeholdelsesbudgetlinjer** viser alle de budgetlinjer, der er oprettet for det budget, der er valgt på siden **Vedligeholdelsesbudgetter**.</span><span class="sxs-lookup"><span data-stu-id="44a62-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="44a62-105">(Yderligere oplysninger finder du under [Oprette vedligeholdelsesbudgetter](create-maintenance-budget.md)). Du kan genberegne og regulere vedligeholdelsesbudgetlinjer, indtil vedligeholdelsesbudgettet er godkendt.</span><span class="sxs-lookup"><span data-stu-id="44a62-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="44a62-106">Når budgetperioden er overskredet, og omkostningerne er bogført i Styring af aktiver, kan du også opdatere budgetlinjerne med faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="44a62-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="44a62-107">Genberegne et vedligeholdelsesbudget</span><span class="sxs-lookup"><span data-stu-id="44a62-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="44a62-108">Du kan genberegne et vedligeholdelsesbudget på siden **Vedligeholdelsesbudgetlinjer**.</span><span class="sxs-lookup"><span data-stu-id="44a62-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="44a62-109">Når du genberegner et vedligeholdelsesbudget, slettes de eksisterende budgetlinjer, og der udføres en ny beregning.</span><span class="sxs-lookup"><span data-stu-id="44a62-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="44a62-110">Vælg **Genberegn** på siden **Vedligeholdelsesbudgetlinjer**.</span><span class="sxs-lookup"><span data-stu-id="44a62-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="44a62-111">Foretag de nødvendige ændringer for den nye beregning i dialogboksen **Genberegn budget**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="44a62-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="44a62-112">Nye budgetlinjer oprettes ud fra de værdier, du angiver.</span><span class="sxs-lookup"><span data-stu-id="44a62-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="44a62-113">Justere budgetlinjer</span><span class="sxs-lookup"><span data-stu-id="44a62-113">Adjust budget lines</span></span>

<span data-ttu-id="44a62-114">I stedet for at genberegne hele vedligeholdelsesbudgettet kan du regulere udvalgte linjer, der er relateret til budgetomkostninger.</span><span class="sxs-lookup"><span data-stu-id="44a62-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="44a62-115">Vælg de linjer, som budgetomkostningerne skal opdateres for, på siden **Vedligeholdelsesbudgetlinjer**.</span><span class="sxs-lookup"><span data-stu-id="44a62-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="44a62-116">Vælg **Juster**.</span><span class="sxs-lookup"><span data-stu-id="44a62-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="44a62-117">Hvis du vil føje et beløb til de valgte linjer, skal du markere afkrydsningsfeltet **Tilføj omkostninger** og derefter angive værdien i feltet **Tilføj værdi**.</span><span class="sxs-lookup"><span data-stu-id="44a62-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="44a62-118">Hvis du vil gange budgetomkostningen på de valgte budgetlinjer med en faktor, skal du markere afkrydsningsfeltet **Multiplicer omkostninger** og angive faktoren i feltet **Multiplikationsværdi**.</span><span class="sxs-lookup"><span data-stu-id="44a62-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="44a62-119">Hvis du f.eks. indtaster **1,2** i feltet **Multiplikationsværdi**, øger du budgetomkostningerne på de valgte linjer med 20 procent.</span><span class="sxs-lookup"><span data-stu-id="44a62-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="44a62-120">Hvis du angiver **0,7**, reducerer du budgetomkostningerne på de valgte linjer med 30 procent.</span><span class="sxs-lookup"><span data-stu-id="44a62-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="44a62-121">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="44a62-121">Select **OK**.</span></span>

<span data-ttu-id="44a62-122">De valgte budgetlinjer opdateres i henhold til de værdier, du angiver i trin 3 eller 4.</span><span class="sxs-lookup"><span data-stu-id="44a62-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="44a62-123">Opdatere faktiske omkostninger</span><span class="sxs-lookup"><span data-stu-id="44a62-123">Update actual costs</span></span>

<span data-ttu-id="44a62-124">Når datoerne på budgetlinjerne er overskredet, og faktiske omkostninger er bogført i Styring af aktiver, kan du opdatere vedligeholdelsesbudgettet med de faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="44a62-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="44a62-125">Vælg **Opdater omkostning** på siden **Vedligeholdelsesbudgetlinjer**.</span><span class="sxs-lookup"><span data-stu-id="44a62-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="44a62-126">Vælg **OK** i dialogboksen **Beregn faktiske omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="44a62-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="44a62-127">Felterne for **Faktiske omkostninger** på budgetlinjerne opdateres, hvis de faktiske omkostninger er blevet bogført.</span><span class="sxs-lookup"><span data-stu-id="44a62-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="44a62-128">Der kan genereres nye budgetlinjer, hvis der er oprettet nye aktivtyper, siden du oprettede budgettet, og om disse aktivtyper er blevet brugt på aktiver, der er oprettet arbejdsordrer for, og hvor der er blevet bogført relaterede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="44a62-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="44a62-129">Nye budgetlinjer viser kun faktiske omkostninger, da der ikke er beregnet budgetomkostninger for dem.</span><span class="sxs-lookup"><span data-stu-id="44a62-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="44a62-130">Hvis du vil have vist en oversigt over de faktiske omkostninger inddelt i forebyggende og korrigerende omkostninger og investeringsomkostninger, kan du foretage en beregning for den samme periode på siden **Omkostningsstyring for aktiv**.</span><span class="sxs-lookup"><span data-stu-id="44a62-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="44a62-131">Tilføje budgetlinjer manuelt</span><span class="sxs-lookup"><span data-stu-id="44a62-131">Manually add budget lines</span></span>

<span data-ttu-id="44a62-132">På siden **Vedligeholdelsesbudgetlinjer** kan du manuelt tilføje en ny budgetlinje ved at vælge **Ny** og derefter foretage valg på linjen.</span><span class="sxs-lookup"><span data-stu-id="44a62-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="44a62-133">Her er nogle eksempler på situationer, hvor denne metode kan være nyttig:</span><span class="sxs-lookup"><span data-stu-id="44a62-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="44a62-134">Du ved, at der i øjeblikket planlægges fornyelse af udstyr for nogle aktiver, men at der endnu ikke er oprettet relaterede job i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="44a62-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="44a62-135">Du vil dog gerne have, at budgetomkostninger for disse job skal indgå i vedligeholdelsesbudgettet.</span><span class="sxs-lookup"><span data-stu-id="44a62-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="44a62-136">Der er blevet oprettet nye aktiver eller aktivtyper, siden du lagde vedligeholdelsesbudgettet, men der er endnu ikke konfigureret vedligeholdelsesplaner for disse aktiver eller aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="44a62-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="44a62-137">Du vil dog gerne have, at budgetomkostninger for disse aktivtyper skal indgå i vedligeholdelsesbudgettet.</span><span class="sxs-lookup"><span data-stu-id="44a62-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]