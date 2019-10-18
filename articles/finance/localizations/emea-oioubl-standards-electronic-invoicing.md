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
ms.openlocfilehash: c1d1ec695626404389dec2b07dd6e34358cd2d5a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175698"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Understøttede standarder til elektronisk fakturering i Europa

[!include [banner](../includes/banner.md)]

I dette emne beskrives det dækningsniveau, der findes for elektronisk fakturering for Europa. 

Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater. Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering. Disse .XML-filer skal opfylde bestemte standarder. Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport. Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål. Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.

## <a name="what-electronic-invoice-formats-are-currently-available-in-dynamics-365-finance"></a>Hvilke elektroniske fakturaformater er i øjeblikket tilgængelige i Dynamics 365 Finance?

Der findes følgende landespecifikke formater for elektroniske fakturaer:

-   OIOUBL-v.2.02 for Danmark
-   EHF v.2.0.8 for Norge
-   PEPPOL BIS v.2 for Østrig, Frankrig og Belgien
-   UBL-OHNL 1.9 for Nederlandene
-   FacturaE v.3.2.1 for Spanien
-   FatturaPA v.1.2 for Italien

Elektronisk fakturering er baseret på [elektronisk indberetning](../../dev-itpro/analytics/general-electronic-reporting.md). Der er en **Debitorfakturamodel**-datamodel, og der er oprettet en række landespecifikke konfigurationer for elektroniske indberetningsformater for Østrig (AT), Danmark (DK), Italien (IT), Norge (NO), Spanien (ES), Frankrig (FR), Belgien (BE) Nederlandene (NL).

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

De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden. Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet. Sættet af nødvendige oplysninger kan variere fra land til land. Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.

## <a name="additional-information"></a>Yderligere oplysninger
Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-and-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:

 - Konfigurere elektronisk OIOUBL-fakturering
 - Importere OIOUBL elektroniske faktureringskonfigurationer
 - Konfigurere debitorkonti til elektronisk OIOUBL-fakturering

> [!NOTE] 
> Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande, med mindre afvigelser.
