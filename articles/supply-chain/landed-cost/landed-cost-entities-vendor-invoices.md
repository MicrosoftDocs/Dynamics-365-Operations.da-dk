---
title: Enheder til kreditorfaktura
description: Denne artikel indeholder oplysninger om kreditorfakturaenheder, der gør det muligt at konfigurere omkostningstypekoder for interne omkostninger eller eksternt afledte omkostninger.
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
ms.openlocfilehash: f0371cf9862afaf3bc43a44def725c420e9aaf56
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166737"
---
# <a name="vendor-invoice-entities"></a>Kreditorfakturaenheder

[!include [banner](../includes/banner.md)]

I modulet **Landingsomkostninger** kan der konfigureres koder for omkostningstyper til interne omkostninger eller eksternt afledte omkostninger. Hvis en omkostning er ekstern for et firma, forventes der en faktura fra serviceudbyderen. Fakturaen behandles som en fakturakladde, der kan knyttes til en rute, og fakturaens værdi kan fordeles på tværs af en eller flere omkostninger for ruten.

Kreditorfakturaenhederne giver mulighed for, at værdien af en kladdelinje fordeles på tværs af en eller flere ruteomkostninger, der deler samme omkostningstypekode.

Der kan kun fordeles en omkostning, hvis fakturakladdehovedet og fakturakladdelinjerne findes.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Omkostningstildeling for leverandørrute (ITMLedgerJournalCostLinesVoyagesEntity)

Du kan bruge dataenheden for leverandørrutens omkostningsfordelinger til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på ruteomkostningsområdet. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesVoyagesEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |
| Fragt | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Omkostningsfordelinger for leverandørforsendelsescontainer (ITMLedgerJournalCostLinesContainersEntity)

Du kan bruge dataenheden for leverandørforsendelsescontainerens omkostningsfordelinger til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på omkostningsområdet for forsendelsescontainer. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesContainersEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Forsendelsescontainer | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |
| Fragt | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Omkostningsfordelinger for leverandørfolio (ITMLedgerJournalCostLinesFoliosEntity)

Du kan bruge dataenheden for leverandørfolioens omkostningsfordelinger til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på folioomkostningsområdet. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesFoliosEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Omkostningsfordelinger for kreditorindkøbsordre (ITMLedgerJournalCostLinesPurchTableEntity)

Du kan bruge dataenheden til omkostningsfordelinger for leverandørindkøbsordrer til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på omkostningsområdet for indkøbsordrer. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesPurchTableEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |
| Indkøbsordre | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Omkostningsfordelinger for leverandørvare (ITMLedgerJournalCostLinesPurchLineEntity)

Du kan bruge dataenheden for leverandørvarens omkostningsfordelinger til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på vareomkostningsområdet. Varens omkostningsområde dækker omkostningerne på indkøbsordrelinjen. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesPurchLineEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |
| Indkøbsordre | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |
| Nummer på indkøbsordrelinje | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Omkostningsfordelinger for leverandøroverførslers ordrelinjer (ITMLedgerJournalCostLinesTransferLineEntity)

Du kan bruge dataenheden til omkostningsfordelinger for leverandøroverførslers ordrelinjer til at fordele en kreditorfakturalinje på tværs af en eller flere omkostninger, der anvendes på omkostningsområdet for overførselslinjer. Denne funktion understøttes af enheden `ITMLedgerJournalCostLinesTransferLineEntity`. Følgende tabel indeholder de felter og tilknytninger, der udgør denne enhed.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Fordelt beløb | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Nej | Nej |
| Omkostningstransaktionslinjenummer | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdelinjenummer | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ja** | Nej |
| Kladdenummer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ja** | Nej |
| Overførselsordre | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ja** | Nej |
| Nummer på overførselsordrelinje | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ja** | Nej |

### <a name="reference-table"></a>Referencetabel

Ruteomkostningslinjer har en direkte tilknytning til en omkostningstransaktionspost. Denne post indeholder værdien **Referencetabel-id**. Denne værdi er entydig for hvert omkostningsområde (rute, forsendelsescontainer osv). Når der refereres til bestemte tabelnumre for data, der oprettes ved hjælp af dataenheder, fordeles enhederne på basis af værdier for **Referencetabel-id**.

Værdierne for referencetabellen (`RefTableId`) og transaktionstypen (`TransType`) er implicitte i valget af indkøbslinjen Landingsomkostninger eller enheden for overførselslinjen Landingsomkostninger.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Kreditorfakturakladdelinjer (VendorInvoiceJournalLineEntity)

Før en kladdelinjeværdi kan fordeles på en eller flere omkostninger i modulet **Landingsomkostninger**, skal kladdelinjen knyttes til et omkostningsområde. For at understøtte denne funktion føjer modulet **Landingsomkostninger** nogle nye felter til kladdelinjetabellen (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Felter, der er føjet til kladdelinjeenheden for kreditorfaktura

Følgende tabel indeholder de felter, som modulet **Landingsomkostninger** føjer til kreditorfakturakladdelinjens enhed (`VendorInvoiceJournalLineEntity`). Disse felter sætter systemet i stand til at oprette kladdelinjer og fordele omkostninger på dem.

| Navn | Tilknytning | Datatype | Nøgle | Obligatorisk |
|---|---|---|---|---|
| Omkostningsområde | LedgerJournalTrans.ITMCostArea | Int | Nej | Nej |
| Omkostningstypekode | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nej | Nej |

### <a name="mainoffset-account"></a>Hovedkonto/modkonto

Hoved-/modkontoen for en fakturakladdelinje, der er tilknyttet en rute for landingsomkostninger, bestemmes af omkostningstypekoden. Når omkostningstypekoden medtages på fakturakladdelinjen, bruges clearingkontoen for koden enten som hovedkonto eller modkonto afhængigt af scenariet:

- **Enkeltlinjekladde** – Hvis der er defineret en hovedkonto (dvs. kreditorkontoen), og der er angivet en omkostningstypekode, angives clearingkontoværdien for den pågældende omkostningstypekode på modkontoen.
- **Flerlinjekladde** – Hvis der ikke er defineret en hovedkonto, men der er angivet en omkostningstypekode, angives clearingkontoværdien for den pågældende omkostningstypekode som hovedkontoen. Den kladdelinje, der krediterer kreditoren, refererer ikke til en omkostningstypekode.

## <a name="sequencing"></a>Rækkefølge

På grund af afhængigheder mellem kladde- og kladdelinjetabeller, skal ruteposten oprettes først. Rutelinjerne kan kun oprettes, når ruten, forsendelsescontaineren og folioerne er oprettet.

Hvis du vil fordele en rutefaktura, skal systemet behandle enhederne i følgende rækkefølge:

1. Fakturakladdehoved (`VendInvoiceJournalHeaderEntity`)
1. Fakturakladdelinje (`VendInvoiceJournalLineEntity`)
1. Fordelinger af landingsomkostninger (`ITMLedgerJournalEntities`)
