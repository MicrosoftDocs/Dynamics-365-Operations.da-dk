---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (1. oktober 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 15b5fd7095a62aa9b7b79ebfcada667959b756aa
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "858738"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="353aa-103">Nyheder eller ændringer i Dynamics 365 for Talent Core HR (1. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="353aa-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="353aa-104">**Build 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="353aa-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="353aa-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="353aa-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="353aa-106">Slå validering af elektroniske betalinger fra</span><span class="sxs-lookup"><span data-stu-id="353aa-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="353aa-107">Validering af elektroniske betalingsoplysninger foretages, hvis du konfigurerer udbetalinger til direkte indbetaling enten via **Medarbejderselvbetjening**-arbejdsområdet (ESS) eller direkte i medarbejderformen.</span><span class="sxs-lookup"><span data-stu-id="353aa-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="353aa-108">Denne indstilling giver dig mulighed for at fjerne denne validering, hvis du ikke har brug valideringskontrol af beløb og resterende værdier.</span><span class="sxs-lookup"><span data-stu-id="353aa-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="353aa-109">Denne funktion er nyttig, hvis du integrerer med et eksternt lønsystem, der har andre krav.</span><span class="sxs-lookup"><span data-stu-id="353aa-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="353aa-110">Selvbetjening for leder - Tilføj mål for teammedlemmer via feltet Mål for teamperformance</span><span class="sxs-lookup"><span data-stu-id="353aa-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="353aa-111">Før denne version kan ledere føje mål til deres medarbejdere individuelt via performancemål, der er knyttet til hver medarbejder.</span><span class="sxs-lookup"><span data-stu-id="353aa-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="353aa-112">Med denne opdatering kan ledere få adgang til feltet **Mål for teamperformance** og oprette nye mål ved at vælge en af deres direkte underordnede.</span><span class="sxs-lookup"><span data-stu-id="353aa-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="353aa-113">Selvbetjening for leder - Tilføj evalueringer for teammedlemmer via feltet Evalueringer af teamperformance</span><span class="sxs-lookup"><span data-stu-id="353aa-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="353aa-114">Før denne version kan ledere føje evalueringer til deres medarbejdere individuelt via de evalueringer, der er knyttet til hver medarbejder.</span><span class="sxs-lookup"><span data-stu-id="353aa-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="353aa-115">Med denne opdatering kan ledere få adgang til feltet **Evalueringer af teamperformance** og oprette nye evalueringer ved at vælge en af deres direkte underordnede.</span><span class="sxs-lookup"><span data-stu-id="353aa-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="353aa-116">Konfigurer indstillinger for proportionalitet efter orlovsplan</span><span class="sxs-lookup"><span data-stu-id="353aa-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="353aa-117">Organisationer beregner fravær forskelligt afhængigt af, hvornår medarbejdere starter i eller forlader firmaet.</span><span class="sxs-lookup"><span data-stu-id="353aa-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="353aa-118">For visse organisationer får medarbejderne fuld tildeling på deres startdato, mens andre beregner bonus forholdsmæssigt.</span><span class="sxs-lookup"><span data-stu-id="353aa-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="353aa-119">Der findes nye indstillinger i denne version, så du kan vælge, hvordan forholdsmæssig bonus og periodisering beregnes for nytilkomne og afgående personer i en organisation.</span><span class="sxs-lookup"><span data-stu-id="353aa-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="353aa-120">Indstillingerne omfatter: Beregnet forholdsmæssigt, Fuld periodisering og Ingen periodisering.</span><span class="sxs-lookup"><span data-stu-id="353aa-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="353aa-121">Andre ændringer</span><span class="sxs-lookup"><span data-stu-id="353aa-121">Other changes</span></span>

-   <span data-ttu-id="353aa-122">Medarbejderenhed opdateret – Titlen **Personligt** kan nu opdateres ved hjælp af Excel-tilføjelsesprogram/datastyring.</span><span class="sxs-lookup"><span data-stu-id="353aa-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="353aa-123">Sikkerhedsændring, der tillader fjernelse af knapperne **Slet** og **Deaktiver** i medarbejderselvbetjeningens betalingsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="353aa-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="353aa-124">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="353aa-124">Known issue</span></span>

-   <span data-ttu-id="353aa-125">**Problem:** Når du føjer en ny vedhæftet fil til en arbejder, bliver **Ny**- og **Rediger**-knapperne nedtonede. **Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukkede.</span><span class="sxs-lookup"><span data-stu-id="353aa-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="353aa-126">Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil **Vedhæftede filer**-knapperne blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="353aa-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="353aa-127">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="353aa-127">(This issue will be fixed in the next platform update.)</span></span>
