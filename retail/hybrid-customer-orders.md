---
title: Hybride kundeordrer
description: "En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2bc0a8e59075b25ca48b09c1145820a2a604950e
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="hybrid-customer-orders"></a>Hybride kundeordrer

[!include[banner](includes/banner.md)]


En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan sælges ud af butikken af kunden, samt produkter, der skal afhentes eller sendes senere.

I Microsoft Dynamics 365 for Operations - Retail kan du vælge enten at udføre alle produkter eller udføre udvalgte produkter for en kunde. De produktlinjer, der er markeret til udførelse, faktureres automatisk, efter at ordren er oprettet. På samme måde er dette det samme for en ordre, der skal afhentes, efter at ordren er oprettet. Det skyldige beløb på hybrid ordrer bestemmes ved at tilføje indbetalingsprocenten på plukning og forsendelsesproduktlinjer med det fulde beløb for udførelseslinjerne. For hybride ordrer skifter systemet mellem kundeordretilstanden og cash og carry-tilstand på følgende måde:

-   Hvis alle produkter i indkøbskurven er indstillet til **Udfør levering**, håndteres ordren som en postering af typen cash og carry.
-   Hvis nogle af eller alle linjer i kurven er indstillet til enten **Pluk** eller **Send levering**, skal ordren behandles som en debitorordretransaktion.

Hvis der er valgt en indkøbskurvlinje og **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er markeret, angives kun den specifikke indkøbskurvlinje med denne leveringsmetode. I så fald fortsætter downstreamflowet af handlingen som sædvanligt. Men hvis **Pluk markerede**, **Afsendelse valgt** eller **Udfør valgte** er valgt, uden at der er valgt en indkøbskurvlinje, åbnes en ny side, der viser alle indkøbskurvlinjerne. På dette skærmbillede kan du vælge flere linjer på en gang for at angive leveringsmetoden. Når du bruger denne metode til at markere linjer, tilsidesættes alle tidligere leveringsmetoder, der er knyttet til linjen.

<a name="see-also"></a>Se også
--------

[Oversigt over kundeordrer](customer-orders-overview.md)




