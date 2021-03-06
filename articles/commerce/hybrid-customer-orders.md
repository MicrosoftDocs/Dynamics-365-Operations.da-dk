---
title: Hybride kundeordrer
description: En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6357c034059523f83ba05a1da53cae691ef74758
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798931"
---
# <a name="hybrid-customer-orders"></a>Hybride kundeordrer

[!include [banner](includes/banner.md)]

En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere.

I Commerce kan du vælge enten at udføre alle produkter eller udføre udvalgte produkter for en kunde. De produktlinjer, der er markeret til udførelse, faktureres automatisk, efter at ordren er oprettet. På samme måde er dette det samme for en ordre, der skal afhentes, efter at ordren er oprettet. Det skyldige beløb på hybrid ordrer bestemmes ved at tilføje indbetalingsprocenten på plukning og forsendelsesproduktlinjer med det fulde beløb for udførelseslinjerne. For hybride ordrer skifter systemet mellem kundeordretilstanden og cash og carry-tilstand på følgende måde:

- Hvis alle produkter i indkøbskurven er indstillet til **Udfør levering**, håndteres ordren som en postering af typen cash og carry.
- Hvis nogle af eller alle linjer i kurven er indstillet til enten **Pluk** eller **Send levering**, skal ordren behandles som en debitorordretransaktion.

Hvis der er valgt en indkøbskurvlinje og **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er markeret, angives kun den specifikke indkøbskurvlinje med denne leveringsmetode. I så fald fortsætter downstreamflowet af handlingen som sædvanligt. Men hvis **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er valgt, uden at der er valgt en indkøbskurvlinje, åbnes en ny side, der viser alle indkøbskurvlinjerne. På dette skærmbillede kan du vælge flere linjer på en gang for at angive leveringsmetoden. Når du bruger denne metode til at markere linjer, tilsidesættes alle tidligere leveringsmetoder, der er knyttet til linjen.

## <a name="additional-resources"></a>Yderligere ressourcer

[Kundeordrer i Modern POS (MPOS)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]