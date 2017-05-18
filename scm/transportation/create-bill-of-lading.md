---
title: Opret en fragtseddel
description: "I dette emne beskrives det, hvordan du opretter en fragtseddel, når du bruger lagerstyringsprocesser."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2a0ce07dab60b8ad660008cd77fbeadbf652224e
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="create-a-bill-of-lading"></a>Opret en fragtseddel

[!include[banner](../includes/banner.md)]


I dette emne beskrives det, hvordan du opretter en fragtseddel, når du bruger lagerstyringsprocesser.  

En fragtseddel er et juridisk dokument mellem den virksomhed, der leverer varerne, og transportvirksomheden. Dokumentet ledsager de leverede varer, og den fungerer som en kvittering for levering, når varerne leveres til destinationen. Hvis du bruger lagerstyring, er der to metoder til at generere en fragtseddel:

  -   Opret rapporten manuelt ved hjælp af siden **Fragtseddel**.
  -   Generér rapporten fra **Panelet lastplanlægning**.

Hvis du genererer fragtsedlen fra **Panelet lastplanlægning**, skal laststatus være **Leveret.** Hvis der er mere end én leverance i belastningen, oprettes en fragtseddel for hver leverance. Når en fragtseddel er blevet oprettet, du kan foretage ændringer af den på siden **Fragtseddel**.

## <a name="master-bill-of-lading"></a>Hovedfragtseddel
Hvis der er mere end en levering i lasten, kan du generere en hovedfragtseddel. Den har samme layout og oplysninger som en fragtseddel, men indeholder det opsummerede indhold for alle leverancer. Hvis indstillingen **Opret en hovedfragtseddel, når der er mere end én leverance i en last** er angivet til **Ja** på siden **Transportstyringsparametre**, genereres der automatisk en hovedfragtseddel, hvis du opretter en fragtseddel fra **Panelet lastplanlægning**, og der er mere end én leverance. Du kan også få en oversigt over fragtsedlerne ved at klikke på **Relaterede oplysninger** &gt; **Fragtseddel**. Hvis du vil oprette fragtsedler manuelt, kan du oprette en hovedfragtseddel på siden **Fragtseddel**.




