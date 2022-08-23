---
title: " Definere bonuspoint for fordelskunde"
description: Denne procedure gennemgår definition af fordelskundebelønningspoint.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailLoyaltyRewardPoints
ms.openlocfilehash: 9acd1429d17393f19a5e059b90a48b0b103535d3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268886"
---
# <a name="define-loyalty-reward-points"></a> Definere bonuspoint for fordelskunde

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår definition af fordelskundebelønningspoint. Du bør definere fordelskundebelønningspoint, før du konfigurerer et fordelskundeprogram. Proceduren bruger USRT-demodatafirmaet.

1. Gå til Retail og Commerce > Kunder > Loyalitet > Fordelskundebelønningspoint.
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
