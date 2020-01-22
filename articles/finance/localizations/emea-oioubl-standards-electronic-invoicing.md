---
title: Understøttede standarder til elektronisk fakturering i Europa
description: I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2fb188498705dcbad841645ced43e6a1715cbbd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915160"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Understøttede standarder til elektronisk fakturering i Europa

[!include [banner](../includes/banner.md)]

I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa. 

Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater. Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering. Disse .XML-filer skal opfylde bestemte standarder. Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport. Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål. Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a>Hvilke elektroniske fakturaformater er i øjeblikket tilgængelige i Dynamics 365 Finance?

Der findes følgende landespecifikke formater for elektroniske fakturaer:

-   OIOUBL-v.2.02 for Danmark
-   EHF v.3.0 for Norge
-   PEPPOL BIS v.2 for Østrig, Frankrig og Belgien
-   UBL-OHNL 1.9 for Nederlandene
-   FacturaE v.3.2.1 for Spanien
-   FatturaPA v.1.2 for Italien
-   xRechnung v.1.2 for Tyskland
-   Åbn PEPPOL BIS Billing v.3.0 for Den Europæiske Union

Elektronisk fakturering er baseret på [Elektronisk indberetning (ER)](../../dev-itpro/analytics/general-electronic-reporting.md). Der er blevet oprettet en **Debitorfakturamodel**-datamodel og adskillige lande-/regionspecifikke ER-formatkonfigurationer for Østrig (AT), Danmark (DK), Italien (IT), Norge (NO), Spanien (ES), Frankrig (FR), Belgien (BE), Nederlandene (NL) og Tyskland (DE) samt Den Europæiske Union (EU).

-   OIOUBL salgsfaktura - for AT, DK og NO
-   OIOUBL salgskreditnota - for AT, DK og NO
-   OIOUBL projektfaktura - for AT, DK og NO
-   OIOUBL projektkreditnota - for AT, DK og NO
-   UBL-salgsfaktura FR
-   UBL-salgskreditnota FR
-   UBL-projektfaktura FR
-   UBL-projektkreditnota FR
-   UBL-salgsfaktura BE
-   UBL-salgskreditnota BE
-   UBL-projektfaktura BE
-   UBL-projektkreditnota BE
-   UBL-salgsfaktura NL
-   UBL-salgskreditnota NL
-   UBL-projektfaktura NL
-   UBL-projektkreditnota NL 
-   Salgsfaktura (ES)
-   Salgsfaktura (IT)
-   Projektfaktura (ES)
-   Projektfaktura (IT)
-   Salgsfaktura DE
-   Projektfaktura DE
-   Peppol Salgsfaktura - for EU
-   Peppol Salgskreditnota - for EU
-   Peppol Projektfaktura - for EU
-   Peppol Projektkreditnota - for EU

De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden. Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet. Sættet af nødvendige oplysninger kan variere fra land til land. Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.

## <a name="additional-information"></a>Yderligere oplysninger
Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:

 - Konfigurere elektronisk OIOUBL-fakturering
 - Importere OIOUBL elektroniske faktureringskonfigurationer
 - Konfigurere debitorkonti til elektronisk OIOUBL-fakturering

> [!NOTE] 
> Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande, med mindre afvigelser.
