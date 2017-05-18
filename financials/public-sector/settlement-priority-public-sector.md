---
title: Udligningsprioritet i den offentlige sektor
description: "I Microsoft Dynamics 365 for Operations kan du vælge at udligne transaktionerne manuelt eller bruge funktionen til automatisk udligning. Offentlige organisationer har flere muligheder for at prioritere af udligninger ved hjælp af faktureringsklassifikationer. Disse indstillinger kan bruges sammen med automatisk eller manuel udligning."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustBillingClassification, CustBillingCode, CustParameters, CustSettlementPrioritySetup, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19551
ms.assetid: b6f96e12-5614-4edf-9f67-47bf011b6ee7
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: fd69ffd6cc6784b57aaed7090c99b92fbeabe1c9
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="settlement-priority-in-the-public-sector"></a>Udligningsprioritet i den offentlige sektor

[!include[banner](../includes/banner.md)]


I Microsoft Dynamics 365 for Operations kan du vælge at udligne transaktionerne manuelt eller bruge funktionen til automatisk udligning. Offentlige organisationer har flere muligheder for at prioritere af udligninger ved hjælp af faktureringsklassifikationer. Disse indstillinger kan bruges sammen med automatisk eller manuel udligning.

<a name="how-to-set-the-general-ledger-parameters-and-accounts-receivable-parameters-for-settlement-priority"></a>Sådan indstilles parametrene Finans og Debitor for udligningsprioritet
---------------------------------------------------------------------------------------------------

Hvis du vil bruge faktureringsklassifikationer til at kontrollere udligningsprioriteter, skal du angive både parameteren moms i appen Finans og udligningsparametre i appen Debitor. 

> [!NOTE]
> Dine faktureringsklassifikationer bør være helt oprettet og aktiveret, før du angiver disse parametre. Så snart du aktiverer faktureringsklassifikationer, bliver faktureringsklassifikation et obligatorisk felt på fritekstfakturaen. 

Du kan få flere oplysninger om faktureringsklassifikationer, herunder hvordan du kan aktivere dem, i [Faktureringsklassifikationer og faktureringskoder i den offentlige sektor](billing-classifications-billing-codes-public-sector.md).

-   På siden **Økonomiparametre** i afsnittet **Moms** på oversigtspanelet **Momsindstillinger** skal du vælge indstillingen **Momsbeløb pr. fakturalinje**.
-   På siden **Debitorparametre** i afsnittet **Udligning** skal du benytte følgende fremgangsmåde:
    -   Markér indstillingen for at markere linjer til fritekstfakturaer og rentenotaer.
    -   Vælg indstillingen for at prioritere udligning.
    -   Klik på **Administrer prioritet**, og rediger siden for at gøre attributten **Fakturering** aktiv og for at angive fakturalinjeprioriteten og relaterede indstillinger. Attributten **Fakturering** er ikke tilgængelig, før faktureringsklassifikationer er aktiveret.

Tre indstillinger er tilgængelige for fakturalinjeprioriteten: **Ingen**, **Faktureringskode** og **Proportionalitet**.

-   Hvis du vælger **Ingen** for fakturaprioriteten, prioriteres udligning af faktureringsklassifikationer. Når du gør dette, anvendes først betalinger til transaktioner med den højeste faktureringsklassifikationsprioritet. En eventuel resterende betaling anvendes på den faktureringsklassifikationsprioritet, der har den næstehøjeste prioritet osv., indtil betalingen er opbrugt.
-   Hvis du vælger **Faktureringskode**, prioriteres udligning af faktureringsklassifikationer, og faktureringskoder bruges til at finjustere udligningsprioriteten. Når du gør dette, kan du vælge, om du vil udvide faktureringskoder på tværs af alle fakturaer. Lad os antage, at du har tre fakturaer, der har faktureringsklassifikationen Parker. Alle tre fakturaer har fire linjer, og alle fire linjer har faktureringskoder.
    -   Hvis du udvider faktureringskoder på tværs af alle fakturaer, ser udligningsprocessen på alle 12 linjer og udligner betalingen efter faktureringskodeprioritet. Alle linjer, der har den højeste prioritetsfaktureringskode, udlignes derfor, før hver linje, der har den næsthøjeste prioritetsfaktureringskode, udlignes.
    -   Hvis du ikke udvider faktureringskoder på tværs af alle fakturaer, ser udligningsprocessen på linjerne på alle fakturaer separat. Alle linjer på den første faktura udlignes efter faktureringskodeprioriteten, før en linje på næste faktura er udlignet.
-   Hvis du vælger **Proportionalitet**, prioriteres udligning af faktureringsklassifikationer, og proportionalitet bruges til at finjustere udligningsprioriteten inden for faktureringsklassifikationer. Når du gør dette, kan du vælge, om du vil bruge samme eller proportional proportionalitet. I begge tilfælde skal alle linjerne på en faktura udlignes, inden en linje på næste faktura er udlignet. Lad os antage, at du har tre fakturaer, der har faktureringsklassifikationen Parker. Hver enkelt faktura indeholder fire linjer for $200, $400, $600 og $800. Der blev modtaget en betaling på $2500.
    -   Hvis du bruger samme proportionalitet, bliver et betalingsbeløb, der ikke vil betale en faktura i sin helhed, opdelt i fire lige store dele. En del anvendes på hver linje. Resultatet vil f.eks. være som følger:
        -   Den første faktura udlignes helt, og der resterer $500 til at anvende på næste faktura.
        -   De resterende $500 er opdelt i fire lige store dele af $125 og anvendes på hver fakturalinje i den anden faktura.
        -   Der anvendes ikke noget til en linje på den tredje faktura.
    -   Hvis du bruger proportional proportionalitet, bliver et betalingsbeløb, der ikke vil betale en faktura i sin helhed, opdelt i forholdsmæssige mængder og anvendes på hver fakturalinje. Delen er baseret på linjebeløbet i forhold til det samlede fakturabeløb. Resultatet vil f.eks. være som følger:
        -   Den første faktura udlignes helt, og der resterer $500 til at anvende på næste faktura.
        -   De resterende $500 er opdelt i fire proportionale beløb på $50, $100, $150 og 200 $ og anvendes på de tilhørende linjer på den anden faktura.
        -   Der anvendes ikke noget til en linje på den tredje faktura.

## <a name="how-to-set-the-settlement-priority-of-billing-codes-billing-classifications-and-settlement-attributes"></a>Hvordan du kan angive udligningsprioriteten af faktureringskoder, faktureringsklassifikationer og udligningsattributter
Under udligningsprocessen kommer udligningsattributter i betragtning først, derefter faktureringsklassifikationer og faktureringskoder.

-   Når du har føjet faktureringskoder til en faktureringsklassifikation, skal du bruge knapperne **Op** og **Ned** på oversigtspanelet **Faktureringskoder** til at arrangere faktureringskoder i prioriteringsrækkefølge. (Dette er kun nødvendigt, hvis du planlægger at bruge **Faktureringskode** som din fakturalinjeprioritet).
-   Når du har oprettet alle de faktureringsklassifikationer for organisationen, kan du bruge knapperne **Op** og **Ned** øverst på siden **Faktureringsklassifikationer** til at arrangere faktureringsklassifikationer i prioriteringsrækkefølge.
-   Når du har aktiveret attributten **Fakturering** på siden **Udligningsprioritet**, skal du bruge knapperne **Op** og **Ned** øverst på siden til at arrangere de aktive udligningsattributter i prioriteringsrækkefølge.






