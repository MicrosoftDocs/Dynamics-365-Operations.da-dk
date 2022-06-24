---
title: Begrænse betalingsmetoder for returneringer uden kvittering
description: Denne artikel beskriver, hvordan der kan være begrænsede refusionsmuligheder for bestemte betalingstyper, hvis varerne returneres uden kvittering.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 091d39ea9fe41d78b7f34f85ecd1894047e022d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896947"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrænse betalingsmetoder for returneringer uden kvittering


[!include [banner](includes/banner.md)]

De enkelte betalingstyper, som en detailhandlende accepterer, skal konfigureres, når systemet konfigureres. Denne artikel beskriver, hvordan der kan være begrænsede refusionsmuligheder for bestemte betalingstyper, hvis varerne returneres uden kvittering.

## <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Når du vil konfigurere betalingsmetoder, skal følgende opgaver være fuldført.
1. Opret de betalingsmetoder, der accepteres af hele organisationen.
2. Oprettelse af korttyper og kortnumre i hele organisationen. Hvis der skal accepteres kredit- eller debetkort, skal du oprette én betalingsmetode for kort og derefter oprette korttyper og kortnumre, der gælder for hele organisationen.
3. Konfigurer betalingsmetoder for butikken. Tilknyt betalingsmetoder til de enkelte butikker, og angiv derefter butiksspecifikke indstillinger for de enkelte betalingsmetoder.
4. Konfigurer betalingsmetoder for butikker. For alle kortbetalingsmetoder, som butikken accepterer, skal du udføre kortopsætningen.

![Butiksopsætning.](media/NoReceiptReturns1.png "Konfiguration af Retail Store") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Begrænse betalingsmetoder for returneringer uden kvittering

For hver betalingsmetode i en butik skal du på siden **Butiksstyring** under **Returneringer uden kvittering** indstille **Begræns for returneringer uden kvittering** til **Ja**. 

Standardværdien for ja/nej-knappen er **Nej**, hvilket sikrer, at betalingsmetoden er tilladt for refusioner. 

Når **Begræns for returneringer uden kvittering** er indstillet til **Ja**, er den valgte betalingsmetode ikke tilladt for refusioner. 

![Gemme betalingsmetode.](media/NoReceiptReturns3.png "Betalingsmetode for Retail Store") 

> [!NOTE]
> Når en kasserer vælger en betalingsmåde, hvor der er begrænsede refusionsmuligheder uden kvittering, vises en meddelelse til kontrol af godkendte betalingsmetoder.

![Acceptable betalingsmetoder.](media/NoReceiptReturns4.png "Acceptable betalingsmetoder") 

Hvis en transaktion har både en returnering med kvittering og en returnering uden kvittering, gennemtvinges begrænsningsbetingelserne ikke, fordi transaktionen bliver en returneringsarbejdsgang med en kvittering. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]