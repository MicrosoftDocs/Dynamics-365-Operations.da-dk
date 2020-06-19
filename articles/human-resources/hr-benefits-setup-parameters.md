---
title: Angive parametre for administration af frynsegoder
description: Konfigurere parametre for administration af frynsegoder i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429977"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="7e88b-103">Angive parametre til administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="7e88b-103">Set Benefits management parameters</span></span>

<span data-ttu-id="7e88b-104">Før du kan oprette orlovsplaner i Microsoft Dynamics 365 Human Resources, skal du konfigurere parametre for administration af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="7e88b-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="7e88b-105">Disse parametre angiver standardværdier, årsagskoder og andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="7e88b-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="7e88b-106">Konfigurere generelle parametre</span><span class="sxs-lookup"><span data-stu-id="7e88b-106">Configure general parameters</span></span>

1. <span data-ttu-id="7e88b-107">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="7e88b-108">Angiv værdier for følgende felter under fanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="7e88b-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="7e88b-109">Felt</span><span class="sxs-lookup"><span data-stu-id="7e88b-109">Field</span></span> | <span data-ttu-id="7e88b-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7e88b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7e88b-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="7e88b-111">**Country/region**</span></span> | <span data-ttu-id="7e88b-112">Feltet **Land/område** bestemmer, hvilken visningsrækkefølgen for postnumre/stater.</span><span class="sxs-lookup"><span data-stu-id="7e88b-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="7e88b-113">Det valgte land vises først på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="7e88b-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="7e88b-114">**Årsagskode for tilmelding**</span><span class="sxs-lookup"><span data-stu-id="7e88b-114">**Enrollment reason code**</span></span> | <span data-ttu-id="7e88b-115">Vælg en standardårsagskode, der skal bruges, når der oprettes medarbejderplaner under behandling af en åben tilmelding.</span><span class="sxs-lookup"><span data-stu-id="7e88b-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="7e88b-116">**Årsagskode for annullering**</span><span class="sxs-lookup"><span data-stu-id="7e88b-116">**Cancellation reason code**</span></span> | <span data-ttu-id="7e88b-117">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres.</span><span class="sxs-lookup"><span data-stu-id="7e88b-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="7e88b-118">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="7e88b-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="7e88b-119">Brugerne kan eventuelt ændre den i **Årsagskode til annullering**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="7e88b-120">**Årsagskode for genåbning**</span><span class="sxs-lookup"><span data-stu-id="7e88b-120">**Reopen reason code**</span></span> | <span data-ttu-id="7e88b-121">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan genåbnes.</span><span class="sxs-lookup"><span data-stu-id="7e88b-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="7e88b-122">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="7e88b-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="7e88b-123">Brugerne kan eventuelt ændre den i **Åbn årsagskode igen**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="7e88b-124">**Årsagskode for livshændelse**</span><span class="sxs-lookup"><span data-stu-id="7e88b-124">**Life event reason code**</span></span> | <span data-ttu-id="7e88b-125">Den årsagskode, der skal bruges, når der indtræffer en livshændelse.</span><span class="sxs-lookup"><span data-stu-id="7e88b-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="7e88b-126">**Årsagskode for satsændring**</span><span class="sxs-lookup"><span data-stu-id="7e88b-126">**Rate change reason code**</span></span> | <span data-ttu-id="7e88b-127">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres og genåbnes under behandlingen af opdateret satsændring.</span><span class="sxs-lookup"><span data-stu-id="7e88b-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="7e88b-128">Den angiver, hvilke poster der er ændret af opdateringsprocessen for satsændringen.</span><span class="sxs-lookup"><span data-stu-id="7e88b-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="7e88b-129">**Ny ansættelse berettiget**</span><span class="sxs-lookup"><span data-stu-id="7e88b-129">**New hire eligible**</span></span> | <span data-ttu-id="7e88b-130">Angiver, om nyansatte er berettigede.</span><span class="sxs-lookup"><span data-stu-id="7e88b-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="7e88b-131">**Periode for tilmelding af nyansat**</span><span class="sxs-lookup"><span data-stu-id="7e88b-131">**New hire enrollment period**</span></span> | <span data-ttu-id="7e88b-132">Den tidsperiode, hvor tilmelding for den nyansatte er tilladt.</span><span class="sxs-lookup"><span data-stu-id="7e88b-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="7e88b-133">**Bemærk** Denne indstilling tilsidesætter en eventuel tilmeldingsperiode for nyansatte, som du angiver for berettigelsesreglen for planen.</span><span class="sxs-lookup"><span data-stu-id="7e88b-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="7e88b-134">**Livshændelser er aktiveret**</span><span class="sxs-lookup"><span data-stu-id="7e88b-134">**Life events enabled**</span></span> | <span data-ttu-id="7e88b-135">Aktiverer levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="7e88b-135">Enables life events.</span></span> |
   | <span data-ttu-id="7e88b-136">**Skjul formularer for ældre frynsegoder**</span><span class="sxs-lookup"><span data-stu-id="7e88b-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="7e88b-137">Giver dig mulighed for at skjule ældre frynsegodeformularer.</span><span class="sxs-lookup"><span data-stu-id="7e88b-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="7e88b-138">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="7e88b-139">Konfigurere parametre for medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="7e88b-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="7e88b-140">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="7e88b-141">Angiv værdier for følgende felter under fanen **Medarbejderselvbetjening**:</span><span class="sxs-lookup"><span data-stu-id="7e88b-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="7e88b-142">Felt</span><span class="sxs-lookup"><span data-stu-id="7e88b-142">Field</span></span> | <span data-ttu-id="7e88b-143">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="7e88b-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7e88b-144">**Frynsegodebekræftelse**</span><span class="sxs-lookup"><span data-stu-id="7e88b-144">**Benefit verification**</span></span> | <span data-ttu-id="7e88b-145">Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder.</span><span class="sxs-lookup"><span data-stu-id="7e88b-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="7e88b-146">**Vælg automatisk udpegede modtagere**</span><span class="sxs-lookup"><span data-stu-id="7e88b-146">**Auto select designees**</span></span> | <span data-ttu-id="7e88b-147">Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger.</span><span class="sxs-lookup"><span data-stu-id="7e88b-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="7e88b-148">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="7e88b-148">Select **Save**.</span></span>
