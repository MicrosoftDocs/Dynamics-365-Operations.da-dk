---
title: Deaktivere regler i konsistenskontrol af detailtransaktioner
description: Dette emne beskriver funktionen til deaktivering af regler i konsistenskontrol af detailtransaktion Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586291"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Deaktivere regler i konsistenskontrol af detailtransaktioner 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Detailhandlere kan have forretningsscenarier og -processer, der er specifikke for dem. Derfor gælder alle de regler, der som standard er inkluderet i konsistenskontrollen af detailtransaktioner, ikke for alle detailforretninger. For at sørge for tilpasning til forskellige situationer, indeholder Microsoft Dynamics 365 Retail funktionalitet, der kan bruges til at deaktivere de regler, der ikke er relevante.

Hvis du vil have vist en liste over de regler, der er tilgængelige i konsistenskontrollen af detailtransaktioner i dit miljø, og have vist status for hver regel, skal du gå til **Retail \> Konfiguration af hovedkontor \> Parametre \> Detailparametre** og vælge fanen **Transaktionsvalidering**.

Status for alle regler angives som standard til **Aktiveret**. Derfor bruges alle reglerne til at validere detailtransaktioner, før de trækkes ind i detailopgørelserne. Hvis du vil deaktivere en regel, skal du ændre dens status til **Deaktiveret**. Deaktiverede regler tages ikke i betragtning, når detailtransaktioner valideres under beregningsprocessen for opgørelsen.

Hvis du vil springe hele valideringsprocessen over, uanset hvilke regler der er aktiveret, skal du gå til **Retail \> Konfiguration af hovedkontor \> Parametre \> Detailparametre** og derefter under fanen **Transaktionsvalidering** angive indstillingen **Deaktiver konsistenskontrol for detailtransaktioner** til **Ja**. Når denne indstilling er angivet til **Nej**, kan den ikke indstilles tilbage til **Ja** fra brugergrænsefladen.
