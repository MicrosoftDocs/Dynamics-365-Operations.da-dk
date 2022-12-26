---
title: Fjernede eller udfasede funktioner i Dynamics 365 Finance
description: Denne artikel beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 25d13aa26565e5753b87c843b43cf46f8276b642
ms.sourcegitcommit: 6c05bcd27e6ee72f01cb66e2cfd1e929e0365830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/16/2022
ms.locfileid: "9854073"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Fjernede eller udfasede funktioner i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Denne artikel beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i programmer til finans og drift i [Technical Reference-rapporterne](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af programmer til finans og drift.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.31 udgaven

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>EDIFACT PAYMUL-konfiguration (AT) under Betalingsmodel

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt format, der er baseret på ISO 20022 pain.001.001.09. | 
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfaset: Banker i Østrig vil udfase EDICFACT-PAYMUL for betalinger ved grænsebetalinger senest i november 2022 og vil erstatte den med XML-version pain.001.001.09N. Der er tilføjet en ny konfiguration under det globale konfigurationslager, som giver brugerne mulighed for at fuldføre betalingsanmodningen, der går ud på tværs af grænser. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.30 udgaven

### <a name="revenue-recognition"></a>Indtægtsføring

[Indtægtsføring](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsagen til forældelsen/fjernelsen** |Erstattet af forbedret funktionalitet, [Abonnementsfakturering](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt** | Applikation |
| **Installationsindstilling** | Alt |
| **Status** | Udfaset: Efter april 2023 understøttes funktionen Indtægtsføring i Dynamics 365 Finance ikke længere med modtagelse af programrettelser. Kunderne bliver bedt om at bruge den forbedrede funktion, [Fakturering af abonnement](../../finance/accounts-receivable/subscription-billing-summary.md). I oktober 2023 er funktionen Indtægtsføring ikke længere tilgængelig. Kunderne bliver bedt om at bruge den forbedrede funktionalitet, Fakturering af abonnement. Til bundtfunktionen som en del af indtægtsføring er der ikke planlagt nogen erstatningsfunktionalitet på dette tidspunkt.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.29 udgaven

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Overføre lagerbeholdningsordrer, der har moms på overførselsprisen

[Overføre lagerbeholdningsordrer, der har moms på overførselsprisen](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af forbedret funktionalitet, [Ordrer til overførsler af lagerbeholdning for Indien](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt** | Applikation |
| **Installationsindstilling** | Alt |
| **Status** | Udfases: Efter april 2023 understøttes funktionen **Flytteordrer til lagerbeholdning, der har moms på flytteprisen** ikke længere med rettelser og sikkerhedsrettelser. Kunderne bliver bedt om at bruge den forbedrede funktion, [Ordrer til overførsler af lagerbeholdning for Indien](../../finance/localizations/apac-ind-stock-transfer.md). Efter oktober 2023 vil funktionen **Flytteordrer til lagerbeholdning, der har moms på flytteprisen** ikke længere være tilgængelig, og kunderne vil blive bedt om at gå til den forbedrede funktion. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Import og eksport af bankkontoudtog for positiv lønfil

| &nbsp;  | &nbsp;  |
|---|---|
| **Årsagen til forældelsen/fjernelsen** |Erstattes af forbedret funktionalitet, importer bankkontoudtog, og eksporter positive lønfiler.| 
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådet: XSLT-funktionalitet til import og eksport af filer vil ikke længere få understøttelse af rettelser og sikkerhedsrettelser. Kunderne bliver bedt om at bruge den forbedrede funktion: [Opret positive betalingsfiler ved at bruge elektronisk rapportering](../../finance/accounts-payable/set-up-positive-pay-er.md) og [Konfigurere avanceret import af bankafstemning ved hjælp af elektronisk rapportering](../../finance/accounts-payable/import-bai2-er.md). Efter september 2022 vil XSLT-funktionen ikke længere være tilgængelig, og kunderne vil blive bedt om at flytte til den forbedrede funktionalitet.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.26 udgaven

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Momsrapport for Finland (design baseret på rapporteringskoder)

[Momsrapport for Finland](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Finland](../localizations/emea-fin-vat-declaration.md). |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Den 1. marts 2023 har vi planer om ikke længere at understøtte momsrapporten for Finland (finsk rapportlayout). Der introduceres nye ER-formater (elektronisk rapportering) for **Momsopgørelsestekst (FI**) og **Momsopgørelse Excel (FI)** under modellen **Momsopgørelse**. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.24 udgaven

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Momsrapport for Sverige (design baseret på rapporteringskoder)

[Momsrapport for Sverige](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Sverige](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Den 1. december 2022 planlægger vi ikke længere at understøtte momsrapporten for Sverige (svensk rapportlayout). Der introduceres nye ER-formater (elektronisk rapportering) for **Momsopgørelse (SE**) og **Momsopgørelse Excel (SE)** under modellen **Momsopgørelse**. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Momsopgørelse for Østrig (design baseret på rapporteringskoder)

[Momsopgørelsesoplysninger for Østrig](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Østrig](../localizations/emea-aut-vat-declaration-austria.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Den 1. december 2022 planlægger vi ikke længere at understøtte ER-formatet (elektronisk rapportering) **Momsopgørelse (AT)** under **Momsopgørelsesmodel**. Der introduceres nye formater for **Momsopgørelse (AT)** og **Momsopgørelse Excel (AT)** under modellen **Momsopgørelse**. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes-electronic-tax-declaration-log-menu-item-and-page-electronic-tax-declaration-setup-menu-item-and-page-german-report-layout-taxreport_de-ssrs-format"></a>ELSTER-opgørelse for Tyskland (design baseret på rapporteringskoder), \"Log over elektronisk momsopgørelse\" menupunkt og side \"Konfiguration af elektronisk momsopgørelse\" menupunkt og side til opsætning af elektronisk momsopgørelse, tysk rapportlayout (TaxReport_DE) SSRS-format

[Momsopgørelse](../localizations/emea-de-vat-declaration.md)</br>
[Konfigurere elektronisk momsopgørelse for Tyskland](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Tyskland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alle |
| **Status**                         | Udfases: den 1. december 2022 planlægger vi ikke længere at understøtte ER-formaterne (elektronisk rapportering) **Elster (DE)** og **Elster-model**. Der introduceres nye ER-formater for **Momsopgørelse (DE)** og **Momsopgørelse Excel (DE)** under modellen **Momsopgørelse**. Vi understøtter heller ikke længere menupunktet og -siden til **Moms** \> **Opgørelser** \> **Salgsmoms** \> menupunktet **Log over elektronisk momsopgørelse** menupunktet **Moms** \> **Opsætning** \> **Salgsmoms** \> **Konfiguration af elektronisk momsopgørelse** og siden **Moms** \> **Opsætning** \> **Salgsmoms** \> **Elektroniske momscertifikater** menupunktet og siden samt det tyske rapportlayout (TaxReport\_DE) SQL Server Reporting Services (SSRS). Processen til momsrapportering i Tyskland understøttes i funktionen [Elektronisk meddelelse](../general-ledger/electronic-messaging.md). Yderligere oplysninger finder du i [momsopgørelsen for Tyskland](../localizations/emea-deu-vat-declaration-germany.md). |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes-electronic-ob-declaration-menu-item-and-page-dutch-report-layout-taxreport_nl-ssrs-format"></a>OB-opgørelse for Holland (design baseret på rapporteringskoder), menupunktet og siden \"Elektronisk OB-opgørelse\", hollandsk rapportlayout (TaxReport_NL) SSRS-format

[OB-opgørelse](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Nederlandene](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alle |
| **Status**                         | Udfases: Den 1. december 2022 planlægger vi ikke længere at understøtte ER-formatet (elektronisk rapportering) **OB-opgørelse (NL)** og **OB-opgørelsesmodel**. Der introduceres nye ER-formater for **Momsopgørelse (NL)** og **Momsopgørelse Excel (NL)** under modellen **Momsopgørelse**. Vi vil heller ikke længere understøtte menupunktet og -siden **Moms** \> **Erklæringer** \> **Salgsmoms** \> **Electronisk OB-erklæring** samt det hollandske rapportlayout (TaxReport_NL) SSRS-format. Processen til momsrapportering i Holland understøttes i funktionen [Elektronisk meddelelse](../general-ledger/electronic-messaging.md). Yderligere oplysninger finder du i [momsopgørelsen for Holland](../localizations/emea-nl-vat-declaration-netherlands.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.20 udgaven

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>ER-formatkonfiguration af "RTIR-forespørgsel på anmodning om fakturadata (HU)"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Udelukket fra elektronisk behandling af meddelelse om kommunikationsproces med det ungarske online faktureringssystem |
| **Erstattet af en anden funktion?**   | Nej |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Senest den 15. april 2022 har vi planer om ikke længere at understøtte formatkonfigurationen af "RTIR-forespørgsel på anmodning om fakturadata (HU)". |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"Fransk FEC-revisionsfil" – Elektronisk rapporteringsformat (ER) for Frankrig under formatet "Tysk revisionsfiloutput"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af det nye format "FEC-revisionsfil (FR)" |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Pr. 1. maj 2022 planlægger vi ikke længere at understøtte "Fransk FEC-revisionsfil" – Elektronisk rapportering (ER)-format for Frankrig under formatet "Tysk revisionsfiloutput". Der introduceres et nyt format for FEC-revisionsfilen (FR) i stedet for under "Dataeksportmodellen". |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.17 udgaven

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-lager som en mulighed for lagring af konfigurationer til elektronisk rapportering

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af det nye globale RCS-lager (Regulatory Configuration Service) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Dynamics 365 Finance, Supply Chain Management og Project Operations-produkter|
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfaset: Den 1. april 2022 planlægger vi ikke længere at understøtte Microsoft Dynamics Lifecycle Services-lageret (LCS) som en lagringsindstilling for elektronisk rapportering (ER-konfigurationer). Nye Microsoft ER-konfigurationer udgives udelukkende til download fra Global-lager. Der er adgang til det globale lager fra Dynamics 365-produkterne og RCS. Du kan finde flere oplysninger i [Importere ER-konfigurationer fra RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) og [Regulatory Configuration Service – Lifecycle Services-lagerudfasning](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.16 udgaven

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>"Momsopgørelse (CZ)" og "Kontrolopgørelseseksport (CZ)" Elektronisk rapporteringsformater for Tjekkiet

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af nye formater |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådet: Senest den 22. januar 2022 planlægger vi ikke længere at understøtte "momsopgørelse", "Kontrolopgørelseseksport (CZ)" Elektronisk rapportering (ER) formater. Der introduceres nye XML-formater for momsopgørelse (CZ), Momsopgørelse Excel (CZ), momsopgørelse XML (CZ)-formater introduceres i stedet i henhold til "Momsopgørelsesmodellen". |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Eksportformat for finanspost (BE)" Elektronisk rapporteringsformat og tilsvarende "finanspost for eksport (BE)" model for Belgien

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet med nyt ER-format under "standardrevisionsfil (SAF-T)"-modellen.  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet: Pr. 1. december 2021 planlægger vi ikke længere at understøtte "Finanspostens eksportformat (BE)" Elektronisk rapporteringsformat (ER) og de tilhørende "Eksport af finanstransaktioner (standard)". Et nyt format af typen "Dataeksport i Finans (standard)" sammen med "Tilknytning af finansdatamodel" introduceres i stedet for modellen "Standardrevisionsfilen (SAF-T)". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>"moms 100"-rapport the Storbritannien i SSRS-format

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af det nye ER-format – "momsopgørelse Excel (UK)" under "momsopgørelsesmodel".  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet: Pr. 1. december 2021 planlægger vi ikke længere at understøtte "Moms 100-rapporten" i SSRS-format. Der blev introduceret et nyt format "momsopgørelses Excel (UK)" under "momsopgørelsesmodel" i [MTD Momsfunktionen](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.15 udgaven

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-understøttelse af Dynamics 365 udfases

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Internet Explorer 11-understøttelsen af alle Dynamics 365-produkter udfases fra december 2020, og Internet Explorer 11 understøttes ikke efter august 2021.<br><br>Dette vil påvirke kunder, der bruger Dynamics 365-produkter, som er udviklet til brug via en Internet Explorer 11-grænseflade. Efter august 2021 er Internet Explorer 11 ikke understøttet for sådanne Dynamics 365-produkter. |
| **Erstattet af en anden funktion?**   | Vi anbefaler, at kunderne overgår til Microsoft Edge.|
| **Produktområder, der er berørt**         | Alle Dynamics 365-produkter |
| **Installationsindstilling**              | Alt|
| **Status**                         | Forældet. Internet Explorer 11 understøttes ikke efter august 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.12 udgaven

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Ikke udfaset: Polske SSRS-rapporter: Momsregister, Købsmomsregister, EU-oversigt over momsregister– funktionsreference PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ikke juridisk krævet.  |
| **Erstattet af en anden funktion?**   | Ja (Excel-format til standardrevisionsfil med momsopgørelse – JPK_VDEK) |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Ikke udfaset: Fra d. 27. juli 2021 planlægger vi ikke længere at understøtte SSRS-rapporter: **Momsregister, Købsmomsregister, EU-oversigt over momsregister – funktionsreference PL-00014**. Eksempel i Excel-format på standardrevisionsfil med momsopgørelse (JPK_VDEK) er også blevet introduceret. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.11 udgaven

### <a name="norwegian-standard-main-accounts"></a>Norske standardhovedkonti

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Omdesign  |
| **Erstattet af en anden funktion?**   | Ja (erstattet af programspecifikke parametre for ER-format) |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Fra og med d. 1. april 2021 planlægger vi ikke længere at understøtte funktionalitet, der er relateret til standardhovedkonti: Referencefelt, relateret tabel, dataobjekt. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.7 udgaven

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ændret til funktionen med valg af kontogrupper.  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Arbejdsgang |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Pr. 1. december 2020 planlægger vi ikke længere at understøtte opsætning af kinesiske bilagstyper uden valg af kontogrupper. Få flere oplysninger om den nye design i [Nyheder i 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

