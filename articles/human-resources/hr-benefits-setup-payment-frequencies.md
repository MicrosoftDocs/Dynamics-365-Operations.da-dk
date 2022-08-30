---
title: Konfigurere betalingshyppigheder
description: Microsoft Dynamics 365 Human Resources bruger betalingsfrekvenser til at beregne den årlige frynsegodeløn, bestemme det beløb for frynsegodepræmie, som medarbejderen betaler hver lønperiode, og hvor ofte udbyderne betales.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0472e2203cc20fcf0904d22778092721b4cbce41
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323922"
---
# <a name="set-up-payment-frequencies"></a>Konfigurere betalingshyppigheder


Microsoft Dynamics 365 Human Resources bruger betalingsfrekvenser til at beregne den årlige frynsegodeløn, bestemme det beløb for frynsegodepræmie, som medarbejderen betaler hver lønperiode, og hvor ofte udbyderne betales.

Betalingsfrekvenser for frynsegoder bruger omregningsfaktorer til at omregne frynsegodebetalingsperioder mellem betalingsfrekvenser, som kan være månedlige, halvmånedlige, for to uger, ugentlige og daglige. Det giver firmaer mulighed for at definere den interne afhængighed mellem betalingsfrekvenserne i frynsegodeplanen.

Felterne til omregningsfaktorer identificerer omregningsfaktoren fra betalingsfrekvensen til standardbetalingsperioderne og giver systemet mulighed for at foretage beregninger mellem betalingsfrekvenserne. Omregningsfaktorbeløbet bestemmer også beløbet for frynsegodepræmien, som en medarbejder skal betale pr. frekvens.

1. I arbejdsområdet **Frynsegodeadministration** skal du vælge **Betalingsfrekvenser** under **Konfiguration**.

2. Vælg **Ny**.

3. Angiv værdier for følgende felter:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Betalingshyppighed** | Det entydige navn på en betalingsfrekvens. |
   | **Beskrivelse** | En beskrivelse af betalingsfrekvensen. |
   | **Termin** | Den relevante periode, der passer bedst til frynsegodeudbyderens eller medarbejderens betalingsfrekvens. Periodelisten består af standardbetalingsperioderne. |
   | **Antal lønperioder** | Antallet af betalingsperioder, der angiver, hvor ofte frynsegodeudbyderen eller medarbejderne skal betales. Dette beløb bruges til at beregne medarbejderens årlige beløb for frynsegodeløn. |
   | **Årlig omregningsfaktor** | Den årlige omregningsfaktor for betalingsfrekvensen. Den årlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/1 år) = 12 |
   | **Halvårlig omregningsfaktor** | Den havlårlige omregningsfaktor for betalingsfrekvensen. Den halvårlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/2 gange om året) = 6 |
   | **Kvartalsvis omregningsfaktor** | Den kvartalsvise omregningsfaktor for betalingsfrekvensen. Den kvartalsvise omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/4 kvartaler) = 3 |
   | **Månedlig omregningsfaktor** | Den månedlige omregningsfaktor for betalingsfrekvensen. Den månedlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/12 måneder) = 1 |
   | **Halvmånedlig omregningsfaktor** | Den halvmånedlige omregningsfaktor for betalingsfrekvensen. Den halvmånedlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/24 (2 x en måned)) = 0,5 | 
   | **Omregningsfaktor for hver 14. dag** | Den årlige omregningsfaktor for betalingsfrekvensen. Den årlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/26 uger) = 0,461538 |
   | **Ugentlig omregningsfaktor** | Den årlige omregningsfaktor for betalingsfrekvensen. Den årlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/52 uger) = 0,230769 |
   | **Daglig omregningsfaktor** | Den årlige omregningsfaktor for betalingsfrekvensen. Den årlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/365 dage) = 0,032877 |
   | **Omregningsfaktor pr. time** | Den årlige omregningsfaktor for betalingsfrekvensen. Den årlige omregningsfaktor for den månedlige betalingsfrekvens er f.eks.: </br></br>(12 månedlige betalinger/2080 timer) = 0,005769

4. Vælg **Gem**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
