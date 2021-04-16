---
title: Projektregnskab med generelle budgetreservationer
description: Dette emne indeholder oplysninger om projektregnskab, der bruger generelle budgetreservationer til den offentlige sektor.
author: AlexRenney
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetReservation_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0de631891e2ec146541218be2569f92f53f12ca8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820462"
---
# <a name="project-accounting-with-general-budget-reservations"></a><span data-ttu-id="b7b65-103">Projektregnskab med generelle budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="b7b65-103">Project accounting with general budget reservations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b65-104">Hvis din organisation bruger projektregnskab, kan du medtage referencer til dit projekt i generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="b7b65-104">If your organization uses project accounting, you can include references to your project in general budget reservations.</span></span> <span data-ttu-id="b7b65-105">Disse referencer kan påvirke budgettering, bindende omkostninger og reservationer og forbrug af finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="b7b65-105">These references can affect budgeting, committed costs, and the reservation and consumption of funding sources.</span></span>

<span data-ttu-id="b7b65-106">Nogle udgifter er planlagt til at blive faktureres til projekter.</span><span class="sxs-lookup"><span data-stu-id="b7b65-106">Some expenditures are planned to be charged to projects.</span></span> <span data-ttu-id="b7b65-107">Når du opretter en generel budgetreservation, kan du angive det , at det projekt og den projektkategori, som et planlagt indkøb er til.</span><span class="sxs-lookup"><span data-stu-id="b7b65-107">When you create a general budget reservation, you can specify the project and project category that a planned purchase is for.</span></span> <span data-ttu-id="b7b65-108">Du kan også angive andre projektrelaterede oplysninger, f.eks. den forventede salgspris.</span><span class="sxs-lookup"><span data-stu-id="b7b65-108">You can also specify other project-related information, such as the expected sales price.</span></span> <span data-ttu-id="b7b65-109">(For enheder i den offentlige sektor er den forventede salgspris typisk kostprisen). Alle disse oplysninger findes i de indkøbsdokumenter, der genereres for projekter senere.</span><span class="sxs-lookup"><span data-stu-id="b7b65-109">(For public sector entities, the expected sales price is typically the cost price.) All this information is included on the purchasing documents that are generated for projects later.</span></span>

<span data-ttu-id="b7b65-110">Hvis den generelle budgetreservation indeholder en projektfordeling, skal den købsordre, indkøbsrekvisition eller en kreditorfaktura, der henviser til reservationen, omfatte projektfordelingen og alle projektoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b7b65-110">If the general budget reservation contains a project distribution, the purchase order, purchase requisition, or vendor invoice that references the reservation must include the project distribution and all project information.</span></span> <span data-ttu-id="b7b65-111">Disse oplysninger kopieres automatisk til kildedokumentet fra den generelle budgetreservation.</span><span class="sxs-lookup"><span data-stu-id="b7b65-111">This information is automatically copied to the source document from the general budget reservation.</span></span>

## <a name="turn-on-tracking-of-committed-costs-for-general-budget-reservations"></a><span data-ttu-id="b7b65-112">Aktivere sporing af bindende omkostninger for generelle budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="b7b65-112">Turn on tracking of committed costs for general budget reservations</span></span>

<span data-ttu-id="b7b65-113">Bindende projektomkostninger oprettes, når købsdokumenterne er godkendt, bekræftet eller bogført.</span><span class="sxs-lookup"><span data-stu-id="b7b65-113">Project committed costs are created when purchasing documents are approved, confirmed, or posted.</span></span> <span data-ttu-id="b7b65-114">Omkostningerne repræsenterer beløb, der skal bruges på et projekt.</span><span class="sxs-lookup"><span data-stu-id="b7b65-114">The costs represent amounts that will be spent on a project.</span></span> <span data-ttu-id="b7b65-115">Projektledere kan få vist ventende omkostninger for et projekt for at spore nøjagtige oplysninger om deres projektomkostninger.</span><span class="sxs-lookup"><span data-stu-id="b7b65-115">Project managers can view pending costs for a project to track accurate information about their project's costs.</span></span>

1. <span data-ttu-id="b7b65-116">Gå til **Projektstyring og regnskab \> Opsætning \> Parametre for projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-116">Go to **Project management and accounting \> Setup \> Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="b7b65-117">Under fanen **Omkostningsstyring** i oversigtspanelet **Udgiftsforpligtelser** skal du vælge **Ja** i indstillingen **Generel budgetreservation**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-117">On the **Cost control** tab, on the **Cost commitments** FastTab, set the **General budget reservation** option to **Yes**.</span></span>

    - <span data-ttu-id="b7b65-118">Indstillingerne **Indkøbsrekvisition**, **Indkøbsordre** og **Kreditorfaktura** bliver automatisk indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-118">The **Purchase requisition**, **Purchase order**, and **Vendor invoice** options will automatically be set to **Yes**.</span></span>
    - <span data-ttu-id="b7b65-119">Når den generelle budgetreservation er bogført, tæller den med i projektets bindende omkostninger.</span><span class="sxs-lookup"><span data-stu-id="b7b65-119">When the general budget reservation is posted, it will be counted in the project's committed costs.</span></span>

## <a name="specify-project-information-in-a-general-budget-reservation"></a><span data-ttu-id="b7b65-120">Angive projektoplysninger i en generel budgetreservation</span><span class="sxs-lookup"><span data-stu-id="b7b65-120">Specify project information in a general budget reservation</span></span>

1. <span data-ttu-id="b7b65-121">Gå til **Budgettering \> Generelle budgetreservationer**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-121">Go to **Budgeting \> General budget reservations**.</span></span>
2. <span data-ttu-id="b7b65-122">Opret en generel budgetreservation.</span><span class="sxs-lookup"><span data-stu-id="b7b65-122">Create a general budget reservation.</span></span>
3. <span data-ttu-id="b7b65-123">Tilføj et projekt-id og en projektkategori for hver relevant reservationslinje i oversigtspanelet **Generelle budgetreservationslinjer**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-123">On the **General budget reservation lines** FastTab, add a project ID and project category for each applicable reservation line.</span></span> <span data-ttu-id="b7b65-124">Oplysninger fra projektet kopieres automatisk til reservationen.</span><span class="sxs-lookup"><span data-stu-id="b7b65-124">Information from the project will automatically be copied to the reservation.</span></span>
4. <span data-ttu-id="b7b65-125">Valgfrit: Hvis du vil have vist projektdetaljerne, skal du vælge fanen **Projekt** i oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-125">Optional: To view the project details, on the **Line details** FastTab, select the **Project** tab.</span></span>

## <a name="view-project-committed-costs-for-a-general-budget-reservation"></a><span data-ttu-id="b7b65-126">Få vist bindende projektomkostninger for en generel budgetreservation</span><span class="sxs-lookup"><span data-stu-id="b7b65-126">View project committed costs for a general budget reservation</span></span>

<span data-ttu-id="b7b65-127">Når du bogfører en generel budgetreservation for et projekt, oprettes der en bindende omkostning for reservationsbeløbet i forhold til projektet.</span><span class="sxs-lookup"><span data-stu-id="b7b65-127">When you post a general budget reservation for a project, a committed cost is created for the reservation amount against that project.</span></span> <span data-ttu-id="b7b65-128">Den bindende omkostning repræsenterer det samlede beløb for fordelingerne til det pågældende projekt.</span><span class="sxs-lookup"><span data-stu-id="b7b65-128">The committed cost represents the total amount of the distributions to that project.</span></span>

1. <span data-ttu-id="b7b65-129">Gå til **Budgettering \> Generelle budgetreservationer**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-129">Go to **Budgeting \> General budget reservations**.</span></span>
2. <span data-ttu-id="b7b65-130">Åbn den ønskede bogførte generelle budgetreservation, og vælg en reservationslinje.</span><span class="sxs-lookup"><span data-stu-id="b7b65-130">Open the posted general budget reservation that you want, and select a reservation line.</span></span>
3. <span data-ttu-id="b7b65-131">Vælg **Bindende omkostninger**.</span><span class="sxs-lookup"><span data-stu-id="b7b65-131">Select **Committed costs**.</span></span> <span data-ttu-id="b7b65-132">Siden **Bindende omkostninger** åbnes og viser de bindende omkostninger, der er relateret til den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="b7b65-132">The **Committed costs** page appears and shows the committed costs that are related to the selected line.</span></span>

    <span data-ttu-id="b7b65-133">Bindende omkostninger for generelle budgetreservationer er baseret på beløb, uanset om den bindende omkostning indeholder et bestemt antal og kostpris.</span><span class="sxs-lookup"><span data-stu-id="b7b65-133">Committed costs for general budget reservations are based on amount, regardless of whether the committed cost includes a discrete quantity and unit cost.</span></span> <span data-ttu-id="b7b65-134">Antallet for bindende omkostninger vil altid være 1.</span><span class="sxs-lookup"><span data-stu-id="b7b65-134">The committed cost quantity will always be 1.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]