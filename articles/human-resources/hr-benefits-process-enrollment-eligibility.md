---
title: Behandle tilmeldingsberettigelse
description: I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.
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
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429283"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="f1436-103">Behandle tilmeldingsberettigelse</span><span class="sxs-lookup"><span data-stu-id="f1436-103">Process enrollment eligibility</span></span>

<span data-ttu-id="f1436-104">I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.</span><span class="sxs-lookup"><span data-stu-id="f1436-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="f1436-105">Vælg **Behandling af berettigelse til tilmelding** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="f1436-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="f1436-106">Angiv værdier for følgende felter i dialogboksen **Kør behandling af berettigelse til frynsegodetilmelding**:</span><span class="sxs-lookup"><span data-stu-id="f1436-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="f1436-107">Felt</span><span class="sxs-lookup"><span data-stu-id="f1436-107">Field</span></span> | <span data-ttu-id="f1436-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f1436-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f1436-109">**Tilmeldingsperiode**</span><span class="sxs-lookup"><span data-stu-id="f1436-109">**Enrollment period**</span></span> | <span data-ttu-id="f1436-110">Den tilmeldingsperiode, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="f1436-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="f1436-111">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="f1436-111">**Legal entity**</span></span> | <span data-ttu-id="f1436-112">Den juridiske enhed, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="f1436-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="f1436-113">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="f1436-113">**Worker**</span></span> | <span data-ttu-id="f1436-114">Den arbejder, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="f1436-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="f1436-115">Hvis du ikke udfylder dette felt, behandles berettigelsen til tilmelding for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="f1436-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="f1436-116">**Frynsegodeplan**</span><span class="sxs-lookup"><span data-stu-id="f1436-116">**Benefit plan**</span></span> | <span data-ttu-id="f1436-117">Den frynsegodeplan, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="f1436-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="f1436-118">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="f1436-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="f1436-119">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="f1436-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="f1436-120">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1436-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="f1436-121">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1436-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="f1436-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1436-122">Select **OK**.</span></span> <span data-ttu-id="f1436-123">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="f1436-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="f1436-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1436-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="f1436-125">Vis procesresultater</span><span class="sxs-lookup"><span data-stu-id="f1436-125">View Process Results</span></span>

<span data-ttu-id="f1436-126">I denne artikel beskrives, hvordan du få vist resultater af berettigelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="f1436-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="f1436-127">Vælg **Procesresultater** under **Behandling** i arbejdsområdet **Administration af frynsegoder**.</span><span class="sxs-lookup"><span data-stu-id="f1436-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="f1436-128">Følgende felter er angivet i formularen **Procesresultater**:</span><span class="sxs-lookup"><span data-stu-id="f1436-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="f1436-129">Felt</span><span class="sxs-lookup"><span data-stu-id="f1436-129">Field</span></span> | <span data-ttu-id="f1436-130">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="f1436-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f1436-131">**Proces-id**</span><span class="sxs-lookup"><span data-stu-id="f1436-131">**Process ID**</span></span> | <span data-ttu-id="f1436-132">Det entydige id for kombinationen af Arbejder, Juridisk enhed og Proceskørsel.</span><span class="sxs-lookup"><span data-stu-id="f1436-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="f1436-133">**Procestype**</span><span class="sxs-lookup"><span data-stu-id="f1436-133">**Process type**</span></span> | <span data-ttu-id="f1436-134">Det identificerer den proces, der blev kørt.</span><span class="sxs-lookup"><span data-stu-id="f1436-134">This identifies the process that was run.</span></span> <span data-ttu-id="f1436-135">Eksempel: Tilmelding.</span><span class="sxs-lookup"><span data-stu-id="f1436-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="f1436-136">**Registreringstidspunkt**</span><span class="sxs-lookup"><span data-stu-id="f1436-136">**Time stamp**</span></span> | <span data-ttu-id="f1436-137">Det tidspunkt, hvor berettigelsesprocessen blev kørt.</span><span class="sxs-lookup"><span data-stu-id="f1436-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="f1436-138">**Juridisk enhed**</span><span class="sxs-lookup"><span data-stu-id="f1436-138">**Legal entity**</span></span> | <span data-ttu-id="f1436-139">Den juridiske enhed, der er angivet under tilmeldingsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f1436-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="f1436-140">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="f1436-140">**Worker**</span></span> | <span data-ttu-id="f1436-141">Den arbejder, der blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="f1436-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="f1436-142">\*\*Plan</span><span class="sxs-lookup"><span data-stu-id="f1436-142">\*\*Plan</span></span> | <span data-ttu-id="f1436-143">Den frynsegodeplan, som tilmeldingen blev forsøgt for.</span><span class="sxs-lookup"><span data-stu-id="f1436-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="f1436-144">**Berettigelsesregel**</span><span class="sxs-lookup"><span data-stu-id="f1436-144">**Eligibility rule**</span></span> | <span data-ttu-id="f1436-145">Den berettigelsesregel, der blev behandlet.</span><span class="sxs-lookup"><span data-stu-id="f1436-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="f1436-146">Hvis der blev fundet en fejl, før berettigelsen blev kørt, vil dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="f1436-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="f1436-147">Eksempel: Hvis der ikke er defineret kompensation for en arbejder, vil berettigelsesprocessen ikke blive kørt, og dette felt vil være tomt.</span><span class="sxs-lookup"><span data-stu-id="f1436-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="f1436-148">**Resultatstatus**</span><span class="sxs-lookup"><span data-stu-id="f1436-148">**Result status**</span></span> | <span data-ttu-id="f1436-149">Det vil være Berettiget eller Ikke-berettiget.</span><span class="sxs-lookup"><span data-stu-id="f1436-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="f1436-150">Resultatstatussen vil være Ikke-berettiget, hvis arbejderen ikke opfylder kriterierne for berettigelsesreglen, hvis arbejderen mangler påkrævede oplysninger som f.eks. en betalingsfrekvens eller fast løn, eller hvis der mangler oplysninger i frynsegodeplanen, der forhindrer, at arbejdere kan tilmeldes.</span><span class="sxs-lookup"><span data-stu-id="f1436-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="f1436-151">**Resultatmeddelelse**</span><span class="sxs-lookup"><span data-stu-id="f1436-151">**Result message**</span></span> | <span data-ttu-id="f1436-152">Angiver, hvorfor en arbejder ikke er berettiget til en frynsegodeplan, eller hvis berettigelsesreglen er overført.</span><span class="sxs-lookup"><span data-stu-id="f1436-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

