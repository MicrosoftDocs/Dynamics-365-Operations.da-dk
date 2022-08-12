---
title: Integreret kreditormaster
description: Denne artikel beskriver integrationen af kreditordata mellem programmer til finans og drift og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112188"
---
# <a name="integrated-vendor-master"></a>Integreret kreditormaster

[!include [banner](../../includes/banner.md)]



Termen *Kreditor* henviser til en leverandørorganisation eller en solovirksomhed, der leverer varer eller ydelser til en virksomhed. Selvom *kreditor* er et etableret begreb i Microsoft Dynamics 365 Supply Chain Management, findes der ikke et kreditorbegreb i Customer Engagement-apps. Du kan dog også overbelaste tabellen **Konto/Kontaktperson**, når du vil gemme kreditoroplysninger. Den integrerede kreditormaster introducerer et eksplicit leverandørbegreb i Customer Engagement-apps. Du kan enten bruge det nye kreditordesign eller gemme kreditordata i tabellen **Konto/Kontaktperson**. Dobbeltskrivning understøtter begge metoder.

I begge fremgangsmåder integreres leverandørdataene mellem Dynamics 365 Supply Chain Management-, Dynamics 365 Sales-, Dynamics 365 Field Service- og Power Apps-portaler. I Supply Chain Management er data tilgængelige i arbejdsgange, f.eks. indkøbsrekvisitioner og indkøbsordrer.

## <a name="vendor-data-flow"></a>Kreditordataflow

Hvis du ikke vil gemme kreditordata i tabellen **Konto/Kontaktperson** i Dataverse, kan du bruge det nye kreditordesign.

![Kreditordataflow.](media/dual-write-vendor-data-flow.png)

Hvis du fortsat vil gemme kreditordata i tabellen **Konto/Kontaktperson**, kan du bruge det udvidede kreditordesign. Hvis du vil bruge det udvidede leverandørdesign, skal du konfigurere leverandørarbejdsgangene i Dobbeltskrivnings-løsningspakken. Du kan finde flere oplysninger i [Skifte mellem kreditordesign](vendor-switch.md).

![Udvidet kreditordataflow.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Hvis du bruger Power Apps-portaler til leverandørselvbetjening, kan kreditoroplysningerne flyde direkte til programmer til finans og drift.

## <a name="templates"></a>Skabeloner

Kreditordata indeholder alle oplysninger om kreditoren, f.eks kreditorens gruppe, adresser, kontaktoplysninger, betalingsprofil og fakturaprofil. En samling af tabeltilknytninger arbejder sammen under interaktion med kreditordata, som vist i følgende tabel.

Programmer til finans og drift | Kundeengagementapps     | Betegnelse
----------------------------|-----------------------------|------------
[CDS kontakter V2](mapping-reference.md#115) | kontakter | Denne skabelon synkroniserer alle primære, sekundære og tertiære kontaktoplysninger for både kunder og leverandører.
[Foranstillede navne](mapping-reference.md#155) | msdyn_nameaffixes | Denne skabelon synkroniserer referencedata for foranstillede navne for både kunder og leverandører.
[Betalingsdagslinjer CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Denne skabelon synkroniserer betalingsdagslinjers referencedata for både kunder og leverandører.
[Betalingsdage CDS](mapping-reference.md#158) | msdyn_paymentdays | Denne skabelon synkroniserer referencedata for linjer for betalingsdage for både kunder og leverandører.
[Betalingsplanlinjer](mapping-reference.md#159) | msdyn_paymentschedulelines | Synkroniserer betalingsdagsskemalinjers referencedata for både kunder og leverandører.
[Betalingsplan](mapping-reference.md#160) | msdyn_paymentschedules | Denne skabelon synkroniserer referencedata for betalingsskemaer for både kunder og leverandører.
[Betalingsbetingelse](mapping-reference.md#161) | msdyn_paymentterms | Denne skabelon synkroniserer referencedata for betalingsbetingelser (betalingsvilkår) for både kunder og leverandører.
[Kreditorer V2](mapping-reference.md#202) | msdyn_vendors | Virksomheder, der bruger en tilpasset løsning til leverandører, kan drage fordel af det standardkoncept for leverandører, der introduceres i Dataverse på grund af integrationen af programmer til finans og drift.
[Kreditorgrupper](mapping-reference.md#200) | msdyn_vendorgroups | Denne skabelon synkroniserer oplysninger om leverandørgrupper.
[Kreditorbetalingsmetode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Denne skabelon synkroniserer oplysninger om leverandørers betalingsmetoder.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

