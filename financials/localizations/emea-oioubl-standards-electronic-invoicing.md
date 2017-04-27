---
title: OIOUBL-standarder til elektronisk fakturering
description: "Dette emne forklarer, hvilket niveau af dækning vi har til elektronisk fakturering i Microsoft Dynamics 365 for Operations i det europæiske område."
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

[!include[banner](../includes/banner.md)]


Dette emne forklarer, hvilket niveau af dækning vi har til elektronisk fakturering i Microsoft Dynamics 365 for Operations i det europæiske område. 

[Europa-Kommissionen](http://ec.europa.eu/finance/payments/einvoicing/index_en.htm) beskriver elektronisk rapporteringsnetværk med følgende ord: "Elektronisk fakturering – e-fakturering – er elektronisk overførsel af faktureringsoplysninger (fakturering og betaling) mellem forretningspartnere (leverandøren og køberen). Det er en vigtig del af en effektiv økonomiforsyningskæde, og det sammenkæder de interne processer i virksomheder med betalingssystemer." Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater. Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering. Disse .XML-filer skal opfylde bestemte standarder. Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](http://www.peppol.eu/peppol_elements/einvoicing)-specifikationer og adgangspunkter til validering og transport. Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål. Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.

<a name="what-electronic-invoice-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Hvilke formater for elektroniske fakturaer understøttes i øjeblikket i Dynamics 365 for Operations?
---------------------------------------------------------------------------------------

Dynamics 365 for Operations (1611) tilbyder gennemførelse af elektronisk fakturering baseret på [elektronisk indberetning](/dynamics365/operations/dev-itpro/analytics/general-electronic-reporting). Der er en **Debitorfakturamodel**-datamodel, og der er oprettet en række landespecifikke konfigurationer for elektroniske indberetningsformater for Østrig, Danmark, Italien, Norge og Spanien:
-   OIOUBL salgs- og projektfaktura (AT, DK, NO)
-   OIOUBL salgs- og projektkreditnota (AT, DK, NO)
-   Salgs- og projektfaktura (ES)
-   Salgs- og projektfaktura (IT)

De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden. I Microsoft Dynamics 365 for Operations anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet. Sættet af nødvendige oplysninger kan variere fra land til land. Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.



