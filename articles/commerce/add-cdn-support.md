---
title: Tilføje understøttelse af et netværk, der leverer indhold (CDN)
description: Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.
author: brianshook
ms.date: 03/17/2021
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
ms.openlocfilehash: 85ca468fe6c440fb333b4c32f59f1d41eb89f4e6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346822"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Tilføje understøttelse af et netværk, der leverer indhold (CDN)

[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du føjer et CDN (Content Delivery Network) til dit Microsoft Dynamics 365 Commerce-miljø.

Når du konfigurerer et e-handels-miljø i Dynamics 365 Commerce, kan du konfigurere det til at arbejde sammen med CDN-tjenesten. 

Dit brugerdefinerede domæne kan aktiveres under klargøringsprocessen for e-handels-miljøet. Du kan også bruge en serviceanmodning til at konfigurere den, når klargøringsprocessen er fuldført. Klargøringsprocessen for e-handelsmiljøet genererer et værtsnavn, der er knyttet til miljøet. Dette værtsnavn har følgende format, hvor \<*e-commerce-tenant-name*\> er navnet på dit miljø:

&lt;e-handels-lejernavn&gt;.commerce.dynamics.com

Det værtsnavn eller slutpunkt, der genereres under klargøringsprocessen, understøtter kun et SSL-certifikat (Secure Sockets Layer) for \*.commerce.dynamics.com. Det understøtter ikke SSL for brugerdefinerede domæner. Derfor skal du afslutte SSL for brugerdefinerede domæner i CDN og videresende trafik fra CDN til det værtsnavn eller slutpunkt, som Commerce genererede. 

Derudover betjenes *statiske filer* (JavaScript- eller \[CSS\]-filer (overlappende typografiark)) fra Commerce fra det slutpunkt, som Commerce genererede (\*.commerce.dynamics.com). De statiske filer kan kun cachelagres, hvis det værtsnavn eller slutpunkt, som Commerce genererede, placeres bag CDN'et.

## <a name="set-up-ssl"></a>Konfigurer SSL

Når du har klargjort Commerce-miljøet med det brugerdefinerede domæne, der er leveret, eller når du har angivet det brugerdefinerede domæne for dit miljø ved hjælp af en serviceanmodning, skal du samarbejde med Commerce-onboardingteamet omkring planlægning af DNS.

Som tidligere nævnt understøtter det genererede værtsnavn eller slutpunkt kun et SSL-certifikat for \*.commerce.dynamics.com. Det understøtter ikke SSL for brugerdefinerede domæner.

## <a name="cdn-services"></a>CDN-tjenester

Der kan bruges en CDN-tjeneste sammen med et Commerce-miljø. Her er to eksempler:

- **Microsoft Azure Front Door Service** – Azure CDN-løsningen. Du kan finde flere oplysninger om Azure Front Door Service i [Dokumentation til Azure Front Door Service](/azure/frontdoor/) (artiklen er muligvis på engelsk).
- **Akamai Dynamic Site Accelerator** – du kan finde flere oplysninger i [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-opsætning

CDN-konfigurationsprocessen består af følgende generelle trin:

1. Tilføj en front-end-vært.
1. Konfigurer en back-end-pulje.
1. Konfigurer regler for ruteplanlægning.

### <a name="add-a-front-end-host"></a>Tilføj en front-end-vært

Alle CDN-tjenester kan bruges, men i eksemplet i dette emne bruges Azure Front Door Service. 

Du kan finde oplysninger om, hvordan du konfigurerer Azure Front Door Service, i [Hurtigstart: Opret en Front Door til et globalt webprogram med høj tilgængelighed](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Konfigurere en back-end-pulje i Azure Front Door Service

Benyt følgende fremgangsmåde for at konfigurere en back-end-pulje i Azure Front Door Service.

1. Føj **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** til en backend-pulje som en brugerdefineret vært, der har et backend-værtshoved, der er det samme som **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. Lad standardværdierne stå under **Belastningsjustering**.
1. Deaktiver sundhedstjek for backend-puljen.

I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med back-end-værtsnavnet indtastet.

![Dialogboksen Tilføj en back-end-pulje.](./media/CDN_BackendPool.png)

I følgende illustration vises dialogboksen **Tilføj en back-end-pulje** i Azure Front Door Service med standardværdier for justering af belastning.

![Dialogboksen Tilføj en back-end-pulje fortsat.](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Sørg for at deaktivere **Tilstandsundersøgelser**, når du konfigurerer din egen Azure Front Door Service til Commerce.


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


> [!WARNING]
> Hvis det domæne, du vil bruge, allerede er aktivt og live, kan du oprette en supportanmodning fra **Support**-feltet i [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) for at få hjælp til de næste trin. Du kan finde flere oplysninger i [Få support til Finance and Operations-apps eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Hvis dit domæne er nyt og ikke er et eksisterende Live-domæne, kan du føje dit tilpassede domæne til konfigurationen for Azure Front Door Service. Dette gør det muligt for webtrafik at dirigere til dit websted via forekomsten af Azure Front Door. Hvis du vil tilføje det brugerdefinerede domæne (f.eks. `www.fabrikam.com`), skal du konfigurere et vedtaget navn (CNAME) for domænet.

I følgende illustration vises dialogboksen **CNAME-konfiguration** i Azure Front Door Service.

![Dialogboksen CNAME-konfiguration.](./media/CNAME_Configuration.png)

Du kan bruge Azure Front Door Service til at administrere certifikatet, eller du kan bruge dit eget certifikat til det brugerdefinerede domæne.

I følgende illustration vises dialogboksen **HTTPS for brugerdefineret domæne** i Azure Front Door Service.

![Dialogboksen HTTPS for brugerdefineret domæne.](./media/Custom_Domain_HTTPS.png)

Detaljerede oplysninger om, hvordan du føjer et brugerdefineret domæne Azure Front Door, finder du under [Føje et brugerdefineret domæne til Front Door](/azure/frontdoor/front-door-custom-domain).

Dit CDN bør nu være korrekt konfigureret, så det kan bruges sammen med Commerce-webstedet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Indstillinger for implementering af netværk for indholdslevering](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]