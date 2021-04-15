---
title: Oprette en arbejdsgang for orlovsanmodninger
description: Opret en arbejdsgang for orlovs- og fraværsanmodninger for at administrere anmodninger om orlov i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 218e5a6fc95e92bb631ee568a79b7dfe05f425e6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794535"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="90cee-103">Oprette en arbejdsgang for orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="90cee-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="90cee-104">Du kan oprette en arbejdsgang i Dynamics 365 Human Resources for at administrere orlovs- og fraværsanmodninger konsekvent.</span><span class="sxs-lookup"><span data-stu-id="90cee-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="90cee-105">En **Orlovs- og fraværsarbejdsgang** giver dig mulighed for at:</span><span class="sxs-lookup"><span data-stu-id="90cee-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="90cee-106">Definere opgaver</span><span class="sxs-lookup"><span data-stu-id="90cee-106">Define tasks</span></span>
- <span data-ttu-id="90cee-107">Afgøre, hvem der skal udføre opgaverne</span><span class="sxs-lookup"><span data-stu-id="90cee-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="90cee-108">Angive, hvem der kan godkende eller afvise anmodninger</span><span class="sxs-lookup"><span data-stu-id="90cee-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="90cee-109">Oprette en arbejdsgang for orlovs- og fraværsanmodninger</span><span class="sxs-lookup"><span data-stu-id="90cee-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="90cee-110">På siden **Orlov og fravær** skal du vælge fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="90cee-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="90cee-111">Vælg **Arbejdsgange for Human Resources** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="90cee-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="90cee-112">Vælg **Ny**, og vælg derefter **Anmodning om orlov og fravær**.</span><span class="sxs-lookup"><span data-stu-id="90cee-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="90cee-113">Når meddelelsen **Åbn denne fil?** vises, skal du vælge **Åbn** og logge på med dit firmas legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="90cee-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="90cee-114">Brug arbejdsgangseditoren til at oprette en arbejdsgang til orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="90cee-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="90cee-115">Yderligere oplysninger om at arbejde med arbejdsgange finder du i [Oversigt over oprettelse af arbejdsgange](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="90cee-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="90cee-116">Dataelementer for arbejdsgang for orlovs- og fraværsanmodninger</span><span class="sxs-lookup"><span data-stu-id="90cee-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="90cee-117">Du kan bruge følgende dataelementer til at oprette betingede eller automatiske godkendelser i arbejdsgange for orlovs- og fraværsanmodninger:</span><span class="sxs-lookup"><span data-stu-id="90cee-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="90cee-118">**Beløb**</span><span class="sxs-lookup"><span data-stu-id="90cee-118">**Amount**</span></span>
- <span data-ttu-id="90cee-119">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="90cee-119">**Comment**</span></span>
- <span data-ttu-id="90cee-120">**Regnskab**</span><span class="sxs-lookup"><span data-stu-id="90cee-120">**Company**</span></span>
- <span data-ttu-id="90cee-121">**Oprettet af**</span><span class="sxs-lookup"><span data-stu-id="90cee-121">**Created by**</span></span>
- <span data-ttu-id="90cee-122">**Dato og klokkeslæt for oprettelse**</span><span class="sxs-lookup"><span data-stu-id="90cee-122">**Created date and time**</span></span>
- <span data-ttu-id="90cee-123">**Slutdato**</span><span class="sxs-lookup"><span data-stu-id="90cee-123">**End date**</span></span>
- <span data-ttu-id="90cee-124">**Orlovstype**</span><span class="sxs-lookup"><span data-stu-id="90cee-124">**Leave type**</span></span>
- <span data-ttu-id="90cee-125">**Ændret af**</span><span class="sxs-lookup"><span data-stu-id="90cee-125">**Modified by**</span></span>
- <span data-ttu-id="90cee-126">**Dato og klokkeslæt for ændring**</span><span class="sxs-lookup"><span data-stu-id="90cee-126">**Modified date and time**</span></span>
- <span data-ttu-id="90cee-127">**Årsagskode**</span><span class="sxs-lookup"><span data-stu-id="90cee-127">**Reason code**</span></span>
- <span data-ttu-id="90cee-128">**Anmodnings-id**</span><span class="sxs-lookup"><span data-stu-id="90cee-128">**Request ID**</span></span>
- <span data-ttu-id="90cee-129">**Igangsæt dato**</span><span class="sxs-lookup"><span data-stu-id="90cee-129">**Start date**</span></span>
- <span data-ttu-id="90cee-130">**Status**</span><span class="sxs-lookup"><span data-stu-id="90cee-130">**Status**</span></span> 
- <span data-ttu-id="90cee-131">**Indsendelsesdato**</span><span class="sxs-lookup"><span data-stu-id="90cee-131">**Submission date**</span></span>
- <span data-ttu-id="90cee-132">**Sendt af**</span><span class="sxs-lookup"><span data-stu-id="90cee-132">**Submitted by**</span></span>
- <span data-ttu-id="90cee-133">**Sendt af HR**</span><span class="sxs-lookup"><span data-stu-id="90cee-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="90cee-134">**Sendt af leder**</span><span class="sxs-lookup"><span data-stu-id="90cee-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="90cee-135">**Sendt på vegne af**</span><span class="sxs-lookup"><span data-stu-id="90cee-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="90cee-136">**Arbejdstråd**</span><span class="sxs-lookup"><span data-stu-id="90cee-136">**Worker**</span></span>
- <span data-ttu-id="90cee-137">**Arbejdertype**</span><span class="sxs-lookup"><span data-stu-id="90cee-137">**Worker type**</span></span>

<span data-ttu-id="90cee-138">Disse eksempler viser, hvordan du kan oprette forskellige typer betingelser for arbejdsgange via disse dataelementer:</span><span class="sxs-lookup"><span data-stu-id="90cee-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="90cee-139">Brug **Årsagskode** i en betingelsessætning til at sende orlovsanmodninger for sygefravær med årsagskoden **Kirurgi** til HR mht. godkendelse – andre årsagskoder sendes til lederen.</span><span class="sxs-lookup"><span data-stu-id="90cee-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="90cee-140">Du kan finde flere oplysninger om betingelsessætninger under [Konfigurere betingede beslutninger i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="90cee-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="90cee-141">Brug **Sendt af HR** og **Sendt af leder** i en automatisk handling for at godkende orlovsanmodninger automatisk, som disse roller sender på vegne af medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="90cee-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="90cee-142">Du kan finde flere oplysninger om automatiske handlinger under [Konfigurere godkendelsesprocesser i en arbejdsgang](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="90cee-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="90cee-143">Brug **Orlovstype** i en betingelsessætning eller automatisk handling til at styre, hvordan arbejdsgangen sender anmodninger med bestemte orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="90cee-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="90cee-144">Se også</span><span class="sxs-lookup"><span data-stu-id="90cee-144">See also</span></span>

- [<span data-ttu-id="90cee-145">Oversigt over orlov og fravær</span><span class="sxs-lookup"><span data-stu-id="90cee-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]