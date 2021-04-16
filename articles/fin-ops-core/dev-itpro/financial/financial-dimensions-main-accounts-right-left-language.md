---
title: Økonomiske dimensioner og hovedkonti på højre mod venstre-sprog
description: I dette emne beskrives nogle beslutninger, du skal overveje, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 508f4ed4de367770acddc77a6ff5e7e36fd20729
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748131"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Økonomiske dimensioner og hovedkonti på højre mod venstre-sprog

[!include [banner](../includes/banner.md)]

I dette emne beskrives nogle af de implementeringsbeslutninger, der skal overvejes, når du bruger et højre mod venstre-sprog, og du skal oprette økonomiske dimensioner og hovedkonti.

Økonomiske dimensioner og hovedkonti er centrale komponenter i planlægningsfasen for en implementering. Når økonomiske dimensioner og hovedkonti oprettes i systemet, bruges de på siderne **Konfigurer kontostrukturer**, **Avancerede regelstrukturer** og **Konfiguration af økonomisk dimension til integrering af programmer**. Den rækkefølge, der er defineret på siderne, bruges til dataindtastning og forbrug i systemet. Nogle steder i systemet vises de økonomiske dimensioner og hovedkonti i separate felter. På andre steder, såsom kladder, økonomiske dimensioner og hovedkonti, vises de som en enkelt streng.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Bedste fremgangsmåder til at oprette økonomiske dimensioner og hovedkonti i et højre mod venstre-system

- Når du vælger afgrænsningstegn til kontoplaner, kan du vælge en af indstillingerne for dobbelt afgrænser: dobbelt bindestreg (`--`), dobbeltstreg (`||`) eller dobbelt punktum (`..`) eller dobbelt et understregningstegn (`\\`).
- Når du opretter en økonomisk dimension og hovedkontoværdier, skal du kun bruge tal og tegn fra højre mod venstre-sprog.
- Undgå at bruge den valgte kontoplans afgrænser i den økonomiske dimension og hovedkontoværdier.

Ved at følge disse anbefalinger kan du bedre sikre ensartet repræsentation af den brugerdefinerede rækkefølge i hele systemet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]