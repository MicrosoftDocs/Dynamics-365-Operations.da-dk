---
title: Debitorer i den offentlige sektor
description: "I dette emne beskrives de funktioner for Debitorer, som er tilgængelige for den offentlige sektor."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustInvoiceJournal, CustParameters, CustTradingPartnerCode
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 26281
ms.assetid: a411ec87-a209-471c-a141-5f5a92f2e45e
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 21ff81ac0fd30952b6482bd10c2ad620cb638401
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="accounts-receivable-in-the-public-sector"></a>Debitorer i den offentlige sektor

[!include[banner](../includes/banner.md)]


I dette emne beskrives de funktioner for Debitorer, som er tilgængelige for den offentlige sektor.

<a name="how-do-i-set-accounts-receivable-parameters-for-the-public-sector"></a>Hvordan indstiller jeg Debitorparametre for den offentlige sektor?
------------------------------------------------------------------

De fleste Debitorparametre angives på samme måde, uanset om du er i den offentlige sektor eller private sektor. De parametre, der kræves til faktureringsklassifikationer og faktureringskoder, bruges imidlertid kun af den offentlige sektor. Du kan få flere oplysninger i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).

-   Du kan aktivere brugen af faktureringsklassifikationer og faktureringskoder i afsnittet **Generelt** på oversigtspanelet **Salgsopsætning** og ved at vælge **Brug faktureringsklassifikationer**.
-   For at prioritere udligningen af fritekstfakturaer skal du se de påkrævede parameterindstillinger i [Udligningsprioritet i den offentlige sektor](settlement-priority-public-sector.md) og [Fritekstfakturaer i den offentlige sektor](free-text-invoices-public-sector.md).
-   Hvis du vil bruge faktureringskoder med Projektregnskab, skal du vælge indstillingen til at få vist projektrelaterede felter på fritekstfakturaer. Når du gør det, sker der to ting:
    -   Projektrelaterede felter vises både på fritekstfakturaer og faktureringskoder.
    -   Den finanskonto, der er knyttet til projektet, anvendes automatisk på fritekstfakturaen. Vælg indstillingen for at tillade finanskontonummeret at blive redigeret for at tillade brugere at ændre finanskontoen på fritekstfakturaen og i regnskabsfordelinger.

## <a name="how-do-i-control-the-settlement-order-for-accounts-receivable-transactions"></a>Hvordan styrer jeg udligningsrækkefølgen for debitorposteringer?
Du kan bruge faktureringsklassifikationer sammen med andre faktureringsattributter til at styre den rækkefølge, der er udlignet i dine debitorposteringer. Du kan få flere oplysninger i [Udligningsprioritet i den offentlige sektor](settlement-priority-public-sector.md).

## <a name="is-there-an-easy-way-to-review-reimbursement-transactions"></a>Er der en nem måde at gennemgå refusionsposteringer på?
Du kan bruge faktureringsklassifikationer til at oprette en separat refusionstransaktion for hver faktureringsklassifikation. Når du gør det, grupperes refusionsposteringer efter den entydige bogføringstype for debitorsaldo og faktureringsklassifikation. Du kan få flere oplysninger i [Udligninger i den offentlige sektor](reimbursements-public-sector.md).

## <a name="where-are-the-trading-partner-codes-that-i-need-for-gfrs-and-facts-i-reporting"></a>Hvor er de handelspartnerkoder, jeg skal bruge til GFRS- og FACTS I-rapportering?
De handelspartnerkoder, som er nødvendige for GFRS- og FACTS I-rapportering, bliver fastlagt af det amerikanske finans- og skatteministerium. Enhver virksomhed, der følger amerikanske statslige rapporteringsregler for debitorer, bør tilføje handelspartnerkoder til deres debitorkontooplysninger for de organer, som de gør forretninger med. For eksempel hvis kontoret handler med Federal Trade Commission, skal du gå til siden **Handelspartnerkoder** og oprette handelspartnerkode 29. Derefter, på siden med kundedetaljer for FTC, skal du skrive 29 i feltet **Handelspartnerkode**.

### <a name="i-created-default-financial-dimensions-for-a-customer-group-but-one-customer-in-the-group-needs-a-different-value-for-one-of-the-financial-dimensions-whats-the-easiest-way-to-handle-this"></a>Jeg har oprettet økonomiske standarddimensioner for en debitorgruppe, men én kunde i gruppen skal have en anden værdi for en af de økonomiske dimensioner. Hvad er den nemmeste måde at håndtere dette på?

Du kan bevare de økonomiske standarddimensioner for debitorgruppen. Bare gå til kundeposten for den debitor, der skal have en anden værdi, og angiv de økonomiske standarddimensioner for debitoren. Kundens økonomiske standarddimensioner tilsidesætter de økonomiske standarddimensioner, der er angivet for debitorgruppen.

## <a name="what-can-i-use-accounts-receivable-posting-definitions-for"></a>Hvad kan jeg bruge bogføringsdefinitioner for debitor til?
Du kan bruge bogføringsdefinitioner til at oprette reskontrokladdelinjer til kildetransaktioner, der opfylder de valgte kriterier – f.eks. til at generere flere, afstemte finansposter baseret på attributter, som f.eks. transaktionstyper og konti. Hvis du vil vide mere om bogføringsdefinitioner, skal du se [Bogføringsdefinitioner i den offentlige sektor](posting-definitions-public-sector.md).

<a name="see-also"></a>Se også
--------

[Debitor](..\accounts-receivable\accounts-receivable.md)




