---
title: " Definere bonuspoint for fordelskunde"
description: Denne procedure gennemgår definition af fordelskundebelønningspoint.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ae26123d41fa74d32b102ddb7f021e9846a676
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564310"
---
# <a name="define-loyalty-reward-points"></a> Definere bonuspoint for fordelskunde

[!include[task guide banner](../includes/task-guide-banner.md)]

Denne procedure gennemgår definition af fordelskundebelønningspoint. Du bør definere fordelskundebelønningspoint, før du konfigurerer et fordelskundeprogram. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Detail og handel > Kunder > Loyalitet > Fordelskundebelønningspoint.
2. Klik på Ny.
3. Indtast en værdi i feltet Belønningspoint-id.
4. Skriv en værdi i feltet Beskrivelse.
5. Vælg en indstilling i feltet Belønningspointtype.
    * Vælg antal, hvis belønningspointene skal afrundes til nærmeste heltal. Vælg Beløb, hvis belønningspointene skal afrundes i overensstemmelse med reglerne for valutaafrunding. Hvis du vælger Antal, kan du springe næste trin i denne procedure over.  
6. Skriv en værdi i feltet Valuta.
    * For belønningspoint af typen Beløb får alle udstedte point den valgte valuta. For belønningspoint af typen Antal gælder dette felt ikke. Spring dette trin over.  
7. Markér eller fjern markeringen af afkrydsningsfeltet Kan indløses.
8. Angiv et tal i feltet Indløs rangering.
    * Indløs rangering bruges, når to eller flere indløselige belønningspoint kan bruges til at betale for produkter. Hvis to belønningspoint har samme indløsningsrangering, anvendes det, der skal sænke antallet af point.  
9. Angiv et tal i feltet Værdi for udløbstidspunkt.
    * Belønningspoint udløber det angivne antal dage, måneder eller år efter, at pointene blev udstedt. En værdi på "0" betyder, at fordelskundebelønningspoint aldrig udløber.  
10. Vælg en indstilling i feltet Enhed for udløbstidspunkt.
11. Klik på Gem.

