---
title: Behandle tilmeldingsberettigelse
description: I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008433"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="d39cc-103">Behandle tilmeldingsberettigelse</span><span class="sxs-lookup"><span data-stu-id="d39cc-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d39cc-104">I denne artikel beskrives, hvordan du kan køre processen til berettigelse af tilmelding.</span><span class="sxs-lookup"><span data-stu-id="d39cc-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="d39cc-105">Vælg **Behandling af berettigelse til tilmelding** under **Behandling** i arbejdsområdet **Frynsegodeadministration**.</span><span class="sxs-lookup"><span data-stu-id="d39cc-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="d39cc-106">Angiv værdier for følgende felter i dialogboksen **Kør behandling af berettigelse til frynsegodetilmelding**:</span><span class="sxs-lookup"><span data-stu-id="d39cc-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="d39cc-107">Felt</span><span class="sxs-lookup"><span data-stu-id="d39cc-107">Field</span></span> | <span data-ttu-id="d39cc-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d39cc-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d39cc-109">Tilmeldingsperiode</span><span class="sxs-lookup"><span data-stu-id="d39cc-109">Enrollment period</span></span> | <span data-ttu-id="d39cc-110">Den tilmeldingsperiode, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="d39cc-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="d39cc-111">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="d39cc-111">Legal entity</span></span> | <span data-ttu-id="d39cc-112">Den juridiske enhed, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="d39cc-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="d39cc-113">Arbejdstråd</span><span class="sxs-lookup"><span data-stu-id="d39cc-113">Worker</span></span> | <span data-ttu-id="d39cc-114">Den arbejder, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="d39cc-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="d39cc-115">Hvis du ikke udfylder dette felt, behandles berettigelsen til tilmelding for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="d39cc-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="d39cc-116">Frynsegodeplan</span><span class="sxs-lookup"><span data-stu-id="d39cc-116">Benefit plan</span></span> | <span data-ttu-id="d39cc-117">Den frynsegodeplan, der skal behandles berettigelse til tilmelding for.</span><span class="sxs-lookup"><span data-stu-id="d39cc-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="d39cc-118">Hvis du vil køre processen i baggrunden, skal du vælge **Kør i baggrunden** og udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="d39cc-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="d39cc-119">Angiv oplysninger om processen.</span><span class="sxs-lookup"><span data-stu-id="d39cc-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="d39cc-120">Hvis du vil konfigurere et tilbagevendende job, skal du vælge **Gentagelse**, angive gentagelsesoplysningerne og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d39cc-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="d39cc-121">Hvis du vil oprette en jobpåmindelse, skal du vælge **Påmindelser**, vælge de påmindelser, du vil modtage, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d39cc-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="d39cc-122">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d39cc-122">Select **OK**.</span></span> <span data-ttu-id="d39cc-123">Processen køres med de parametre, du angiver.</span><span class="sxs-lookup"><span data-stu-id="d39cc-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="d39cc-124">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d39cc-124">Select **OK**.</span></span>
