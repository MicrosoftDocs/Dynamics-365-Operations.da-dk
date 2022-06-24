---
title: Foretage fejlfinding af opsætning af likviditetsbudget
description: Denne artikel giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0e3438bc07fde28d5d9d2d5b3d83bbe70692c0bd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878064"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Foretage fejlfinding af opsætning af likviditetsbudget

[!include [banner](../includes/banner.md)]

Denne artikel giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Hvorfor vises der kun likviditet for én juridisk enhed?

Likviditetsbudgettering konfigureres og beregnes pr. juridisk enhed. Power BI-rapporterne og funktionen til likviditetsbudgetter i Finance Insights viser resultaterne.

Der skal oprettes likviditetsbudget for hver juridisk enhed, du vil have vist et budget for. Gennemse konfigurationen af likviditetsbudgettering i alle de juridiske enheder. Alternativt kan du gennemse konfigurationen af alle juridiske enheder til likviditetsbudgettering og sikre dig, at de er indstillet efter behov.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Hvorfor vises alle Power BI-likviditetsdata ikke?

Der er flere trin, der skal udføres, før likviditetsbudgetter kan vises i Power BI-visninger. Gennemse følgende checkliste, og kontroller, at alle trin er udført:

- Konfigurer likviditet for hver juridisk enhed.
- Angiv systemvalutaen og systemvalutakurstypen i økonomiparametrene.
- Angiv finansregnskabsvalutaen og valutakurstypen.
- Angiv valutakurser mellem transaktionsvalutaen og regnskabsvalutaen.
- Angiv valutakurser mellem regnskabsvalutaen og systemvalutaen.
- Angiv valutakurser mellem regnskabsvalutaen og hver bankvaluta.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Hvorfor blev Power BI-likviditetsarbejdet i tidligere versioner, men det er nu tomt?

Kontroller, at målingerne "Likviditetsmåleenhed V2" og "LedgerCovLiquidityMeasurement" fra en enhed er konfigureret. Du kan finde flere oplysninger om, hvordan du arbejder med data i enhedslager, i [Power BI-integration med enhedslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Kontrollér, at alle trin, der kræves for at se Power BI-indhold, er fuldført. Du kan finde flere oplysninger i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Er enhederne i enhedslageret blevet opdateret?

Du skal opdatere enhederne jævnligt for at sikre, at dataene er aktuelle og nøjagtige. Hvis du vil opdatere en bestemt enhed manuelt, skal du gå til **Systemadministration \> Opsætning \> Enhedslager** og vælge enheden og derefter vælge **Opdater**. Dataene kan også opdateres automatisk. På siden **Enhedslager** skal du indstille til **Automatisk opdatering aktiveret** til **Ja**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Hvilken beregningsmetode skal bruges ved beregning af likviditetsbudgetter?

Beregningsmetoden likviditetsbudget har to vigtige valgmuligheder. Indstillingen **Ny** beregner likviditetsbudgetter for nye dokumenter og dokumenter, der er ændret, siden det seneste batchjob blev kørt. Denne indstilling betyder, at det køres hurtigere, fordi den behandler et mindre undersæt af dokumenterne. Indstillingen **Total** genberegner likviditetsbudgetter for hvert dokument i systemet. Denne indstilling tager længere tid, fordi der er mere arbejde at udføre.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Hvordan forbedrer jeg ydeevnen for det batchjob, der gentages ved likviditetsbudgettering?

Det anbefales, at du kører likviditetsbudgettet én gang om dagen på de mindst belastede tidspunkter ved hjælp af beregningsmetoden **Ny**. Det anbefales at bruge denne fremgangsmåde seks dage om ugen. Kør derefter et likviditetsbudget én gang om ugen med brug af metoden **Total** på dagen med mindst aktivitet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

