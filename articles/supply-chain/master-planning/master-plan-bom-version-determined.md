---
title: Bestemme styklisteversionen
description: "Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e6745a52138e545b557fa1aa286cd49481b2ecd
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="determine-the-bom-version"></a>Bestemme styklisteversionen

[!include[banner](../includes/banner.md)]


Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning. 

Lokationsdimensionen kendes altid og er anført i efterspørgselsposteringen. Følgende proces bruges til fastlæggelse af den styklisteversion, der skal anvendes:

-   Hvis en styklisteversion er defineret for varen på efterspørgselslokationen, bruges den lokationsspecifikke stykliste.
-   Hvis der ikke er defineret en lokationsspecifik styklisteversion for en vare på efterspørgselslokationen, bruges der en generel stykliste. En generel stykliste angiver ikke en lokation og er gyldig for flere lokationer. Hvis der findes en generel stykliste, bruges den.
-   Hvis der ikke findes en generel stykliste, som kan bruges, standser efterspørgselsudfoldningen her.

En gyldig styklisteversion skal opfylde de krævede kriterier for dato og antal, uanset om den er lokationsspecifik eller generel.






