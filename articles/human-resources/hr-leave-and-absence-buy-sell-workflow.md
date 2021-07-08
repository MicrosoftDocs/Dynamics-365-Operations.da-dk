---
title: Oprette en arbejdsproces for køb og salg af orlov
description: Opret en arbejdsproces for køb og salg af orlov for at administrere anmodninger om køb og salg af orlov i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ec21cda4779fea8c28b73d25842219da900da9d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271469"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="c70e8-103">Oprette en arbejdsproces for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="c70e8-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c70e8-104">Du kan oprette en arbejdsproces i Dynamics 365 Human Resources for at administrere anmodninger om køb og salg af orlov konsekvent.</span><span class="sxs-lookup"><span data-stu-id="c70e8-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="c70e8-105">En arbejdsproces for **Køb og salg af orlov** giver dig mulighed for at:</span><span class="sxs-lookup"><span data-stu-id="c70e8-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="c70e8-106">Definere opgaver</span><span class="sxs-lookup"><span data-stu-id="c70e8-106">Define tasks</span></span>
- <span data-ttu-id="c70e8-107">Afgøre, hvem der skal udføre opgaverne</span><span class="sxs-lookup"><span data-stu-id="c70e8-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="c70e8-108">Angive, hvem der kan godkende eller afvise anmodninger</span><span class="sxs-lookup"><span data-stu-id="c70e8-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="c70e8-109">Oprette en arbejdsproces for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="c70e8-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="c70e8-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="c70e8-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c70e8-111">Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c70e8-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="c70e8-112">Vælg **Ny**, og vælg derefter **Anmodning om køb og salg af orlov**.</span><span class="sxs-lookup"><span data-stu-id="c70e8-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="c70e8-113">Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="c70e8-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="c70e8-114">Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="c70e8-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="c70e8-115">Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="c70e8-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="c70e8-116">Dataelementer for arbejdsgang for orlovs- og fraværsanmodninger</span><span class="sxs-lookup"><span data-stu-id="c70e8-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="c70e8-117">Du kan bruge følgende dataelementer til at oprette betingede eller automatiske godkendelser i arbejdsgange for anmodninger om køb og salg af orlov:</span><span class="sxs-lookup"><span data-stu-id="c70e8-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="c70e8-118">**Beløb**</span><span class="sxs-lookup"><span data-stu-id="c70e8-118">**Amount**</span></span>
- <span data-ttu-id="c70e8-119">**Politik for køb og salg af orlov**</span><span class="sxs-lookup"><span data-stu-id="c70e8-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="c70e8-120">**Regnskab**</span><span class="sxs-lookup"><span data-stu-id="c70e8-120">**Company**</span></span>
- <span data-ttu-id="c70e8-121">**Oprettet af**</span><span class="sxs-lookup"><span data-stu-id="c70e8-121">**Created by**</span></span>
- <span data-ttu-id="c70e8-122">**Dato og klokkeslæt for oprettelse**</span><span class="sxs-lookup"><span data-stu-id="c70e8-122">**Created date and time**</span></span>
- <span data-ttu-id="c70e8-123">**Slutdato**</span><span class="sxs-lookup"><span data-stu-id="c70e8-123">**End date**</span></span>
- <span data-ttu-id="c70e8-124">**Orlovstype**</span><span class="sxs-lookup"><span data-stu-id="c70e8-124">**Leave type**</span></span>
- <span data-ttu-id="c70e8-125">**Ændret af**</span><span class="sxs-lookup"><span data-stu-id="c70e8-125">**Modified by**</span></span>
- <span data-ttu-id="c70e8-126">**Dato og klokkeslæt for ændring**</span><span class="sxs-lookup"><span data-stu-id="c70e8-126">**Modified date and time**</span></span>
- <span data-ttu-id="c70e8-127">**Anmodnings-id**</span><span class="sxs-lookup"><span data-stu-id="c70e8-127">**Request ID**</span></span>
- <span data-ttu-id="c70e8-128">**Igangsæt dato**</span><span class="sxs-lookup"><span data-stu-id="c70e8-128">**Start date**</span></span>
- <span data-ttu-id="c70e8-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="c70e8-129">**Status**</span></span> 
- <span data-ttu-id="c70e8-130">**Indsendelsesdato**</span><span class="sxs-lookup"><span data-stu-id="c70e8-130">**Submission date**</span></span>
- <span data-ttu-id="c70e8-131">**Sendt af**</span><span class="sxs-lookup"><span data-stu-id="c70e8-131">**Submitted by**</span></span>
- <span data-ttu-id="c70e8-132">**Sendt af HR**</span><span class="sxs-lookup"><span data-stu-id="c70e8-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="c70e8-133">**Sendt af leder**</span><span class="sxs-lookup"><span data-stu-id="c70e8-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="c70e8-134">**Sendt på vegne af**</span><span class="sxs-lookup"><span data-stu-id="c70e8-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="c70e8-135">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="c70e8-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="c70e8-136">Eksempler på arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="c70e8-136">Workflow examples</span></span>

<span data-ttu-id="c70e8-137">Disse eksempler viser, hvordan du kan oprette forskellige typer betingelser for arbejdsgange via disse dataelementer:</span><span class="sxs-lookup"><span data-stu-id="c70e8-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="c70e8-138">Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende anmodninger om for køb og salg af orlov automatisk, som disse roller sender på vegne af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c70e8-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="c70e8-139">Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c70e8-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="c70e8-140">Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="c70e8-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="c70e8-141">Se også</span><span class="sxs-lookup"><span data-stu-id="c70e8-141">See also</span></span>

[<span data-ttu-id="c70e8-142">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="c70e8-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="c70e8-143">Administrere politikker for køb og salg af orlov</span><span class="sxs-lookup"><span data-stu-id="c70e8-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[<span data-ttu-id="c70e8-144">Køb og sælg orlov</span><span class="sxs-lookup"><span data-stu-id="c70e8-144">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
