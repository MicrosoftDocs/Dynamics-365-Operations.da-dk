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
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bb190e720e5040d446d75a2e8c39cb360019d42
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256871"
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