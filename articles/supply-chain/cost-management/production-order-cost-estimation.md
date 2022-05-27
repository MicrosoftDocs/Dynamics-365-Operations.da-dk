---
title: Forkalkulation af produktionsordre
description: Denne artikel indeholder oplysninger om produktionsforkalkulation. Forkalkulation af produktion giver dig oplysninger om de budgetterede omkostninger til materiale- og kapacitetsforbrug til fremstilling af en vare i det planlagte produktionsordreantal.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac658b49109a3fb3f987cf30bfa0b62bbff3d1c2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672256"
---
# <a name="production-order-cost-estimation"></a>Forkalkulation af produktionsordre

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om produktionsforkalkulation. Forkalkulation af produktion giver dig oplysninger om de budgetterede omkostninger til materiale- og kapacitetsforbrug til fremstilling af en vare i det planlagte produktionsordreantal. 

Når du opretter en produktionsordre, skal du forkalkulere produktionsomkostningerne. Formålet er at beregne vare- og ruteforbruget i produktionsprocessen, fordi disse forkalkulationer danner grundlaget for efterfølgende planlægnings- og produktionsprocesser.

## <a name="production-cost-estimation"></a>Forkalkulation af produktionsomkostninger
Forkalkulationer af produktionsomkostninger er baseret på følgende oplysninger:

-   Mængden i produktionsordren
-   Komponenterne på produktionsstyklisterne
-   Ruteplanlægningsoperationer i produktionsruten
-   De indirekte omkostninger, der gælder for komponenter og operationer
-   Aktive omkostningsdata pr. beregningsdatoen

Hvis der er en fantomlinjevare på produktionsstyklisterne, afspejler beregningerne fantomets komponenter og ruteoperationer. Du kan bruge forkalkuleringsopgaven til at genberegne forkalkulerede omkostninger, så de afspejler opdaterede oplysninger. De opdaterede oplysninger kan f.eks. være ændringer i mængden på produktionsordren, komponenterne på produktionsstyklisterne, ruteoperationerne i produktionsruten, de indirekte omkostninger, der gælder for disse komponenter og operationer, eller de aktive omkostningsdata pr. beregningsdatoen. I beregningen af forkalkulerede omkostninger foreslås også en salgspris for produktionsvaren baseret på en beregning af omkostninger plus avance. Beregningen af forkalkulerede omkostninger kan også gælde for referenceordrer, der afspejler andre produktionsordrer, som er knyttet til produktionsordren.

## <a name="view-the-estimated-costs"></a>Se de forkalkulerede omkostninger
Når du kører forkalkulationen, kan du se resultatet på siden **Prisberegning**. Forkalkulationen beregner følgende værdier:

-   **Produktionsomkostninger** – Produktionsomkostninger er den øverste linje i forkalkulationen. Den viser de samlede omkostninger til kørslen af produktionsordren og den samlede salgspris for produktionen. Det er summen af alle omkostningslinjer i forkalkulationen.
-   **Rute-eller ressourceomkostninger** – Rute-eller ressourceomkostninger er omkostninger for produktionsoperationerne. De omfatter omkostningen for elementer som opstillingstid, operationstid og indirekte omkostninger.
-   **Materialeomkostninger** – Materialeomkostninger er omkostningerne til og priserne på de styklistekomponenter, der skal bruges til at producere varen. De er fastlagt og indsat i systemet tidligere.

## <a name="other-uses-of-cost-estimation"></a>Andre formål med forkalkulationer
En forkalkulation giver dig også følgende oplysninger:

-   Brugbare pristilbud
-   Estimater af rentabiliteten af ordren
-   Estimater af råvareforbruget
-   Sammenligninger med omkostningsoplysninger fra tidligere produktioner
-   Budgetterings- og prognoseoplysninger
-   Forkalkulationer af den produktionsstørrelse, der kræves for at opretholde en bestemt omkostning.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]