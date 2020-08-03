---
title: Angive parametre for administration af frynsegoder
description: Konfigurere parametre for administration af frynsegoder i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599350"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="f2fcd-103">Angive parametre til administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="f2fcd-103">Set Benefits management parameters</span></span>

<span data-ttu-id="f2fcd-104">Før du kan oprette orlovsplaner i Microsoft Dynamics 365 Human Resources, skal du konfigurere parametre for administration af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="f2fcd-105">Disse parametre angiver standardværdier, årsagskoder og andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="f2fcd-106">Konfigurere generelle parametre</span><span class="sxs-lookup"><span data-stu-id="f2fcd-106">Configure general parameters</span></span>

1. <span data-ttu-id="f2fcd-107">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Delte Human Resources-parametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="f2fcd-108">Angiv værdier for følgende felter under fanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="f2fcd-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="f2fcd-109">Felt</span><span class="sxs-lookup"><span data-stu-id="f2fcd-109">Field</span></span> | <span data-ttu-id="f2fcd-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f2fcd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f2fcd-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-111">**Country/region**</span></span> | <span data-ttu-id="f2fcd-112">Feltet **Land/område** bestemmer, hvilken visningsrækkefølgen for postnumre/stater.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="f2fcd-113">Det valgte land vises først på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="f2fcd-114">**Årsagskode for tilmelding**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-114">**Enrollment reason code**</span></span> | <span data-ttu-id="f2fcd-115">Vælg en standardårsagskode, der skal bruges, når der oprettes medarbejderplaner under behandling af en åben tilmelding.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="f2fcd-116">**Årsagskode for annullering**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-116">**Cancellation reason code**</span></span> | <span data-ttu-id="f2fcd-117">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="f2fcd-118">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="f2fcd-119">Brugerne kan eventuelt ændre den i **Årsagskode til annullering**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="f2fcd-120">**Årsagskode for genåbning**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-120">**Reopen reason code**</span></span> | <span data-ttu-id="f2fcd-121">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan genåbnes.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="f2fcd-122">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="f2fcd-123">Brugerne kan eventuelt ændre den i **Åbn årsagskode igen**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="f2fcd-124">**Årsagskode for livshændelse**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-124">**Life event reason code**</span></span> | <span data-ttu-id="f2fcd-125">Den årsagskode, der skal bruges, når der indtræffer en livshændelse.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="f2fcd-126">**Årsagskode for satsændring**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-126">**Rate change reason code**</span></span> | <span data-ttu-id="f2fcd-127">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres og genåbnes under behandlingen af opdateret satsændring.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="f2fcd-128">Den angiver, hvilke poster der er ændret af opdateringsprocessen for satsændringen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="f2fcd-129">**Årlig løn som personalegoder**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-129">**Benefits annual salary**</span></span> | <span data-ttu-id="f2fcd-130">Giver dig mulighed for at angive et beløb for **Årlig frynsegodeløn** for en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="f2fcd-131">Human Resources skal bruge beløbet for **Årlig frynsegodeløn** til bestemmelse af dækningsbeløb i stedet for disponerings beløb, i stedet for det årlige beløb for fast løn.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="f2fcd-132">**Ny ansættelse berettiget**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-132">**New hire eligible**</span></span> | <span data-ttu-id="f2fcd-133">Angiver, om nyansatte er berettigede.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="f2fcd-134">**Periode for tilmelding af nyansat**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-134">**New hire enrollment period**</span></span> | <span data-ttu-id="f2fcd-135">Den tidsperiode, hvor tilmelding for den nyansatte er tilladt.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="f2fcd-136">**Bemærk** Denne indstilling tilsidesætter en eventuel tilmeldingsperiode for nyansatte, som du angiver for berettigelsesreglen for planen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="f2fcd-137">**Standardlønfrekvens**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-137">**Default pay frequency**</span></span> | <span data-ttu-id="f2fcd-138">Den standardlønsats, der skal bruges, når der tilføjes nye arbejdere.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="f2fcd-139">**Livshændelser er aktiveret**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-139">**Life events enabled**</span></span> | <span data-ttu-id="f2fcd-140">Aktiverer levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-140">Enables life events.</span></span> |
   | <span data-ttu-id="f2fcd-141">**Skjul formularer for ældre personalegoder**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="f2fcd-142">Giver dig mulighed for at skjule ældre frynsegodeformularer.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="f2fcd-143">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="f2fcd-144">Konfigurere parametre for medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="f2fcd-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="f2fcd-145">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="f2fcd-146">Angiv værdier for følgende felter under fanen **Medarbejderselvbetjening**:</span><span class="sxs-lookup"><span data-stu-id="f2fcd-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="f2fcd-147">Felt</span><span class="sxs-lookup"><span data-stu-id="f2fcd-147">Field</span></span> | <span data-ttu-id="f2fcd-148">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f2fcd-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f2fcd-149">**Frynsegodebekræftelse**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-149">**Benefit verification**</span></span> | <span data-ttu-id="f2fcd-150">Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="f2fcd-151">**Vælg automatisk udpegede modtagere**</span><span class="sxs-lookup"><span data-stu-id="f2fcd-151">**Auto select designees**</span></span> | <span data-ttu-id="f2fcd-152">Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="f2fcd-153">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-153">Select **Save**.</span></span>
