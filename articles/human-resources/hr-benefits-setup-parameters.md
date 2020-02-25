---
title: Angive parametre for administration af frynsegoder
description: Konfigurere parametre for administration af frynsegoder i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008495"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="86bfc-103">Angive parametre for administration af frynsegoder</span><span class="sxs-lookup"><span data-stu-id="86bfc-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="86bfc-104">Før du kan oprette orlovsplaner i Microsoft Dynamics 365 Human Resources, skal du konfigurere parametre for administration af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="86bfc-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="86bfc-105">Disse parametre angiver standardværdier, årsagskoder og andre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="86bfc-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="86bfc-106">Konfigurere generelle parametre</span><span class="sxs-lookup"><span data-stu-id="86bfc-106">Configure general parameters</span></span>

1. <span data-ttu-id="86bfc-107">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="86bfc-108">Angiv værdier for følgende felter under fanen **Generelt**:</span><span class="sxs-lookup"><span data-stu-id="86bfc-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="86bfc-109">Felt</span><span class="sxs-lookup"><span data-stu-id="86bfc-109">Field</span></span> | <span data-ttu-id="86bfc-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="86bfc-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="86bfc-111">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="86bfc-111">**Country/region**</span></span> | <span data-ttu-id="86bfc-112">Feltet **Land/område** bestemmer, hvilken visningsrækkefølgen for postnumre/stater.</span><span class="sxs-lookup"><span data-stu-id="86bfc-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="86bfc-113">Det valgte land vises først på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="86bfc-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="86bfc-114">**Årsagskode for tilmelding**</span><span class="sxs-lookup"><span data-stu-id="86bfc-114">**Enrollment reason code**</span></span> | <span data-ttu-id="86bfc-115">Vælg en standardårsagskode, der skal bruges, når der oprettes medarbejderplaner under behandling af en åben tilmelding.</span><span class="sxs-lookup"><span data-stu-id="86bfc-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="86bfc-116">**Årsagskode for annullering**</span><span class="sxs-lookup"><span data-stu-id="86bfc-116">**Cancellation reason code**</span></span> | <span data-ttu-id="86bfc-117">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres.</span><span class="sxs-lookup"><span data-stu-id="86bfc-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="86bfc-118">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="86bfc-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="86bfc-119">Brugerne kan eventuelt ændre den i **Årsagskode til annullering**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="86bfc-120">**Årsagskode for genåbning**</span><span class="sxs-lookup"><span data-stu-id="86bfc-120">**Reopen reason code**</span></span> | <span data-ttu-id="86bfc-121">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan genåbnes.</span><span class="sxs-lookup"><span data-stu-id="86bfc-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="86bfc-122">Den vises i en dialogboks under annulleringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="86bfc-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="86bfc-123">Brugerne kan eventuelt ændre den i **Åbn årsagskode igen**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="86bfc-124">**Årsagskode for livshændelse**</span><span class="sxs-lookup"><span data-stu-id="86bfc-124">**Life event reason code**</span></span> | <span data-ttu-id="86bfc-125">Den årsagskode, der skal bruges, når der indtræffer en livshændelse.</span><span class="sxs-lookup"><span data-stu-id="86bfc-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="86bfc-126">**Årsagskode for satsændring**</span><span class="sxs-lookup"><span data-stu-id="86bfc-126">**Rate change reason code**</span></span> | <span data-ttu-id="86bfc-127">Den årsagskode, der skal bruges, når en medarbejders frynsegodeplan annulleres og genåbnes under behandlingen af opdateret satsændring.</span><span class="sxs-lookup"><span data-stu-id="86bfc-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="86bfc-128">Den angiver, hvilke poster der er ændret af opdateringsprocessen for satsændringen.</span><span class="sxs-lookup"><span data-stu-id="86bfc-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="86bfc-129">**Ny ansættelse berettiget**</span><span class="sxs-lookup"><span data-stu-id="86bfc-129">**New hire eligible**</span></span> | <span data-ttu-id="86bfc-130">Angiver, om nyansatte er berettigede.</span><span class="sxs-lookup"><span data-stu-id="86bfc-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="86bfc-131">**Periode for tilmelding af nyansat**</span><span class="sxs-lookup"><span data-stu-id="86bfc-131">**New hire enrollment period**</span></span> | <span data-ttu-id="86bfc-132">Den tidsperiode, hvor tilmelding for den nyansatte er tilladt.</span><span class="sxs-lookup"><span data-stu-id="86bfc-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="86bfc-133">**Bemærk** Denne indstilling tilsidesætter en eventuel tilmeldingsperiode for nyansatte, som du angiver for berettigelsesreglen for planen.</span><span class="sxs-lookup"><span data-stu-id="86bfc-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="86bfc-134">**Forbedring af årlig løn**</span><span class="sxs-lookup"><span data-stu-id="86bfc-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="86bfc-135">Angiver, om beløbet for **Årlig frynsegodeløn** automatisk skal beregnes i **Oplysninger om medarbejders frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="86bfc-136">Det er baseret på medarbejderens **Lønssats for fast kompensation**, **Gennemsnitligt antal timer** og **Betalingsfrekvens**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="86bfc-137">**Gennemsnitligt antal timer** x **Fast lønsats** x **Betalingsfrekvens** (antal lønperioder) = **Årlig frynsegodeløn**</span><span class="sxs-lookup"><span data-stu-id="86bfc-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="86bfc-138">Hvis nogen af værdierne i felterne **Gennemsnitligt antal timer**, **Lønsats for fast kompensation** eller **Betalingsfrekvens** ændres, genberegnes beløbet for medarbejderens **Årlige frynsegodeløn** automatisk på basis af de ændrede værdier.</span><span class="sxs-lookup"><span data-stu-id="86bfc-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="86bfc-139">Systemet opretter en **Gyldig fra**-post for at identificere den nøjagtige dato og det nøjagtige klokkeslæt, hvor ændringen fandt sted.</span><span class="sxs-lookup"><span data-stu-id="86bfc-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="86bfc-140">Du kan eventuelt redigere beløbet for **Årlig frynsegodeløn** manuelt.</span><span class="sxs-lookup"><span data-stu-id="86bfc-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="86bfc-141">**Livshændelser er aktiveret**</span><span class="sxs-lookup"><span data-stu-id="86bfc-141">**Life events enabled**</span></span> | <span data-ttu-id="86bfc-142">Aktiverer levetidshændelser.</span><span class="sxs-lookup"><span data-stu-id="86bfc-142">Enables life events.</span></span> |
   | <span data-ttu-id="86bfc-143">**Skjul formularer for ældre frynsegoder**</span><span class="sxs-lookup"><span data-stu-id="86bfc-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="86bfc-144">Giver dig mulighed for at skjule ældre frynsegodeformularer.</span><span class="sxs-lookup"><span data-stu-id="86bfc-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="86bfc-145">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="86bfc-146">Konfigurere parametre for medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="86bfc-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="86bfc-147">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="86bfc-148">Angiv værdier for følgende felter under fanen **Medarbejderselvbetjening**:</span><span class="sxs-lookup"><span data-stu-id="86bfc-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="86bfc-149">Felt</span><span class="sxs-lookup"><span data-stu-id="86bfc-149">Field</span></span> | <span data-ttu-id="86bfc-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="86bfc-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="86bfc-151">**Frynsegodebekræftelse**</span><span class="sxs-lookup"><span data-stu-id="86bfc-151">**Benefit verification**</span></span> | <span data-ttu-id="86bfc-152">Den kontroltekst, der skal bruges under betaling af selvbetjeningsfrynsegoder.</span><span class="sxs-lookup"><span data-stu-id="86bfc-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="86bfc-153">**Vælg automatisk udpegede modtagere**</span><span class="sxs-lookup"><span data-stu-id="86bfc-153">**Auto select designees**</span></span> | <span data-ttu-id="86bfc-154">Angiver, om der automatisk skal vælges afhængige og modtagere baseret på deres berettigelse til planindstillinger.</span><span class="sxs-lookup"><span data-stu-id="86bfc-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="86bfc-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86bfc-155">Select **Save**.</span></span>
