---
title: Foretage fejlfinding af opsætning af likviditetsbudget
description: Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985281"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Foretage fejlfinding af opsætning af likviditetsbudget

[!include [banner](../includes/banner.md)]

Dette emne giver svar på spørgsmål, som du kan have, når du konfigurerer likviditetsbudgettering. Den løser ofte stillede spørgsmål om opsætningen af likviditet, opdateringer til likviditet og Power BI-pengestrøm.

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

Kontroller, at målingerne "Likviditetsmåleenhed V2" og "LedgerCovLiquidityMeasurement" fra en enhed er konfigureret. Du kan få flere oplysninger om, hvordan du arbejder med data i Enhedslager, under [Power BI-integration med enhedslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Bekræft, at alle trin til visning af Power BI-indhold er udført. Du kan finde flere oplysninger i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Er enhederne i enhedslageret blevet opdateret?

Du skal opdatere enhederne jævnligt for at sikre, at dataene er aktuelle og nøjagtige. Hvis du vil opdatere en bestemt enhed manuelt, skal du gå til **Systemadministration \> Opsætning \> Enhedslager** og vælge enheden og derefter vælge **Opdater**. Dataene kan også opdateres automatisk. På siden **Enhedslager** skal du indstille til **Automatisk opdatering aktiveret** til **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]