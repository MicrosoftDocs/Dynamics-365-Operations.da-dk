---
title: Konfigurere dit domænenavn
description: I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770452"
---
# <a name="configure-your-domain-name"></a>Konfigurere dit domænenavn

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted. 

## <a name="add-domains-during-e-commerce-initialization"></a>Tilføje domæner under initialisering af e-handel

Hvis du vil knytte domæner til e-handelsmiljøet, skal du initialisere e-handel som beskrevet i [Implementere et nyt e-handelswebsted](deploy-ecommerce-site.md). Under initialiseringen bliver du bedt om at angive oplysninger, der skal bruges til at klargøre e-handelsmiljøet. Tilføj alle de domæner, du planlægger at bruge til dette miljø, i feltet **Understøttede værtsnavne**. Flere domæner skal adskilles med semikolon. På denne måde konfigureres domænerne i alle de påkrævede e-handelskomponenter, og de er klar til at blive brugt, når du skifter trafik fra CDN (Content Delivery Network) eller webserveren og peger på dem i e-handelsbutikkerne.

## <a name="add-domains-after-e-commerce-initialization"></a>Tilføje domæner efter initialisering af e-handel

Hvis du vil knytte nye domæner til e-handelsmiljøet efter e-handelsinitialiseringen, skal du sende en serviceanmodning.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over onlinebutik](online-store-overview.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)
