---
title: Dimensioner for omkostningsobjekt
description: "Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til. Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger. Dette emne indeholder oplysninger om omkostningsobjektdimensioner."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 87c13e268ab8825e06095d24e03694cf0f271a63
ms.openlocfilehash: 6029fbc070c3d476bb0918b60f43c8c33e8e0bc6
ms.lasthandoff: 03/31/2017


---

# <a name="cost-object-dimensions"></a>Dimensioner for omkostningsobjekt

Når du analyserer omkostninger, kan du bruge omkostningselementdimensioner til at bestemme, hvor omkostningerne skal flyde til. Du kan bruge omkostningsobjektdimensioner til at bestemme, hvor du skal tildele omkostninger. Dette emne indeholder oplysninger om omkostningsobjektdimensioner.

Et omkostningsobjekt kan være en hvilken som helst type objekt, du vil vurdere, allokere omkostninger til eller måle direkte. Typiske omkostningsobjekter omfatter produkter, projekter, ressourcer, afdelinger, bærere og geografiske områder. Ledelsen bruger omkostningsobjekter til at kvantificere omkostninger og oprette rentabilitetsanalyser.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Omkostningsobjektdimensioner og omkostningsobjekters dimensionsmedlemmer
Omkostningsobjekter er kendt som *omkostningsobjektdimensioner*. Når du har besluttet, hvilkel enhed omkostningsobjektdimensionen skal referere til, skal du angive de enkelte dimensionsværdier eller importere dem til omkostningsregnskabet fra andre kildesystemer. De enkelte dimensionsværdier kaldes *omkostningsobjekters dimensionsmedlemmer*. For eksempel vil du bruge den økonomiske dimension, der hedder Bærer, som omkostningsobjektdimensionen. Hvis du vil se, hvordan omkostninger flyder til de enkelte bærer, skal du importere omkostningsobjektets dimensionsmedlemmer. I dette tilfælde er omkostningsobjektets dimensionsmedlemmer faktiske bærere som salg, produktion, administration og geografiske placeringer. Følgende skærmbillede vises et eksempel på bærere som omkostningsobjekdimension med dets faktiske bærere som dimensionsmedlemmer af omkostningsobjektet. 

[![omkostninger-objekt-dimensioner](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Importere omkostningsobjekters dimensionsmedlemmer gennem dataforbindelser
For at gøre import af omkostningsobjekters dimensionsmedlemmer nemmere kan du bruge dataforbindelser til at hente værdierne fra de enheder, du vil bruge som omkostningsobjektdimensioner. Du kan bruge de færdigbyggede dataforbindelser eller tilpassede dataforbindelser, du bygger.

