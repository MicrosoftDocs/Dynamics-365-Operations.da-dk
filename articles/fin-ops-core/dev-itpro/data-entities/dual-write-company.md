---
title: Firmakoncept i Common Data Service
description: I dette emne beskrives integrationen af firmadata mellem Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 21c2143f4fa58d51f64e349c7963cb17e04bad97
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772431"
---
## <a name="company-concept-in-common-data-service"></a>Firmakoncept i Common Data Service

[!include [banner](../includes/banner.md)]

I Finance and Operations er konceptet et *firma* både en juridisk konstruktion og en forretningskonstruktion. Det er også en sikkerheds- og synlighedsgrænse for data. Brugere arbejder altid i konteksten af et enkelt firma, og de fleste data stripes (spredes) af firmaet.

Common Data Service har ikke et tilsvarende koncept. Det tætteste koncept er *virksomhedsenhed*, som primært er en sikkerheds- og synlighedsgrænse for brugerdata. Dette koncept har ikke samme juridiske eller forretningsmæssige implikationer som firmakonceptet.

Da virksomhedsenhed og firma ikke er tilsvarende koncepter, er det ikke muligt at gennemtvinge en en-til-en (1:1) tilknytning mellem dem med henblik på Common Data Service-integration. Men da brugere som standard skal kunne se de samme poster i programmet og Common Data Service, har Microsoft introduceret en ny enhed i Common Data Service, der hedder cdm\_Company. Denne enhed svarer til enheden Firma i programmet. For at hjælpe med at sikre, at synlighed af poster som standard er ens mellem programmet og Common Data Service, anbefaler vi følgende opsætning af data i Common Data Service:

+ For hver firmapost i Finance and Operations, der er aktiveret til dobbeltskrivning, oprettes der en tilknyttet cdm\_Company-post.
+ Når en cdm\_Company-post oprettes og aktiveres til dobbeltskrivning oprettes der en standardvirksomhedsenhed med samme navn. Selvom der automatisk oprettes et standardteam for denne virksomhedsenhed, bruges virksomhedsenheden ikke.
+ Der oprettes et separat ejerteam med samme navn. Det er også tilknyttet virksomhedsenheden.
+ Som standard angives ejeren af enhver post, der oprettes og dobbeltskrives til Common Data Service, til "DW-ejer"-teamet, der er knyttet til den tilknyttede virksomhedsenhed.

I følgende illustration vises et eksempel på denne dataopsætning i Common Data Service.

![Dataopsætning i Common Data Service](media/dual-write-company-1.png)

På grund af denne konfiguration ejes alle poster, der er relateret til USMF-firmaet, af et team, der er knyttet til USMF-virksomhedsenheden i Common Data Service. Derfor kan alle brugere, der har adgang til den pågældende virksomhedsenhed via en sikkerhedsrolle, der er angivet til synlighed på virksomhedsenhedsniveau, nu se disse poster. Følgende eksempel viser, hvordan teams kan bruges til at give den korrekte adgang til disse poster.

+ Rollen "Sales Manager" er tildelt medlemmer af teamet "USMF Sales".
+ Brugere, der har rollen "Sales Manager", kan få adgang til alle firmaposter, der er medlemmer af den samme virksomhedsenhed, som de er medlem af.
+ Teamet "USMF Sales" er knyttet til den USMF-virksomhedsenhed, der er nævnt tidligere.
+ Derfor kan medlemmer af teamet "USMF Sales" se enhver konto, der ejes af brugeren "USMF DW", som ville være kommet fra USMF-firmaenheden i Finance and Operations.

![Sådan kan teams bruges](media/dual-write-company-2.png)

Som den foregående illustration viser, er denne 1:1-tilknytning mellem virksomhedsenhed, firma og team blot et udgangspunkt. I dette eksempel oprettes der manuelt en ny "Europe"-virksomhedsenhed i Common Data Service som overordnet til både DEMF og ESMF. Denne nye rodvirksomhedsenhed er ikke relateret til dobbeltskrivning. Den kan dog bruges til at give medlemmerne af "EUR Sales"-teamet adgang til kontodata i både DEMF og ESMF ved at indstille datasynlighed til **Parent/Child BU** i den tilknyttede sikkerhedsrolle.

Et sidste emne, der skal omtales, er, hvordan dobbeltskrivning afgør, hvilket ejerteam det skal tildeles poster. Denne funktionsmåde styres af feltet **Standardejerteam** på cdm\_Company-posten. Når en cdm\_Company-post er aktiveret til dobbeltskrivning, opretter en plug-in automatisk den tilknyttede virksomhedsenhed og ejerteamet (hvis den ikke allerede findes) og indstiller feltet **Standardejerteam**. Administratoren kan ændre dette felt til en anden værdi. Men administratoren kan ikke rydde feltet, så længe enheden er aktiveret til dobbeltskrivning.

> [!div class="mx-imgBorder"]
![Standardfelt for ejerskab af team](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Firma-striping og bootstrapping

Common Data Service-integration giver firmaparitet ved at bruge en firmaidentifikator til at stripe data. Som det fremgår af følgende illustration, udvides alle firmaspecifikke enheder, så de har en mange-til-en-relation (N:1) med enheden cdm\_Company.

> [!div class="mx-imgBorder"]
![N:1-relation mellem en firmaspecifik enhed og enheden cdm_Company](media/dual-write-bootstrapping.png)

+ Når et firma er tilføjet og gemt i poster, bliver værdien skrivebeskyttet. Derfor skal brugerne sørge for, at de vælger det rigtige firma.
+ Kun poster, der har firmadata, er kvalificerede til dobbeltskrivning mellem programmet og Common Data Service.
+ For eksisterende Common Data Service-data vil en administrativ bootstrapping-oplevelse snart være tilgængelig.
