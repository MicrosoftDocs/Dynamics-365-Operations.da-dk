---
title: Deaktivere regler i konsistenskontrol af detailtransaktioner
description: Dette emne beskriver funktionen til deaktivering af regler i konsistenskontrol af transaktion i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: ce2abe7e15773edc3122a1bfdf40f3b830e8790e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792889"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Deaktivere regler i konsistenskontrol af detailtransaktioner 

[!include [banner](../includes/banner.md)]

Detailhandlere kan have forretningsscenarier og -processer, der er specifikke for dem. Derfor gælder alle de regler, der som standard er inkluderet i konsistenskontrollen af handelstransaktioner, ikke for alle detailforretninger. For at sørge for tilpasning til forskellige situationer, indeholder Microsoft Dynamics 365 Commerce funktionalitet, der kan bruges til at deaktivere de regler, der ikke er relevante.

Hvis du vil have vist en liste over de regler, der er tilgængelige i konsistenskontrollen af transaktioner i dit miljø, og have vist status for hver regel, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** og vælge fanen **Transaktionsvalidering**.

Status for alle regler angives som standard til **Aktiveret**. Derfor bruges alle reglerne til at validere transaktioner, før de trækkes ind i handelsopgørelserne. Hvis du vil deaktivere en regel, skal du ændre dens status til **Deaktiveret**. Deaktiverede regler tages ikke i betragtning, når transaktioner valideres under beregningsprocessen for opgørelsen.

Hvis du vil springe hele valideringsprocessen over, uanset hvilke regler der er aktiveret, skal du gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Commerce-parametre** og derefter under fanen **Transaktionsvalidering** angive indstillingen **Deaktiver konsistenskontrol for Commerce-transaktioner** til **Ja**. Når denne indstilling er angivet til **Nej**, kan den ikke indstilles tilbage til **Ja** fra brugergrænsefladen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]