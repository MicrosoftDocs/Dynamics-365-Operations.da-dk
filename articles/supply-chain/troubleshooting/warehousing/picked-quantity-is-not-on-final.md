---
title: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
description: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301299"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="a6cb6-103">Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer</span><span class="sxs-lookup"><span data-stu-id="a6cb6-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="a6cb6-104">Fejlkode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="a6cb6-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="a6cb6-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a6cb6-105">Symptoms</span></span>

<span data-ttu-id="a6cb6-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="a6cb6-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="a6cb6-107">Nogle af varerne, der skal bruges til lasten %1, er endnu ikke plukket og flyttet til den endelige afsendelseslokation.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="a6cb6-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a6cb6-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="a6cb6-109">Cause</span></span>

<span data-ttu-id="a6cb6-110">Lasten eller forsendelsen kan ikke bekræftes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:</span><span class="sxs-lookup"><span data-stu-id="a6cb6-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="a6cb6-111">Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="a6cb6-112">Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="a6cb6-113">Lokationsvejledningen er konfigureret med pakkelokation som den endelig forsendelseslokation ved brug af containerisering for bølgeskabeloner.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="a6cb6-114">Løsning</span><span class="sxs-lookup"><span data-stu-id="a6cb6-114">Resolution</span></span>

<span data-ttu-id="a6cb6-115">Lasten eller forsendelsen er i øjeblikket i en tilstand, hvor forsendelsesbekræftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="a6cb6-116">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="a6cb6-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="a6cb6-117">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="a6cb6-118">Annuller de arbejds-id'er, der er oprettet med pakkelokationen som den endelige forsendelseslokation, konfigurer lokationsvejledningen igen, og frigiv lasten igen.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="a6cb6-119">Gennemse dine lastlinjer, og kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens</span><span class="sxs-lookup"><span data-stu-id="a6cb6-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="a6cb6-120">Brug følgende procedure til at gennemse dine lastlinjer og kontrollere, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="a6cb6-121">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a6cb6-122">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="a6cb6-123">Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="a6cb6-124">Notér værdien for feltet **Antal oprettet under arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="a6cb6-125">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="a6cb6-126">Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="a6cb6-127">Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="a6cb6-128">Annuller de arbejds-id'er, der er oprettet med pakkelokationen som den endelige forsendelseslokation, konfigurer lokationsvejledningen igen, og frigiv lasten igen</span><span class="sxs-lookup"><span data-stu-id="a6cb6-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="a6cb6-129">Du kan bruge følgende procedure til at annullere de arbejds-id'er, der har pakkelokationen som den endelige læg på lager-lokation med automatisk containerisering på plads.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="a6cb6-130">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="a6cb6-131">Dialogboksen **Annuller arbejde** åbnes.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="a6cb6-132">Angiv id'et for det arbejde, du vil annullere, i feltet **Arbejds-id**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="a6cb6-133">For det valgte arbejds-id skal værdien for **Arbejdsstatus** være *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="a6cb6-134">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-134">Select **OK**.</span></span>
1. <span data-ttu-id="a6cb6-135">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="a6cb6-136">Gentag denne procedure for de andre arbejds-id'er, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="a6cb6-137">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="a6cb6-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="a6cb6-138">Benyt følgende fremgangsmåde for at genkonfigurere lokationsvejledningen, så den ikke bruger pakkelokationen som den endelige forsendelseslokation, når der er konfigureret automatisk containerisering for bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="a6cb6-139">Gå til **Lokationsstyring \> Opsætning \> Lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a6cb6-140">I feltet **Arbejdsordretype** skal du vælge *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="a6cb6-141">Vælg den lokationsvejledning, du bruger til automatiseret containerisering.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="a6cb6-142">Vælg **Rediger forespørgsel** på værktøjslinjen i oversigtspanelet **Handlinger for lokationsvejledninger**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="a6cb6-143">Find den række, hvor **Felt** er angivet til *Lokationsprofil*, i dialogboksen med forespørgselseditoren under fanen **Interval**, og kontrollér, at feltet **Kriterie** for den pågældende række ikke er angivet til en lokationsprofil, hvor **Lokationstype** er *Emballage*.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="a6cb6-144">Juster feltet **Kriterie** for at rette den endelige placering.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="a6cb6-145">Benyt følgende fremgangsmåde for at frigive lasten igen og oprette arbejds-id'er med den korrekte endelige forsendelseslokation.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="a6cb6-146">Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="a6cb6-147">Find den last, der skal frigives, i sektionen **Laster**.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="a6cb6-148">Vælg **Frigiv \> Frigiv til lagersted** på værktøjslinjen for sektionen **Laster** for at frigive den valgte last til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="a6cb6-149">Gentag denne procedure for de andre laster, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="a6cb6-149">Repeat this procedure for the other loads as needed.</span></span>
