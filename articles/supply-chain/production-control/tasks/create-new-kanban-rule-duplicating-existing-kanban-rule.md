---
title: Oprette en ny kanban-regel ved at duplikere en eksisterende kanban-regel
description: Denne procedure fokuserer på oprettelse en dublet af en eksisterende kanban-regel.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149181"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>Oprette en ny kanban-regel ved at duplikere en eksisterende kanban-regel

[!include [banner](../../includes/banner.md)]

Denne procedure fokuserer på oprettelse en dublet af en eksisterende kanban-regel. Dette er nyttigt, hvis du vil oprette nye kanban-regler baseret på eksisterende kanban-regler. Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen til et nyt produktionsflow eller en ny genopfyldningsregel.


## <a name="select-a-kanban-rule"></a>Vælg en kanban-regel
1. Gå til kanban-regler.
2. Find og vælg den ønskede post på listen.
    * Vælg kanban-regel 000017 for Produkt M0006.  

## <a name="duplicate-a-kanban-rule"></a>Dupliker en kanban-regel
1. Klik på Dupliker kanban-regel.
    * Når du kopierer en kanban-regel, er det muligt at ændre type, datoer, aktiviteter og produktvalg. Skift produktet for denne procedure i næste trin.  
2. Indtast eller vælg en værdi i feltet Produkt.
    * Vælg M0007.  
3. Klik på OK.
    * Bemærk, at der oprettes en dublet af kanban-regel 000017.    

