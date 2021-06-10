---
title: Tildele trinikoner og titler til mobilappen Warehouse Management
description: I dette emne beskrives, hvordan du tildeler trinikoner og titler til nye eller tilpassede opgaveflow for mobilappen Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049358"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ff0f3-103">Tildele trinikoner og titler til mobilappen Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="ff0f3-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff0f3-104">I dette emne beskrives, hvordan du tildeler trinikoner og trintitler til nye eller tilpassede opgaveflow for mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ff0f3-105">Følgende illustrationer viser, hvordan trinikoner og titler vises i mobilappen Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ff0f3-106">![Eksempel på et trinikon og en trintitel i mobilappen Warehouse Management](media/step-icon-example.png "Eksempel på et trinikon og en trintitel i mobilappen Warehouse Management")</span><span class="sxs-lookup"><span data-stu-id="ff0f3-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="ff0f3-107">Aktivere denne funktion i systemet</span><span class="sxs-lookup"><span data-stu-id="ff0f3-107">Turn on this feature in your system</span></span>

<span data-ttu-id="ff0f3-108">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ff0f3-109">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ff0f3-110">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="ff0f3-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ff0f3-111">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="ff0f3-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ff0f3-112">**Funktionsnavn:** *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp*</span><span class="sxs-lookup"><span data-stu-id="ff0f3-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="ff0f3-113">Standardtrin-id'er, klasser og ikoner</span><span class="sxs-lookup"><span data-stu-id="ff0f3-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="ff0f3-114">Hvert trin i et opgaveflow identificeres af et trin-id, og hvert trin-id har en tilsvarende trinklasse.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="ff0f3-115">Trinikonet og titlen angives i hver trinklasse.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="ff0f3-116">Trin-id'er og trinklasser</span><span class="sxs-lookup"><span data-stu-id="ff0f3-116">Step IDs and step classes</span></span>

<span data-ttu-id="ff0f3-117">I følgende tabel vises alle de trin-id'er, der i øjeblikket er tilgængelige, og den tilsvarende trinklasse.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="ff0f3-118">Kontrolnavnet på det primære inputfelt bruges som trin-id.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="ff0f3-119">Du kan se et eksempel, der viser, hvordan disse trin-id'er og klasser bruges, i implementeringen af `WHSMobileAppStepInfoBuilder.stepId()`-metoden i afsnittet [Eksempel: Tildele trinikoner og titler til et brugerdefineret flow](#example) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="ff0f3-120">Trin-id</span><span class="sxs-lookup"><span data-stu-id="ff0f3-120">Step ID</span></span> | <span data-ttu-id="ff0f3-121">Trinklasse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="ff0f3-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-122">BatchDisposition</span></span> | <span data-ttu-id="ff0f3-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="ff0f3-124">Fragtmand</span><span class="sxs-lookup"><span data-stu-id="ff0f3-124">Carrier</span></span> | <span data-ttu-id="ff0f3-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="ff0f3-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="ff0f3-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-126">CatchWeight</span></span> | <span data-ttu-id="ff0f3-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff0f3-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="ff0f3-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff0f3-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff0f3-130">CatchWeightTag</span></span> | <span data-ttu-id="ff0f3-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff0f3-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ff0f3-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="ff0f3-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="ff0f3-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ff0f3-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="ff0f3-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="ff0f3-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="ff0f3-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff0f3-136">CheckDigit</span></span> | <span data-ttu-id="ff0f3-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff0f3-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="ff0f3-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-138">ClusterId</span></span> | <span data-ttu-id="ff0f3-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="ff0f3-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="ff0f3-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff0f3-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-142">ClusterPosition</span></span> | <span data-ttu-id="ff0f3-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="ff0f3-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-144">ConfigId</span></span> | <span data-ttu-id="ff0f3-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="ff0f3-146">Bekræftelse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-146">Confirmation</span></span> | <span data-ttu-id="ff0f3-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="ff0f3-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="ff0f3-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="ff0f3-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="ff0f3-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="ff0f3-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="ff0f3-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="ff0f3-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-154">ContainerType</span></span> | <span data-ttu-id="ff0f3-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="ff0f3-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff0f3-156">CountingReasonCode</span></span> | <span data-ttu-id="ff0f3-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff0f3-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="ff0f3-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ff0f3-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="ff0f3-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="ff0f3-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="ff0f3-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="ff0f3-160">CycleCountQty1</span></span> | <span data-ttu-id="ff0f3-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff0f3-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="ff0f3-162">CycleCountQty2</span></span> | <span data-ttu-id="ff0f3-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff0f3-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="ff0f3-164">CycleCountQty3</span></span> | <span data-ttu-id="ff0f3-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff0f3-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="ff0f3-166">CycleCountQty4</span></span> | <span data-ttu-id="ff0f3-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ff0f3-168">Disposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-168">Disposition</span></span> | <span data-ttu-id="ff0f3-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="ff0f3-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="ff0f3-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="ff0f3-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-172">DriverCheckInId</span></span> | <span data-ttu-id="ff0f3-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="ff0f3-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="ff0f3-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="ff0f3-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-176">DriverCheckOutId</span></span> | <span data-ttu-id="ff0f3-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="ff0f3-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ff0f3-178">ExpDate</span></span> | <span data-ttu-id="ff0f3-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="ff0f3-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="ff0f3-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-180">FromBatchDisposition</span></span> | <span data-ttu-id="ff0f3-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="ff0f3-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ff0f3-182">FromInventoryStatus</span></span> | <span data-ttu-id="ff0f3-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="ff0f3-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="ff0f3-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-184">FullQty</span></span> | <span data-ttu-id="ff0f3-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="ff0f3-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-186">InboundPut</span></span> | <span data-ttu-id="ff0f3-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="ff0f3-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-188">InventBatchId</span></span> | <span data-ttu-id="ff0f3-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="ff0f3-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="ff0f3-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-190">InventColorId</span></span> | <span data-ttu-id="ff0f3-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="ff0f3-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-192">InventLocation</span></span> | <span data-ttu-id="ff0f3-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="ff0f3-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-194">InventLocationId</span></span> | <span data-ttu-id="ff0f3-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="ff0f3-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-196">InventSerialId</span></span> | <span data-ttu-id="ff0f3-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="ff0f3-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-198">InventSizeId</span></span> | <span data-ttu-id="ff0f3-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="ff0f3-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-200">InventStatusId</span></span> | <span data-ttu-id="ff0f3-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="ff0f3-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="ff0f3-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-202">InventStyleId</span></span> | <span data-ttu-id="ff0f3-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="ff0f3-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-204">InventVersionId</span></span> | <span data-ttu-id="ff0f3-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="ff0f3-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-206">ItemId</span></span> | <span data-ttu-id="ff0f3-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="ff0f3-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="ff0f3-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-208">ITMContainerID</span></span> | <span data-ttu-id="ff0f3-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="ff0f3-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-210">ITMShipmentID</span></span> | <span data-ttu-id="ff0f3-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="ff0f3-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-212">KanbanCardId</span></span> | <span data-ttu-id="ff0f3-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ff0f3-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ff0f3-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="ff0f3-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="ff0f3-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-216">KanbanOrCardId</span></span> | <span data-ttu-id="ff0f3-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="ff0f3-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ff0f3-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-218">LicensePlateId</span></span> | <span data-ttu-id="ff0f3-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="ff0f3-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="ff0f3-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-220">LoadId</span></span> | <span data-ttu-id="ff0f3-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="ff0f3-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="ff0f3-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="ff0f3-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-224">LocOrLP</span></span> | <span data-ttu-id="ff0f3-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="ff0f3-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="ff0f3-226">LocOrLP_From</span></span> | <span data-ttu-id="ff0f3-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ff0f3-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="ff0f3-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="ff0f3-228">LocOrLP_To</span></span> | <span data-ttu-id="ff0f3-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ff0f3-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="ff0f3-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff0f3-230">LocOrLPCheck</span></span> | <span data-ttu-id="ff0f3-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff0f3-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="ff0f3-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-232">LocVerification</span></span> | <span data-ttu-id="ff0f3-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="ff0f3-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff0f3-234">LPAdjustIn</span></span> | <span data-ttu-id="ff0f3-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff0f3-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="ff0f3-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-236">LPBreakChildLP</span></span> | <span data-ttu-id="ff0f3-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="ff0f3-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-238">LPBreakParentLP</span></span> | <span data-ttu-id="ff0f3-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="ff0f3-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-240">LPBuildChildLP</span></span> | <span data-ttu-id="ff0f3-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="ff0f3-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-242">LPBuildParentLP</span></span> | <span data-ttu-id="ff0f3-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="ff0f3-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-244">LPVerification</span></span> | <span data-ttu-id="ff0f3-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="ff0f3-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-246">MergeContainerId</span></span> | <span data-ttu-id="ff0f3-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="ff0f3-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-248">MixedLPLineNum</span></span> | <span data-ttu-id="ff0f3-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="ff0f3-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="ff0f3-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="ff0f3-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="ff0f3-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ff0f3-252">MovementConfirmCancel</span></span> | <span data-ttu-id="ff0f3-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="ff0f3-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="ff0f3-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-254">NewCaptureWeight</span></span> | <span data-ttu-id="ff0f3-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff0f3-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-256">NewQty</span></span> | <span data-ttu-id="ff0f3-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="ff0f3-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff0f3-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="ff0f3-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff0f3-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ff0f3-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-260">OutboundPut</span></span> | <span data-ttu-id="ff0f3-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="ff0f3-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-262">OutboundWeight</span></span> | <span data-ttu-id="ff0f3-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ff0f3-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-264">OverridePutNewLocation</span></span> | <span data-ttu-id="ff0f3-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="ff0f3-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="ff0f3-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff0f3-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-268">POLineNum</span></span> | <span data-ttu-id="ff0f3-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="ff0f3-270">Indkøbsordrenummer</span><span class="sxs-lookup"><span data-stu-id="ff0f3-270">PONum</span></span> | <span data-ttu-id="ff0f3-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="ff0f3-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ff0f3-272">PositionFull</span></span> | <span data-ttu-id="ff0f3-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="ff0f3-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="ff0f3-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-274">PositionFullQty</span></span> | <span data-ttu-id="ff0f3-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="ff0f3-276">Styrke</span><span class="sxs-lookup"><span data-stu-id="ff0f3-276">Potency</span></span> | <span data-ttu-id="ff0f3-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="ff0f3-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="ff0f3-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ff0f3-278">PrinterName</span></span> | <span data-ttu-id="ff0f3-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="ff0f3-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="ff0f3-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-280">ProdId</span></span> | <span data-ttu-id="ff0f3-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="ff0f3-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="ff0f3-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="ff0f3-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-284">ProductConfirmation</span></span> | <span data-ttu-id="ff0f3-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="ff0f3-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="ff0f3-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="ff0f3-288">Læg på lager</span><span class="sxs-lookup"><span data-stu-id="ff0f3-288">Put</span></span> | <span data-ttu-id="ff0f3-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="ff0f3-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-290">PutawayClusterId</span></span> | <span data-ttu-id="ff0f3-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="ff0f3-292">Antal</span><span class="sxs-lookup"><span data-stu-id="ff0f3-292">Qty</span></span> | <span data-ttu-id="ff0f3-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="ff0f3-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff0f3-294">QtyAdjust</span></span> | <span data-ttu-id="ff0f3-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff0f3-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ff0f3-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ff0f3-296">QtyShort</span></span> | <span data-ttu-id="ff0f3-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="ff0f3-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="ff0f3-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-298">QtyToConsume</span></span> | <span data-ttu-id="ff0f3-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="ff0f3-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="ff0f3-300">QtyToPick</span></span> | <span data-ttu-id="ff0f3-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="ff0f3-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="ff0f3-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-302">QtyToPut</span></span> | <span data-ttu-id="ff0f3-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="ff0f3-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff0f3-304">QtyToScrap</span></span> | <span data-ttu-id="ff0f3-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff0f3-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="ff0f3-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-306">QtyVerification</span></span> | <span data-ttu-id="ff0f3-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ff0f3-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="ff0f3-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="ff0f3-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="ff0f3-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ff0f3-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="ff0f3-310">ReasonString</span></span> | <span data-ttu-id="ff0f3-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="ff0f3-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="ff0f3-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-312">RecvLocationId</span></span> | <span data-ttu-id="ff0f3-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="ff0f3-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-314">RemoveContainerId</span></span> | <span data-ttu-id="ff0f3-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="ff0f3-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="ff0f3-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="ff0f3-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-318">RMANum</span></span> | <span data-ttu-id="ff0f3-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="ff0f3-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff0f3-320">ShortPickReason</span></span> | <span data-ttu-id="ff0f3-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff0f3-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="ff0f3-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-322">SortConOrLP</span></span> | <span data-ttu-id="ff0f3-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="ff0f3-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-324">SortLicensePlateId</span></span> | <span data-ttu-id="ff0f3-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="ff0f3-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-326">SortPositionId</span></span> | <span data-ttu-id="ff0f3-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="ff0f3-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-328">SortVerification</span></span> | <span data-ttu-id="ff0f3-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="ff0f3-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="ff0f3-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-330">StartLocationId</span></span> | <span data-ttu-id="ff0f3-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="ff0f3-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="ff0f3-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="ff0f3-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-334">TargetLicensePlateId</span></span> | <span data-ttu-id="ff0f3-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="ff0f3-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-336">TOLineNum</span></span> | <span data-ttu-id="ff0f3-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="ff0f3-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-338">ToLocation</span></span> | <span data-ttu-id="ff0f3-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="ff0f3-340">TONum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-340">TONum</span></span> | <span data-ttu-id="ff0f3-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="ff0f3-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-342">ToWarehouse</span></span> | <span data-ttu-id="ff0f3-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="ff0f3-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="ff0f3-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-344">TransportLoadId</span></span> | <span data-ttu-id="ff0f3-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="ff0f3-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-346">WaveLabelId</span></span> | <span data-ttu-id="ff0f3-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="ff0f3-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-348">WaveLblQty</span></span> | <span data-ttu-id="ff0f3-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="ff0f3-350">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-350">Weight</span></span> | <span data-ttu-id="ff0f3-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="ff0f3-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-352">WeightToConsume</span></span> | <span data-ttu-id="ff0f3-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="ff0f3-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-354">WHSAdjustmentType</span></span> | <span data-ttu-id="ff0f3-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="ff0f3-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff0f3-356">WHSReceivingException</span></span> | <span data-ttu-id="ff0f3-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff0f3-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="ff0f3-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ff0f3-358">WHSWorkException</span></span> | <span data-ttu-id="ff0f3-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="ff0f3-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="ff0f3-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="ff0f3-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="ff0f3-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-362">WMSLocationId</span></span> | <span data-ttu-id="ff0f3-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="ff0f3-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-364">WorkId</span></span> | <span data-ttu-id="ff0f3-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="ff0f3-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff0f3-366">WorkIdToCancel</span></span> | <span data-ttu-id="ff0f3-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff0f3-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="ff0f3-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff0f3-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="ff0f3-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff0f3-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="ff0f3-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-370">WorkPoolId</span></span> | <span data-ttu-id="ff0f3-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="ff0f3-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-372">ZoneId</span></span> | <span data-ttu-id="ff0f3-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="ff0f3-374">Tilgængelige trinikoner</span><span class="sxs-lookup"><span data-stu-id="ff0f3-374">Available step icons</span></span>

<span data-ttu-id="ff0f3-375">Systemet indeholder en samling standardtrinikoner, som du også kan bruge til dine brugerdefinerede trin.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="ff0f3-376">Du kan i øjeblikket ikke uploade brugerdefinerede trinikoner.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="ff0f3-377">Derfor skal du altid vælge et af standardtrinikonerne.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="ff0f3-378">I følgende tabel vises alle tilgængelige standardtrinikoner og navnet.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Trinikonet Om"><br><span data-ttu-id="ff0f3-380">Om</span><span class="sxs-lookup"><span data-stu-id="ff0f3-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Trinikonet Tilføj id eller vare"><br><span data-ttu-id="ff0f3-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="ff0f3-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Trinikonet Batchdisposition"><br><span data-ttu-id="ff0f3-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Trinikonet Fragtmand"><br><span data-ttu-id="ff0f3-386">Fragtmand</span><span class="sxs-lookup"><span data-stu-id="ff0f3-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Trinikonet Kode for fastvægt"><br><span data-ttu-id="ff0f3-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="ff0f3-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Trinikonet Kode for fastvægt"><br><span data-ttu-id="ff0f3-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Trinikonet Kontrol af ciffer"><br><span data-ttu-id="ff0f3-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="ff0f3-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Trinikonet Tjek id ind eller ud"><br><span data-ttu-id="ff0f3-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Trinikonet Underordnet id"><br><span data-ttu-id="ff0f3-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Trinikonet Klynge-id"><br><span data-ttu-id="ff0f3-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Trinikonet Klyngeplacering"><br><span data-ttu-id="ff0f3-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Trinikonet Konfigurations-id"><br><span data-ttu-id="ff0f3-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Trinikonet Konfigureret felt"><br><span data-ttu-id="ff0f3-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="ff0f3-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Trinikonet Con eller LP"><br><span data-ttu-id="ff0f3-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Trinikonet Konsolider fra id"><br><span data-ttu-id="ff0f3-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Trinikonet Konsolider til id"><br><span data-ttu-id="ff0f3-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Trinikonet Objektbeholdertype"><br><span data-ttu-id="ff0f3-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Trinikonet Optælling"><br><span data-ttu-id="ff0f3-414">Tælling</span><span class="sxs-lookup"><span data-stu-id="ff0f3-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Trinikonet Optælling af årsagskode"><br><span data-ttu-id="ff0f3-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="ff0f3-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Trinikonet Kode for oprindelsesland"><br><span data-ttu-id="ff0f3-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="ff0f3-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Trinikonet Disposition"><br><span data-ttu-id="ff0f3-420">Disposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Trinikonet Færdig"><br><span data-ttu-id="ff0f3-422">Færdig</span><span class="sxs-lookup"><span data-stu-id="ff0f3-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Trinikonet Bekræftelse af chaufførs check-in"><br><span data-ttu-id="ff0f3-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Trinikonet Id for chaufførs check-in"><br><span data-ttu-id="ff0f3-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Trinikonet Id for chaufførs check-out"><br><span data-ttu-id="ff0f3-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Trinikonet Udløbsdato"><br><span data-ttu-id="ff0f3-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="ff0f3-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Trinikonet Felt"><br><span data-ttu-id="ff0f3-432">Felt</span><span class="sxs-lookup"><span data-stu-id="ff0f3-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Trinikonet Fra batchdisposition"><br><span data-ttu-id="ff0f3-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Trinikonet Fra lagerstatus"><br><span data-ttu-id="ff0f3-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="ff0f3-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Trinikonet Id-attribut"><br><span data-ttu-id="ff0f3-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="ff0f3-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Trinikonet Lagerbatch-id"><br><span data-ttu-id="ff0f3-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Trinikonet Lagerfarve-id"><br><span data-ttu-id="ff0f3-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Trinikonet Lagerplacering"><br><span data-ttu-id="ff0f3-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Trinikonet Lagerserie-id"><br><span data-ttu-id="ff0f3-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Trinikonet Lagerstørrelses-id"><br><span data-ttu-id="ff0f3-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Trinikonet Lagerstatus-id"><br><span data-ttu-id="ff0f3-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Trinikonet Lagertypografi-id"><br><span data-ttu-id="ff0f3-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Trinikonet Lagerversions-id"><br><span data-ttu-id="ff0f3-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Trinikonet Vare-id"><br><span data-ttu-id="ff0f3-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Trinikonet ITM-objektbeholder-id"><br><span data-ttu-id="ff0f3-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Trinikonet ITM-forsendelses-id"><br><span data-ttu-id="ff0f3-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Trinikonet Kanban-kort-id"><br><span data-ttu-id="ff0f3-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Trinikonet Kanban- eller kort-id"><br><span data-ttu-id="ff0f3-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Trinikonet Licens-id"><br><span data-ttu-id="ff0f3-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Trinikonet Last-id"><br><span data-ttu-id="ff0f3-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Trinikonet Placering af lokations-id"><br><span data-ttu-id="ff0f3-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="ff0f3-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Trinikonet Placering eller id"><br><span data-ttu-id="ff0f3-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Trinikonet Kontrol af placering eller id"><br><span data-ttu-id="ff0f3-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="ff0f3-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Trinikonet Placering eller id fra"><br><span data-ttu-id="ff0f3-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="ff0f3-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Trinikonet Placering eller id til"><br><span data-ttu-id="ff0f3-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="ff0f3-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Trinikonet Afsluttet lang proces"><br><span data-ttu-id="ff0f3-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="ff0f3-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Trinikonet LP-pause for overordnet LP"><br><span data-ttu-id="ff0f3-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Trinikonet Flet objektbeholder-id"><br><span data-ttu-id="ff0f3-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Trinikonet Blandet id-linjenummer"><br><span data-ttu-id="ff0f3-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Trinikonet Udgående vægt"><br><span data-ttu-id="ff0f3-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="ff0f3-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Trinikonet Ejer"><br><span data-ttu-id="ff0f3-490">Ejer</span><span class="sxs-lookup"><span data-stu-id="ff0f3-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Trinikonet Overordnet id"><br><span data-ttu-id="ff0f3-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="ff0f3-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Trinikonet Bekræft"><br><span data-ttu-id="ff0f3-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="ff0f3-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Trinikonet Nummer på indkøbsordrelinje"><br><span data-ttu-id="ff0f3-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Trinikonet Nummer på indkøbsordre"><br><span data-ttu-id="ff0f3-498">Indkøbsordrenummer</span><span class="sxs-lookup"><span data-stu-id="ff0f3-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Trinikonet Position fuld"><br><span data-ttu-id="ff0f3-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="ff0f3-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Trinikonet Styrke"><br><span data-ttu-id="ff0f3-502">Styrke</span><span class="sxs-lookup"><span data-stu-id="ff0f3-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Trinikonet Printernavn"><br><span data-ttu-id="ff0f3-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="ff0f3-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Trinikonet Produkt-id"><br><span data-ttu-id="ff0f3-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Trinikonet Produktbekræftelse"><br><span data-ttu-id="ff0f3-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Trinikonet Læg på lager"><br><span data-ttu-id="ff0f3-510">Læg på lager</span><span class="sxs-lookup"><span data-stu-id="ff0f3-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Trinikonet Læg på lager-klynge-id"><br><span data-ttu-id="ff0f3-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Trinikonet Antal"><br><span data-ttu-id="ff0f3-514">Antal</span><span class="sxs-lookup"><span data-stu-id="ff0f3-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Trinikonet Justering af antal ind"><br><span data-ttu-id="ff0f3-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="ff0f3-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Trinikonet Manglende antal"><br><span data-ttu-id="ff0f3-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="ff0f3-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Trinikonet Antal, der skal forbruges"><br><span data-ttu-id="ff0f3-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Trinikonet Antal, der skal lægges på lager"><br><span data-ttu-id="ff0f3-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="ff0f3-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Trinikonet Antal, der skal kasseres"><br><span data-ttu-id="ff0f3-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="ff0f3-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Trinikonet Bekræftelse af antal"><br><span data-ttu-id="ff0f3-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Trinikonet Færdigmelding af job"><br><span data-ttu-id="ff0f3-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="ff0f3-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Trinikonet Modtag placerings-id"><br><span data-ttu-id="ff0f3-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Trinikonet Fjern objektbeholder-id"><br><span data-ttu-id="ff0f3-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Trinikonet RMA-nummer"><br><span data-ttu-id="ff0f3-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Trinikonet Vælg ordre"><br><span data-ttu-id="ff0f3-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="ff0f3-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Trinikonet Kort plukårsag"><br><span data-ttu-id="ff0f3-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="ff0f3-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Trinikonet Sortér placerings-id"><br><span data-ttu-id="ff0f3-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Trinikonet Mållicens-id"><br><span data-ttu-id="ff0f3-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Trinikonet Til linjenummer"><br><span data-ttu-id="ff0f3-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Trinikonet Til placering"><br><span data-ttu-id="ff0f3-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="ff0f3-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Trinikonet Til nummer"><br><span data-ttu-id="ff0f3-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="ff0f3-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Trinikonet Til lager"><br><span data-ttu-id="ff0f3-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Trinikonet Transportlast-id"><br><span data-ttu-id="ff0f3-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Trinikonet Leverandørbatch-id"><br><span data-ttu-id="ff0f3-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Trinikonet Bølgeetiket-id"><br><span data-ttu-id="ff0f3-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Trinikonet Bølgeetiketantal"><br><span data-ttu-id="ff0f3-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="ff0f3-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Trinikonet Vægt"><br><span data-ttu-id="ff0f3-560">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="ff0f3-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Trinikonet Vægt, der skal forbruges"><br><span data-ttu-id="ff0f3-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="ff0f3-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Trinikonet WHS-reguleringstype"><br><span data-ttu-id="ff0f3-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="ff0f3-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Trinikonet WHS-modtagelsesundtagelse"><br><span data-ttu-id="ff0f3-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="ff0f3-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Trinikonet WMS-placerings-id"><br><span data-ttu-id="ff0f3-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Trinikonet Arbejds-id"><br><span data-ttu-id="ff0f3-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Trinikonet Arbejds-id, der skal annulleres"><br><span data-ttu-id="ff0f3-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="ff0f3-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Trinikonet Arbejdslicens-id"><br><span data-ttu-id="ff0f3-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="ff0f3-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Trinikonet Arbejdslicens-id for lægge på lager-klynge"><br><span data-ttu-id="ff0f3-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="ff0f3-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Trinikonet Arbejdspulje-id"><br><span data-ttu-id="ff0f3-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Trinikonet Zone-id"><br><span data-ttu-id="ff0f3-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="ff0f3-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="ff0f3-581">Eksempel: Tildele trinikoner og titler til et brugerdefineret flow</span><span class="sxs-lookup"><span data-stu-id="ff0f3-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="ff0f3-582">I dette eksempel forklares det, hvordan du konfigurerer trinikoner og titler for et brugerdefineret opgaveflow.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="ff0f3-583">Scenariet bygger på et eksempel på et brugerdefineret opgaveflow, der præsenteres og udforskes mere detaljeret i følgende blogindlæg: [Tilpasning af mobilappen Lagersted](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="ff0f3-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="ff0f3-584">Opgaveflowet fungerer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="ff0f3-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="ff0f3-585">Appen viser en side, hvor arbejderen bliver bedt om at angive et container-id (for eksempel ved at scanne en stregkode).</span><span class="sxs-lookup"><span data-stu-id="ff0f3-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="ff0f3-586">Hvis container-id'et er gyldigt, åbner appen en ny side, hvor arbejderen bliver bedt om at angive vægten.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="ff0f3-587">Hvis objektbeholder-id'et ikke er gyldigt, returneres arbejderen til den første side.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="ff0f3-588">Når arbejderen angiver en gyldig vægt, gemmer systemet vægten og returnerer arbejderen til den første side.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="ff0f3-589">Følgende illustration viser dette opgaveflow.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="ff0f3-590">![Diagram over opgaveflow](media/step-icons-example-task-flow.png "Diagram over opgaveflow")</span><span class="sxs-lookup"><span data-stu-id="ff0f3-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="ff0f3-591">Oprette en trinklasse til inputsiden for objektbeholderen</span><span class="sxs-lookup"><span data-stu-id="ff0f3-591">Create a step class for the container input page</span></span>

<span data-ttu-id="ff0f3-592">På inputsiden for objektbeholderen kan arbejderen scanne eller angive et objektbeholder-id.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="ff0f3-593">![Inputsiden for objektbeholder](media/step-icons-example-container-input.png "Inputsiden for objektbeholder")</span><span class="sxs-lookup"><span data-stu-id="ff0f3-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="ff0f3-594">På inputsiden for objektbeholderen er kontrolelementnavnet på inputfeltetet `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="ff0f3-595">Da dette kontrolelementnavn ikke findes på [listen over trin-id'er](#step-ids-classes), finder du ikke et eksisterende trin, der er baseret på det.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="ff0f3-596">Derfor skal du oprette en trinklasse, der repræsenterer trinnet.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="ff0f3-597">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="ff0f3-598">Id'et for trinikonet gemmes i `defaultStepIcon`-klassemedlemmet, og trintitlen gemmes i `defaultStepTitle`-klassemedlemmet.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="ff0f3-599">Hvis du vil tildele et trinikon, skal du angive `defaultStepIcon` til et af de ikon-id'er, der er angivet i afsnittet [Tilgængelige trinikoner](#step-icons) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="ff0f3-600">Brug et standardikon eller et brugerdefineret trinikon og en titel til vægtinputtet</span><span class="sxs-lookup"><span data-stu-id="ff0f3-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="ff0f3-601">På siden med vægtinput kan arbejderen angive en vægt.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="ff0f3-602">![Siden Vægtinput](media/step-icons-example-weight-input.png "Siden Vægtinput")</span><span class="sxs-lookup"><span data-stu-id="ff0f3-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="ff0f3-603">På siden til vægtinput er kontrolelementnavnet på inputfeltet `Weight`, som findes på [listen over trin-id'er](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="ff0f3-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="ff0f3-604">Hvis det trinikon og den titel, der er defineret i `WHSMobileAppStepWeight`-klassen, derfor kan accepteres af dig, behøver du ikke at ændre noget for dette trin.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="ff0f3-605">Men hvis du foretrækker at bruge et andet ikon eller en anden titel til dette trin, kan du tilsidesætte enten `stepId()`-metoden eller `stepInfo()`-metoden i generatorklassen.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="ff0f3-606">Hvert opgaveflow har sin egen generator af trinoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="ff0f3-607">Tilsidesætte metoden stepId()</span><span class="sxs-lookup"><span data-stu-id="ff0f3-607">Override the stepId() method</span></span>

<span data-ttu-id="ff0f3-608">I følgende eksempel vises en måde, hvorpå du kan ændre en generatorklasse ved at tilsidesætte `stepId()`-metoden.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="ff0f3-609">Derefter opretter du en trinklasse til `NewWeight`-trinnet.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="ff0f3-610">Koden skal ligne koden for det `ContainerId`-eksempel, der blev vist tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="ff0f3-611">Tilsidesætte metoden stepInfo()</span><span class="sxs-lookup"><span data-stu-id="ff0f3-611">Override the stepInfo() method</span></span>

<span data-ttu-id="ff0f3-612">I følgende eksempel vises en måde, hvorpå du kan ændre en generatorklasse ved at tilsidesætte `stepInfo()`-metoden.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="ff0f3-613">Derefter konstruerer du et `WHSMobileAppStepInfo`-objekt og angiver ikonet og/eller titlen direkte.</span><span class="sxs-lookup"><span data-stu-id="ff0f3-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff0f3-614">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ff0f3-614">Additional resources</span></span>

- [<span data-ttu-id="ff0f3-615">Installere og tilslutte mobilapp til lagerstedsadministration</span><span class="sxs-lookup"><span data-stu-id="ff0f3-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="ff0f3-616">Indstillinger for mobilenhedsbruger</span><span class="sxs-lookup"><span data-stu-id="ff0f3-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
