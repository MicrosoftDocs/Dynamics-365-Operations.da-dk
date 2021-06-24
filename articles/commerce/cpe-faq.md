---
title: Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø
description: Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til evalueringsversionen af Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a0c6f82432a4786f23f12122f3806c3b96a05c8f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193588"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Konfigurere Dynamics 365 Commerce-Ofte stillede spørgsmål

[!include [banner](includes/banner.md)]

Dette emne indeholder svar på ofte stillede spørgsmål om miljøet til evalueringsversionen af Microsoft Dynamics 365 Commerce.

**Kan vi bruge miljøet til evalueringsversionen af Commerce som en e-handel-butiksfacade for kunder, der i øjeblikket implementerer Retail?**

Nr. Commerce-evalueringsmiljøet er kun til evaluering. Hvis du har brug for et miljø til en kunde, der implementerer Retail, skal du kontakte Microsoft.

**Kan evalueringsmiljøet til af Commerce bruges til at klargøre e-handel-funktionerne oven på et eksisterende program/miljø, der implementerer Retail?**

Nej (hovedsageligt). Commerce-evalueringskomponenterne er kun tilgængelige for de miljøer, der svarer til de konfigurationer, der er angivet i guiden for forudsætninger og klargøring. Derudover er de nødvendige grundlæggende demonstrationsdata ikke tilgængelige i miljøer, der er implementeret med en første udgivelse, der er tidligere end 10.0.8. 

**Hvilke omkostninger er der forbundet med implementeringen af evalueringsmiljøet til Commerce på Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**

Et traditionelt demonstrationsmiljø for Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce-hovedkontoret (virtuel maskine \[VM\]) hostes i dit Azure-abonnement. Du kan bruge [Azure prisberegneren](https://azure.microsoft.com/pricing/calculator/) til at anslå denne omkostning.

Andre komponenter som f. eks. Commerce Scale Unit, Commerce Site Builder, og dit e-handels-websted vil være tilgængeligt som software som en tjeneste (SaaS) og hostes af Microsoft.

**Hvilke geografiske Azure-områder understøttes i øjeblikket for evalueringsmiljøet til Commerce?**

Evalueringsmiljøet til Commerce kan kun implementeres i det nordamerikanske område.

**Findes der en virtuel harddisk (VHD), der kan downloades, og som har den komplette indstilling for en virtuel maskine med én boks (VM)?**

Dynamics 365 Commerce og Commerce Scale Unit er udelukkende software som en service (SaaS) og skal være hostet i skyen.

**Hvor længe kan evalueringsmiljøet til Commerce bruges?**

Der er en frist på 30 dage for Commerce-evalueringsmiljøet fra den dato, hvor SaaS-komponenter som f.eks. Commerce Scale Unit, Commerce-webstedsgenerator og dit e-handelssted klargøres.

**Kan jeg forlænge fristen for mit evalueringsmiljø til Commerce?**

Forlængelsen af tidsfristen er en undtagelse fra normen og tages i betragtning ved hvert enkelt tilfælde. Du skal rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]