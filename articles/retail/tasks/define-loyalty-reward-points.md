--- 
title: " Definere bonuspoint for fordelskunde"
description: "Denne procedure gennemgår definition af fordelskundebelønningspoint."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05237a0ba3aa785432c8b1fc36284a47f9aabd4a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

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


