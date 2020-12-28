---
title: Lokalisere fejl i produktkvitteringer og fakturering
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktkvitteringer og fakturering.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425053"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Lokalisere fejl i produktkvitteringer og fakturering

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktkvitteringer og fakturering.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Jeg kan ikke bogføre mere end én faktura på en indkøbsordrelinje, der har kategoribaserede varer.

Et antal skal angives, hvis du vil bogføre fakturaer. Hvis hele antallet på en linje kun er faktureret for et delvist beløb, kan du derfor ikke fakturere restbeløbet på en anden faktura.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Jeg får vist fejlmeddelelsen "Objektreferencen er ikke angivet" under bekræftelse af indkøbsordren, eller der er opstået "Destinationen for en aktivering udløste en undtagelse" under bogføring af kreditorfakturaen.

Dette problem kan opstå på grund af inkonsistens i indkøbsordrefordeling.

Hvis du vil løse dette problem og nulstille indkøbsordren til en *Kladde*-tilstand, skal du gå til **Indkøb og forsyning \> Periodiske opgaver \> Oprydning \> Nulstil indkøbsordrefordeling**. Du kan finde flere oplysninger i følgende blogindlæg: [Løse fejl i indkøbsordrefordeling i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Jeg kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre.

Du kan ikke konsolidere flere produktkvitteringer i en enkelt indkøbsordre, hvis de forskellige produktkvitteringslinjer har forskellige regnskabsdatoer.

I tidligere versioner af Microsoft Dynamics 365 Supply Chain Management var konsolidering tilladt i denne situation. Det er dog fejlrisiko ved denne praksis. Regnskabsdatoen på de indkøbsordrelinjer, der oprettes, bør ikke være forskellige fra regnskabsdatoen på de produktkvitteringslinjer, som disse indkøbsordrelinjer er oprettet ud fra. (Regnskabsdatoen på indkøbsordrelinjerne svarer til regnskabsdatoen på indkøbsordrehovedet). Det er derfor ikke længere tilladt at konsolidere flere produktkvitteringer i en enkelt indkøbsordre.

Regnskabsdatoen bruges f.eks. ved budgetreservationer og behæftelser. Derfor skal den beholdes under overgangen fra produktkvittering til indkøbsordre.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Når produktkvitteringer annulleres, kan transaktionerne bogføres på en suspenderet finanskonto.

### <a name="issue-description"></a>Problembeskrivelse

Hvis en produktkvittering annulleres, tillader systemet, at der bogføres transaktioner på suspenderede finanskonti, selvom hovedkontiene er suspenderet.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. På siden **Kreditorparametre** skal du under fanen **Generelt** kontrollere, at indstillingen **Bogfør produktkvittering i finans** er angivet til *Ja*.
1. Opret en indkøbsordre, og tilføj en ordrelinje, der har et antal på *1.000* for et produkt.
1. Bekræft indkøbsordren.
1. Bogfør produktkvitteringen, og kontrollér bilagene.
1. Suspender de relevante hovedkonti, *200140* og *140200*.
1. Annuller den bogførte produktkvittering.
1. Bemærk, at transaktioner kan bogføres på de suspenderede finanskonti.

### <a name="issue-resolution"></a>Problemløsning

Transaktioner kan bogføres på de suspenderede finanskonti, når produktkvitteringer annulleres, da denne funktionsmåde giver mulighed for korrekte bogføringer.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Bilagsnummeret på produktkvitteringen forbruges, selvom der ikke genereres et økonomisk bilag under produktkvittering.

Hvis indstillingen **Periodiser passiver ved produktmodtagelse** er angivet til *Nej* for varemodelgruppen, vil der ikke blive bogført til Finans. Der vil dog blive registreret en fysisk hændelse med det formål at foretage regnskabsføring i en reskontro, og den pågældende hændelse kræver et bilagsnummer. Dette bilagsnummer er det bilagsnummer, der refereres til i lagertransaktionerne.

Det anbefales, at du angiver indstillingen **Periodiser passiver ved produktmodtagelse** til *Ja* som beskrevet i følgende blogindlæg: [Bogføre diverse gebyrer på tidspunktet for produktmodtagelse](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Indstillingen Vil du bogføre på omkostningskontoen i finans? er ikke aktiveret.

### <a name="issue-description"></a>Problembeskrivelse

Dette problem opstår, når en indkøbsordre faktureres, hvis indstillingen **Vil du bogføre på omkostningskontoen i finans?** er angivet til *Ja* under fanen **Faktura** på siden **Kreditorparametre**.

### <a name="reproduce-the-issue"></a>Genskabe problemet

Følgende procedurer viser en måde at genskabe problemet på.

1. Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
1. Under fanen **Faktura** skal du angive **Vil du bogføre på omkostningskontoen i finans?** til *Ja*.
1. Gå til **Lagerstyring \> Konfiguration \> Bogføring \> Bogføring**.
1. Under fanen **Indkøbsordre** skal du sikre dig, at du har slettet alle linjerne i købsudgiften for produktet.
1. Gå til **Kreditor \> Indkøbsordrer \> Alle indkøbsordrer**.
1. Oprette en indkøbsordre. Vælg **1001 ACME kontorartikler** i feltet *Kreditorkonto*.
1. Tilføj en indkøbsordrelinje, der har følgende indstillinger:

    - **Varenummer:** *D0011 laserprojektor*
    - **Lokation:** *1*
    - **Lagersted:** *11*
    - **Antal:** *4*

1. Vælg **Bekræft** i gruppen **Handling** under fanen **Indkøb** i handlingsruden.
1. Gå til handlingsruden, og vælg **Produktkvittering** i gruppen **Generér** under fanen **Modtag**.
1. Angiv et vilkårligt nummer i feltet **Produktkvittering** i dialogboksen **Konterer produktkvittering**, og vælg derefter **OK**.
1. Vælg **Faktura** i gruppen **Generér** under fanen **Faktura** i handlingsruden.
1. Angiv et vilkårligt nummer som fakturanummer i feltet **Nummer**.
1. Opdater status for sammenholdelse, og bogfør.
1. Bemærk, at du nu får vist følgende fejl, når du opretter en faktura ud fra en indkøbsordre: "Kontonummer for konteringstypen Indkøbsudgifter for produkt findes ikke".

### <a name="issue-resolution"></a>Problemløsning

Dette afhænger af parameterindstillingerne for fakturaer og fakturagrupper. Du kan finde flere oplysninger i følgende blogindlæg: [Regnskabsføring for indkøbstillæg og lagervariation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
