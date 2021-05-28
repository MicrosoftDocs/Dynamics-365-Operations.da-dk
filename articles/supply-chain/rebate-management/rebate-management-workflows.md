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
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020380"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="1e59d-103">Arbejdsprocesser for rabatstyringsaftale</span><span class="sxs-lookup"><span data-stu-id="1e59d-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e59d-104">Når rabataftaler skal godkendes, bruger Rabatstyring samme arbejdsprocesplatform som andre Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="1e59d-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="1e59d-105">Der er knyttet to jobprocesser til hver arbejdsproces:</span><span class="sxs-lookup"><span data-stu-id="1e59d-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="1e59d-106">Et element i arbejdsprocessen aktiverer aftalen, så brugeren eller arbejdsprocessen kan godkende transaktionerne.</span><span class="sxs-lookup"><span data-stu-id="1e59d-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="1e59d-107">Et element i arbejdsprocessen godkender aftalen.</span><span class="sxs-lookup"><span data-stu-id="1e59d-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="1e59d-108">Før du kan bruge en rabataftale, skal den være aktiv i modulet **Rabatstyring**.</span><span class="sxs-lookup"><span data-stu-id="1e59d-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="1e59d-109">Hvis du vil aktivere en aftale, skal du først oprette og konfigurere en *Arbejdsproces for rabatstyringsaftale*.</span><span class="sxs-lookup"><span data-stu-id="1e59d-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="1e59d-110">Når der er aktiveret en arbejdsproces for Rabatstyring, kan brugerne ikke godkende aftaler manuelt.</span><span class="sxs-lookup"><span data-stu-id="1e59d-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="1e59d-111">Arbejdsprocessen skal altid bruges.</span><span class="sxs-lookup"><span data-stu-id="1e59d-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="1e59d-112">Oprette og administrere arbejdsprocesser for rabatstyringsaftale</span><span class="sxs-lookup"><span data-stu-id="1e59d-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="1e59d-113">Du kan arbejde med arbejdsprocesser for rabatstyringsaftaler ved at gå til **Rabatstyring \> Konfiguration \> Arbejdsprocesser for rabatstyring**.</span><span class="sxs-lookup"><span data-stu-id="1e59d-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="1e59d-114">Her kan du se, oprette og opdatere arbejdsprocesser efter behov.</span><span class="sxs-lookup"><span data-stu-id="1e59d-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="1e59d-115">Der kan kun være én aktiv arbejdsproces ad gangen af denne type.</span><span class="sxs-lookup"><span data-stu-id="1e59d-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="1e59d-116">Yderligere oplysninger om arbejdsprocesser, hvordan du arbejder med siden **Arbejdsprocesser for rabatstyring**, og hvordan du opretter arbejdsprocesser, finder du i [oversigten over arbejdsprocessystemet](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) og de relaterede emner.</span><span class="sxs-lookup"><span data-stu-id="1e59d-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="1e59d-117">Bruge en arbejdsproces til at aktivere en aftale</span><span class="sxs-lookup"><span data-stu-id="1e59d-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="1e59d-118">Hvis du vil aktivere en aftale via en arbejdsproces, skal du åbne aftalen (f.eks. på siden **Alle rabatstyringsaftaler**).</span><span class="sxs-lookup"><span data-stu-id="1e59d-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="1e59d-119">Vælg derefter **Arbejdsproces \> Send** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1e59d-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="1e59d-120">Når den nye aftale er behandlet og godkendt via arbejdsprocessen, er den aktiv og klar til brug.</span><span class="sxs-lookup"><span data-stu-id="1e59d-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="1e59d-121">Når en aftale er blevet aktiveret, kan du ikke ændre opsætningen.</span><span class="sxs-lookup"><span data-stu-id="1e59d-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="1e59d-122">Hvis du skal ændre en aktiv aftale, skal du deaktivere den og derefter oprette en ny aftale.</span><span class="sxs-lookup"><span data-stu-id="1e59d-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="1e59d-123">Hvis den nye aftale skal ligne den gamle aftale, kan du oprette den ved at kopiere den gamle aftale.</span><span class="sxs-lookup"><span data-stu-id="1e59d-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
