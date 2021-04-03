---
title: Aktivere registrering af lokationsbaserede butikker
description: I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478182"
---
# <a name="enable-location-based-store-detection"></a>Aktivere registrering af lokationsbaserede butikker

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.

Med registrering af lokationsbaserede butikker i Commerce kan du levere relevant webstedsindhold til kunderne på baggrund af deres placering. Hvis registrering af lokationsbaserede butikker er slået til, bruger Commerce-gengivelsestjenesten land/område-oplysningerne fra IP-adressen på kundens webbrowser til at dirigere kunden til den bedst mulige geografiske lokationskonfiguration.

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

[Implementere en ny e-handelslejer](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)

[Konfigurere en B2C-lejer i Commerce](set-up-B2C-tenant.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Konfigurere flere B2C-lejere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
