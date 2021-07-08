---
title: Importere indgående ASN'er via V2-dataenheden
description: I dette emne forklares, hvordan du kan administrere importen af indgående ASN-meddelelser (Advanced Shipping Notices) via den indgående ASN V2-dataenhed.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249075"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="b651e-103">Importere indgående ASN'er via V2-dataenheden</span><span class="sxs-lookup"><span data-stu-id="b651e-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b651e-104">ASN'er (Advanced Shipping Notices) giver dig besked om leverandørleverancer.</span><span class="sxs-lookup"><span data-stu-id="b651e-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="b651e-105">De hjælper afsenderen med at beskrive indholdet af en forsendelse og flere oplysninger om den, for eksempel varer og emballage.</span><span class="sxs-lookup"><span data-stu-id="b651e-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="b651e-106">ASN'er kan hjælpe lagerarbejdere med at finde ud af, hvad der ankommer hvornår.</span><span class="sxs-lookup"><span data-stu-id="b651e-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="b651e-107">De kan derfor forberede sig.</span><span class="sxs-lookup"><span data-stu-id="b651e-107">Therefore, they can prepare.</span></span> <span data-ttu-id="b651e-108">Derudover kan lagerarbejdere bruge ASN'er til at sammenligne detaljerne for en forsendelse med den relaterede indkøbsordre, der er oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="b651e-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="b651e-109">Dette emne indeholder en samling scenarier, der viser eksempler på, hvordan du kan arbejde med ASN-filer.</span><span class="sxs-lookup"><span data-stu-id="b651e-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b651e-110">*Indgående ASN*-import gælder kun for varer, der er aktiveret til avanceret lagerstedsstyring (WMS).</span><span class="sxs-lookup"><span data-stu-id="b651e-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="b651e-111">Før du modtager en ASN, skal der være registreret en indkøbsordre i systemet for den leverandør, der sender ASN'en.</span><span class="sxs-lookup"><span data-stu-id="b651e-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="b651e-112">Indgående ASN V2-enhed</span><span class="sxs-lookup"><span data-stu-id="b651e-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="b651e-113">Du importerer indgående ASN'er ved hjælp af den sammensatte *indgående ASN V2*-dataenhed.</span><span class="sxs-lookup"><span data-stu-id="b651e-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="b651e-114">*Indgående ASN V2* benytter følgende enheder:</span><span class="sxs-lookup"><span data-stu-id="b651e-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="b651e-115">Overskrift for indgående belastning</span><span class="sxs-lookup"><span data-stu-id="b651e-115">Inbound load header</span></span>
- <span data-ttu-id="b651e-116">Overskrift til indgående forsendelse</span><span class="sxs-lookup"><span data-stu-id="b651e-116">Inbound shipment header</span></span>
- <span data-ttu-id="b651e-117">Pakkestrukturer for indgående belastning</span><span class="sxs-lookup"><span data-stu-id="b651e-117">Inbound load packing structures</span></span>
- <span data-ttu-id="b651e-118">Pakkestruktursager for indgående belastninger</span><span class="sxs-lookup"><span data-stu-id="b651e-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="b651e-119">Pakkestruktursagslinjer for indgående belastninger</span><span class="sxs-lookup"><span data-stu-id="b651e-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="b651e-120">Pakkestrukturlinjer for indgående belastninger</span><span class="sxs-lookup"><span data-stu-id="b651e-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="b651e-121">Den sammensatte *indgående ASN V2*-dataenhed er beregnet til asynkrone integrationsscenarier, hvor der bruges XML-filbaserede importer.</span><span class="sxs-lookup"><span data-stu-id="b651e-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="b651e-122">XML-format til import af ASN'er</span><span class="sxs-lookup"><span data-stu-id="b651e-122">XML format for importing ASNs</span></span>

<span data-ttu-id="b651e-123">Microsoft Dynamics 365 Supply Chain Management understøtter følgende XML-format til import af ASN'er.</span><span class="sxs-lookup"><span data-stu-id="b651e-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="b651e-124">Hver node i XML-filen repræsenterer en attribut fra en individuel enhed.</span><span class="sxs-lookup"><span data-stu-id="b651e-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="b651e-125">Eksempler</span><span class="sxs-lookup"><span data-stu-id="b651e-125">Examples</span></span>

<span data-ttu-id="b651e-126">Følgende undersektioner indeholder eksempler på ASN XML-importfiler til leverandørforsendelser.</span><span class="sxs-lookup"><span data-stu-id="b651e-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="b651e-127">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b651e-127">Example 1</span></span>

<span data-ttu-id="b651e-128">I følgende eksempel vises en XML-fil til import af leverandørforsendelser for en indkøbsordre, hvor der ikke er medtaget sagsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b651e-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="b651e-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b651e-129">Example 2</span></span>

<span data-ttu-id="b651e-130">I følgende eksempel vises en XML-fil til import af leverandørforsendelser for en indkøbsordre, hvor der er medtaget sagsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b651e-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="b651e-131">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b651e-131">Example 3</span></span>

<span data-ttu-id="b651e-132">I følgende eksempel vises en XML-fil til import af leverandørforsendelser for flere indkøbsordrer, hvor der er medtaget sagsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b651e-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="b651e-133">Undersøge resultaterne af import af en ASN-fil</span><span class="sxs-lookup"><span data-stu-id="b651e-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="b651e-134">Udfør disse trin for at undersøge resultaterne af import af en ASN-fil.</span><span class="sxs-lookup"><span data-stu-id="b651e-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="b651e-135">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="b651e-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b651e-136">Find og åbn en last, der er oprettet som del af en ASN-import.</span><span class="sxs-lookup"><span data-stu-id="b651e-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="b651e-137">I oversigtspanelet **Last** kan du se værdier, der er baseret på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b651e-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="b651e-138">I oversigtspanelet **Lastlinjer** kan du se indkøbsordrenumre og varedetaljer, der er baseret på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b651e-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="b651e-139">Vælg **Pakkestruktur** i gruppen **Modtag** under fanen **Levér og modtag** i handlingsruden for at gennemse pakkestrukturen for lasten.</span><span class="sxs-lookup"><span data-stu-id="b651e-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="b651e-140">I oversigtspanelet **Paller** kan du se id'er, der er baseret på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b651e-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="b651e-141">I oversigtspanelet **Sager** kan du se sager, der er baseret på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b651e-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="b651e-142">I oversigtspanelet **Varer** kan du se varer og mængder, der er baseret på XML-filen.</span><span class="sxs-lookup"><span data-stu-id="b651e-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
