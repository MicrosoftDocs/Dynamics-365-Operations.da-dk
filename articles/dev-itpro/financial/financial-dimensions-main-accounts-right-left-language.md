---
title: "Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog"
description: "I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: e28d3b318c2efa0b9d0da1154692f8e64c553e64
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog

[!include[banner](../includes/banner.md)]


I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti.

Økonomiske dimensioner og hovedkonti er centrale komponenter i planlægningsfasen for en implementering. Når økonomiske dimensioner og hovedkonti oprettes i systemet, bruges de på siderne **Konfigurer kontostrukturer**, **Avancerede regelstrukturer** og **Konfiguration af økonomisk dimension til integrering af programmer**. Den rækkefølge, der er defineret på siderne, bruges til dataindtastning og forbrug i systemet. Nogle steder i systemet vises de økonomiske dimensioner og hovedkonti i separate felter. Men på andre steder, såsom kladder, økonomiske dimensioner og hovedkonti, vises de som en enkelt streng.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Bedste fremgangsmåder til at oprette økonomiske dimensioner og hovedkonti i et højre mod venstre-system

-   Når du vælger afgrænsningstegn til kontoplaner, kan du vælge en af indstillingerne for dobbelt afgrænser: dobbelt bindestreg (--), dobbeltstreg (||) eller dobbelt punktum (..) eller dobbelt et understregningstegn (\_\_).
-   Når du opretter en økonomisk dimension og hovedkontoværdier, skal du kun bruge tal og tegn fra højre mod venstre-sprog.
-   Undgå at bruge den valgte kontoplans afgrænser i den økonomiske dimension og hovedkontoværdier.

Ved at følge disse anbefalinger kan du bedre sikre ensartet repræsentation af den brugerdefinerede rækkefølge i hele systemet.



