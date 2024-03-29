---
title: Oversigt over planlægning af laster ved hjælp af hubkonsolidering
description: I denne artikel beskrives funktionen til konsolidering af leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når du modtager varer fra flere leverandører på det samme lagersted.
author: Weijiesa
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92273"
- intro-internal
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 055d7c53b771e09002c84c643c45d3da9f71aca0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676545"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Oversigt over planlægning af laster ved hjælp af hubkonsolidering

[!include [banner](../includes/banner.md)]

I denne artikel beskrives funktionen til konsolidering af leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når du modtager varer fra flere leverandører på det samme lagersted.

Det kan være nyttigt at konsolidere leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når varer leveres fra flere leverandører til det samme lagersted.

## <a name="building-loads"></a>Opbygning af belastninger
Før du kan bruge hubkonsolidering, skal du aktivere indstillingen **Planlægning i transit** på siden **Transportstyringsparametre**. Du skal også oprette hubberne, hvor konsolideringen skal finde sted. I følgende diagram vises et eksempel på hubkonsolidering. I dette tilfælde går salgsordrer fra forskellige lagersteder til den samme kunde. De grundlæggende belastninger oprettes ud fra salgsordrer på den sædvanlige måde ved hjælp af siden **Panelet Lastplanlægning**. Du kan konsolidere de to belastninger i en hub, før de leveres til kunden, ved på siden **Panelet Lastplanlægning** i feltet **Transport** at vælge **Hubkonsolidering**. Når du vælger den korrekte hub for hver belastning, har belastningerne hubben som "indleveringsdestination". Du får også to "Linjer i transportanmodning" i sektionen **Udbud og efterspørgsel** på siden **Panelet Lastplanlægning**. Du kan derefter tilføje disse to linjer til en ny belastning. Denne nye belastning har både salgsordrelinjer og får også hubben som "afhentningsadresse" og kunde A som "indleveringsdestination". De tre belastninger er derefter klar til at blive vurderet og sendt som andre belastninger. Du kan vælge den fragtmand, som systemet foreslår for hver belastning. [![Hubkonsolidering.](./media/hubconsol.jpg)](./media/hubconsol.jpg) Du kan også bruge den samme metode til at konsolidere belastninger for flere flytteordrer. I dette tilfælde er kunde A i det foregående diagram et lagersted. Alternativt kan du konsolidere belastninger for flere indkøbsordrer, hvor belastningerne er leveret fra forskellige leverandører til det samme lagersted. Du kan have mere end én konsolideringshub, og du kan konsolidere i flere hubber for flere belastninger, der kommer fra forskellige lagersteder. Når du opbygger dine grundlæggende belastninger og bruger hubkonsolideringsindstillingen, kan du opbygge de nye belastninger ved hjælp af de konsoliderede transportanmodningslinjer. Derefter vurderer og lægge ruten for dine belastninger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]