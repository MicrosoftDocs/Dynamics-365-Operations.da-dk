---
title: Fjernede eller udfasede funktioner i Dynamics 365 Finance
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.
author: kfend
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6df84e5c2d530e708560495bceaeb23e2ee0dd4b
ms.sourcegitcommit: acac5e59be7c8f4e9a7ae9be58c636c70342e784
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/23/2022
ms.locfileid: "8466828"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Fjernede eller udfasede funktioner i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finans- og driftsapps i [Technical Reference-rapporterne](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finans- og driftsapps.

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

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER-opgørelse for Tyskland (design baseret på rapporteringskoder)

[Momsopgørelse](../localizations/emea-de-vat-declaration.md)</br>
[Konfigurere elektronisk momsopgørelse for Tyskland](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Elektronisk overførsel for momsangivelse (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Tyskland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Den 1. december 2022 planlægger vi ikke længere at understøtte ER-formaterne (elektronisk rapportering) **Elster (DE)** og **Elster-model**. Der introduceres nye formater for **Momsopgørelse (DE)** og **Momsopgørelse Excel (DE)** under modellen **Momsopgørelse**. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>OB-opgørelse for Nederlandene (design baseret på rapporteringskoder)

[OB-opgørelse](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af et nyt momsopgørelsesdesign, [momsopgørelse for Nederlandene](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Den 1. december 2022 planlægger vi ikke længere at understøtte ER-formatet (elektronisk rapportering) **OB-opgørelse (NL)** og **OB-opgørelsesmodel**. Der introduceres nye formater for **Momsopgørelse (NL)** og **Momsopgørelse Excel (NL)** under modellen **Momsopgørelse**. |

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
