---
title: "Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog"
description: "I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog i Microsoft Dynamics 365 for Operations, og du skal oprette økonomiske dimensioner og hovedkonti."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0a2fcbbc91960e0602f42d89ca5e46b8d51f98d6
ms.openlocfilehash: da5c53ddf113daf19a9832cf59f7a231a00b3367
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Økonomiske dimensioner og hovedkonti på et højre mod venstre-sprog

I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog i Microsoft Dynamics 365 for Operations, og du skal oprette økonomiske dimensioner og hovedkonti.

Økonomiske dimensioner og hovedkonti er centrale komponenter i planlægningsfasen for en implementering. Når økonomiske dimensioner og hovedkonti oprettes i systemet, bruges de på siderne **Konfigurer kontostrukturer**, **Avancerede regelstrukturer** og **Konfiguration af økonomisk dimension til integrering af programmer**. Den rækkefølge, der er defineret på siderne, bruges til dataindtastning og forbrug i systemet. Nogle steder i systemet vises de økonomiske dimensioner og hovedkonti i separate felter. Men på andre steder, såsom kladder, økonomiske dimensioner og hovedkonti, vises de som en enkelt streng.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Bedste fremgangsmåder til at oprette økonomiske dimensioner og hovedkonti i et højre mod venstre-system

-   Når du vælger afgrænsningstegn til kontoplaner, kan du vælge en af indstillingerne for dobbelt afgrænser: dobbelt bindestreg (-), dobbeltstreg (|) eller dobbelt punktum (.) eller dobbelt understregning (\_\_).
-   Når du opretter en økonomisk dimension og hovedkontoværdier, skal du kun bruge tal og tegn fra højre mod venstre-sprog.
-   Undgå at bruge den valgte kontoplans afgrænser i den økonomiske dimension og hovedkontoværdier.

Ved at følge disse anbefalinger kan du bedre sikre ensartet repræsentation af den brugerdefinerede rækkefølge i hele systemet.

