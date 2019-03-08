---
title: Bestemme styklisteversionen
description: Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf125e2b75c4dfa406f4f05b249e6fdb49c84b7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "325083"
---
# <a name="determine-the-bom-version"></a>Bestemme styklisteversionen

[!include [banner](../includes/banner.md)]

Hvis en vare har standardordre af typen Produktion, finder planlægningssystemet en gyldig styklisteversion ud fra lokationen under en efterspørgselsudfoldning. 

Lokationsdimensionen kendes altid og er anført i efterspørgselsposteringen. Følgende proces bruges til fastlæggelse af den styklisteversion, der skal anvendes:

-   Hvis en styklisteversion er defineret for varen på efterspørgselslokationen, bruges den lokationsspecifikke stykliste.
-   Hvis der ikke er defineret en lokationsspecifik styklisteversion for en vare på efterspørgselslokationen, bruges der en generel stykliste. En generel stykliste angiver ikke en lokation og er gyldig for flere lokationer. Hvis der findes en generel stykliste, bruges den.
-   Hvis der ikke findes en generel stykliste, som kan bruges, standser efterspørgselsudfoldningen her.

En gyldig styklisteversion skal opfylde de krævede kriterier for dato og antal, uanset om den er lokationsspecifik eller generel.





