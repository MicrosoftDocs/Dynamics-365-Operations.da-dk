---
title: Tilføje understøttelse af et netværk, der leverer indhold (CDN)
description: Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.
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
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945622"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Tilføje understøttelse af et netværk, der leverer indhold (CDN)

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.

## <a name="overview"></a>Oversigt

Når du konfigurerer et e-handels-miljø i Dynamics 365 Commerce, kan du konfigurere det til at arbejde sammen med CDN-tjenesten. 

Dit brugerdefinerede domæne kan aktiveres under klargøringsprocessen for e-handels-miljøet. Du kan også bruge en serviceanmodning til at konfigurere den, når klargøringsprocessen er fuldført. Klargøringsprocessen for e-handels miljøet genererer et værtsnavn, der er knyttet til miljøet. Dette værtsnavn har følgende format, hvor *e-handels-lejernavn* er navnet på dit miljø:

&lt;e-handels-lejernavn&gt;.commerce.dynamics.com

Det værtsnavn eller slutpunkt, der genereres under klargøringsprocessen, understøtter kun et SSL-certifikat (Secure Sockets Layer) for \*.commerce.dynamics.com. Det understøtter ikke SSL for brugerdefinerede domæner. Derfor skal du afslutte SSL for brugerdefinerede domæner i CDN og videresende trafik fra CDN til det værtsnavn eller slutpunkt, som Commerce genererede. 

Derudover betjenes *statiske filer* (JavaScript- eller \[CSS\]-filer (overlappende typografiark)) fra Commerce fra det slutpunkt, som Commerce genererede (\*.commerce.dynamics.com). De statiske filer kan kun cachelagres, hvis det værtsnavn eller slutpunkt, som Commerce genererede, placeres bag CDN'et.

## <a name="set-up-ssl"></a>Konfigurer SSL

For at sikre, at SSL konfigureres, og at statiske filer cachelagres, skal du konfigurere CDN, så det er knyttet til det værtsnavn, som Commerce genererede for dit miljø. Du skal også cachelagre følgende mønster udelukkende for statiske filer: 

/\_msdyn365/\_scnr/\*

Når du har klargjort Commerce-miljøet med det tilpassede domæne, der er angivet, eller når du har angivet det brugerdefinerede domæne for miljøet ved hjælp af en serviceanmodning, skal du sørge for, at det brugerdefinerede domæne peger på det værtsnavn eller slutpunkt, som Commerce genererede.

Som tidligere nævnt understøtter det genererede værtsnavn eller slutpunkt kun et SSL-certifikat for \*.commerce.dynamics.com. Det understøtter ikke SSL for brugerdefinerede domæner.

## <a name="cdn-services"></a>CDN-tjenester

Der kan bruges en CDN-tjeneste sammen med et Commerce-miljø. Her er to eksempler:

- **Microsoft Azure Front Door Service** – Azure CDN-løsningen. Du kan finde flere oplysninger om Azure Front Door Service i [Dokumentation til Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/) (artiklen er muligvis på engelsk).
- **Akamai Dynamic Site Accelerator** – du kan finde flere oplysninger i [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-opsætning

CDN-konfigurationsprocessen består af følgende generelle trin:

1. Tilføj en front-end-vært.
1. Konfigurer en back-end-pulje.
1. Konfigurer regler for routing og cachelagring.

### <a name="add-a-front-end-host"></a>Tilføj en front-end-vært

Alle CDN-tjenester kan bruges, men i eksemplet i dette emne bruges Azure Front Door Service. 

Du kan finde oplysninger om, hvordan du konfigurerer Azure Front Door Service, i [Hurtigstart: Opret en Front Door til et globalt webprogram med høj tilgængelighed](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Konfigurere en back-end-pulje i Azure Front Door Service

Benyt følgende fremgangsmåde for at konfigurere en back-end-pulje i Azure Front Door Service.

1. Føj **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** til en back-end-pulje som en brugerdefineret vært, der har en tom back-end-værtsheader.
1. Under **Tilstandsundersøgelser** i feltet **Sti** skal du angive **/keepalive**.
1. I feltet **Intervaller (sekunder)** skal du indtaste **255**.
1. Lad standardværdierne stå under **Belastningsjustering**.

I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service.

![Dialogboksen Tilføj en back-end-pulje](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Konfigurere regler i Azure Front Door Service

Benyt følgende fremgangsmåde for at konfigurere en ruteplanlægningsregel i Azure Front Door Service.

1. Tilføj en ruteplanlægningsregel.
1. I feltet **Navn** skal du angive **standard**.
1. I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.
1. I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.
1. Under **Mønstre, der skal matche** skal du angive **/\*** i det øverste felt.
1. Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.
1. I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.
1. I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**. 
1. Angiv indstillingen **URL Rewrite** til **Deaktiveret**.
1. Angiv indstillingen **Cachelagring** til **Deaktiveret**.

Benyt følgende fremgangsmåde for at konfigurere en cachelagringsregel i Azure Front Door Service.

1. Tilføj en cachelagringsregel.
1. I feltet **Navn** skal du angive **statiske filer**.
1. I feltet **Accepteret protokol** skal du vælge **HTTP og HTTPS**.
1. I feltet **Front-end-værter** skal du angive **dynamics-ecom-lejernavn.azurefd.net**.
1. Under **Mønstre, der skal matche** skal du angive **/\_msdyn365/\_scnr/\*** i det øverste felt.
1. Under **Rutedetaljer** skal du angive indstillingen **Rutetype** til **Fremad**.
1. I feltet **Back-end-pulje** skal du vælge **ecom-back-end**.
1. I feltgruppen **Videresendelsesprotokol** skal du vælge indstillingen **Match anmodning**.
1. Angiv indstillingen **URL Rewrite** til **Deaktiveret**.
1. Angiv indstillingen **Cachelagring** til **Deaktiveret**.
1. I feltet **Cachefunktionsmåde for forespørgselsstreng** skal du vælge **Cache hver entydige URL**.
1. I feltgruppen **Dynamisk komprimering** skal du vælge indstillingen **Aktiveret**.

Følgende illustration viser dialogboksen **Tilføj en regel** i Azure Front Door Service.

![Dialogboksen Tilføj en regel](./media/CDN_CachingRule.png)

Når denne indledende konfiguration er installeret, skal du føje det brugerdefinerede domæne til konfigurationen for Azure Front Door Service. Hvis du vil tilføje det brugerdefinerede domæne (f.eks. `www.fabrikam.com`), skal du konfigurere et vedtaget navn (CNAME) for domænet.

I følgende illustration vises dialogboksen **CNAME-konfiguration** i Azure Front Door Service.

![Dialogboksen CNAME-konfiguration](./media/CNAME_Configuration.png)

> [!NOTE]
> Hvis det domæne, du vil bruge, allerede er aktivt og live, skal du kontakte support for at aktivere dette domæne med Azure Front Door Service

Du kan bruge Azure Front Door Service til at administrere certifikatet, eller du kan bruge dit eget certifikat til det brugerdefinerede domæne.

I følgende illustration vises dialogboksen **HTTPS for brugerdefineret domæne** i Azure Front Door Service.

![Dialogboksen HTTPS for brugerdefineret domæne](./media/Custom_Domain_HTTPS.png)

Dit CDN bør nu være korrekt konfigureret, så det kan bruges sammen med Commerce-webstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Konfigurere dit domænenavn](configure-your-domain-name.md)

[Implementere et nyt websted for e-handel](deploy-ecommerce-site.md)

[Oprette et websted for e-handel](create-ecommerce-site.md)

[Tilknytte et onlinewebsted til en kanal](associate-site-online-store.md)

[Administrer robots.txt-filer](manage-robots-txt-files.md)

[Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md)

[Aktivere registrering af lokationsbaseret lager](enable-store-detection.md)