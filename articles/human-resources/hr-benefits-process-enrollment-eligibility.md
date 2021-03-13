---
title: Behandle tilmeldingsberettigelse
description: I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 69ea23e4051a6975a5892cd027777c5a88472509
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111957"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="28047-103">Behandle tilmeldingsberettigelse</span><span class="sxs-lookup"><span data-stu-id="28047-103">Process enrollment eligibility</span></span>

<span data-ttu-id="28047-104">I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.</span><span class="sxs-lookup"><span data-stu-id="28047-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="28047-105">Vælg **Behandling af berettigelse til tilmelding** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="28047-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="28047-106">Angiv værdier for følgende felter i dialogboksen **Kør behandling af berettigelse til frynsegodetilmelding**:</span><span class="sxs-lookup"><span data-stu-id="28047-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="28047-107">Felt</span><span class="sxs-lookup"><span data-stu-id="28047-107">Field</span></span> | <span data-ttu-id="28047-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="28047-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28047-109">**Tilmeldingsperiode**</span><span class="sxs-lookup"><span data-stu-id="28047-109">**Enrollment period**</span></span> | <span data-ttu-id="28047-110">Den tilmeldingsperiode, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="28047-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="28047-111">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="28047-111">**Legal entity**</span></span> | <span data-ttu-id="28047-112">Den juridiske enhed, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="28047-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="28047-113">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="28047-113">**Worker**</span></span> | <span data-ttu-id="28047-114">Den arbejder, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="28047-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="28047-115">Hvis du ikke udfylder dette felt, behandles berettigelsen til tilmelding for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="28047-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="28047-116">**Frynsegodeplan**</span><span class="sxs-lookup"><span data-stu-id="28047-116">**Benefit plan**</span></span> | <span data-ttu-id="28047-117">Den frynsegodeplan, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="28047-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="28047-118">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="28047-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="28047-119">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="28047-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="28047-120">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="28047-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="28047-121">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="28047-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="28047-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="28047-122">Select **OK**.</span></span> <span data-ttu-id="28047-123">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="28047-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="28047-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="28047-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="28047-125">Vis procesresultater</span><span class="sxs-lookup"><span data-stu-id="28047-125">View Process Results</span></span>

<span data-ttu-id="28047-126">I denne artikel beskrives, hvordan du få vist resultater af berettigelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="28047-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="28047-127">Vælg **Procesresultater** under **Behandling** i arbejdsområdet **Administration af frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="28047-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="28047-128">Følgende felter er angivet i formularen **Procesresultater**:</span><span class="sxs-lookup"><span data-stu-id="28047-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="28047-129">Felt</span><span class="sxs-lookup"><span data-stu-id="28047-129">Field</span></span> | <span data-ttu-id="28047-130">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="28047-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28047-131">**Proces-id**</span><span class="sxs-lookup"><span data-stu-id="28047-131">**Process ID**</span></span> | <span data-ttu-id="28047-132">Det entydige id for kombinationen af Arbejder, Juridisk enhed og Proceskørsel.</span><span class="sxs-lookup"><span data-stu-id="28047-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="28047-133">**Procestype**</span><span class="sxs-lookup"><span data-stu-id="28047-133">**Process type**</span></span> | <span data-ttu-id="28047-134">Det identificerer den proces, der blev kørt.</span><span class="sxs-lookup"><span data-stu-id="28047-134">This identifies the process that was run.</span></span> <span data-ttu-id="28047-135">Eksempel: Tilmelding.</span><span class="sxs-lookup"><span data-stu-id="28047-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="28047-136">**Registreringstidspunkt**</span><span class="sxs-lookup"><span data-stu-id="28047-136">**Time stamp**</span></span> | <span data-ttu-id="28047-137">Det tidspunkt, hvor berettigelsesprocessen blev kørt.</span><span class="sxs-lookup"><span data-stu-id="28047-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="28047-138">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="28047-138">**Legal entity**</span></span> | <span data-ttu-id="28047-139">Den juridiske enhed, der er angivet under tilmeldingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="28047-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="28047-140">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="28047-140">**Worker**</span></span> | <span data-ttu-id="28047-141">Den arbejder, der blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="28047-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="28047-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="28047-142">\*\*Plan</span></span> | <span data-ttu-id="28047-143">Den frynsegodeplan, som tilmeldingen blev forsøgt for.</span><span class="sxs-lookup"><span data-stu-id="28047-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="28047-144">**Berettigelsesregel**</span><span class="sxs-lookup"><span data-stu-id="28047-144">**Eligibility rule**</span></span> | <span data-ttu-id="28047-145">Den berettigelsesregel, der blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="28047-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="28047-146">Hvis der blev fundet en fejl, før berettigelsen blev kørt, vil dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="28047-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="28047-147">Eksempel: Hvis der ikke er defineret kompensation for en arbejder, vil berettigelsesprocessen ikke blive kørt, og dette felt vil være tomt.</span><span class="sxs-lookup"><span data-stu-id="28047-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="28047-148">**Resultatstatus**</span><span class="sxs-lookup"><span data-stu-id="28047-148">**Result status**</span></span> | <span data-ttu-id="28047-149">Det vil være Berettiget eller Ikke-berettiget.</span><span class="sxs-lookup"><span data-stu-id="28047-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="28047-150">Resultatstatussen vil være Ikke-berettiget, hvis arbejderen ikke opfylder kriterierne for berettigelsesreglen, hvis arbejderen mangler påkrævede oplysninger som f.eks. en betalingsfrekvens eller fast løn, eller hvis der mangler oplysninger i frynsegodeplanen, der forhindrer, at arbejdere kan tilmeldes.</span><span class="sxs-lookup"><span data-stu-id="28047-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="28047-151">**Resultatmeddelelse**</span><span class="sxs-lookup"><span data-stu-id="28047-151">**Result message**</span></span> | <span data-ttu-id="28047-152">Angiver, hvorfor en arbejder ikke er berettiget til en frynsegodeplan, eller hvis berettigelsesreglen er overført.</span><span class="sxs-lookup"><span data-stu-id="28047-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

