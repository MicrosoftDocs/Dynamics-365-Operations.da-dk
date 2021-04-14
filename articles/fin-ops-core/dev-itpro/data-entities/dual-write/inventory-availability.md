---
title: Lagertilgængelighed i dobbeltskrivning
description: I dette emne får du oplysninger om, hvordan du kontrollerer lagertilgængelighed i dobbeltskrivning.
author: yijialuan
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748559"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="876f9-103">Lagertilgængelighed i dobbeltskrivning</span><span class="sxs-lookup"><span data-stu-id="876f9-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="876f9-104">Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til siden **Tilbud**, **Ordrer** eller **Fakturaer** i Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="876f9-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="876f9-105">Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en nøgleopgave i processen for [kundeemne til kontant](dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="876f9-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="876f9-106">Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange.</span><span class="sxs-lookup"><span data-stu-id="876f9-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="876f9-107">Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="876f9-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="876f9-108">Disponibel lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="876f9-108">On-hand inventory</span></span>

<span data-ttu-id="876f9-109">I sidehovedet for formularerne **Tilbud**, **Ordrer** og **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="876f9-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="876f9-110">Når du vælger knappen, vises en dialogboks, hvor du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for.</span><span class="sxs-lookup"><span data-stu-id="876f9-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="876f9-111">I denne dialogboks vises de samme oplysninger som [disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span><span class="sxs-lookup"><span data-stu-id="876f9-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="876f9-112">Dialogboksen returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="876f9-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="876f9-113">Disse oplysninger indeholder følgende antal:</span><span class="sxs-lookup"><span data-stu-id="876f9-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="876f9-114">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="876f9-114">On-hand quantity</span></span>
- <span data-ttu-id="876f9-115">Reserveret disponibelt antal</span><span class="sxs-lookup"><span data-stu-id="876f9-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="876f9-116">Tilgængeligt disponibelt antal</span><span class="sxs-lookup"><span data-stu-id="876f9-116">Available on-hand quantity</span></span>
- <span data-ttu-id="876f9-117">Bestilt antal</span><span class="sxs-lookup"><span data-stu-id="876f9-117">Ordered quantity</span></span>
- <span data-ttu-id="876f9-118">Antal i bestilling</span><span class="sxs-lookup"><span data-stu-id="876f9-118">On-order quantity</span></span>
- <span data-ttu-id="876f9-119">Reserveret bestilt mængde</span><span class="sxs-lookup"><span data-stu-id="876f9-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="876f9-120">Disponibelt antal i alt</span><span class="sxs-lookup"><span data-stu-id="876f9-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="876f9-121">DTT-oplysninger</span><span class="sxs-lookup"><span data-stu-id="876f9-121">ATP information</span></span>

<span data-ttu-id="876f9-122">I Sales er der føjet en ny knap for **DTT-oplysninger** til linjeelementer på siderne **Tilbud**, **Ordrer** og **Fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="876f9-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="876f9-123">Når du vælger knappen, vises en dialogboks, hvor du kan angive firma, produkt, lagerlokation, lagersted og ordreantal.</span><span class="sxs-lookup"><span data-stu-id="876f9-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="876f9-124">Denne dialogboks har de samme indstillinger, som er beskrevet under [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span><span class="sxs-lookup"><span data-stu-id="876f9-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="876f9-125">Dialogboksen returnerer DTT-oplysningerne fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="876f9-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="876f9-126">Disse oplysninger indeholder følgende antal:</span><span class="sxs-lookup"><span data-stu-id="876f9-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="876f9-127">DTT-antal</span><span class="sxs-lookup"><span data-stu-id="876f9-127">ATP quantity</span></span>
- <span data-ttu-id="876f9-128">Tilgangsantal</span><span class="sxs-lookup"><span data-stu-id="876f9-128">Receipt quantity</span></span>
- <span data-ttu-id="876f9-129">Afgangsantal</span><span class="sxs-lookup"><span data-stu-id="876f9-129">Issue quantity</span></span>
- <span data-ttu-id="876f9-130">Beholdningsantal</span><span class="sxs-lookup"><span data-stu-id="876f9-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="876f9-131">Sådan fungerer det</span><span class="sxs-lookup"><span data-stu-id="876f9-131">How it works</span></span>

<span data-ttu-id="876f9-132">Når du vælger knappen **Disponibel lagerbeholdning** på siden **Tilbud**, **Ordrer** eller **Fakturaer**, foretages der et direkte opkald om dobbeltskrivning til API'en **Disponibel lagerbeholdning**.</span><span class="sxs-lookup"><span data-stu-id="876f9-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="876f9-133">API'en beregner den disponible beholdning for det givne produkt.</span><span class="sxs-lookup"><span data-stu-id="876f9-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="876f9-134">Resultatet gemmes i tabellerne **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og skrives derefter til Dataverse via dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="876f9-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="876f9-135">Hvis du vil bruge denne funktion, skal du køre følgende dobbeltskrivningstilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="876f9-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="876f9-136">Spring den første synkronisering over, når du kører tilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="876f9-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="876f9-137">CDS Poster for disponibel lagerbeholdning (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="876f9-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="876f9-138">CDS Anmodninger om disponibel lagerbeholdning (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="876f9-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="876f9-139">Skabeloner</span><span class="sxs-lookup"><span data-stu-id="876f9-139">Templates</span></span>
<span data-ttu-id="876f9-140">Der findes følgende skabeloner til visning af de disponible lagerbeholdningsdata.</span><span class="sxs-lookup"><span data-stu-id="876f9-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="876f9-141">Finance and Operations-apps</span><span class="sxs-lookup"><span data-stu-id="876f9-141">Finance and Operations apps</span></span> | <span data-ttu-id="876f9-142">Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="876f9-142">Customer engagement app</span></span> | <span data-ttu-id="876f9-143">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="876f9-143">Description</span></span> 
---|---|---
[<span data-ttu-id="876f9-144">Posteringer til disponibelt CDS-lager</span><span class="sxs-lookup"><span data-stu-id="876f9-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="876f9-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="876f9-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="876f9-146">Anmodninger om disponibelt CDS-lager</span><span class="sxs-lookup"><span data-stu-id="876f9-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="876f9-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="876f9-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="876f9-148">CDS Poster for disponibel lagerbeholdning (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="876f9-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="876f9-149">Denne skabelon synkroniserer data mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="876f9-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="876f9-150">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="876f9-150">Finance and Operations field</span></span> | <span data-ttu-id="876f9-151">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="876f9-151">Map type</span></span> | <span data-ttu-id="876f9-152">Customer Engagement-felt</span><span class="sxs-lookup"><span data-stu-id="876f9-152">Customer engagement field</span></span> | <span data-ttu-id="876f9-153">Standardværdi</span><span class="sxs-lookup"><span data-stu-id="876f9-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="876f9-154">CDS Anmodninger om disponibel lagerbeholdning (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="876f9-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="876f9-155">Denne skabelon synkroniserer data mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="876f9-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="876f9-156">Finance and Operations-felt</span><span class="sxs-lookup"><span data-stu-id="876f9-156">Finance and Operations field</span></span> | <span data-ttu-id="876f9-157">Tilknytningstype</span><span class="sxs-lookup"><span data-stu-id="876f9-157">Map type</span></span> | <span data-ttu-id="876f9-158">Customer Engagement-felt</span><span class="sxs-lookup"><span data-stu-id="876f9-158">Customer engagement field</span></span> | <span data-ttu-id="876f9-159">Standardværdi</span><span class="sxs-lookup"><span data-stu-id="876f9-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]