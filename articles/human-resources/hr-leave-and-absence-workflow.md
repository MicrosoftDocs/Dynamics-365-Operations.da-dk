---
title: Oprette en arbejdsgang for orlovsanmodninger
description: Opret en arbejdsgang for orlovs- og fraværsanmodninger for at administrere anmodninger om orlov i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
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
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353682"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="f39c4-103">Oprette en arbejdsgang for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="f39c4-103">Create a leave request workflow</span></span>

<span data-ttu-id="f39c4-104">Du kan oprette en arbejdsgang i Dynamics 365 Human Resources for at administrere orlovs- og fraværsanmodninger konsekvent.</span><span class="sxs-lookup"><span data-stu-id="f39c4-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="f39c4-105">En **Orlovs- og fraværsarbejdsgang** giver dig mulighed for at:</span><span class="sxs-lookup"><span data-stu-id="f39c4-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="f39c4-106">Definere opgaver</span><span class="sxs-lookup"><span data-stu-id="f39c4-106">Define tasks</span></span>
- <span data-ttu-id="f39c4-107">Afgøre, hvem der skal udføre opgaverne</span><span class="sxs-lookup"><span data-stu-id="f39c4-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="f39c4-108">Angive, hvem der kan godkende eller afvise anmodninger</span><span class="sxs-lookup"><span data-stu-id="f39c4-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="f39c4-109">Oprette en arbejdsgang for orlovs- og fraværsanmodninger</span><span class="sxs-lookup"><span data-stu-id="f39c4-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="f39c4-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="f39c4-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="f39c4-111">Vælg **Arbejdsgange for Personale** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f39c4-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="f39c4-112">Vælg **Ny**, og vælg derefter **Anmodning om orlov og fravær**.</span><span class="sxs-lookup"><span data-stu-id="f39c4-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="f39c4-113">Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="f39c4-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="f39c4-114">Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="f39c4-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="f39c4-115">Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="f39c4-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="f39c4-116">Dataelementer for arbejdsgang for orlovs- og fraværsanmodninger</span><span class="sxs-lookup"><span data-stu-id="f39c4-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="f39c4-117">Du kan bruge følgende dataelementer til at oprette betingede eller automatiske godkendelser i arbejdsgange for orlovs- og fraværsanmodninger:</span><span class="sxs-lookup"><span data-stu-id="f39c4-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="f39c4-118">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="f39c4-118">**Comment**</span></span>
- <span data-ttu-id="f39c4-119">**Regnskab**</span><span class="sxs-lookup"><span data-stu-id="f39c4-119">**Company**</span></span>
- <span data-ttu-id="f39c4-120">**Oprettet af**</span><span class="sxs-lookup"><span data-stu-id="f39c4-120">**Created by**</span></span>
- <span data-ttu-id="f39c4-121">**Dato og klokkeslæt for oprettelse**</span><span class="sxs-lookup"><span data-stu-id="f39c4-121">**Created date and time**</span></span>
- <span data-ttu-id="f39c4-122">**Slutdato**</span><span class="sxs-lookup"><span data-stu-id="f39c4-122">**End date**</span></span>
- <span data-ttu-id="f39c4-123">**Orlovstype**</span><span class="sxs-lookup"><span data-stu-id="f39c4-123">**Leave type**</span></span>
- <span data-ttu-id="f39c4-124">**Ændret af**</span><span class="sxs-lookup"><span data-stu-id="f39c4-124">**Modified by**</span></span>
- <span data-ttu-id="f39c4-125">**Dato og klokkeslæt for ændring**</span><span class="sxs-lookup"><span data-stu-id="f39c4-125">**Modified date and time**</span></span>
- <span data-ttu-id="f39c4-126">**Årsagskode**</span><span class="sxs-lookup"><span data-stu-id="f39c4-126">**Reason code**</span></span>
- <span data-ttu-id="f39c4-127">**Anmodnings-id**</span><span class="sxs-lookup"><span data-stu-id="f39c4-127">**Request ID**</span></span>
- <span data-ttu-id="f39c4-128">**Igangsæt dato**</span><span class="sxs-lookup"><span data-stu-id="f39c4-128">**Start date**</span></span>
- <span data-ttu-id="f39c4-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="f39c4-129">**Status**</span></span> 
- <span data-ttu-id="f39c4-130">**Indsendelsesdato**</span><span class="sxs-lookup"><span data-stu-id="f39c4-130">**Submission date**</span></span>
- <span data-ttu-id="f39c4-131">**Sendt af**</span><span class="sxs-lookup"><span data-stu-id="f39c4-131">**Submitted by**</span></span>
- <span data-ttu-id="f39c4-132">**Sendt af HR**</span><span class="sxs-lookup"><span data-stu-id="f39c4-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="f39c4-133">**Sendt af leder**</span><span class="sxs-lookup"><span data-stu-id="f39c4-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="f39c4-134">**Sendt på vegne af**</span><span class="sxs-lookup"><span data-stu-id="f39c4-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="f39c4-135">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="f39c4-135">**Worker**</span></span>
- <span data-ttu-id="f39c4-136">**Arbejdertype**</span><span class="sxs-lookup"><span data-stu-id="f39c4-136">**Worker type**</span></span>

<span data-ttu-id="f39c4-137">Disse eksempler viser, hvordan du kan oprette forskellige typer betingelser for arbejdsgange via disse dataelementer:</span><span class="sxs-lookup"><span data-stu-id="f39c4-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="f39c4-138">Brug **Årsagskode** i en betingelsessætning til at sende orlovsanmodninger for sygefravær med årsagskoden **Kirurgi** til HR mht. godkendelse – andre årsagskoder sendes til lederen.</span><span class="sxs-lookup"><span data-stu-id="f39c4-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="f39c4-139">Du kan finde flere oplysninger om betingelsessætninger under [Konfigurere betingede beslutninger i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="f39c4-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="f39c4-140">Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende orlovsanmodninger automatisk, som disse roller sender på vegne af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="f39c4-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="f39c4-141">Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="f39c4-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="f39c4-142">Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="f39c4-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="f39c4-143">Se også</span><span class="sxs-lookup"><span data-stu-id="f39c4-143">See also</span></span>

- [<span data-ttu-id="f39c4-144">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="f39c4-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
