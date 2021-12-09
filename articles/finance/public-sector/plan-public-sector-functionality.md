---
title: Planlægge funktioner til den offentlige sektor
description: I dette emne foreslås de første trin i opsætningen af funktioner til den offentlige sektor.
author: v-kiarnd
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 19851
ms.assetid: 877eabf3-19c7-4897-b33e-c5a8a319cb35
ms.search.region: Global
ms.search.industry: Public sector
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e90a9c3ae020e8e55323a5e78da1a97e7860c1f
ms.sourcegitcommit: 52a6b038d42ab28092bb942c61f5196330db3a7b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2021
ms.locfileid: "7817761"
---
# <a name="plan-for-public-sector-functionality"></a>Planlægge funktioner til den offentlige sektor

[!include [banner](../includes/banner.md)]

I dette emne foreslås de første trin i opsætningen af funktioner til den offentlige sektor.

## <a name="what-should-i-do-first"></a>Hvad skal jeg først gøre?

Før du konfigurerer den offentlige sektor og begynder at tilføje dine data, bør du overveje, hvordan du vil bruge denne funktion. Din overvejelse skal identificere de moduler, der skal være indstillet til at bruge funktioner i den offentlige sektor. Den offentlige sektor integreres med følgende områder i Dynamics 365 Finance. 

### <a name="accounts-payable"></a>Kreditor

Forside til betalingsrapporten Indkøbsordrelinjebeløb

### <a name="accounts-receivable"></a>Debitor

- Faktureringsklassifikationer
- Brugerdefinerede felter for faktureringskode
- Faktureringskoder
- Brugerdefinerede felter for fritekstfakturalinjer
- Handelspartnerkoder

### <a name="budgeting"></a>Budgetlægning

- Budgetanalyse
- Budgetanalyse for reviderede budgetter
- Budgetanalyse for faktiske udgifter
- Budgetanalyse for behæftelser
- Budgetanalyse for budgetreservationer

### <a name="french-regulatory-options"></a>Indstillinger for franske myndighedskrav

**Bemærk!** Du kan finde oplysninger om indstillinger for franske myndighedskrav i [Kontering for den offentlige sektor i Frankrig](../localizations/emea-fra-public-sector-accounting.md). Følgende sider er kun tilgængelige, hvis følgende betingelser er opfyldt:

- Konfigurationsnøglen **Offentlig sektor** er valgt.
- Konfigurationsundernøglen **Franske myndighedskrav** er valgt.
- Indstillingen **Brug konteringsreglerne for den franske offentlige sektor** er valgt på siden **Budgetparametre**.

- Saldooversigt
- Tilsagn lukket
- Vedligehold mandats de paiement
- Vedligehold titres de recette
- Købsaftale, afdelingsadgang
- Forbrugsgrænser for købsaftalegrænser efter kategori
- Hold-historik for kreditorfakturabetaling

### <a name="general-ledger"></a>Finans

- Avancerede finansposter
- Tilknyt afledte økonomiske hierarkier
- Afledte økonomiske hierarkier
- Filtrer resultattyper
- Finansieringskilder
- Gennemse ultimofinanstransaktioner

### <a name="procurement-and-sourcing"></a>Indkøb og forsyning

- Certificeringstype
- Bekræfter IO-koder
- Beløb på indkøbsordrelinjer

## <a name="additional-resources"></a>Yderligere ressourcer

[Startside for offentlig sektor](public-sector-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
