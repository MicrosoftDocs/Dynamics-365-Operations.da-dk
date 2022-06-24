---
title: Aktivere registrering af placeringsbaseret lager
description: Denne artikel beskriver, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0e0fcea2f53a8e1fea5a411981a317eabe94bddb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892039"
---
# <a name="enable-location-based-store-detection"></a>Aktivere registrering af placeringsbaseret lager

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.

Med registrering af lokationsbaserede butikker i Commerce kan du levere relevant webstedsindhold til kunderne på baggrund af deres placering. Hvis registrering af lokationsbaserede butikker er slået til, bruger Commerce-gengivelsestjenesten land/område-oplysningerne fra IP-adressen på kundens webbrowser til at dirigere kunden til den bedst mulige geografiske lokationskonfiguration.

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Hvis du slår funktionen til registrering af lokationsbaserede butikker til, sendes oplysninger fra kundens browser til en Microsoft-lokationstjeneste. Disse oplysninger bruges derefter til at angive det kundeindhold, der er relevant for det sted, hvor vedkommende kunde befinder sig. Både de oplysninger, der sendes fra kundens browser, og de lokationsbaserede oplysninger, der returneres til kunden, kræver overholdelse af politikker om beskyttelse af personlige oplysninger og politikker om cookies.

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
