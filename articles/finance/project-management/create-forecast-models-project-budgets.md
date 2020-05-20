---
title: Oprette budgetmodeller for projektbudgetter
description: I dette emne beskrives, hvordan du opretter en budgetmodel for resterende budgetter.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321773"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="38c18-103">Oprette budgetmodeller for projektbudgetter</span><span class="sxs-lookup"><span data-stu-id="38c18-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38c18-104">I dette emne beskrives, hvordan du opretter en budgetmodel for resterende budgetter.</span><span class="sxs-lookup"><span data-stu-id="38c18-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="38c18-105">I et projekt, der er underlagt budgetstyring, bruges to typer af budgetter: oprindeligt og resterende.</span><span class="sxs-lookup"><span data-stu-id="38c18-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="38c18-106">Når du opretter et projektbudget, skal du angive de budgetmodeller for det oprindelige og det resterende budget, der er oprettet på siden **Budgetmodeller**.</span><span class="sxs-lookup"><span data-stu-id="38c18-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="38c18-107">Der oprettes projektbudgetter på basis af de angivne modeller, når du gør projektbudgettet bindende.</span><span class="sxs-lookup"><span data-stu-id="38c18-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="38c18-108">En budgetmodel, der bruges til budgetstyring, kan ikke have en undermodel eller bruges som undermodel.</span><span class="sxs-lookup"><span data-stu-id="38c18-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="38c18-109">Vælg **Projektstyring og regnskab** > **Konfiguration** > **Budgetter**  > **Budgetmodeller**.</span><span class="sxs-lookup"><span data-stu-id="38c18-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="38c18-110">Vælg **Ny** for at oprette en ny budgetmodel, og angiv derefter et id-nummer på den nye model og et navn til den.</span><span class="sxs-lookup"><span data-stu-id="38c18-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="38c18-111">Angiv indstillingen **Stoppet** til **Ja** for at forhindre ændringer af budgetlinjer i budgetmodellen.</span><span class="sxs-lookup"><span data-stu-id="38c18-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="38c18-112">Hvis du vil generere likviditetsbudgetter i finans med de budgetlinjer, som er tilknyttet modellen, skal du angive **Medtage budgetter i likviditetsbudgetter** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="38c18-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="38c18-113">Hvis du vil bruge projektdatoen som fakturadatoen, skal du angive **Budgetfakturadato** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="38c18-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="38c18-114">Vælg en af følgende modeltyper i feltet **Budgettype**:</span><span class="sxs-lookup"><span data-stu-id="38c18-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="38c18-115">**Oprindeligt budget**: Brug denne modeltype til de oprindelige budgetbeløb, der bliver bindende, når det indledende budget er oprettet og godkendt.</span><span class="sxs-lookup"><span data-stu-id="38c18-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="38c18-116">**Resterende budget**: Brug denne modeltype til de resterende budgetbeløb, så længe projektet løber.</span><span class="sxs-lookup"><span data-stu-id="38c18-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="38c18-117">Saldiene i denne budgetmodel reduceres med faktiske posteringer og forøges eller formindskes med budgetrevisioner.</span><span class="sxs-lookup"><span data-stu-id="38c18-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="38c18-118">**Overførsel**: Brug det overførte budgetbeløb for projektet.</span><span class="sxs-lookup"><span data-stu-id="38c18-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="38c18-119">Overførsel er en valgfri proces, der kan bruges til at overføre ikke-anvendte budgetbeløb fra ét regnskabsår til et andet.</span><span class="sxs-lookup"><span data-stu-id="38c18-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="38c18-120">Angiv følgende indstillinger efter behov:</span><span class="sxs-lookup"><span data-stu-id="38c18-120">Set the following options as required:</span></span>

   - <span data-ttu-id="38c18-121">Aktivér **Budgetfakturadato** for at bruge projektdatoen som fakturadatoen.</span><span class="sxs-lookup"><span data-stu-id="38c18-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="38c18-122">Aktivér **Budget med IGVA** for at foretage budgettering baseret på igangværende forarbejdning (IGVF), og vælg derefter IGVA-typen.</span><span class="sxs-lookup"><span data-stu-id="38c18-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="38c18-123">Du kan beholde den standardbaserede **Budgettype** som **Ingen** eller angive en ny type.</span><span class="sxs-lookup"><span data-stu-id="38c18-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="38c18-124">Budgettypen kan ikke ændres, når du har ændret en post.</span><span class="sxs-lookup"><span data-stu-id="38c18-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="38c18-125">Hvis du ændrer standardbudgettypen, er alle andre indstillinger ikke tilgængelige for opdateringer, og du kan ikke genbruge denne budgetmodel.</span><span class="sxs-lookup"><span data-stu-id="38c18-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

