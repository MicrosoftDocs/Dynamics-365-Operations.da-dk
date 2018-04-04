---
title: "Råbalance - økonomiske rapporter"
description: "I denne artikel beskrives standardrapporterne til råbalancer. Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 77e46e8693c65410ac7c44754edcb3c181f2aa18
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="trial-balance-financial-reports"></a>Råbalance - økonomiske rapporter

[!include[banner](../includes/banner.md)]


I denne artikel beskrives standardrapporterne til råbalancer. Her beskrives også de komponenter, der er knyttet til disse rapporter, og hvordan du kan redigere rapporterne, så de passer til virksomhedens behov. 

<a name="default-trial-balance-reports"></a>Standardråbalancerapporter
-----------------------------

Tre råbalancerapporter er tilgængelige i Økonomirapportering i Microsoft Dynamics 365 for Finance and Operations.

| Standardrapport                                 | Hvad den gør                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detaljeret råbalance – standard               | Leverer oplysninger om saldoen for alle konti og medtager har debet- og kreditsaldi, og nettobeløbet for disse saldi, sammen med transaktionsdato, bilag og beskrivelse af kladde.                  |
| Råbalanceoversigt – standard                | Leverer saldooplysninger for alle konti, og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen.                                        |
| Årlig råbalanceoversigt – standard | Leverer saldooplysninger for alle konti og medtager start- og ultimosaldi og debet- og kreditsaldi sammen med nettoforskellen for det aktuelle år og det foregående år. |

## <a name="building-blocks"></a>Komponenter
Råbalance regnskabsrapporter bruger følgende komponenter.

| Standardrapport                                 | Definition af række          | Kolonnedefinition                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Detaljeret råbalance – standard               | Råbalance – standard | Detaljeret råbalance – standard               |
| Råbalanceoversigt – standard                | Råbalance – standard | Råbalanceoversigt – standard                |
| Årlig råbalanceoversigt – standard | Råbalance – standard | Årlig råbalanceoversigt – standard |

### <a name="row-definition"></a>Definition af række

Rækkedefinitionen, råbalance – standard, indeholder en enkelt række, der henter alle hovedkonti. Derfor kan alle oprette rapporten uden at skulle foretage ændringer. Når du får vist rapporten, dykker du ind i den enkelte række for at se detaljer om hver konto. Du kan ændre rækkedefinitionen, så den omfatter flere detaljer. Følg disse trin for at ændre den råbalancen– standardrækkedefinitionen, så den indeholder rækker for alle konti.

1.  Klik på **Rediger**, og klik derefter på **Indsæt rækker fra dimensioner**. Med kommandoen **Indsæt rækker fra dimensioner** kan du vælge de dimensioner, du vil have i din rækkedefinition. For denne rækkedefinition skal du bruge **Hovedkonto**.
2.  Sørg for, at **Hovedkonto** indeholder og-tegn (&), og klik derefter på **OK**.

Rækkedefinitionen indeholder nu alle hovedkonti for den juridiske enhed, der er standard.

### <a name="column-definition"></a>Kolonnedefinition

Hver råbalancerapport bruger en anden kolonnedefinition. Disse kolonnedefinitioner indeholder forskellige typer kolonner, der giver forskellige niveauer af detaljer og økonomiske data.

-   **Detaljeret råbalance – standardkolonnetyper:**
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **ACCT** – Kontokoder
    -   **ATTR (3)** – Attributter:
        -   Posteringsdato
        -   Bilag
        -   Beskrivelse af kladde
    -   **FD** – økonomiske data, der kun indeholder debiteringer
    -   **FD** – økonomiske data, der kun indeholder krediteringer
    -   **CALC** – Nettodifferencen
-   **Opsummeret råbalance – standardkolonnetyper:**
    -   **ACCT** – Kontokoder
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **ATTR** – En attribut:
        -   Bilag
    -   **FD** – primosaldo - økonomiske data
    -   **FD** – Økonomiske data, der kun indeholder debiteringer
    -   **FD** – økonomiske data, der kun indeholder krediteringer
    -   **CALC** – Nettodifferencen
    -   **CALC** – Ultimosaldoen
-   **Årlig råbalanceoversigt – standard:**
    -   **ACCT** – Kontokoder
    -   **DESC** – En beskrivelse af rækkedefinitionen
    -   **ATTR** – En attribut
        -   Bilag
    -   **FD** – Primosaldoen for økonomiske data for indeværende år
    -   **FD** – Økonomiske data, der kun indeholder debiteringer for det indeværende år
    -   **FD** – Økonomiske data, der kun indeholder krediteringer for det indeværende år
    -   **CALC** – Nettodifferencen
    -   **CALC** – Ultimosaldoen
    -   **FD** – Økonomiske data, der kun indeholder debiteringer for sidste år
    -   **FD** – Økonomiske data, der kun indeholder krediteringer for sidste år

 

<a name="see-also"></a>Se også
--------

[Økonomirapportering](financial-reporting-getting-started.md)

[Vis økonomiske rapporter](view-financial-reports.md)

[Dynamics Financial Reporting-blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




