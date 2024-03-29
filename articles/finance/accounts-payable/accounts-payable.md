---
title: Startside for kreditor
description: Denne artikel giver en oversigt over kreditor.
author: sunfzam
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "21901"
- intro-internal
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 5ed6aacb94de14bdb72185cd528f62e74cd3cc15
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946095"
---
# <a name="accounts-payable-home-page"></a>Startside for kreditor

[!include [banner](../includes/banner.md)]

Denne artikel giver en oversigt over kreditor. 

Du kan angive kreditorfakturaer manuelt eller modtage dem elektronisk via en dataenhed. Når fakturaerne er blevet indtastet eller modtaget, kan du gennemse og godkende dem vha. en fakturagodkendelseskladde eller siden **Kreditorfaktura**. Du kan bruge fakturasammenholdelse, kreditorfakturapolitikker og arbejdsgange til at automatisere gennemsynsprocessen, så fakturaer, der overholder visse krav, automatisk bliver godkendt, og de resterende fakturaer markeres til gennemsyn af en autoriseret bruger.

**Forretningsprocesser**

[![Diagram over forretningsprocesser.](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Konfigurere Kreditorer

Konfigurer kreditorgrupper, kreditorer, posteringsprofiler, forskellige betalingsindstillinger og parametre for kreditorer, gebyrer, leveringer og destinationer, egenveksler og andre typer kreditoroplysninger. 

[Oversigt over konfiguration af kreditor](accounts-payable-overview.md)

[Regnskabsfordelinger og kladdepostering for reskontro til kreditorfakturaer](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Værdiregulering af udenlandsk valuta for kreditor og debitor](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Konfigurere kreditorfakturaer

I Kreditorer kan du spore fakturaer og udgående betalinger til kreditorer.

[Oversigt over fakturasammenholdelse for kreditor](accounts-payable-invoice-matching.md)

[Kreditorposteringsprofiler](vendor-posting-profiles.md)

[Konfigurere validering af sammenholdelse af kreditorfakturaer](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Trevejs-sammenholdelsespolitikker](three-way-matching-policies.md)

[Fakturasammenholdelse og interne indkøbsordrer](invoice-matching-intercompany-purchase-orders.md)

[Oversigt over løsning af afvigelser under sammenholdelse af fakturatotaler](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Standardmodkonti for kreditorfakturakladder og fakturagodkendelseskladder](default-offset-accounts-vendor-invoice-journals.md)

[Mobilfakturagodkendelser](mobile-invoice-approvals.md)

[Arbejdsområde for kreditorsamarbejdsfakturering](vendor-portal-invoicing-workspace.md)

[Automatisering af kreditorfaktura](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Konfigurere kreditorbetalinger 

Tildel en systemdefineret betalingstype, f.eks check, elektronisk betaling eller egenveksel, til alle brugerdefinerede betalingsmåder. Betalingstyper er valgfrie, men de er nyttige, når du validerer elektroniske betalinger og vil være i stand til hurtigt at bestemme, hvilken betalingstype der benyttes i en betaling. 

[Arbejdsområde for kreditorbetalinger](vendor-payments-workspace.md)

[Definere kreditorbetalingsgebyrer](tasks/define-vendor-payment-fees.md)

[Definere kreditorbetalingsbetingelser](tasks/define-vendor-payment-terms.md)

[Oversigt over positive betalinger](positive-pay-overview.md)

[Konfigurere og generere filer til positive betalinger](set-up-generate-positive-pay-files.md)

[Oprette kreditorbetalinger ved hjælp af et betalingsforslag](create-vendor-payments-payment-proposal.md)

[Kreditorbetalinger af et delvist beløb](vendor-payments-partial-amount.md)

[Bruge en rabat, der er større end den beregnede rabat, til en kreditorbetaling](take-discount-more-calculated-discount-vendor-payment.md)

[Bruge en kasserabat uden for kasserabatperioden](take-cash-discount-outside-cash-discount-timeframe.md)

[Eksempel på elektronisk rapportering for kreditorchecks](electronic-reporting-sample-vendor-checks.md)

[Tilbageføre en kreditorbetaling](reverse-vendor-payment.md)

[Forudbetalingsfakturaer vs. forudbetalinger](prepayments-invoices-vs-prepayments.md)

[Centraliserede kreditorbetalinger](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Udligninger

Under følgende emner finder du oplysninger om udligninger. Udligningsprocessen omfatter udligning af betalinger med fakturaer. 

[Konfigurere udligning](../cash-bank-management/configure-settlement.md)

[Udligne en delvis kreditorbetaling før rabatdatoen med en endelig betaling efter rabatdatoen](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Udligne en delvis kreditorbetaling med rabatter på kreditorkreditnotaer](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Udligne en delvis kreditorbetaling, der omfatter flere rabatperioder](settle-partial-vendor-payment-multiple-discount-periods.md)

[Udligne en delvis kreditorbetaling og udligne den endelige betaling fuldt ud før rabatdatoen](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Enkelt bilag med flere debitor- eller kreditorposter](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Yderligere ressourcer

#### <a name="whats-new-and-in-development"></a>Nyheder og funktioner under udvikling

Gå til [Microsoft Dynamics 365-frigivelsesplaner](/dynamics365/release-plans/) for at se, hvilke nye funktioner der er planlagt. 

#### <a name="blogs"></a>Blogs

Du kan finde meninger, nyheder og andre oplysninger om Kreditor og andre løsninger på [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og [Microsoft Dynamics 365 Finance and Operations – Finans-bloggen](https://community.dynamics.com/365/financeandoperations/b/financials).

[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) giver Microsoft Dynamics-partnere en samlet ressource, hvor de kan finde oplysninger om nyheder og populære tendenser i Dynamics 365.

#### <a name="community-blogs"></a>Fællesskabsblogge

[Sådan administreres skyldige beløb i Dynamics 365 Finance](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Opgaveguider
Yderligere hjælp er tilgængelig som opgaveguider i applikationen. Du kan få adgang til opgaveguider ved at klikke på knapp​en Hjælp på en vilkårlig side.

#### <a name="videos"></a>Videoer

Se de Sådan-videoer, der er nu tilgængelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
