---
title: Tildele trinikoner og titler til mobilappen Warehouse Management
description: I dette emne beskrives, hvordan du tildeler trinikoner og titler til nye eller tilpassede opgaveflow for mobilappen Warehouse Management.
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a687c26cacc0dbdaf0091b2d26277864553ca1bf
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103307"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Tildele trinikoner og titler til mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du tildeler trinikoner og trintitler til nye eller tilpassede opgaveflow for mobilappen Warehouse Management.

Følgende illustrationer viser, hvordan trinikoner og titler vises i mobilappen Warehouse Management.

![Eksempel på et trinikon og en trintitel i mobilappen Warehouse Management.](media/step-icon-example.png "Eksempel på et trinikon og en trintitel i mobilappen Warehouse Management")

## <a name="turn-this-feature-on-or-off"></a>Aktivere eller deaktivere denne funktion

Hvis du vil bruge den funktionalitet, der er beskrevet i dette emne, skal funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* være aktiveret i systemet. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Brugerindstillinger, ikoner og trintitler til den nye lagerstedsapp* i arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="standard-step-ids-classes-and-icons"></a>Standardtrin-id'er, klasser og ikoner

Hvert trin i et opgaveflow identificeres af et trin-id, og hvert trin-id har en tilsvarende trinklasse. Trinikonet og titlen angives i hver trinklasse.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Trin-id'er og trinklasser

I følgende tabel vises alle de trin-id'er, der i øjeblikket er tilgængelige, og den tilsvarende trinklasse. Kontrolnavnet på det primære inputfelt bruges som trin-id.

Du kan se et eksempel, der viser, hvordan disse trin-id'er og klasser bruges, i implementeringen af `WHSMobileAppStepInfoBuilder.stepId()`-metoden i afsnittet [Eksempel: Tildele trinikoner og titler til et brugerdefineret flow](#example) senere i dette emne.

| Trin-id | Trinklasse |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Fragtmand | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Bekræftelse | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Indkøbsordrenummer | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Styrke | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Læg på lager | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Antal | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Tykkelse | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Tilgængelige trinikoner

Systemet indeholder en samling standardtrinikoner, som du også kan bruge til dine brugerdefinerede trin. Du kan i øjeblikket ikke uploade brugerdefinerede trinikoner. Derfor skal du altid vælge et af standardtrinikonerne.

I følgende tabel vises alle tilgængelige standardtrinikoner og navnet.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Trinikonet Om"><br>Om</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Trinikonet Tilføj id eller vare"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Trinikonet Batchdisposition"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Trinikonet Fragtmand"><br>Fragtmand</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Trinikonet Kode for fastvægt"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Trinikonet Kode for fastvægt"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Trinikonet Kontrol af ciffer"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Trinikonet Tjek id ind eller ud"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Trinikonet Underordnet id"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Trinikonet Klynge-id"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Trinikonet Klyngeplacering"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Trinikonet Konfigurations-id"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Trinikonet Konfigureret felt"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Trinikonet Con eller LP"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Trinikonet Konsolider fra id"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Trinikonet Konsolider til id"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Trinikonet Objektbeholdertype"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Trinikonet Optælling"><br>Tælling</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Trinikonet Optælling af årsagskode"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Trinikonet Kode for oprindelsesland"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Trinikonet Disposition"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Trinikonet Færdig"><br>Færdig</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Trinikonet Bekræftelse af chaufførs check-in"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Trinikonet Id for chaufførs check-in"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Trinikonet Id for chaufførs check-out"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Trinikonet Udløbsdato"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Trinikonet Felt"><br>Felt</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Trinikonet Fra batchdisposition"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Trinikonet Fra lagerstatus"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Trinikonet Id-attribut"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Trinikonet Lagerbatch-id"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Trinikonet Lagerfarve-id"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Trinikonet Lagerplacering"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Trinikonet Lagerserie-id"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Trinikonet Lagerstørrelses-id"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Trinikonet Lagerstatus-id"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Trinikonet Lagertypografi-id"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Trinikonet Lagerversions-id"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Trinikonet Vare-id"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Trinikonet ITM-objektbeholder-id"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Trinikonet ITM-forsendelses-id"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Trinikonet Kanban-kort-id"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Trinikonet Kanban- eller kort-id"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Trinikonet Licens-id"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Trinikonet Last-id"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Trinikonet Placering af lokations-id"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Trinikonet Placering eller id"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Trinikonet Kontrol af placering eller id"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Trinikonet Placering eller id fra"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Trinikonet Placering eller id til"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Trinikonet Afsluttet lang proces"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Trinikonet LP-pause for overordnet LP"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Trinikonet Flet objektbeholder-id"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Trinikonet Blandet id-linjenummer"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Trinikonet Udgående vægt"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Trinikonet Ejer"><br>Ejer</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Trinikonet Overordnet id"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Trinikonet Bekræft"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Trinikonet Nummer på indkøbsordrelinje"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Trinikonet Nummer på indkøbsordre"><br>Indkøbsordrenummer</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Trinikonet Position fuld"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Trinikonet Styrke"><br>Styrke</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Trinikonet Printernavn"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Trinikonet Produkt-id"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Trinikonet Produktbekræftelse"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Trinikonet Læg på lager"><br>Læg på lager</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Trinikonet Læg på lager-klynge-id"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Trinikonet Antal"><br>Antal</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Trinikonet Justering af antal ind"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Trinikonet Manglende antal"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Trinikonet Antal, der skal forbruges"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Trinikonet Antal, der skal lægges på lager"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Trinikonet Antal, der skal kasseres"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Trinikonet Bekræftelse af antal"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Trinikonet Færdigmelding af job"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Trinikonet Modtag placerings-id"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Trinikonet Fjern objektbeholder-id"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Trinikonet RMA-nummer"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Trinikonet Vælg ordre"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Trinikonet Kort plukårsag"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Trinikonet Sortér placerings-id"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Trinikonet Mållicens-id"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Trinikonet Til linjenummer"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Trinikonet Til placering"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Trinikonet Til nummer"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Trinikonet Til lager"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Trinikonet Transportlast-id"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Trinikonet Leverandørbatch-id"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Trinikonet Bølgeetiket-id"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Trinikonet Bølgeetiketantal"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Trinikonet Vægt"><br>Tykkelse</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Trinikonet Vægt, der skal forbruges"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Trinikonet WHS-reguleringstype"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Trinikonet WHS-modtagelsesundtagelse"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Trinikonet WMS-placerings-id"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Trinikonet Arbejds-id"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Trinikonet Arbejds-id, der skal annulleres"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Trinikonet Arbejdslicens-id"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Trinikonet Arbejdslicens-id for lægge på lager-klynge"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Trinikonet Arbejdspulje-id"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Trinikonet Zone-id"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Eksempel: Tildele trinikoner og titler til et brugerdefineret flow

I dette eksempel forklares det, hvordan du konfigurerer trinikoner og titler for et brugerdefineret opgaveflow. Scenariet bygger på et eksempel på et brugerdefineret opgaveflow, der præsenteres og udforskes mere detaljeret i følgende blogindlæg: [Tilpasning af mobilappen Lagersted](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Opgaveflowet fungerer på følgende måde:

1. Appen viser en side, hvor arbejderen bliver bedt om at angive et container-id (for eksempel ved at scanne en stregkode).
1. Hvis container-id'et er gyldigt, åbner appen en ny side, hvor arbejderen bliver bedt om at angive vægten. Hvis objektbeholder-id'et ikke er gyldigt, returneres arbejderen til den første side.
1. Når arbejderen angiver en gyldig vægt, gemmer systemet vægten og returnerer arbejderen til den første side.

Følgende illustration viser dette opgaveflow.

![Diagram over opgaveflow.](media/step-icons-example-task-flow.png "Diagram over opgaveflow")

### <a name="create-a-step-class-for-the-container-input-page"></a>Oprette en trinklasse til inputsiden for objektbeholderen

På inputsiden for objektbeholderen kan arbejderen scanne eller angive et objektbeholder-id.

![Inputsiden for objektbeholder.](media/step-icons-example-container-input.png "Inputsiden for objektbeholder")

På inputsiden for objektbeholderen er kontrolelementnavnet på inputfeltetet `ContainerId`. Da dette kontrolelementnavn ikke findes på [listen over trin-id'er](#step-ids-classes), finder du ikke et eksisterende trin, der er baseret på det. Derfor skal du oprette en trinklasse, der repræsenterer trinnet. Her er et eksempel.

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

Id'et for trinikonet gemmes i `defaultStepIcon`-klassemedlemmet, og trintitlen gemmes i `defaultStepTitle`-klassemedlemmet.

Hvis du vil tildele et trinikon, skal du angive `defaultStepIcon` til et af de ikon-id'er, der er angivet i afsnittet [Tilgængelige trinikoner](#step-icons) tidligere i dette emne.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Brug et standardikon eller et brugerdefineret trinikon og en titel til vægtinputtet

På siden med vægtinput kan arbejderen angive en vægt.

![Siden Vægtinput.](media/step-icons-example-weight-input.png "Siden Vægtinput")

På siden til vægtinput er kontrolelementnavnet på inputfeltet `Weight`, som findes på [listen over trin-id'er](#step-ids-classes). Hvis det trinikon og den titel, der er defineret i `WHSMobileAppStepWeight`-klassen, derfor kan accepteres af dig, behøver du ikke at ændre noget for dette trin.

Men hvis du foretrækker at bruge et andet ikon eller en anden titel til dette trin, kan du tilsidesætte enten `stepId()`-metoden eller `stepInfo()`-metoden i generatorklassen. Hvert opgaveflow har sin egen generator af trinoplysninger.

#### <a name="override-the-stepid-method"></a>Tilsidesætte metoden stepId()

I følgende eksempel vises en måde, hvorpå du kan ændre en generatorklasse ved at tilsidesætte `stepId()`-metoden.

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

Derefter opretter du en trinklasse til `NewWeight`-trinnet. Koden skal ligne koden for det `ContainerId`-eksempel, der blev vist tidligere i dette emne.

#### <a name="override-the-stepinfo-method"></a>Tilsidesætte metoden stepInfo()

I følgende eksempel vises en måde, hvorpå du kan ændre en generatorklasse ved at tilsidesætte `stepInfo()`-metoden.

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

Derefter konstruerer du et `WHSMobileAppStepInfo`-objekt og angiver ikonet og/eller titlen direkte.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Installere og tilslutte mobilapp til lagerstedsadministration](install-configure-warehouse-management-app.md)
- [Indstillinger for mobilenhedsbruger](mobile-device-user-settings.md)
