---
title: Forbedret filtrering i RCS/Globalt lager
description: I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager, der er blevet forbedret, så det indeholder ekstra filtre.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 31df79159caa1094a68743ba07f308a2029e4071
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832638"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Forbedrede filtreringsindstillinger til søgning efter konfigurationer i RCS/det globale lager

[!include [banner](../includes/banner.md)]

I dette emne beskrives udvidede filtreringsmuligheder for det globale RCS-lager (Regulatory Configuration Service), der er blevet forbedret, så det giver mulighed for at filtrere med følgende kriterier: 
- **Land/område** - baseret på ISO-landekoder  
- **Kodetyper** for:
  - Funktionsområde
  - Funktionsområde
  - Branche 
  - Forretningsdokument 

Du kan anvende filtre, enten individuelt eller som gruppe, for at gøre det lettere at finde bestemte eller relaterede konfigurationer. Hvis du f.eks. vil finde en enkelt type af forretningsdokumenter, der kan konfigureres, med relation til kreditorfakturaer, kan du anvende et **Forretningsdokumenttype**-filter til at søge efter den pågældende dokumenttype. 

[![Filtersektion for globalt lager](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Du kan yderligere indsnævre søgningen ved at vælge dokumenttype, f.eks. 'kreditorfaktura', og klikke på **Anvend filter**. Følgende eksempel viser resultaterne, når du filtrerer efter **Forretningsdokumenttype** med tilføjet dokumenttype. 

[![Anvendte filter og import for forretningsdokumenttype](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrerede resultater kan importeres til en brugers RCS-lager eller et Dynamics 365 Finance-miljø, enten individuelt eller som et sæt. Det gør du ved at vælge gruppen af konfigurationer og klikke på **Importér**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]