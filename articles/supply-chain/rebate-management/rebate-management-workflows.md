---
title: Arbejdsprocesser for rabatstyringsaftale
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere en arbejdsproces for rabatstyringsaftaler for at godkende og aktivere aftaler.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270951"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="b08fe-103">Arbejdsprocesser for rabatstyringsaftale</span><span class="sxs-lookup"><span data-stu-id="b08fe-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b08fe-104">Når rabataftaler skal godkendes, bruger Rabatstyring samme arbejdsprocesplatform som andre Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="b08fe-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="b08fe-105">Der er knyttet to jobprocesser til hver arbejdsproces:</span><span class="sxs-lookup"><span data-stu-id="b08fe-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="b08fe-106">Et element i arbejdsprocessen godkender aftalen.</span><span class="sxs-lookup"><span data-stu-id="b08fe-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="b08fe-107">Et element i arbejdsprocessen aktiverer aftalen, så brugeren eller arbejdsprocessen kan godkende transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="b08fe-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="b08fe-108">Før du kan bruge en rabataftale, skal den være aktiv i modulet **Rabatstyring**.</span><span class="sxs-lookup"><span data-stu-id="b08fe-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="b08fe-109">Hvis du vil aktivere en aftale, skal du først oprette og konfigurere en *Arbejdsproces for rabatstyringsaftale*.</span><span class="sxs-lookup"><span data-stu-id="b08fe-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="b08fe-110">Brugere kan ikke godkende aftaler manuelt.</span><span class="sxs-lookup"><span data-stu-id="b08fe-110">Users can't manually approve deals.</span></span> <span data-ttu-id="b08fe-111">Arbejdsprocessen skal altid bruges.</span><span class="sxs-lookup"><span data-stu-id="b08fe-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="b08fe-112">Oprette og administrere arbejdsprocesser for rabatstyringsaftale</span><span class="sxs-lookup"><span data-stu-id="b08fe-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="b08fe-113">Du kan arbejde med arbejdsprocesser for rabatstyringsaftaler ved at gå til **Rabatstyring \> Konfiguration \> Arbejdsprocesser for rabatstyring**.</span><span class="sxs-lookup"><span data-stu-id="b08fe-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="b08fe-114">Her kan du se, oprette og opdatere arbejdsprocesser efter behov.</span><span class="sxs-lookup"><span data-stu-id="b08fe-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="b08fe-115">Der kan kun være én aktiv arbejdsproces ad gangen af denne type.</span><span class="sxs-lookup"><span data-stu-id="b08fe-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="b08fe-116">Yderligere oplysninger om arbejdsprocesser, hvordan du arbejder med siden **Arbejdsprocesser for rabatstyring**, og hvordan du opretter arbejdsprocesser, finder du i [oversigten over arbejdsprocessystemet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterede emner.</span><span class="sxs-lookup"><span data-stu-id="b08fe-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="b08fe-117">Bruge en arbejdsproces til at aktivere en aftale</span><span class="sxs-lookup"><span data-stu-id="b08fe-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="b08fe-118">Hvis du vil aktivere en aftale via en arbejdsproces, skal du åbne aftalen (f.eks. på siden **Alle rabatstyringsaftaler**).</span><span class="sxs-lookup"><span data-stu-id="b08fe-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="b08fe-119">Vælg derefter **Arbejdsproces \> Send** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b08fe-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="b08fe-120">Når den nye aftale er behandlet og godkendt via arbejdsprocessen, er den aktiv og klar til brug.</span><span class="sxs-lookup"><span data-stu-id="b08fe-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="b08fe-121">Når en aftale er blevet aktiveret, kan du ikke ændre det meste af opsætningen.</span><span class="sxs-lookup"><span data-stu-id="b08fe-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="b08fe-122">Hvis du skal ændre en aktiv aftale, skal du først deaktivere den og derefter oprette en ny aftale.</span><span class="sxs-lookup"><span data-stu-id="b08fe-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="b08fe-123">Hvis den nye aftale skal ligne den gamle aftale, kan du oprette den ved at kopiere den gamle aftale.</span><span class="sxs-lookup"><span data-stu-id="b08fe-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="b08fe-124">Du kan ændre følgende indstillinger for en aftale, efter at den er blevet aktiveret:</span><span class="sxs-lookup"><span data-stu-id="b08fe-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="b08fe-125">Afstem efter</span><span class="sxs-lookup"><span data-stu-id="b08fe-125">Reconcile by</span></span>
- <span data-ttu-id="b08fe-126">Akkumuleret garanti</span><span class="sxs-lookup"><span data-stu-id="b08fe-126">Cumulative guarantee</span></span>
- <span data-ttu-id="b08fe-127">Posteringsprofil</span><span class="sxs-lookup"><span data-stu-id="b08fe-127">Posting profile</span></span>
- <span data-ttu-id="b08fe-128">Posteringsprofil for garanti</span><span class="sxs-lookup"><span data-stu-id="b08fe-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="b08fe-129">Dokumentnoter</span><span class="sxs-lookup"><span data-stu-id="b08fe-129">Document notes</span></span>
- <span data-ttu-id="b08fe-130">Valuta</span><span class="sxs-lookup"><span data-stu-id="b08fe-130">Currency</span></span>
- <span data-ttu-id="b08fe-131">Fra-dato</span><span class="sxs-lookup"><span data-stu-id="b08fe-131">From date</span></span>
- <span data-ttu-id="b08fe-132">Til-dato</span><span class="sxs-lookup"><span data-stu-id="b08fe-132">To date</span></span>

<span data-ttu-id="b08fe-133">Derudover kan rabatlinjer fjernes.</span><span class="sxs-lookup"><span data-stu-id="b08fe-133">In addition, rebate lines can be removed.</span></span>
