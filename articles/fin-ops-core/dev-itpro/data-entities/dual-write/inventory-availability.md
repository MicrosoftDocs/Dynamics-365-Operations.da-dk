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
# <a name="inventory-availability-in-dual-write"></a>Lagertilgængelighed i dobbeltskrivning

[!include [banner](../../includes/banner.md)]

Ved hjælp af lagertilgængelighed kan du kontrollere dit lager, før du føjer et produkt til siden **Tilbud**, **Ordrer** eller **Fakturaer** i Microsoft Dynamics 365 Sales. Kontrol af lager og fastlæggelse af en opfyldelsesdato er f.eks. en nøgleopgave i processen for [kundeemne til kontant](dual-write-prospect-to-cash.md).

Hvis du ikke har tilstrækkelig lagerbeholdning, kan du estimere en leveringsdato ud fra projekterede lagertilgange og -afgange. Du kan også kontrollere produktets DTT-oplysninger (disponibelt til tilsagn), hvor du kan finde DTT-antallet i den foruddefinerede tidshorisont.

## <a name="on-hand-inventory"></a>Disponibel lagerbeholdning

I sidehovedet for formularerne **Tilbud**, **Ordrer** og **Fakturaer** i Dynamics 365 Sales er der tilføjet en ny knap **Disponibel lagerbeholdning**. Når du vælger knappen, vises en dialogboks, hvor du kan angive det firma og det produkt, som den disponible lagerbeholdning skal kontrolleres for. I denne dialogboks vises de samme oplysninger som [disponibel lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogboksen returnerer lageroplysningerne fra Dynamics 365 Supply Chain Management. Disse oplysninger indeholder følgende antal:

- Beholdningsantal
- Reserveret disponibelt antal
- Tilgængeligt disponibelt antal
- Bestilt antal
- Antal i bestilling
- Reserveret bestilt mængde
- Disponibelt antal i alt

## <a name="atp-information"></a>DTT-oplysninger

I Sales er der føjet en ny knap for **DTT-oplysninger** til linjeelementer på siderne **Tilbud**, **Ordrer** og **Fakturaer**. Når du vælger knappen, vises en dialogboks, hvor du kan angive firma, produkt, lagerlokation, lagersted og ordreantal. Denne dialogboks har de samme indstillinger, som er beskrevet under [Ordretilsagn](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogboksen returnerer DTT-oplysningerne fra Supply Chain Management. Disse oplysninger indeholder følgende antal:

- DTT-antal
- Tilgangsantal
- Afgangsantal
- Beholdningsantal

## <a name="how-it-works"></a>Sådan fungerer det

Når du vælger knappen **Disponibel lagerbeholdning** på siden **Tilbud**, **Ordrer** eller **Fakturaer**, foretages der et direkte opkald om dobbeltskrivning til API'en **Disponibel lagerbeholdning**. API'en beregner den disponible beholdning for det givne produkt. Resultatet gemmes i tabellerne **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og skrives derefter til Dataverse via dobbeltskrivning. Hvis du vil bruge denne funktion, skal du køre følgende dobbeltskrivningstilknytningerne. Spring den første synkronisering over, når du kører tilknytningerne.

- CDS Poster for disponibel lagerbeholdning (msdyn_inventoryonhandentries)
- CDS Anmodninger om disponibel lagerbeholdning (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Skabeloner
Der findes følgende skabeloner til visning af de disponible lagerbeholdningsdata.

Finance and Operations-apps | Customer Engagement-app | Betegnelse 
---|---|---
[Posteringer til disponibelt CDS-lager](#145) | msdyn_inventoryonhandentries |
[Anmodninger om disponibelt CDS-lager](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>CDS Poster for disponibel lagerbeholdning (msdyn_inventoryonhandentries)

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Dataverse.

Finance and Operations-felt | Tilknytningstype | Customer Engagement-felt | Standardværdi
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

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>CDS Anmodninger om disponibel lagerbeholdning (msdyn_inventoryonhandrequests)

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Dataverse.

Finance and Operations-felt | Tilknytningstype | Customer Engagement-felt | Standardværdi
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