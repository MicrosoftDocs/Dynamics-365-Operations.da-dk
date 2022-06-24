---
title: Enheder til omkostningstransaktioner
description: Denne artikel indeholder oplysninger om omkostningstransaktionsenheder, som gør det muligt at fordele værdien af en omkostning på indholdet af et omkostningsområde ved at vælge en fordelingsmetode.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860806"
---
# <a name="cost-transaction-entities"></a>Omkostningstransaktionsenheder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>Fordeling

Med landingsomkostninger kan værdien af en omkostning fordeles i et omkostningsområde (rute, forsendelsescontainer osv.) ved at vælge en fordelingsmetode. Fordelingsmetoden angives som en del af konfigurationen af automatiske omkostninger, der er baseret på forretningsregler. Den trækkes igennem som en del af omkostningen, når der oprettes en rute.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigurere fordelingstilknytningen til brug med dataenheder

Når en omkostning oprettes ud fra en ekstern kilde, f.eks. en speditør, kan den eksterne kilde ikke angive den foretrukne metode til fordeling af omkostningsværdien. Ved fordelingstilknytningen defineres standardmetoden for fordeling af hver enkelt omkostningstypekode. Tabellen til tilknytning af fordeling åbnes fra siden **Fordelingstilknytning** i Microsoft Dynamics 365 Supply Chain Management (**Landingsomkostninger \> Opsætning af efterkalkulation \> Fordelingstilknytning**).

Hvis der er defineret en tilknytningskombination, og en omkostning, der svarer til omkostningstypekoden, oprettes ved hjælp af en omkostningstransaktionsenhed, bruges den tilknyttede fordelingsmetode i stedet for enhver værdi, der er angivet for enheden.

Hvis der ikke er nogen værdi i tilknytningstabellen, men der er angivet en værdi for enheden, bruges den angivne værdi.

Hvis der ikke findes en værdi i hverken tilknytningstabellen eller den post, der er sendt til enheden, mislykkes oprettelsen.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Fordelingstilknytning (ITMApportionmentMapping)

Fordelingstilknytningsenheden (`ITMApportionmentMapping`) opretter relationer til fordelingstilknytning og giver brugerne mulighed for at oprette eller opdatere poster.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMApportionmentMapping.ApportionmentMethod | Int | Nej | Nej |
| Omkostningstypekode | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Ja** | Nej |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Ruteomkostninger (ITMCostTransVoyageEntity)

Ruteomkostningsenheden (`ITMCostTransVoyageEntity`) opretter ruteomkostningstransaktioner, der anvendes på ruteniveau. Under importprocessen bruger systemet de værdier for **Kategori** og **Fordelingsmetode**, der er medtaget i enheden, til at bestemme, hvordan værdien af omkostningen skal fordeles på tværs af indholdet i ruten.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Fragt | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Omkostninger for forsendelsescontainer (ITMCostTransShippingContainerEntity)

Omkostningsenheden for forsendelsescontainerenheden (`ITMCostTransShippingContainerEntity`) opretter forsendelsescontaineromkostninger, som anvendes på containerniveau. Under importprocessen bruger systemet de værdier for **Kategori** og **Fordelingsmetode**, der er medtaget i enheden, til at bestemme, hvordan værdien af omkostningen skal fordeles på tværs af indholdet i forsendelsescontaineren.

Felterne **Aggregering**, **Etape** og **Tilknyttet etape** er specifikke for poster, hvor værdien af **Omkostningsområde** er *Forsendelsescontainer.* Derfor findes de ikke i dataenheder for andre omkostningsområder.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Aggregering | ITMCostTrans.AggregatedCost | Int | Nej | Nej |
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Tilknyttet etape | ITMCostTrans.LinkLegId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Forsendelsescontainer | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Fragt | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Etape | ITMCostTrans.ShipLegId | Nvarchar(20) | Nej | Nej |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |

## <a name="folio-costs-itmcosttransfolioentity"></a>Folioomkostninger (ITMCostTransFolioEntity)

Folioomkostningsenheden (`ITMCostTransFolioEntity`) opretter poster for omkostningstransaktioner, der gælder for folioniveauet. Under importprocessen bruger systemet de værdier for **Kategori** og **Fordelingsmetode**, der er medtaget i enheden, til at bestemme, hvordan værdien af omkostningen skal fordeles på tværs af indholdet i hver folio.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Indkøbsordreomkostninger (ITMCostTransPurchaseEntity)

Indkøbsordreomkostningsenheden (`ITMCostTransPurchaseEntity`) opretter omkostningstransaktioner, der gælder for indkøberordrehovedet. Under importprocessen bruger systemet de værdier for **Kategori** og **Fordelingsmetode**, der er medtaget i enheden, til at bestemme, hvordan værdien af omkostningen skal fordeles på tværs af indholdet i hver folio.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelingsmetode | ITMCostTrans.ApportionmentMethod | Int | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Indkøbsordre | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |

## <a name="item-costs-itmcosttransitementity"></a>Vareomkostninger (ITMCostTransItemEntity)

Vareomkostningsenheden (`ITMCostTransItemEntity`) opretter omkostningstransaktioner, der gælder for vareniveauet. Denne enhed gælder kun for varer på indkøbsordrelinjer. Værdien af omkostningen anvendes fuldt ud på linjen.

Felterne **Reguleringsbeløb** og **Værdiregulering** er specifikke for omkostningsområderne på linjeniveau. Derfor findes de ikke i dataenheder for andre omkostningsområder.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Reguleringsbeløb | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Indkøbsordre | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Nummer på indkøbsordrelinje | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |
| Værdiregulering | ITMCostTrans.ValueAdjustmentMethod | Int | Nej | Nej |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Overførselslinjeomkostninger (ITMCostTransTransferLineEntity)

Enheden for overførselslinjeomkostning (`ITMCostTransTransferLineEntity`) opretter omkostningstransaktioner, der gælder for overførselsordrens linjeniveau. Værdien af omkostningerne anvendes fuldt ud på overførselsordrelinjen.

Felterne **Reguleringsbeløb** og **Værdiregulering** er specifikke for omkostningsområderne på linjeniveau. Derfor findes de ikke i dataenheder for andre omkostningsområder.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Reguleringsbeløb | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Nej | Nej |
| Omkostningsværdi | ITMCostTrans.CostValue | Numeric(32, 6) | Nej | Nej |
| Valuta | ITMCostTrans.CurrencyCode | Nvarchar(3) | Nej | **Ja** |
| Linjenummer | ITMCostTrans.LineNum | Numeric(32, 16) | **Ja** | Nej |
| Tilknyttet omkostningstype | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Nej | Nej |
| Minimumsomkostning | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Nej | Nej |
| Kategori | ITMCostTrans.ShipCostCategory | Int | Nej | Nej |
| Omkostningstypekode | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Nej | Nej |
| Virksomhed | ITMCostTrans.ShipDataArea | Nvarchar(4) | Nej | **Ja** |
| Overførselsordre | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Nummer på overførselsordrelinje | ITMCostTrans.TransRecId | Nvarchar(20) | **Ja** | Nej |
| Varemomsgruppe | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Nej | Nej |
| Værdiregulering | ITMCostTrans.ValueAdjustmentMethod | Int | Nej | Nej |

### <a name="transaction-table"></a>Transaktionstabel

En omkostningstransaktionspost knyttes til et omkostningsområde ved tildeling af et transaktionstabelnummer (`TransTableId`). Når der kræves specifikke tabelidentifikationsnumre, opdeles enhederne på basis af disse værdier, så der findes en enhed for hvert omkostningsområde.

Værdien for transaktionstabellen (`TransTableId`) vælges implicit som omkostningstransaktionsenhed.

### <a name="calculated-fields"></a>Beregnede felter

Følgende felter kan ikke indsættes eller opdateres, når der bruges en enhed til omkostningstransaktion, da disse felter kun angives, når der er foretaget specifikke handlinger mod ruteposten:

- **Forkalkuleret omkostning** – Dette felt angives, når en faktura bogføres for ruten (indkøbsordren), eller der modtages en overførsel.
- **Valuta for forkalkuleret omkostning** – Dette felt angives, når en faktura bogføres for ruten (indkøbsordren), eller der modtages en overførsel.
- **Faktisk omkostning** – Dette felt angives, når en kreditorfaktura bogføres. Den er tilknyttet omkostningen.

### <a name="find-auto-costs"></a>Søg efter automatiske omkostninger

Knappen **Find automatiske omkostninger**, der er tilgængelig for hvert omkostningsområde (rute, forsendelsescontainer osv.), giver dig mulighed for at opdatere omkostningstransaktionerne for dette omkostningsområde ud fra oplysningerne i konfigurationstabellerne. Når du vælger knappen til et omkostningsområde, ryddes eksisterende omkostninger for dette omkostningsområde, og der oprettes nye poster baseret på den aktuelle konfiguration af tabellerne til opsætning af automatiske omkostninger.

Omkostningstransaktionsposter, der oprettes ved hjælp af en dataenhed, markeres som importerede. Disse poster slettes ikke, når du vælger **Find automatiske omkostninger**, da de ikke oprettes igen fra tabellerne til opsætning af automatiske omkostninger. En post for en omkostningstransaktion, der er markeret som importeret, kan dog stadig slettes.

### <a name="linked-fields"></a>Sammenkædede felter

De enkelte omkostningstransaktioner kan knyttes til en anden post i samme omkostningsområde. Denne tilknytning oprettes via feltet **Sammenkædet omkostningstype**. Det giver mulighed for at beregne en omkostningsværdi som en procentdel af en anden omkostning.

Feltet **Tilknyttet omkostningstype** kan kun valideres, hvis den post, der refereres til, behandles først, eller hvis den allerede findes i tabellen. Det samme krav gælder for feltet **Tilknyttet etape**, som kun bruges til omkostningsområdet for forsendelsescontainer.
