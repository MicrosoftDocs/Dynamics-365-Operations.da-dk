---
title: Projektsalgsordrer
description: Dette emne beskriver, hvordan du opretter projektbaserede salgsordre for tids- og materialeprojekter.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/12/2019
ms.locfileid: "976640"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektsalgsordre for tids- og materialeprojekter

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dette emne beskriver, hvordan du opretter en ny salgsordre for et projekt. Salgsordre kan alene oprettes for projekter af typen **tid og materiale**.

Hvis et tids- og materialeprojekt har flere finansieringskilder i projektkontrakten, skal du slå parametret **Tillad salgsordre for projekter med flere finansieringskilder** til på siden **Projektstyring og regnskabsparametre**. 

> [!NOTE]
> - Understøttelse til projektsalgsordre med flere finansieringskilder bliver tilgængelig i forbindelse med programfrigivelse 10.0.2 og senere versioner.
> - Parametret for at aktivere understøttelse af projektsalgsordre med flere finansieringskilder bliver fjernet i forbindelse med frigivelsesbølgen i april 2020, hvorefter funktionen altid vil være slået til.

Du kan oprette projektbaserede salgsordre på to måder:

- Gå til selve projektet. I handlingsruden skal du på vælge **Administrer > Opgaveelementer > Salgsordre**. Projektoplysningerne er angivet i henhold til standarderne for projektets salgsordre. Hvis projektkontrakten har mere end én finansieringskilde, skal du vælge finansieringskilden for at konfigurere kunden til salgsordren. Hvis projektet alene har én finansieringskilde, bliver kunden automatisk konfigureret.
- Gå til listesiden **Alle salgsordrer**, og opret en ny salgsordre. Du skal vælge projektet for slagsordren. Når du har valgt projektet, bliver kunden konfigureret på grundlag af finansieringskilden, ellers, hvis projektkontrakten har flere finansieringskilder, skal du vælge finansieringskilden.

