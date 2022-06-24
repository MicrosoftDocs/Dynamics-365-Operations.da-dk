---
title: Importere indgående ASN'er via V3-dataenheden
description: Denne artikel forklarer, hvordan du kan administrere importen af indgående ASN-meddelelser (Advanced Shipping Notices) via den indgående ASN-dataenhed.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ac45e070d0473547c48da1380377de3d4bf60bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907110"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Importere indgående ASN'er via V3-dataenheden

[!include [banner](../../includes/banner.md)]

ASN'er (Advanced Shipping Notices) giver dig besked om leverandørleverancer. De hjælper afsenderen med at beskrive indholdet af en forsendelse og flere oplysninger om den, for eksempel varer og emballage.

ASN'er kan hjælpe lagerarbejdere med at finde ud af, hvad der ankommer hvornår. De kan derfor forberede sig. Derudover kan lagerarbejdere bruge ASN'er til at sammenligne detaljerne for en forsendelse med den relaterede indkøbsordre, der er oprettet tidligere.

Denne artikel indeholder en samling scenarier, der viser eksempler på, hvordan du kan arbejde med ASN-filer.

> [!IMPORTANT]
> *Indgående ASN*-import gælder kun for varer, der er aktiveret til avanceret lagerstedsstyring (WMS). Før du modtager en ASN, skal der være registreret en indkøbsordre i systemet for den leverandør, der sender ASN'en.

## <a name="inbound-asn-v3-entity"></a>Indgående ASN V3-enhed

Du importerer indgående ASN'er ved hjælp af den sammensatte *Indgående ASN V3*-dataenhed. *Indgående ASN V3* benytter følgende enheder:

- Overskrift for indgående belastning
- Overskrift til indgående forsendelse
- Pakkestrukturer for indgående belastning
- Pakkestruktursager for indgående belastninger
- Pakkestruktursagslinjer for indgående belastninger
- Pakkestrukturlinjer for indgående belastninger

Den sammensatte *indgående ASN V3*-dataenhed er beregnet til asynkrone integrationsscenarier, hvor der bruges XML-filbaserede importer.

## <a name="xml-format-for-importing-asns"></a>XML-format til import af ASN'er

Microsoft Dynamics 365 Supply Chain Management understøtter følgende XML-format til import af ASN'er. Hver node i XML-filen repræsenterer en attribut fra en individuel enhed.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Eksempler

Følgende undersektioner indeholder eksempler på ASN XML-importfiler til leverandørforsendelser.

### <a name="example-1"></a>Eksempel 1

I følgende eksempel vises en XML-fil til import af leverandørforsendelser for en indkøbsordre, hvor der ikke er medtaget sagsoplysninger.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Eksempel 2

I følgende eksempel vises en XML-fil til import af leverandørforsendelser for en indkøbsordre, hvor der er medtaget sagsoplysninger.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Eksempel 3

I følgende eksempel vises en XML-fil til import af leverandørforsendelser for flere indkøbsordrer, hvor der er medtaget sagsoplysninger.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>Undersøge resultaterne af import af en ASN-fil

Udfør disse trin for at undersøge resultaterne af import af en ASN-fil.

1. Gå til **Lokationsstyring \> Laster \> Alle laster**.
1. Find og åbn en last, der er oprettet som del af en ASN-import.
1. I oversigtspanelet **Last** kan du se værdier, der er baseret på XML-filen.
1. I oversigtspanelet **Lastlinjer** kan du se indkøbsordrenumre og varedetaljer, der er baseret på XML-filen.
1. Vælg **Pakkestruktur** i gruppen **Modtag** under fanen **Levér og modtag** i handlingsruden for at gennemse pakkestrukturen for lasten.
1. I oversigtspanelet **Paller** kan du se id'er, der er baseret på XML-filen.
1. I oversigtspanelet **Sager** kan du se sager, der er baseret på XML-filen.
1. I oversigtspanelet **Varer** kan du se varer og mængder, der er baseret på XML-filen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
