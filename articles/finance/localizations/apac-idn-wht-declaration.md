---
title: A-skatterapport for Indonesien
description: Dette emne forklarer, hvordan du konfigurerer og genererer A-skatteopgørelse for Indonesien.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943655"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>A-skatterapport for Indonesien (ID-00005)

[!include [banner](../includes/banner.md)]

Dette emne indeholder en forklaring på, hvordan du konfigurerer og genererer den A-skattefil til PPH, som juridiske enheder i Indonesien bruger til at rapportere A-skatteposteringer i programmet e-Bupot.

Indonesiens skattemyndigheder (DGT) fastlægger, at momspligtige foretagender (PKP), der er registreret i KPP Pratama og tilbageholder/opkræver indkomstskat (PPh) Artikel 23 og/eller Artikel 26, elektronisk skal indberette indkomstskatteopgørelse Artikel 23 og 26 ved hjælp af programmet e-Bupot. 

- **Artikel 23** – Rapporten indeholder alle A-skatteposteringer fra leverandører, hvor lande-/områdekoden for den primære adresse er koden for Indonesien.
- **Artikel 26** – Rapporten indeholder alle A-skatteposteringer fra leverandører, hvor lande-/områdekoden for den primære adresse ikke er koden for Indonesien.

## <a name="prerequisites"></a>Forudsætninger

- Den primære adresse for den juridiske enhed være i Indonesien.
- I arbejdsområdet **Funktionsstyring** skal funktionen **Global A-skat** være aktiveret. Du kan finde flere oplysninger om aktivering af nye funktioner under [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="download-electronic-reporting-configurations"></a>Hent konfigurationer for elektronisk rapportering

Generering af en importfil er baseret på ER-konfigurationer (elektronisk rapportering). Du kan finde flere oplysninger om egenskaberne og koncepterne ved konfigurerbar rapportering under [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

I forbindelse med produktions- og brugeraccepttestmiljøer (UAT) skal du følge vejledningen i [Hent konfigurationer til elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere importfilen, skal du overføre følgende konfigurationer fra lageret:

- **Momsopgørelsesmodel.version.93.xml** eller senere version
- **Tilknytning til momsopgørelsesmodel.version.93.153.xml** eller senere version
- **WHT PPh-skemaimport (id).version.93.14** eller senere version

## <a name="set-up-general-ledger-parameters"></a>Konfigurer økonomiparametre

1. Gå til **Moms** \> **Konfiguration** \> **Finansparametre**.
2. Under fanen **A-skat** skal du i feltet **Formattilknytning af WHT-opgørelse** vælge **WHT PPh-skemaimport (id)**. 
3. Gå til **Moms** \> **Konfiguration** \> **A-skat** \> **A-skatteindtægtstyper** for at konfigurere **Kode Bukti Potong** som skatteindtsætningstype, og tildel derefter koderne til de relaterede A-skattegrupper for varer. Koderne skal bruges til generering af integrationsfilen ved hjælp af programmet e-Bupot. 

## <a name="generate-the-withholding-import-file"></a>Generere importfilen til A-skat

Processen til forberedelse og generering af e-Bupot-filen for en bestemt periode er baseret på de posteringer for A-skat, der er bogført under afstemning eller bogføring af skattebetalingsjobbet.

Benyt følgende fremgangsmåde for at oprette filen.

1. Gå til **Moms** \> **Erklæringer** \> **A-skat** \> **PPH-importfil e-bupot 23 og 26**.
2. Vælg rapportens "fra" dato og "til" dato, og vælg derefter afregningsperioden.
3. Angiv transaktionsdatoen, og vælg derefter **OK**.
4. Vælg sprog. Alle rapporter oversættes til amerikansk engelsk (**en-us**) og indonesisk (**id**).
5. Vælg forretningstypen, og angiv derefter check- og dokumentnumrene. 
6. Kontrollér, om rapporten er blevet signeret af lederen. Disse oplysninger rapporteres i filen. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
