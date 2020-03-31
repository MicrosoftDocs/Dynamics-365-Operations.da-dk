---
title: Udvidet filtrering i RCS/Globalt lager
description: I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager, der er blevet forbedret, så det indeholder ekstra filtre.
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ed5a217b8844bfc76d53370ab4c4c339f5bece36
ms.sourcegitcommit: 0dcdfedec7125562f6b33deb009a3e044a1243eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2020
ms.locfileid: "3099861"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>Udvidede filtreringsindstillinger for søgning efter konfigurationer i det globale lager

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager (Regulatory Configuration Service), der er blevet forbedret, så det indeholder følgende filtre: 
- **Land/område** baseret på ISO-landekoder  
- **Koder** – for funktions/facilitetsområde; Branche; Forretningsdokumenttype 

Du kan anvende filtre, enten individuelt eller i grupper, til at finde bestemte eller relaterede konfigurationer. Hvis du f.eks. vil finde alle konfigurerbare forretningsdokumenter, der er relateret til kreditorfakturaer, kan du anvende filteret **Forretningsdokumenttype**. 

Du kan yderligere forfine en søgning ved at vælge landekoden og klikke på **Anvend filter**.  

[![Filtersektion for globalt lager](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Følgende eksempel viser resultaterne, når der filtreres efter **Forretningsdokumenttype**. 

[![Anvendte filter og import for forretningsdokumenttype](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrerede resultater kan importeres til brugeres RCS- eller Dynamics 365 Finance-miljø individuelt eller som sæt (ved at vælge gruppen af varianter) og klikke på **Importer**.





