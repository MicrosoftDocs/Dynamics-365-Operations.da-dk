---
title: Oprette en kanban-regel til erstatning
description: Denne procedure drejer sig om at erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de048577ac372474b72728d7774e3159a159afc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221817"
---
# <a name="create-a-replacement-kanban-rule"></a>Oprette en kanban-regel til erstatning

[!include [banner](../../includes/banner.md)]

Denne procedure drejer sig om at erstatte en eksisterende kanban-regel med en ny kanban-regel på en bestemt dato. Dette er nyttigt, når ændringer af produktionsflow eller genopfyldningregler skal koordineres og planlægges. Det demodatafirma, der bruges til at oprette proceduren, er USMF. Denne procedure er beregnet til procesingeniøren eller værdistrømlederen, når de forbereder produktionen til et nyt produktionsflow eller en ny genopfyldningsregel. Denne opgave erstatter kanban-regel 000022 med en ny regel og øger det maksimale antal fra 48 til 100 for den nye regel.


## <a name="select-a-kanban-rule-to-replace"></a>Vælg den kanban-regel, der skal erstattes.
1. Gå til kanban-regler.
2. Find og vælg den ønskede post på listen.
    * Vælg kanban-reglen 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Oprette en kanban-regel til erstatning
1. Klik på Erstat kanban-regel.
2. Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.
    * Vælg en dato i fremtiden, f.eks. en uge fra nu. Dette er den dato og det klokkeslæt, hvor den nye kanban-regel bliver aktiv og erstatter den gamle kanban-regel.  
    * Hvis kanban-reglen får en anden sti i produktionsflowet, kan du vælge en anden aktivitet.  I denne procedure bevarer vi aktiviteten.  
3. Klik på OK.
    * Bemærk, at der oprettes en ny kanban-regel som erstatning for kanban-regel 000022.  
    * Ikrafttrædelsesdatoen angives i overensstemmelse med den valgte dato, når du udskifter kanban-reglen.  
4. Find og vælg den ønskede post på listen.
    * Vælg den erstattede kanban-regel 000022.  
    * Bemærk, at den erstattede kanban-regel har samme dato som udløbsdatoen, fordi det er den dato, hvor den udløber.  
5. Markér række 1 på listen.
    * Vælg den nye kanban-regel øverst på listen. Dette er den kanban-regel, der har det højeste nummer.  
6. Klik op linket i den valgte række på listen.
    * Klik på kanban-regelnummeret for at åbne kanban-reglen.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Ændre maksimumantallet for udskiftning af kanban-regel
1. Angiv Maksimumantal til '100'.
    * Udvid oversigtspanelet Antal for at få vist feltet Maksimalt antal. Hvis du ændrer det maksimale antal til 100, bliver det muligt at behandle op til 100 kanbans.    Dette er det sidste trin i denne opgave.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]