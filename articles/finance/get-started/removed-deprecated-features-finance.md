---
title: Fjernede eller udfasede funktioner i Dynamics 365 Finance
description: Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
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
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127971"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Fjernede eller udfasede funktioner i Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emne beskriver funktioner, der er blevet fjernet eller vil blive fjernet fra Dynamics 365 Finance.

- En *fjernet* funktion er ikke længere tilgængelige i produktet.
- En *forældet* funktion er ikke i aktiv udvikling og fjernes muligvis i en senere opdatering.

Denne liste er beregnet til at hjælpe dig med at overveje disse fjernelser og forældelser for din egen planlægning. 

> [!NOTE]
> Du kan finde detaljerede oplysninger om objekter i Finance and Operations-apps i [Technical Reference-rapporterne](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de forskellige versioner af disse rapporter for at få mere at vide om objekter, der er ændret eller fjernet i hver version af Finance and Operations-apps.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Fjernede eller udfasede funktioner i Finance 10.0.12 udgaven

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Polske SSRS-rapporter: registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister– funktionsreference PL-00014

|   |  |
|------------|--------------------|
| **Årsagen til forældelsen/fjernelsen** | Ikke juridisk krævet.  |
| **Erstattet af en anden funktion?**   | Ja (Excel-format til standardrevisionsfil med momsopgørelse – JPK_VDEK) |
| **Produktområder, der er berørt**         | Applikation |
| **Installationsindstilling**              | Alt |
| **Status**                         | Udfases: Fra og med d. 1. juli 2021 planlægger vi ikke længere at understøtte SSRS-rapporter: **Registrering af salgsmoms, registrering af købsmoms, EU-oversigt af momsregister – funktionsreference PL-00014**. Eksempel i Excel-format til standardrevisionsfil med momsopgørelse (JPK_VDEK) vil blive introduceret i stedet. |

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
