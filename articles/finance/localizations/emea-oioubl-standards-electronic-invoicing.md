---
title: Understøttede standarder til elektronisk fakturering i Europa
description: Denne artikel beskriver det dækningsniveau, der findes for elektronisk fakturering for Europa.
author: mrolecki
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6bbd2acc879447bd7a5883abffdfe0582f6f7554
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906253"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Understøttede standarder til elektronisk fakturering i Europa

[!include [banner](../includes/banner.md)]

Denne artikel beskriver det dækningsniveau, der findes for elektronisk fakturering for Europa. 

Implementering og indførelse overalt i EU af elektronisk fakturering er reguleret [Rådets direktiv 2010/45/EU](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), hvilket har indflydelse på alle EU-medlemsstater. Virksomheder, der gerne vil have fordel af elektronisk fakturering, skal sende salgsordrefakturaer, fritekstfakturaer, projektfakturaer, kreditnotaer for salgsordre og kreditnotaer for projektfakturaer som .XML-filer til offentlige myndigheder eller andre handelspartnere, der bemyndiger anvendelse af elektronisk fakturering. Disse .XML-filer skal opfylde bestemte standarder. Landespecifikke krav og deres gennemførelse kan variere på tværs af EU-medlemsstaterne, men ofte bruger de Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) i forskellige versioner med tilpasninger samt [PEPPOL](https://www.peppol.eu)-specifikationer og adgangspunkter til validering og transport. Den primære fordel ved UBL er, at forretningsdokumenter kan standardiseres til forskellige formål. Da UBL er en fleksibel, international standard, der understøtter mange forretningsmæssige krav, kan disse forretningsdokumenter udveksles på tværs af nationale grænser.

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a>Elektroniske fakturaformater, der i øjeblikket er tilgængelige i Dynamics 365 Finance

Der findes følgende landespecifikke formater for elektroniske fakturaer:

-   OIOUBL-v.2.02 for Danmark
-   EHF v.3.0 for Norge
-   PEPPOL BIS v.2 for Østrig, Frankrig og Belgien
-   UBL-OHNL 1.9 for Nederlandene
-   FacturaE v.3.2.1 for Spanien
-   FatturaPA v.1.2 for Italien
-   xRechnung v.1.2 for Tyskland
-   Åbn PEPPOL BIS Billing v.3.0 for Den Europæiske Union
-   Estisk specifikt format version 1.2
-   Finvoice 3.0 for Finland

Elektronisk fakturering er baseret på [Elektronisk indberetning (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). Der er oprettet en **Fakturamodel**-datamodel, fakturamodeltilknytning og flere forskellige lande-/områdespecifikke formatkonfigurationer for følgende lande/områder: 

- Østrig (AT)
- Danmark (DK)
- Italien (IT)
- Norge (NO)
- Spanien (ES)
- Frankrig (FR)
- Belgien (BE)
- Nederlandene (NL)
- Tyskland (DE)
- Estland (EE)
- Finland (FI)
- Den Europæiske Union (EU)

**Fakturamodel**-datamodel, fakturamodel og lande-/områdespecifikke ER-formatkonfigurationer omfatter:

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
-   Salgsfaktura (EE)
-   Projektfaktura (EE)
-   Salgsfaktura (FI)
-   Projektfaktura (FI)

De elektroniske fakturaer og kreditnotaer, som du genererer, omfatter nødvendige oplysninger som et europæisk varenummer (EAN) og oplysninger om kontakt, dimensionskontonummer og adresse til kunden. Der anvendes valideringsregler, når der genereres fakturaer, så du kan kontrollere, at de korrekte oplysninger er angivet. Sættet af nødvendige oplysninger kan variere fra land til land. Da både kravene og de understøttede lande og formater kan blive ændret, bør du altid gå til det delte aktivbibliotek i Microsoft Dynamics Lifecycle Services (LCS) og få vist den seneste liste over tilgængelige filer, som har aktivtypen **GER-konfiguration**.

## <a name="electronic-invoice-configuration"></a>Konfiguration af elektronisk faktura
Opsætningen og de særlige oplysninger om elektroniske fakturaer afhænger af det land/område, som den er implementeret for. Du kan finde flere oplysninger om, hvordan du konfigurerer og bruger elektroniske debitorfakturaer, i de relaterede lande-/områdespecifikke emner:

- [Italien](emea-ita-e-invoices.md)
- [Norge](emea-nor-e-invoices.md)
- [Danmark](emea-dnk-e-invoices.md)
- [Tyskland](emea-deu-e-invoices.md)
- [Finland](https://support.microsoft.com/help/4559937)
- [Estland](https://support.microsoft.com/help/4552679)
- [PEPPOL](https://support.microsoft.com/help/4490320)

## <a name="additional-resources"></a>Yderligere ressourcer
Du kan få flere oplysninger om opsætning af elektroniske fakturaer ved at afspille følgende [opgaveguider](../../fin-ops-core/fin-ops/get-started/help-overview.md#task-guides) i ruden Hjælp:

 - Konfigurere elektronisk OIOUBL-fakturering
 - Importere OIOUBL elektroniske faktureringskonfigurationer
 - Konfigurere debitorkonti til elektronisk OIOUBL-fakturering

> [!NOTE] 
> Selvom disse opgaveguider er oprettet specifikt til det danske e-fakturaformat *OIOUBL*, gælder de også for andre understøttede lande/områder, med mindre afvigelser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
