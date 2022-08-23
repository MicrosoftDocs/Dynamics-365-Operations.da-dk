---
title: Indstillinger for implementering af netværk for indholdslevering
description: Denne artikel gennemgår de forskellige indstillinger for CDN-implementering (Content Delivery Network), der kan bruges i Microsoft Dynamics 365 Commerce-miljøer. Disse indstillinger inkluderer oprindelige forekomster af Azure Front Door fra Commerce og forekomster, der ejes af kunden, på Azure Front Door.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: de2ecab86809af3ace64ba06956f00137d254ab7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275141"
---
# <a name="content-delivery-network-implementation-options"></a>Indstillinger for implementering af netværk for indholdslevering

[!include [banner](includes/banner.md)]

Denne artikel gennemgår de forskellige indstillinger for CDN-implementering (Content Delivery Network), der kan bruges i Microsoft Dynamics 365 Commerce-miljøer. Disse indstillinger inkluderer oprindelige forekomster af Azure Front Door fra Commerce og forekomster, der ejes af kunden, på Azure Front Door.

Handelskunder har adskillige valgmuligheder, når de overvejer, hvilken CDN-tjeneste der skal bruges sammen med deres handelsmiljø. Handel udgives med grundlæggende understøttelse af Azure Front Door, der dækker grundlæggende vært og brugerdefinerede domænekrav. For firmaer, der ønsker mere kontrol og mere specifikke sikkerhedsevner, som f.eks. en WAF (Web Application Firewall), kan den bedste løsning være enten at bruge en kundeejet forekomst af Azure Front Door eller en ekstern CDN-tjeneste.

Følgende tre indstillinger for implementering af CDN kan bruges sammen med handelsmiljøer:

- Den Commerce-leverede forekomst af Azure Front Door
- En kundeejet forekomst af Azure Front Door (for at øge styringen og flere sikkerhedsfunktioner)
- En ekstern CDN-tjeneste

Alle tre indstillinger for implementeringen af CDN leverer kun dynamisk HTML-indhold fra brugerdefinerede domæner. Ved handel administreres automatisk alle JavaScript, overlappende typografiark (CSS), billeder, video og andet statisk indhold via Microsoft-administrerede CDN'er. Den indstilling, du vælger, bestemmer, hvilke driftsfunktioner, kontrolegenskaber og yderligere sikkerhedsegenskaber der er til rådighed.

I følgende illustration vises en oversigt over Commerce-arkitekturen.

![Oversigt over Commerce-arkitekturen.](media/Commerce_CDN-Option_ComparisonModels.png)

Yderligere oplysninger om, hvordan du konfigurerer en forekomst af Azure Front Door til dit handelswebsted, finder du under [Add CDN Support](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Brug den Commerce-leverede forekomst af Azure Front Door

Følgende tabel indeholder de professionelle og medarbejdere ved at bruge den forekomst af Azure Front Door, der er leveret af Azure Front Door, til at administrere indholdsslutpunkter.

| Fordele | Ulemper |
|------|------|
| <ul><li>Forekomsten er medtaget i Commerce-omkostningen.</li><li>Da forekomsten administreres af Commerce-teamet, kræves der mindre vedligeholdelse, og der er delte opsætningstrin.</li><li>Infrastrukturen, der er tilknyttet Azure, er skalerbar, sikker og pålidelig.</li><li>SSL-certifikatet (Secure Sockets Layer) kræver en engangsopsætning, og det fornys automatisk.</li><li>Forekomsten overvåges for fejl og afvigelser af Commerce-teamet.</li></ul> | <ul><li>WAF understøttes ikke.</li><li>Der findes ingen specifikke tilpasninger eller indstillinger til justeringer.</li><li>Forekomsten afhænger af Commerce-teamet for opdateringer eller ændringer.</li><li>Der skal bruges en separat forekomst af Azure Front Door til apex-domæner og ekstra arbejde for at integrere apex-domæner med Azure DNS.</li><li>Kunden får ingen telemetri for svar pr. anden (RPS) eller fejlprocent.</li></ul> |

I følgende illustration vises arkitekturen for den Azure Front Door-forekomst, der leveres af Commerce.

![Commerce-leverede forekomst af Azure Front Door.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Bruge en Azure Front Door-forekomst, der ejes af kunden

Følgende tabel indeholder de fordele og ulemper ved at bruge den kundeejede forekomst af Azure Front Door til at administrere indholdsslutpunkter.

| Fordele | Ulemper |
|------|------|
| <ul><li>Opsætningen er sikker og let at administrere.</li><li>Infrastrukturen, der er tilknyttet Azure, er skalerbar, sikker og pålidelig.</li><li>Forekomsten giver mulighed for WAF-integration og granuleringsregelkontrol til sikkerhed i finmasket klasse, der specifikt bruges til dit sted.</li><li>Forekomsten giver mulighed for bedre styring af SSL-certifikater (både kundeejet og Azure Front Door-administreret) og domænelinks.</li><li>Forekomsten indeholder en apex-domæneløsning, hvis den er knyttet direkte til Azure DNS.</li><li>Der ydes telemetry og påmindelse.</li><li>SSL-certifikatet (Secure Sockets Layer) kræver en engangsopsætning, og det fornys automatisk.</li></ul> | <ul><li>Forekomsten er selvadministreret.</li><li>Første viden-opkørsel er påkrævet.</li></ul> |

I følgende illustration vises en handelsinfrastruktur, der omfatter en forekomst af Azure Front Door, der ejes af kunden.

![I følgende illustration vises en Commerce-infrastruktur, der omfatter en forekomst af Azure Front Door, der ejes af kunden.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Brug en ekstern CDN-tjeneste

Følgende tabel indeholder fordele og ulemper ved at bruge en ekstern CDN-tjeneste til at administrere indholdsslutpunkter.

| Fordele | Ulemper |
|------|------|
| <ul><li>Denne indstilling er nyttig, når det eksisterende domæne allerede er tilknyttet et eksternt CDN.</li><li>WAF: Afhænger af ekstern udbyder.</li></ul> | <ul><li>Der kræves en separat kontrakt og yderligere omkostninger.</li><li>SSL kan medføre yderligere omkostninger.</li><li>Da tjenesten er adskilt fra Azure-skystrukturen, skal den ekstra infrastruktur administreres.</li><li>Tjenesten kan kræve længere tids investeringer i slutpunkt og sikkerhedsopsætning.</li><li>Tjenesten er selvadministreret.</li><li>Tjenesten er selvovervåget.</li></ul> |

I følgende illustration vises en handelsinfrastruktur, der omfatter en ekstern CDN-tjeneste.

![Commerce-infrastruktur, der omfatter en ekstern CDN-tjeneste.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Tilføje understøttelse af et netværk, der leverer indhold (CDN)](add-cdn-support.md)
