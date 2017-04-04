---
title: Hybrid kundeordrer
description: "En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan udføres på lageret af kunden, samt produkter, der skal afhentes eller sendes senere."
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid kundeordrer

En hybrid kundeordre er en enkelt ordre, der indeholder produkter, der kan udføres på lageret af kunden, samt produkter, der skal afhentes eller sendes senere.

I Microsoft Dynamics 365 for operationer - løssalg, kan du vælge enten udførelsen af alle produkter eller udføre udvalgte produkter for en kunde. Produktet linjer, der er markeret som udfører automatisk faktureres efter ordren er oprettet, på samme måde dette er det samme for en ordre, der skal være plukket op efter ordren er oprettet. Det skyldige beløb på hybrid ordrer bestemmes ved at tilføje depositum procenten på pluk og skibet produktsortiment med det fulde beløb for udførelsen af linjer. For hybride ordrer skifter systemet mellem kundens ordre tilstanden og kontant og afhentet på følgende måde:

-   Hvis alle produkter i vognen er angivet til **foretager levering**, ordren skal håndteres som en postering af typen kontant og afhentet.
-   Hvis nogle af eller alle linjer i vognen er indstillet til enten **pluk** eller **leverer levering**, ordren skal behandles som en debitorpostering ordre.

Hvis der er valgt en Indkøbsvogn linje og **pluk markerede**, **skib, der er valgt**, eller **udfører valgte** er markeret, angives kun den specifikke Indkøbsvogn linje med denne leveringsmetode. I så fald fortsat downstream strømmen af handlingen som sædvanligt. Men hvis **pluk, der er valgt**, **skib, der er valgt**, eller **udføre valgte** er markeret uden en Indkøbsvogn linje der er valgt, en ny side åbnes, vises alle linjerne for indkøbskurv. På dette skærmbillede kan du vælge flere linjer på en gang til at angive leveringsmetode. Når du bruger denne metode til at markere linjer, tilsidesættes alle tidligere leveringsmetode, der er knyttet til linjen.

<a name="see-also"></a>Se også
--------

[Oversigt over ordrer til kunden](customer-orders-overview.md)


