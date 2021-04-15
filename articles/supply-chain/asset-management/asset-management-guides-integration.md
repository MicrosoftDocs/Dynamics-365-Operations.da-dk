---
title: Integrere Dynamics 365 Supply Chain Management (Styring af aktiver) med Dynamics 365 Guides
description: I dette emne forklares, hvordan du kan integrere modulet Styring af aktiver i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for at udnytte Mixed Reality-hjælpelinjer i din service fra dag til dag og dine vedligeholdelsesarbejdsgange.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 4af14a66c839ccee02008057ad1de8ef5b9d291b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813911"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="9bac6-103">Integrere Dynamics 365 Supply Chain Management (Styring af aktiver) med Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="9bac6-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="9bac6-104">Du kan integrere modulet **Styring af aktiver** i Microsoft Dynamics 365 Supply Chain Management med Dynamics 365 Guides for at udnytte Mixed Reality-guider i din service fra dag til og dine vedligeholdelsesarbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="9bac6-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="9bac6-105">Hvis der er knyttet en hjælpelinje til en arbejdsordre i Styring af aktiver, kan en arbejder, der åbner en arbejdsordres vedligeholdelsestjekliste i Supply Chain Management 365 (Dynamics 365)-mobilappen, se, at en hjælpelinje er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="9bac6-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="9bac6-106">Arbejderen kan derefter finde og åbne hjælpelinjen i Dynamics 365 Guides HoloLens-appen.</span><span class="sxs-lookup"><span data-stu-id="9bac6-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9bac6-107">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="9bac6-107">Prerequisites</span></span>

<span data-ttu-id="9bac6-108">Før du kan føje hjælpelinjer til arbejdsordrer i Styring af aktiver, skal du fuldføre disse forudsætninger:</span><span class="sxs-lookup"><span data-stu-id="9bac6-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="9bac6-109">[Konfigurere Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="9bac6-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="9bac6-110">[Slå dobbeltskrivning til for Supply Chain Management-apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="9bac6-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="9bac6-111">[Slå flight til](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for **MRGuidesFeature**-funktionen.</span><span class="sxs-lookup"><span data-stu-id="9bac6-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="9bac6-112">(I forbindelse med produktionsmiljøer skal du først sende en supportanmodning for at få din lejer føjet til flighting-gruppen).</span><span class="sxs-lookup"><span data-stu-id="9bac6-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="9bac6-113">[Slå følgende konfigurationsnøgler til](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) på siden **Licenskonfiguration**:</span><span class="sxs-lookup"><span data-stu-id="9bac6-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="9bac6-114">Styring af aktiver \> Styring af aktiver – Mixed Reality</span><span class="sxs-lookup"><span data-stu-id="9bac6-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="9bac6-115">Mixed Reality \> Hjælpelinje til Mixed Reality</span><span class="sxs-lookup"><span data-stu-id="9bac6-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="9bac6-116">[Konfigurere Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="9bac6-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="9bac6-117">Bruge Dynamics 365 Guides med Styring af aktiver</span><span class="sxs-lookup"><span data-stu-id="9bac6-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="9bac6-118">Hvis du vil tilknytte en hjælpelinje, skal du bruge en vedligeholdelsestjeklistelinje i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="9bac6-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="9bac6-119">Du kan oprette tilknytningen via en vedligeholdelsestjeklisteskabelon, en vedligeholdelsesjobtype eller en arbejdsordre, da alle tre indeholder vedligeholdelsestjeklistelinjer.</span><span class="sxs-lookup"><span data-stu-id="9bac6-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="9bac6-120">Du kan spare tid ved at bruge en skabelon, da en skabelon kan knyttes til alle de vedligeholdelsesjobtyper, der bruger den.</span><span class="sxs-lookup"><span data-stu-id="9bac6-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="9bac6-121">En hjælpelinje, der f.eks. er tilknyttet en vedligeholdelsesjobtype, knyttes automatisk til alle de arbejdsordrer, der angiver den pågældende jobtype.</span><span class="sxs-lookup"><span data-stu-id="9bac6-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="9bac6-122">På den anden side eksisterer en hjælpelinje, der er tilknyttet en arbejdsordre direkte, kun for den pågældende arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="9bac6-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="9bac6-123">Knytte en hjælpelinje til en vedligeholdelsestjeklisteskabelon</span><span class="sxs-lookup"><span data-stu-id="9bac6-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="9bac6-124">Du kan knytte en hjælpelinje til en vedligeholdelsestjekliste ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9bac6-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="9bac6-125">Opret en hjælpelinje ved hjælp af Dynamics 365 Guides-pc- og HoloLens-appen.</span><span class="sxs-lookup"><span data-stu-id="9bac6-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="9bac6-126">Du kan få oplysninger om, hvordan du opretter en hjælpelinje, i følgende emner:</span><span class="sxs-lookup"><span data-stu-id="9bac6-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="9bac6-127">Bruge pc-appen til at oprette en hjælpelinje</span><span class="sxs-lookup"><span data-stu-id="9bac6-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="9bac6-128">Bruge HoloLens-appen til at placere din hologrammer</span><span class="sxs-lookup"><span data-stu-id="9bac6-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="9bac6-129">[Opret en vedligeholdelsestjeklisteskabelon](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9bac6-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="9bac6-130">Knyt den hjælpelinje, du har oprettet, til en vedligeholdelsestjeklistelinje i den nye vedligeholdelsestjeklisteskabelon:</span><span class="sxs-lookup"><span data-stu-id="9bac6-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="9bac6-131">På oversigtspanelet **Vedligeholdelsestjeklistelinjer** skal du vælge den linje, du vil knytte hjælpelinjen til.</span><span class="sxs-lookup"><span data-stu-id="9bac6-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="9bac6-132">Vælg **Tilføj hjælpelinje** på oversigtspanelet **Tilknyttede hjælpelinjer**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="9bac6-133">![Knytte en hjælpelinje til en vedligeholdelsestjeklistelinje](media/am-guides-integration-add-guide.png "Knytte en hjælpelinje til en vedligeholdelsestjeklistelinje")</span><span class="sxs-lookup"><span data-stu-id="9bac6-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="9bac6-134">Vælg en hjælpelinje i feltet **Navn**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="9bac6-135">![Vælge en hjælpelinje i feltet Navn](media/am-guides-integration-select-guide.png "Vælge en hjælpelinje i feltet Navn")</span><span class="sxs-lookup"><span data-stu-id="9bac6-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="9bac6-136">Knyt vedligeholdelsestjeklisteskabelonen til en jobtype:</span><span class="sxs-lookup"><span data-stu-id="9bac6-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="9bac6-137">[Opret en vedligeholdelsesjobtype](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), eller vælg en eksisterende vedligeholdelsesjobtype.</span><span class="sxs-lookup"><span data-stu-id="9bac6-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="9bac6-138">Vælg **Standarder for vedligeholdelsesjobtype** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9bac6-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="9bac6-139">![Knappen Standarder for vedligeholdelsesjobtype](media/am-guides-integration-job-defaults.png "Knappen Standarder for vedligeholdelsesjobtype")</span><span class="sxs-lookup"><span data-stu-id="9bac6-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="9bac6-140">Opret en linje, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="9bac6-141">![Oprette en linje](media/am-guides-integration-add-line.png "Oprette en linje")</span><span class="sxs-lookup"><span data-stu-id="9bac6-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="9bac6-142">Vælg **Vedligeholdelsestjekliste** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9bac6-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="9bac6-143">![Knappen Vedligeholdelsestjekliste](media/am-guides-integration-maintenance-checklist.png "Knappen Vedligeholdelsestjekliste")</span><span class="sxs-lookup"><span data-stu-id="9bac6-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="9bac6-144">På oversigtspanelet **Vedligeholdelsestjeklistelinjer** skal du tilføje en linje og derefter ændre værdien i feltet **Type** til **Skabelon**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="9bac6-145">![Ændre værdien Type](media/am-guides-integration-checklist-lines.png "Ændre værdien Type")</span><span class="sxs-lookup"><span data-stu-id="9bac6-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="9bac6-146">Vælg den skabelon, du har knyttet til hjælpelinjen, i feltet **Skabelon** på oversigtspanelet **Linjedetaljer**, og vælg derefter **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="9bac6-147">![Vælge skabelonen](media/am-guides-integration-checklist-line-details.png "Vælge skabelonen")</span><span class="sxs-lookup"><span data-stu-id="9bac6-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="9bac6-148">[Opret en arbejdsordre](work-orders/manually-created-workorders.md#create-work-order), og vælg derefter den vedligeholdelsesjobtype, der bruger den vedligeholdelsestjeklisteskabelon, du har tilknyttet hjælpelinjen med.</span><span class="sxs-lookup"><span data-stu-id="9bac6-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="9bac6-149">Hjælpelinjen knyttes automatisk til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="9bac6-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="9bac6-150">![Vælge en vedligeholdelsesjobtype](media/am-guides-integration-create-work-order.png "Vælge en vedligeholdelsesjobtype")</span><span class="sxs-lookup"><span data-stu-id="9bac6-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="9bac6-151">Få vist den hjælpelinje, der er tilknyttet arbejdsordren og arbejderne:</span><span class="sxs-lookup"><span data-stu-id="9bac6-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="9bac6-152">Åbn [Arbejdsområdet Styring af aktiver på mobilenheder](asset-management-mobile-workspace.md) for at få adgang til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="9bac6-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="9bac6-153">[Åbn vedligeholdelsestjeklisten](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="9bac6-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="9bac6-154">Vælg en tjeklistelinje for at få vist den tilknyttede hjælpelinje.</span><span class="sxs-lookup"><span data-stu-id="9bac6-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="9bac6-155">![Hjælpelinje knyttet til en tjeklistelinje](media/am-guides-integration-show-guide.png "Hjælpelinje knyttet til en tjeklistelinje")</span><span class="sxs-lookup"><span data-stu-id="9bac6-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="9bac6-156">Åbn hjælpelinjen i HoloLens.</span><span class="sxs-lookup"><span data-stu-id="9bac6-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="9bac6-157">![Åbne hjælpelinjen i HoloLens](media/am-guides-integration-hololens-select.png "Åbne hjælpelinjen i HoloLens")</span><span class="sxs-lookup"><span data-stu-id="9bac6-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="9bac6-158">Du kan også knytte en hjælpelinje direkte til vedligeholdelsestjeklisten for en arbejdsordre eller en jobtype.</span><span class="sxs-lookup"><span data-stu-id="9bac6-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bac6-159">Der er et velkendt problem, når du knytter en vedligeholdelsestjeklisteskabelon til en standardvedligeholdelsesjobtype, hvor hjælpelinjen, der er tilknyttet skabelonen, ikke vises på oversigtspanelet **Tilknyttede hjælpelinjer** på siden **Standarder for vedligeholdelsesjobtype**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="9bac6-160">Hjælpelinjen vises dog, når denne jobtype anvendes på en arbejdsordre på oversigtspanelet **Tilknyttede hjælpelinjer**.</span><span class="sxs-lookup"><span data-stu-id="9bac6-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bac6-161">Se også</span><span class="sxs-lookup"><span data-stu-id="9bac6-161">See also</span></span>

- [<span data-ttu-id="9bac6-162">Oversigt over dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="9bac6-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="9bac6-163">Oversigt over aktivstyring</span><span class="sxs-lookup"><span data-stu-id="9bac6-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]