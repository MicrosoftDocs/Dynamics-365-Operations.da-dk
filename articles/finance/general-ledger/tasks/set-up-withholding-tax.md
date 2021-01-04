---
title: Konfigurere A-skat
description: Dette emne beskriver, hvordan du konfigurerer A-skat.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441469"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="18ffe-103">Konfigurere A-skat</span><span class="sxs-lookup"><span data-stu-id="18ffe-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18ffe-104">Dette emne beskriver, hvordan du konfigurerer A-skat.</span><span class="sxs-lookup"><span data-stu-id="18ffe-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="18ffe-105">*A-skat* er en skat på leverandører, der ikke opretter momstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="18ffe-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="18ffe-106">A-skat, der beregnes på leverandørbetalinger, er et passiv.</span><span class="sxs-lookup"><span data-stu-id="18ffe-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="18ffe-107">Derfor er det kun statuskonti eller passivkonti, der kan bruges til bogføring af A-skat.</span><span class="sxs-lookup"><span data-stu-id="18ffe-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="18ffe-108">Denne opgaveguide viser, hvordan du konfigurerer A-skat.</span><span class="sxs-lookup"><span data-stu-id="18ffe-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="18ffe-109">Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > A-skat > Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="18ffe-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-110">Select **New**.</span></span>
3. <span data-ttu-id="18ffe-111">Skrive en værdi i feltet **Koder for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="18ffe-112">Angiv navnet for koden for A-skat i feltet **Navn på A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="18ffe-113">Vælg hovedkontoen til bogføring af A-skattetilsvar i feltet **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="18ffe-114">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-114">Select **Save**.</span></span>
7. <span data-ttu-id="18ffe-115">Vælg **Værdier** og markér den ønskede post i listen.</span><span class="sxs-lookup"><span data-stu-id="18ffe-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="18ffe-116">Angiv en procentsats, der bruges til beregning af A-skat i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="18ffe-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-117">Select **Save**.</span></span>
10. <span data-ttu-id="18ffe-118">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18ffe-118">Close the page.</span></span>
11. <span data-ttu-id="18ffe-119">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-119">Select **Save**.</span></span>
12. <span data-ttu-id="18ffe-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18ffe-120">Close the page.</span></span>
13. <span data-ttu-id="18ffe-121">Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > A-skat > Grupper for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="18ffe-122">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-122">Select **New**.</span></span>
15. <span data-ttu-id="18ffe-123">Angiv identifikatoren for gruppen for A-skat i feltet **Grupper for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="18ffe-124">Skriv navnet på gruppen for A-skat i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="18ffe-125">Vælg kode for A-skat i feltet **Kode for A-skat**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="18ffe-126">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="18ffe-126">Select **Save**.</span></span>
19. <span data-ttu-id="18ffe-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18ffe-127">Close the page.</span></span>

