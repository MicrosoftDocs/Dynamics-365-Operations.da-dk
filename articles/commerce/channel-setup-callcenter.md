---
title: Konfigurere en callcenter-kanal
description: Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057873"
---
# <a name="set-up-a-call-center-channel"></a>Konfigurere en callcenter-kanal


[!include [banner](includes/banner.md)]

Dette emne beskriver, hvordan du opretter en ny callcenter-kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

I Dynamics 365 Commerce er et callcenter en type kanal, som kan defineres i programmet. Hvis du definerer en kanal til dit callcenter, kan systemet binde specifikke data og ordrebehandlingstandarder til salgsordrer. Et firma kan definere flere callcenter-kanaler i Commerce. 

Før du opretter en ny callcenter-kanal, skal du sikre dig, at du har fuldført [forudsætningerne for kanalopsætning](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Oprette og konfigurere en ny callcenter-kanal

Følg disse trin for at oprette en ny callcenter-kanal.

1. Gå til **Moduler \> Kanaler \> Callcentre \> Alle callcentre** i navigationsruden.
1. Gå til handlingsruden, og vælg **Ny**.
1. Skriv et navn til den nye kanal i feltet **Navn**.
1. Vælg den relevante **juridiske enhed** fra rullelisten.
1. Vælg det relevante **Lagersted** fra rullelisten.
1. Angiv en gyldig standardkunde i feltet **Standardkunde**.
1. Angiv en gyldig mailbeskedprofil i feltet **Profil til e-mail-besked**.
1. Angiv en oplysningskode for **Prisændring**. Bemærk! Du skal måske oprette en oplysningskode til dette først.
1. Angiv en oplysningskode for **Venteposition**. Bemærk! Du skal måske oprette en oplysningskode til dette først.
1. Angiv en oplysningskode for **Kredit**. Bemærk! Du skal måske oprette en oplysningskode til dette først.
1. Vælg **Gem**.

Følgende billede viser oprettelsen af en ny callcenter-kanal.

![Ny callcenter-kanal](media/channel-setup-callcenter-1.png)

Følgende billede viser et eksempel på en callcenter-kanal.

![Eksempel på call center-kanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Yderligere kanalopsætning

Yderligere opgaver, der kræves til konfiguration af callcenter-kanalen, omfatter opsætning af betalingsmetoder og leveringsmåder.

Følgende billede viser opsætningsindstillinger til **Leveringsmetoder** og **Betalingsmetoder** under fanen **Opsætning**.

![Yderligere handlinger til konfiguration af callcenter-kanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Oprette betalingsmåder

Hvis du vil oprette betalingsmetoder, skal du udføre disse trin for hver af de betalingstyper, der understøttes på denne kanal.

1. Vælg fanen **Opsætning** i handlingsruden, og vælg derefter **Betalingsmetoder**.
1. Gå til handlingsruden, og vælg **Ny**.
1. Vælg den ønskede betalingsmetode i navigationsruden.
1. Angiv et **Handlingsnavn** i sektionen **Generelt**, og konfigurer evt. andre ønskede indstillinger.
1. Konfigurer eventuelle yderligere indstillinger, der kræves for betalingstypen.
1. Gå til handlingsruden, og vælg **Gem**.

Følgende billede viser et eksempel på en metode til kontantbetaling.

![Eksempel på betalingsmetoder](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Konfigurer leveringsmåder

Du kan få vist de konfigurerede leveringsmåder ved at vælge **Leveringsmetoder** under fanen **Opsætning** i **Handlingsrude**.  

Udfør følgende trin for at ændre eller tilføje en leveringsmetode.

1. Gå til **Moduler \> Lagerstyring \> Leeringsmetoder** i navigationsruden.
1. Vælg **Ny** i handlingsruden for at oprette en ny leveringsmetode, eller vælg en eksisterende metode.
1. Vælg **Tilføj linje** i sektionen **Detailkanaler** for at tilføje kanalen. Tilføjelse af kanaler ved hjælp af organisationsnoder i stedet for at tilføje hver kanal individuelt kan strømline tilføjelsen af kanaler.

Følgende billede viser et eksempel på en leveringsmetode.

![Konfigurer leveringsmåder](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Forudsætninger for konfiguration af kanal](channels-prerequisites.md)

[Funktionalitet til callcenter-salg](call-center-functionality.md)

[Konfigurere indstillinger for callcenter-ordrebehandling](set-up-order-processing-options.md)

[Callcenter-kataloger](call-center-catalogs.md)

[Konfigurere og arbejde med advarsler om svindel](set-up-fraud-alerts.md)

[Oprette kontinuitetsprogrammer for callcentre](set-up-continuity-program.md)
