---
title: Opsætning af forsendelsesoplysninger
description: Dette emne beskriver, hvordan du konfigurerer forsendelsesoplysninger for modulet Landingsomkostninger.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020881"
---
# <a name="shipping-information-setup"></a>Opsætning af forsendelsesoplysninger

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du konfigurerer forsendelsesoplysninger for modulet **Landingsomkostninger**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Beskrivelse af varer

Beskrivelser af varer gør det lettere at identificere en fragt, forsendelsescontainer eller varefolio og varerne i den. Du kan vælge en beskrivelse af varerne i forsendelsescontainerhovedet eller foliohovedet.

Hvis du vil arbejde med beskrivelser af varer, skal du gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Beskrivelse af varer**. Her kan du se, åbne, oprette og slette poster til varebeskrivelser. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Beskrivelse af varer | Angiv et entydigt id-navn/-nummer for den varetype, som skal bruge denne beskrivelse. |
| Beskrivelse | Angiv en beskrivelse af varetypen i denne kategori. |

## <a name="vessels"></a><a name="vessels"></a>Fartøjer

Et fartøj er det entydige navn på et skib eller fartøj, som fragtfirmaet eller agenturet bruger. Når du opretter en fragt, skal du altid vælge eller angive et fartøj for den. Hvis du ofte bruger de samme fartøjer, kan du gøre det hurtigere og nemmere at oprette en ny fragt ved at oprette en skibspost for hver af dem, hvilket giver brugerne mulighed for at vælge fartøjet på en liste i stedet for at angive navnet eller nummeret manuelt hver gang.

Du kan arbejde med fartøjer ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Fartøjer**. Her kan du se, åbne, oprette og slette poster til fartøjer. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Fartøj | Angiv et entydigt id-navn/nummer for det fartøj, der skal bruges til transport af varer i en fragt. |
| Beskrivelse | Angiv en beskrivelse af fartøjet. Denne beskrivelse identificerer typisk navnet på skibet og fragtfirmaet/-agenten. |
| Leveringsmåde | Vælg den leveringsmåde, som fartøjet anvender (f.eks. _Luft_, _Hav_ eller _Tog_). |

## <a name="exporters"></a>Eksportører

Hver eksportørpost identificerer en leverandør eller eksportør, der kan defineres som leverandøren af en fragt. Eksportøren kan tilknyttes en fragt og bruges til rapportering.

Du kan arbejde med eksportører ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Eksportører**. Her kan du se, åbne, oprette og slette poster til eksportører. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Eksportør | Angiv et entydigt id-navn/nummer for eksportøren af de varer, der skal transporteres i en fragt. |
| Beskrivelse | Angiv en beskrivelse af eksportøren. Denne beskrivelse identificerer typisk det fulde navn på fragtfirmaet/-agenten. |

## <a name="commodity-codes"></a>Varekoder

Du kan bruge varekoder som en hjælp ved identifikation i tolden og til beregning af toldsatser for varer i en fragt. Du kan vælge varekoder på siden **Frigivne produkter**.

Du kan arbejde med varekoder ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Varekoder**. Her kan du se, åbne, oprette og slette poster til varekoder. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Varekode | Angiv en entydig kode for denne varetype. |
| Beskrivelse | Angiv en beskrivelse af varetypen. |

## <a name="customs-description"></a>Toldbeskrivelse

Toldbeskrivelser gør det lettere at identificere varer til toldformål. Du kan vælge en toldbeskrivelse på siden **Frigivne produkter** eller på indkøbsordrelinjer.

Hvis du vil arbejde med toldbeskrivelser, skal du gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Toldbeskrivelse**. Her kan du se, åbne, oprette og slette poster til toldbeskrivelser. I følgende tabel forklares de felter, der er tilgængelige for hver post.

| Felt | Beskrivelse |
|---|---|
| Toldbeskrivelse | Angiv en entydig kode for denne type af toldklassifikation. Ofte vil denne kode være den officielle beskrivelse, der gives af en toldmyndighed for beskrivelsen og den kvalitative værdi af varerne. |
| Beskrivelse | Indtast en beskrivelse af toldklassifikationen. |
