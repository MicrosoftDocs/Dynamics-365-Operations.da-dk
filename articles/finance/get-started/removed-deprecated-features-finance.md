---
title: Fjernede eller udfasede funktioner i Dynamics 365 Finance
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a406db6d78302fa05596a58fffb7464222d4bfea
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689488"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Fjernede eller udfasede funktioner i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.16 udgaven

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Eksportformat for finanspost (BE)" Elektronisk rapporteringsformat og tilsvarende "finanspost for eksport (BE)" model for Belgien

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet med nyt ER-format under "standardrevisionsfil (SAF-T)"-modellen.  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet: Pr. 1. december 2021 planlægger vi ikke længere at understøtte "Finanspostens eksportformat (BE)" Elektronisk rapporteringsformat (ER) og de tilhørende "Eksport af finanstransaktioner (standard)". Et nyt format af typen "Dataeksport i Finans (standard)" sammen med "Tilknytning af finansdatamodel" introduceres i stedet for modellen "Standardrevisionsfilen (SAF-T)". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>"moms 100"-rapport the Storbritannien i SSRS-format

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Erstattet af det nye ER-format – "momsopgørelse Excel (UK)" under "momsopgørelsesmodel".  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Forældet: Pr. 1. december 2021 planlægger vi ikke længere at understøtte "Moms 100-rapporten" i SSRS-format. Der blev introduceret et nyt format "momsopgørelses Excel (UK)" under "momsopgørelsesmodel" i [MTD Momsfunktionen](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.15 udgaven

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-understøttelse af Dynamics 365 udfases

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Microsoft Internet Explorer 11-understøttelsen af alle Dynamics 365-produkter udfases fra december 2020, og Internet Explorer 11 understøttes ikke efter august 2021.<br><br>Dette vil påvirke kunder, der bruger Dynamics 365-produkter, som er udviklet til brug via en Internet Explorer 11-grænseflade. Efter august 2021 er Internet Explorer 11 ikke understøttet for sådanne Dynamics 365-produkter. |
| **Erstattet af en anden funktion?**   | Vi anbefaler, at kunderne overgår til Microsoft Edge.|
| **Produktområder, der er berørt**         | Alle Dynamics 365-produkter |
| **Installationsindstilling**              | Alt|
| **Status**                         | Forældet. Internet Explorer 11 understøttes ikke efter august 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.12 udgaven

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Polske SSRS-rapporter: registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister– funktionsreference PL-00014

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ikke juridisk krævet.  |
| **Erstattet af en anden funktion?**   | Ja (Excel-format til standardrevisionsfil med momsopgørelse – JPK_VDEK) |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Fra og med d. 1. juli 2021 planlægger vi ikke længere at understøtte SSRS-rapporter: **Registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister – funktionsreference PL-00014**. Eksempel i Excel-format til standardrevisionsfil med momsopgørelse (JPK_VDEK) vil blive introduceret i stedet. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.11 udgaven

### <a name="norwegian-standard-main-accounts"></a>Norske standardhovedkonti

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Omdesign  |
| **Erstattet af en anden funktion?**   | Ja (erstattet af programspecifikke parametre for ER-format) |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Fra og med d. 1. april 2021 planlægger vi ikke længere at understøtte funktionalitet, der er relateret til standardhovedkonti: Referencefelt, relateret tabel, dataobjekt. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.7 udgaven

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Ændring af anmodning om arbejdsgang indeholder ikke længere rullelisten Brugervalg
|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ændret til funktionen med valg af kontogrupper.  |
| **Erstattet af en anden funktion?**   | Ja |
| **Produktområder, der er berørt**         | Arbejdsgang |
| **Installationsindstilling**              | Alt |
| **Status**                         | Frarådes: Pr. 1. december 2020 planlægger vi ikke længere at understøtte opsætning af kinesiske bilagstyper uden valg af kontogrupper. Få flere oplysninger om den nye design i [Nyheder i 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere meddelelser om fjernede eller udfasede funktioner
Hvis du vil vide mere om funktioner, der er blevet fjernet eller udfaset i tidligere versioner, kan du se [Fjernede eller udfasede funktioner i tidligere versioner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
