---
title: OIOUBL-standarder til elektronisk fakturering
description: "Dette emne forklarer, hvilket niveau af dækning, vi har til elektronisk fakturering i Microsoft Dynamics 365 for operationer i det europæiske område."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10274
ms.assetid: 3f2a14b0-6580-40e4-a3dc-1d8a0f9201c1
ms.search.region: Austria, Denmark, Italy, Norway, Spain
ms.search.industry: Public sector
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 62dbea0dd573cb5715a68fea59c1c0512d6a8394
ms.lasthandoff: 03/31/2017


---

# <a name="oioubl-standards-for-electronic-invoicing"></a>OIOUBL-standarder til elektronisk fakturering

Dette emne forklarer, hvilket niveau af dækning, vi har til elektronisk fakturering i Microsoft Dynamics 365 for operationer i det europæiske område. 

Den [Europa-Kommissionen](http://ec.europa.eu/finance/payments/einvoicing/index_en.htm) beskriver elektronisk rapportering netværk i følgende ord: "– e-fakturering – elektronisk fakturering er elektronisk overførsel af faktureringsoplysninger (fakturering og betaling) mellem forretningspartnere (leverandøren og køberen). Det er en vigtig del af en effektiv finansielle forsyningskæde og det sammenkæder de interne processer i virksomheder med betalingssystemer." Gennemførelse og vedtagelsen af den Europæiske Union bredt elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), som har indflydelse på alle EU-medlemsstater. Virksomheder, der er villig til at tage fordelene ved elektronisk fakturering skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer salgsordre og projekt faktura kreditnotaer som .XML-filer til staten eller andre handel parter, der kræver anvendelse af elektronisk fakturering. Disse .XML-filer skal opfylde bestemte standarder. De landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](http://www.peppol.eu/peppol_elements/einvoicing) specifikationer og adgangspunkter til validering og transport. Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål. Da UBL er en fleksibel, internationale standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af landegrænser.

<a name="what-electronic-invoice-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hvilke elektronisk fakturaformater understøttes i øjeblikket i Dynamics 365 for operationer?
---------------------------------------------------------------------------------------

Dynamics 365 for operationer (1611 opdager) tilbyder gennemførelse af elektronisk fakturering er baseret på [elektronisk indberetning](/dynamics365/operations/dev-itpro/analytics/general-electronic-reporting). Der er en **kunde faktura model** datamodel og en række landespecifikke elektronisk indberetning formatere konfigurationer, der er oprettet for Østrig, Danmark, Italien, Norge og Spanien:
-   OIOUBL salg & projekt faktura (AT, DK, NO)
-   OIOUBL salg & projekt kreditnota (AT, DK, NO)
-   Salg & projektfaktura (ES)
-   Salg & projektfaktura (IT)

De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden. Valideringsregler anvendes i Microsoft Dynamics 365 for operationer, når fakturaer oprettes, så du kan kontrollere, at de korrekte oplysninger, der er angivet. Sæt af nødvendige oplysninger kan variere fra land til land. Krav som så godt som understøttede lande og formater, der kan ændres, skal du altid gå til den delte aktivbiblioteket på Microsoft Dynamics levetidsservices (LCS) og få vist den seneste liste over tilgængelige filer, som har et anlæg type **TYSK konfiguration**.

