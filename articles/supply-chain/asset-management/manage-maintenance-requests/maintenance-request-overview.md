---
title: Vedligeholdelsesanmodninger
description: Dette emne indeholder en oversigt over administration af vedligeholdelsesanmodninger i Styring af aktiver
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7038269c66092367a0faf147766cb45eb5364e1b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890123"
---
# <a name="maintenance-requests"></a><span data-ttu-id="65e5e-103">Vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="65e5e-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="65e5e-104">Vedligeholdelsesanmodninger er noter eller erklæringer, som er oprettet med henblik på at underrette en leder eller planlægger om, at et aktiv muligvis kræver et vedligeholdelses-eller reparationsjob, men som ikke kræver, at der oprettes en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="65e5e-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="65e5e-105">Hvis indholdet af en vedligeholdelsesanmodning anses for at være gyldigt, kan der derefter oprettes en arbejdsordre på grundlag af vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="65e5e-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="65e5e-106">Der kan oprettes vedligeholdelsesanmodninger for alle aktiver i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="65e5e-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="65e5e-107">Der kan oprettes forskellige typer vedligeholdelsesanmodninger afhængigt af, hvordan din virksomhed anvender vedligeholdelsesanmodninger.</span><span class="sxs-lookup"><span data-stu-id="65e5e-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="65e5e-108">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="65e5e-108">Here are some examples:</span></span>

- <span data-ttu-id="65e5e-109">Vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="65e5e-109">Maintenance requests</span></span>
- <span data-ttu-id="65e5e-110">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="65e5e-110">Notes</span></span>
- <span data-ttu-id="65e5e-111">Rettelser eller forbedringer</span><span class="sxs-lookup"><span data-stu-id="65e5e-111">Corrections or enhancements</span></span>
- <span data-ttu-id="65e5e-112">Investeringer</span><span class="sxs-lookup"><span data-stu-id="65e5e-112">Investments</span></span>
- <span data-ttu-id="65e5e-113">Reparation af depot (denne type anvendes, når du modtager aktiver fra et andet sted, for at gøre det muligt for dig at udføre et vedligeholdelses-eller reparationsjob, og du derefter returnerer aktivet, når jobbet er fuldført).</span><span class="sxs-lookup"><span data-stu-id="65e5e-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="65e5e-114">Se vedligeholdelsesanmodninger</span><span class="sxs-lookup"><span data-stu-id="65e5e-114">View maintenance requests</span></span>

<span data-ttu-id="65e5e-115">Hvis du have vist vedligeholdelsesanmodninger, skal vælge **Styring af aktiver** \> **Almindelig** \> **Vedligeholdelsesanmodninger** \> **Alle vedligeholdelsesanmodninger**, **Aktive vedligeholdelsesanmodninger** eller **Vedligeholdelsesanmodninger for mine arbejdssteder**.</span><span class="sxs-lookup"><span data-stu-id="65e5e-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="65e5e-116">Hver listeside viser nogle af de oplysninger, der er relateret til en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Vis vedligeholdelsesanmodninger](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="65e5e-118">Brug listesiden **Vedligeholdelsesanmodninger for mine arbejdssteder** for at få vist en liste over vedligeholdelsesanmodninger, der indeholder enten arbejdssteder, som du er relateret til som arbejder, eller aktiver, der er installeret på de arbejdssteder, som du er relateret til som arbejder.</span><span class="sxs-lookup"><span data-stu-id="65e5e-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="65e5e-119">(Du finder oplysninger om, hvordan du konfigurerer arbejdssteder for vedligeholdelsesarbejdere, i [Vedligeholdelsesarbejdere og arbejdergrupper](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="65e5e-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="65e5e-120">Selvom kundekontooplysninger er tilgængelige i Styring af tjenesten for aktiver (ekstern vedligeholdelse), er de ikke tilgængelig i Styring af aktiver (intern vedligeholdelse).</span><span class="sxs-lookup"><span data-stu-id="65e5e-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="65e5e-121">For at åbne detaljevisning for en post skal du i gittervisningen på listesiden **Alle vedligeholdelsesanmodninger** vælge et link i kolonnen **Vedligeholdelsesanmodning**.</span><span class="sxs-lookup"><span data-stu-id="65e5e-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Se detaljer om vedligeholdelsesanmodning](media/02-manage-maintenance-requests.png)

<span data-ttu-id="65e5e-123">Knapperne i Handlingsruden er organiseret på faner.</span><span class="sxs-lookup"><span data-stu-id="65e5e-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="65e5e-124">Følgende tabel beskriver kort de knapper, der er relateret til Aktiv styring.</span><span class="sxs-lookup"><span data-stu-id="65e5e-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="65e5e-125">Knapnavn</span><span class="sxs-lookup"><span data-stu-id="65e5e-125">Button name</span></span>                      | <span data-ttu-id="65e5e-126">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="65e5e-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="65e5e-127">Rediger</span><span class="sxs-lookup"><span data-stu-id="65e5e-127">Edit</span></span>                             | <span data-ttu-id="65e5e-128">Rediger den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-129">Nyt</span><span class="sxs-lookup"><span data-stu-id="65e5e-129">New</span></span>                              | <span data-ttu-id="65e5e-130">Opret en ny vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="65e5e-131">Slet</span><span class="sxs-lookup"><span data-stu-id="65e5e-131">Delete</span></span>                           | <span data-ttu-id="65e5e-132">Slet den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-133">Arbejdsordrepulje</span><span class="sxs-lookup"><span data-stu-id="65e5e-133">Work order pool</span></span>                  | <span data-ttu-id="65e5e-134">Knyt den valgte vedligeholdelsesanmodning til en arbejdsordrepulje.</span><span class="sxs-lookup"><span data-stu-id="65e5e-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="65e5e-135">Arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="65e5e-135">Work order</span></span>                       | <span data-ttu-id="65e5e-136">Opret en arbejdsordre på grundlag af den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-137">Fejl for aktivet</span><span class="sxs-lookup"><span data-stu-id="65e5e-137">Asset fault</span></span>                      | <span data-ttu-id="65e5e-138">Klik på **Fejl for aktivet**, hvor du kan oprette en fejlregistrering på den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-139">Arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="65e5e-139">Work orders</span></span>                      | <span data-ttu-id="65e5e-140">Viser en liste over alle arbejdsordrer, der er knyttet til den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-141">Opdater tilstanden for vedligeholdelsesanmodningen</span><span class="sxs-lookup"><span data-stu-id="65e5e-141">Update maintenance request state</span></span> | <span data-ttu-id="65e5e-142">Opdater tilstanden for vedligeholdelsesanmodningen.</span><span class="sxs-lookup"><span data-stu-id="65e5e-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="65e5e-143">Log for livscyklustilstand</span><span class="sxs-lookup"><span data-stu-id="65e5e-143">Lifecycle state log</span></span>              | <span data-ttu-id="65e5e-144">Se en log, der viser livscyklustilstande for den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-145">Detaljer for vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-145">Maintenance request details</span></span>      | <span data-ttu-id="65e5e-146">Udskriv en rapport, der viser detaljerne for den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-147">Send udlånsaktiv</span><span class="sxs-lookup"><span data-stu-id="65e5e-147">Send loan asset</span></span>                  | <span data-ttu-id="65e5e-148">Vælg et udlånsaktiv, der skulle have været en midlertidig erstatning for det aktiv, der er valgt i den valgte vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="65e5e-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="65e5e-149">Returner udlånsaktivet</span><span class="sxs-lookup"><span data-stu-id="65e5e-149">Return loan asset</span></span>                | <span data-ttu-id="65e5e-150">Registrer udlånsaktivet som returneret.</span><span class="sxs-lookup"><span data-stu-id="65e5e-150">Register the loan asset as returned.</span></span> |

