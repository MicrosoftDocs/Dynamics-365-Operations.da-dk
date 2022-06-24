---
title: Dimensioner for omkostningsobjekt
description: Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til. Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger. Denne artikel indeholder oplysninger om omkostningsobjektdimensioner.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ee481b9dafe202e0a850a31b6ab036d52a20547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874632"
---
# <a name="cost-object-dimensions"></a>Dimensioner for omkostningsobjekt

[!include [banner](../includes/banner.md)]

Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til. Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger. Denne artikel indeholder oplysninger om omkostningsobjektdimensioner.

Et omkostningsobjekt kan være en hvilken som helst type objekt, du vil vurdere, allokere omkostninger til eller måle direkte. Typiske omkostningsobjekter omfatter produkter, projekter, ressourcer, afdelinger, bærere og geografiske områder. Ledelsen bruger omkostningsobjekter til at kvantificere omkostninger og oprette rentabilitetsanalyser.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Omkostningsobjektdimensioner og omkostningsobjekters dimensionsmedlemmer
Omkostningsobjekter er kendt som *omkostningsobjektdimensioner*. Når du har besluttet, hvilkel enhed omkostningsobjektdimensionen skal referere til, skal du angive de enkelte dimensionsværdier eller importere dem til omkostningsregnskabet fra andre kildesystemer. De enkelte dimensionsværdier kaldes *omkostningsobjekters dimensionsmedlemmer*. For eksempel vil du bruge den økonomiske dimension, der hedder Bærer, som omkostningsobjektdimensionen. Hvis du vil se, hvordan omkostninger flyder til de enkelte bærer, skal du importere omkostningsobjektets dimensionsmedlemmer. I dette tilfælde er omkostningsobjektets dimensionsmedlemmer faktiske bærere som salg, produktion, administration og geografiske placeringer. Følgende skærmbillede vises et eksempel på bærere som omkostningsobjekdimension med dets faktiske bærere som dimensionsmedlemmer af omkostningsobjektet. 

[![Skærmbillede, der viser Bærer som omkostningsobjektdimension.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importere omkostningsobjekters dimensionsmedlemmer gennem dataconnectorer
For at gøre import af omkostningsobjekters dimensionsmedlemmer nemmere kan du bruge dataconnectorer til at hente værdierne fra de enheder, du vil bruge som omkostningsobjektdimensioner. Du kan bruge de færdigbyggede dataforbindelser eller tilpassede dataconnectorer, du bygger.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
