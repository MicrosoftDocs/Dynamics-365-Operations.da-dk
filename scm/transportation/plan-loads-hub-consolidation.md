---
title: "Planlægge belastninger ved hjælp af hubkonsolidering"
description: "I denne artikel beskrives funktionen til konsolidering af leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når du modtager varer fra flere leverandører på det samme lagersted."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e0bd837a441a17e53982d5c5a7a7983f40e471c5
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="plan-loads-using-hub-consolidation"></a>Planlægge belastninger ved hjælp af hubkonsolidering

[!include[banner](../includes/banner.md)]


I denne artikel beskrives funktionen til konsolidering af leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når du modtager varer fra flere leverandører på det samme lagersted.

Det kan være nyttigt at konsolidere leverancer på en hub, når du leverer varer fra forskellige lagersteder til samme kunde, eller når varer leveres fra flere leverandører til det samme lagersted.

## <a name="building-loads"></a>Opbygning af belastninger
Før du kan bruge hubkonsolidering, skal du aktivere indstillingen **Planlægning i transit** på siden **Transportstyringsparametre**. Du skal også oprette hubberne, hvor konsolideringen skal finde sted. I følgende diagram vises et eksempel på hubkonsolidering. I dette tilfælde går salgsordrer fra forskellige lagersteder til den samme kunde. De grundlæggende belastninger oprettes ud fra salgsordrer på den sædvanlige måde ved hjælp af siden **Panelet Lastplanlægning**. Du kan konsolidere de to belastninger i en hub, før de leveres til kunden, ved på siden **Panelet Lastplanlægning** i feltet **Transport** at vælge **Hubkonsolidering**. Når du vælger den korrekte hub for hver belastning, har belastningerne hubben som "indleveringsdestination". Du får også to "Linjer i transportanmodning" i sektionen **Udbud og efterspørgsel** på siden **Panelet Lastplanlægning**. Du kan derefter tilføje disse to linjer til en ny belastning. Denne nye belastning har både salgsordrelinjer og får også hubben som "afhentningsadresse" og kunde A som "indleveringsdestination". De tre belastninger er derefter klar til at blive vurderet og sendt som andre belastninger. Du kan vælge den fragtmand, som systemet foreslår for hver belastning. [![Hubkonsolidering](./media/hubconsol.jpg)](./media/hubconsol.jpg) Du kan også bruge den samme metode til at konsolidere belastninger for flere flytteordrer. I dette tilfælde er kunde A i det foregående diagram et lagersted. Alternativt kan du konsolidere belastninger for flere indkøbsordrer, hvor belastningerne er leveret fra forskellige leverandører til det samme lagersted. Du kan have mere end én konsolideringshub, og du kan konsolidere i flere hubber for flere belastninger, der kommer fra forskellige lagersteder. Når du opbygger dine grundlæggende belastninger og bruger hubkonsolideringsindstillingen, kan du opbygge de nye belastninger ved hjælp af de konsoliderede transportanmodningslinjer. Derefter vurderer og lægge ruten for dine belastninger.




