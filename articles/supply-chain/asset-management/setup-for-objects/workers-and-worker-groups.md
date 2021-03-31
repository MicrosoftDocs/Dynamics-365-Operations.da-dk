---
title: Vedligeholdelsesarbejdere og arbejdergrupper
description: I dette emne forklares vedligeholdelsesarbejdere og arbejdergrupper i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00ada9e43ae08e1757de618bd2d63dc147beeca0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226827"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="94ee2-103">Vedligeholdelsesarbejdere og arbejdergrupper</span><span class="sxs-lookup"><span data-stu-id="94ee2-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="94ee2-104">I dette emne forklares vedligeholdelsesarbejdere og arbejdergrupper i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="94ee2-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="94ee2-105">I Styring af aktiver kan du knytte vedligeholdelsesarbejdere til arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="94ee2-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="94ee2-106">(Du finder flere oplysninger om arbejdssteder under [Opret arbejdssteder](../functional-locations/create-functional-locations.md).) Denne funktion kan være nyttig, hvis du eksempelvis planlægger et vedligeholdelsesjob på en maskine, der er placeret i arbejdssted 01, og du vil allokere vedligeholdelsesarbejdere fra samme sted til at udføre jobbet.</span><span class="sxs-lookup"><span data-stu-id="94ee2-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="94ee2-107">Du kan også oprette vedligeholdelsesarbejdergrupper og knytte vedligeholdelsesarbejdere til dem.</span><span class="sxs-lookup"><span data-stu-id="94ee2-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="94ee2-108">Denne funktion er nyttig, når du laver enkel arbejdsordreplanlægning, og du vil planlægge en gruppe vedligeholdelsesarbejdere på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="94ee2-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="94ee2-109">Du kan bruge vedligeholdelsesarbejdere og vedligeholdelsesarbejdergrupper til at oprette foretrukne vedligeholdelsesarbejdere og ansvarlige vedligeholdelsesarbejdere.</span><span class="sxs-lookup"><span data-stu-id="94ee2-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="94ee2-110">Opret medarbejdere</span><span class="sxs-lookup"><span data-stu-id="94ee2-110">Create workers</span></span>

1. <span data-ttu-id="94ee2-111">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="94ee2-112">Vælg **Ny** for at føje en arbejder til listen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="94ee2-113">I feltet **Arbejder** skal du vælge arbejderen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="94ee2-114">Angiv indstillingen **Aktiv** til **Ja** for at planlægge arbejderen på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="94ee2-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="94ee2-115">I oversigtspanelet **Generelt** udfyldes felterne **Ressource** og **Beskrivelse** automatisk, hvis der er valgt en ressource for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="94ee2-116">Feltet **Kalender** udfyldes også automatisk, forudsat at du har oprettet arbejderen som en ressource og har allokeret en kalender til den pågældende ressource på siden **Ressourcer** (**Organisationsadministration** \> **Ressourcer** \> **Ressourcer**).</span><span class="sxs-lookup"><span data-stu-id="94ee2-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="94ee2-117">I oversigtspanelet **Grupper** skal du vælge **Tilføj** og derefter vælge en vedligeholdelsesarbejdergruppe for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="94ee2-118">En arbejder kan knyttes til mere end én gruppe.</span><span class="sxs-lookup"><span data-stu-id="94ee2-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="94ee2-119">I standardopsætningen er en arbejders tilknytning til en gruppe gældende fra den dato, hvor du tilføjer gruppen, og den udløber aldrig.</span><span class="sxs-lookup"><span data-stu-id="94ee2-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="94ee2-120">Denne dato vises i feltet **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="94ee2-121">Hvis du vil se feltet **Gyldig**, skal du vælge **Se** \> **Alle**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="94ee2-122">Hvis arbejderens tilknytning til en gruppe bør begrænses til en bestemt periode, skal du bruge felterne **Gyldig** og **Udløb** til at definere perioden.</span><span class="sxs-lookup"><span data-stu-id="94ee2-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="94ee2-123">I oversigtspanelet **Arbejdssteder** skal du vælge **Tilføj** og derefter vælge et arbejdssted for vedligeholdelsesarbejderen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="94ee2-124">Angiv også, hvilket sted der er arbejderens primære arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="94ee2-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="94ee2-125">Når du føjer arbejdssteder til en arbejder, vises alle aktive aktiver, der er relateret til disse arbejdssteder, på forskellige menupunkter såsom **Mine aktive aktiver** og **Mine aktive arbejdssteder**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="94ee2-126">De fremgår også af de opslag i aktiver, der vises, når du opretter et nyt aktiv, en vedligeholdelsesanmodning eller en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="94ee2-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="94ee2-127">Felterne i oversigtspanelet **Detaljer** viser antallet af vedligeholdelsesarbejdergrupper og de arbejdssteder, som den valgte vedligeholdelsesarbejder er relateret til.</span><span class="sxs-lookup"><span data-stu-id="94ee2-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="94ee2-128">Opret arbejdergrupper</span><span class="sxs-lookup"><span data-stu-id="94ee2-128">Create worker groups</span></span>

1. <span data-ttu-id="94ee2-129">Vælg **Styring af aktiver** \> **Opsætning** \> **Arbejdere** \> **Vedligeholdelsesarbejdergrupper**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="94ee2-130">Vælg **Ny** for at føje en arbejdergruppe til listen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="94ee2-131">I feltet **Vedligeholdelsesarbejdergruppe** skal du indtaste et ID for gruppen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="94ee2-132">Indtast et navn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="94ee2-133">I oversigtspanelet **Arbejdere** skal du vælge **Tilføj** og derefter vælge en vedligeholdelsesarbejder for arbejdergruppen.</span><span class="sxs-lookup"><span data-stu-id="94ee2-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="94ee2-134">Yderligere oplysninger om felterne **Gyldig** og **Udløb** finder du i trin 6 i den forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="94ee2-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="94ee2-135">Hvis en ressourcegruppe skal relateres til den valgte vedligeholdelsesarbejdergruppe, skal du vælge **Kopiér fra ressourcegruppe**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="94ee2-136">Vælg den ressourcegruppe, du vil kopiere kalenderindstillinger fra, i feltet **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="94ee2-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="94ee2-137">I feltet **Arbejdergruppe** skal du derefter vælge den arbejdergruppe, som ressourcegruppens kalenderindstillinger skal kopieres til.</span><span class="sxs-lookup"><span data-stu-id="94ee2-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="94ee2-138">Dette trin er kun relevant, hvis du ønsker, at vedligeholdelsesarbejderne skal bruge den kalender, der er relateret til en ressource (arbejdscenter) under planlægningen af arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="94ee2-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="94ee2-139">Feltet i oversigtspanelet **Detaljer** viser antallet af vedligeholdelsesarbejdere, som er blevet konfigureret for den valgte vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="94ee2-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]