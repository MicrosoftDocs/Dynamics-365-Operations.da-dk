---
title: Aktivere registrering af lokationsbaserede butikker
description: I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003088"
---
# <a name="enable-location-based-store-detection"></a>Aktivere registrering af lokationsbaserede butikker


[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.

## <a name="overview"></a>Oversigt

Med registrering af lokationsbaserede butikker i Commerce kan du levere relevant webstedsindhold til kunderne på baggrund af deres placering. Hvis registrering af lokationsbaserede butikker er slået til, bruger Commerce-gengivelsestjenesten lande-/områdeoplysningerne fra IP-adressen på kundens webbrowser til at dirigere kunden til den bedst mulige geografiske lokationskonfiguration.

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Hvis du slår funktionen til registrering af lokationsbaserede butikker til, sendes oplysninger fra kundens browser til en Microsoft-lokationstjeneste. Disse oplysninger bruges derefter til at angive det kundeindhold, der er relevant for det sted, hvor vedkommende befinder sig. Både de oplysninger, der sendes fra kundens browser, og de lokationsbaserede oplysninger, der returneres til kunden, kræver overholdelse af politikker om beskyttelse af personlige oplysninger og politikker om cookies.

## <a name="turn-on-location-based-store-detection"></a>Aktivere registrering af lokationsbaserede butikker

Udfør følgende trin for at aktivere registrering af lokationsbaserede butikker i Commerce.

1. Gå til dit websted i oprettelsesværktøjet.
1. Vælg **Administration af websted** i navigationsruden til venstre.
1. Vælg **Indstillinger for websted**.
1. Vælg **Til** i indstillingen **Aktivere registrering af lokationsbaseret lager**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Administrer robots.txt-filer](manage-robots-txt-files.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)
