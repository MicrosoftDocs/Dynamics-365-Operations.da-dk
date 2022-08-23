---
title: Lagertilgængelighed i dobbeltskrivning
description: Denne artikel har oplysninger om, hvordan du kontrollerer lagertilgængelighed i dobbeltskrivning.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 442486550d3a7c5132e26f663caaa7c2c02eeb6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289202"
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

Finans og drift-apps | Kundeengagementapps     | Betegnelse
---|---|---
[Posteringer til disponibelt CDS-lager](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[Anmodninger om disponibelt CDS-lager](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
