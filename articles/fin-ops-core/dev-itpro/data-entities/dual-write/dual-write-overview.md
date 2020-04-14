---
title: Oversigt over dobbeltskrivning
description: Dette emne giver en oversigt over dobbeltskrivning. Dobbeltskrivning er en infrastruktur, der giver næsten realtidsinteraktion mellem Microsoft Dynamics 365 modelbaserede apps og Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172778"
---
# <a name="dual-write-overview"></a>Oversigt over dobbeltskrivning

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a>Hvad er dobbeltskrivning?

Dobbeltskrivning er en brugsklar infrastruktur, der giver næsten realtidsinteraktion mellem modelbaserede apps i Microsoft Dynamics 365 og Finance and Operations-apps. Når data om kunder, produkter, personer og handlinger går ud over programgrænserne, styrkes alle afdelinger i en organisation.

Dobbeltskrivning giver en tæt kombineret, tovejsintegration mellem Finance and Operations-apps og Common Data Service. Alle dataændringer i Finance and Operations-apps forårsager ændringer i Common Data Service, og alle dataændringer i Common Data Service medfører ændringer i Finance and Operations-apps. Dette automatiserede dataflow giver en integreret brugeroplevelse på tværs af apps.

![Datarelation mellem apps](media/dual-write-overview.jpg)

Dobbeltskrivning har to aspekter: et *infrastruktur*-aspekt og et *program*-aspekt.

### <a name="infrastructure"></a>Infrastruktur

Dobbeltskrivningsinfrastrukturen kan udvides og er pålidelig og indeholder følgende nøglefunktioner:

+ Synkrone og tovejsdatastrømme mellem programmer
+ Synkronisering sammen med kørsels-, pause- og catch-up-tilstande til at understøtte systemet i onlinetilstand samt offline/asynkron-tilstand.
+ Mulighed for at synkronisere indledende data mellem programmerne
+ Konsolideret visning af aktivitet og fejllogfiler for dataadministratorer
+ Mulighed for at konfigurere brugerdefinerede påmindelser og tærskler og til at abonnere på beskeder
+ Intuitiv brugergrænseflade (UI) til filtrering og transformationer
+ Mulighed for at angive og få vist enhedsafhængigheder og relationer
+ Udvidelse til både standard- og brugerdefinerede enheder og kort
+ Pålidelig administration af programlevetiden
+ Brugsklar opsætningsoplevelse for nye kunder

### <a name="application"></a>Applikation

Dobbeltskrivning opretter en tilknytning mellem koncepter i Finance and Operations-apps og koncepter i modelbaserede apps i Dynamics 365. Denne integration understøtter følgende scenarier:

+ Integreret kundemaster
+ Adgang til kundefordelskundekort og belønningspoint
+ Samlet produktmasteroplevelse
+ Bevidsthed om organisationens hierarki
+ Integreret kreditormaster
+ Adgang til finansierings- og momsreferencedata
+ Prisprogramoplevelse efter behov
+ Integreret kundeemne-til-køb-oplevelse
+ Mulighed for at betjene både interne aktiver og kundeaktiver via feltagenter
+ Integreret oplevelse fra indkøb til betaling
+ Integrerede aktiviteter og notater til kundedata og -dokumenter
+ Mulighed for at slå disponibel lagertilgængelighed op og få detaljer herom
+ Oplevelsen projekt til kontant
+ Mulighed for at håndtere flere adresser og roller via partskonceptet
+ Enkel kildestyring til brugere
+ Integrerede kanaler til detailhandel og marketing
+ Synlighed i kampagner og rabatter
+ Funktioner for anmodning om tjenester
+ Integrerede tjenestehandlinger

## <a name="top-reasons-to-use-dual-write"></a>De vigtigste grunde til at bruge dobbeltskrivning

Dobbeltskrivning giver dataintegration på tværs af Microsoft Dynamics 365-programmer. Denne solide rammer forbinder miljøer og giver forskellige virksomhedsprogrammer mulighed for at arbejde sammen. Her er de vigtigste grunde til, at du skal bruge dobbeltskrivning:

+ Dobbeltskrivning giver tæt kombineret, nær-realtidsintegration tovejsintegration mellem Finance and Operations-apps og modelbaserede apps i Dynamics 365. Denne integration gør Microsoft Dynamics 365 til en fælles løsning for alle dine virksomhedsløsninger. Kunder, der bruger Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruger løsninger fra andre leverandører end Microsoft til kunderelationsstyring (CRM), hælder mod Dynamics 365 for så vidt angår understøttelse af dobbeltskrivning.
+ Data fra kunder, produkter, handlinger, projekter og Tingenes internet flyder automatisk over til Common Data Service via dobbeltskrivning. Denne forbindelse er meget anvendelig for virksomheder, der er interesserede i Microsoft Power Platform-udvidelser.
+ Infrastrukturen med dobbeltskrivninger følger princippet om ingen kode/lav kode. Der kræves en minimal teknisk indsats for at udvide standard tabel-til-tabel-tilknytningerne og for at medtage brugerdefinerede kort.
+ Dobbeltskrivning understøtter både onlinetilstand og offlinetilstand. Microsoft er det eneste firma, der tilbyder support til online- og offline-tilstand.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Hvad betyder dobbeltskrivning for brugere og arkitekter af CRM-produkter?

Dobbeltskrivning automatiserer datastrømmen mellem Finance and Operations-apps og Common Data Service. I fremtidige udgivelser vil koncepterne i modelbaserede apps i Dynamics 365 (f.eks. kunde, kontaktperson, tilbud og ordre) blive skaleret til mellemstore og større mellemstore kunder.

I den første version håndteres det meste af automatiseringen af dobbeltskrivningsløsninger. I fremtidige versioner bliver løsningerne en del af Common Data Service. Når du forstår de kommende ændringer af Common Data Service, kan du spare en del på lang sigt. Her er nogle af de vigtigste ændringer:

+ Common Data Service vil få nye begreber såsom firma og part. Disse begreber påvirker alle de apps, der er baseret på Common Data Service, som f.eks. Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.
+ Aktiviteter og noter samles og udvides til at understøtte både C1s (brugere af systemet) og C2s (systemkunder).
+ Her er nogle af de kommende ændringer i Common Data Service:

    - Datatypen decimal vil erstatte datatypen penge.
    - Datoudnyttelse understøtter tidligere, nuværende og fremtidige data på samme sted.
    - Der vil være mere understøttelse af valuta og valutakurser, og API'en (Application Programming Interface) **Valutakurs** vil blive revideret.
    - Enhedsomregninger understøttes.

Yderligere oplysninger om kommende ændringer finder du i [Data i Common Data Service – fase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
