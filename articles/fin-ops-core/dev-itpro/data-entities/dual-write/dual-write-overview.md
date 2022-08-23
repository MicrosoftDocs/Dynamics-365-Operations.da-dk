---
title: Oversigt over dobbeltskrivning
description: Denne artikel indeholder en oversigt over dobbeltskrivning, der giver næsten realtidsinteraktion mellem kundeengagementapps og programmer til finans og drift.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289632"
---
# <a name="dual-write-overview"></a>Oversigt over dobbeltskrivning

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Hvad er dobbeltskrivning?

Dobbeltskrivning er et indbygget infrastrukturprodukt, der giver næsten realtidsinteraktion mellem kundeengagementapps og programmer til finans og drift. Når data om kunder, produkter, personer og handlinger går ud over programgrænserne, styrkes alle afdelinger i en organisation.

Dobbeltskrivning giver en tæt tovejsintegration mellem programmer til finans og drift og Dataverse. Alle dataændringer i programmer til finans og drift forårsager ændringer i Dataverse, og alle dataændringer i Dataverse medfører ændringer i programmer til finans og drift. Dette automatiserede dataflow giver en integreret brugeroplevelse på tværs af apps.

![Datarelation mellem apps.](media/dual-write-overview.jpg)

Dobbeltskrivning har to aspekter: et *infrastruktur*-aspekt og et *program*-aspekt.

### <a name="infrastructure"></a>Infrastruktur

Dobbeltskrivningsinfrastrukturen kan udvides og er pålidelig og indeholder følgende nøglefunktioner:

+ Synkrone og tovejsdatastrømme mellem programmer
+ Synkronisering sammen med kørsels-, pause- og catch-up-tilstande til at understøtte systemet i onlinetilstand samt offline/asynkron-tilstand.
+ Mulighed for at synkronisere indledende data mellem programmerne
+ Kombineret visning af aktivitet og fejllogfiler for dataadministratorer
+ Mulighed for at konfigurere brugerdefinerede påmindelser og tærskler og til at abonnere på beskeder
+ Intuitiv brugergrænseflade (UI) til filtrering og transformationer
+ Mulighed for at angive og se tabelafhængigheder og relationer
+ Udvidelse til både standard- og brugerdefinerede tabeller og tilknytninger
+ Pålidelig administration af programlevetiden
+ Brugsklar opsætningsoplevelse for nye kunder

### <a name="application"></a>Applikation

Dobbeltskrivning opretter en tilknytning mellem koncepter i programmer til finans og drift og koncepter i kundeengagementapps. Denne integration understøtter følgende scenarier:

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


## <a name="top-reasons-to-use-dual-write"></a>De vigtigste grunde til at bruge dobbeltskrivning

Dobbeltskrivning giver dataintegration på tværs af Microsoft Dynamics 365-programmer. Denne solide rammer forbinder miljøer og giver forskellige virksomhedsprogrammer mulighed for at arbejde sammen. Her er de vigtigste grunde til, at du skal bruge dobbeltskrivning:

+ Dobbeltskrivning giver tæt kombineret, nær-realtidsintegration tovejsintegration mellem Finans- og driftsapps og Customer Engagement-apps. Denne integration gør Microsoft Dynamics 365 til en fælles løsning for alle dine virksomhedsløsninger. Kunder, der bruger Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruger løsninger fra andre leverandører end Microsoft til kunderelationsstyring (CRM), hælder mod Dynamics 365 for så vidt angår understøttelse af dobbeltskrivning.
+ Data fra kunder, produkter, handlinger, projekter og Tingenes internet flyder automatisk over til Dataverse via dobbeltskrivning. Denne forbindelse er nyttig for virksomheder, der er interesserede i Power Platform-udvidelser.
+ Infrastrukturen med dobbeltskrivninger følger princippet om ingen kode/lav kode. Der kræves en minimal teknisk indsats for at udvide standard tabel-til-tabel-tilknytningerne og for at medtage brugerdefinerede kort.
+ Dobbeltskrivning understøtter både onlinetilstand og offlinetilstand. Microsoft er det eneste firma, der tilbyder support til online- og offline-tilstand.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Hvad betyder dobbeltskrivning for udviklere og arkitekter af kundeengagementapps?

Dobbeltskrivning automatiserer datastrømmen mellem programmer til finans og drift og kundeengagementapps. Dobbeltskrivning består af to AppSource-løsninger, der er installeret på Dataverse. Løsningerne udvider tabelskemaet, plug-ins og arbejdsprocesser på Dataverse, så de kan skaleres til ERP-størrelse. For at opnå en vellykket implementering skal udviklere og arkitekter af kundeengagementapps forstå disse ændringer og samarbejde med deres kolleger på programmer til finans og drift.

For at skabe paritet med programmer til finans og drift foretager dobbeltskrivning vigtige ændringer i Dataverse-skemaet. Hvis du forstår planen, kan du slippe for at ændre noget design og udvikling fremover.

+ Når AppSource-pakken til dobbeltskrivning er installeret, vil Dataverse have nye begreber som f.eks. firma og part. Disse koncepter hjælper programmer, der bygger på Dataverse, herunder Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, med problemfri interaktion med programmer til finans og drift.

+ Aktiviteter og noter samles og udvides til at understøtte både C1s (brugere af systemet) og C2s (systemkunder).

+ Hvis du vil undgå tab af data i forbindelse med valutaoverførsel mellem programmer til finans og drift og Dataverse, kan du udvide antallet af decimaler i valutadatatypen for kundeengagementapps. Med denne funktion oversættes eksisterende rækker automatisk til den nye udvidede tilstand på metadatalaget. I løbet af denne proces oversættes valutaværdien til decimaldata og ikke til pengedata, og valutaværdien understøtter 10 decimalpladser. Denne funktion er et tilvalg, og organisationer, der ikke har brug for mere end 4 decimaler, behøver ikke at tilmelde sig. Du kan finde flere oplysninger under [Migrering af valutadatatype til dobbeltskrivning](currrency-decimal-places.md).

+ [Gyldighedsdato](../../dev-tools/date-effectivity.md) vil blive føjet til Dataverse. Den understøtter tidligere, nuværende og fremtidige data på samme tabel.

+ Produktets [enhedsomregninger](../../../../supply-chain/pim/tasks/manage-unit-measure.md) understøttes for produkter, tilbud, ordrer og fakturaer.

Yderligere oplysninger om kommende ændringer finder du i [Nyheder eller ændringer i dobbeltskrivning](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

