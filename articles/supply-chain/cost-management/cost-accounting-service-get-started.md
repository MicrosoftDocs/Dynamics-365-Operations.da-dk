---
title: Introduktion til omkostningsregnskabstjenesten
description: Dette emne indeholder licensoplysninger og installationsinstruktioner til omkostningsregnskabstjenesten.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276900"
---
# <a name="get-started-with-the-cost-accounting-service"></a>Introduktion til omkostningsregnskabstjenesten

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> De funktioner, der er anført i dette emne, er tilgængelige som en del af en privat prøveversion. Indholdet af dette emne og den funktionalitet, det beskriver, kan ændres. Du kan finde flere oplysninger om prøveversioner i [Ofte stillede spørgsmål om One Version-tjenesteopdateringer](../../fin-ops-core/fin-ops/get-started/one-version.md).

Med tjenesten til omkostningsregnskab kan du udføre flere lagerregnskaber i de finansposter for driftsregnskab, som du har oprettet. Du skal knytte hver finanspost for driftsregnskab til en *konvention*. En konvention er en samling af følgende typer regnskabspolitikker:

- Omkostningsobjekt
- Basis for inputmåling
- Forudsætning for omkostningsforløb
- Omkostningselement

> [!NOTE]
> Selv efter at du har slået omkostningsregnskabstjenesten til, kan du stadig udføre lagerregnskab i Microsoft Dynamics 365 Supply Chain Management som normalt.

Omkostningsregnskabstjenesten er et tilføjelsesprogram. For at gøre dets funktioner tilgængelige skal du installere det fra Microsoft Dynamics Lifecycle Services (LCS). Derfor kan du vælge at evaluere det i et testmiljø, før du slår det til i produktionsmiljøer.

Omkostningsregnskabstjenesten understøtter i øjeblikket ikke alle de funktioner til omkostningsstyring, der er indbygget i Dynamics 365 Supply Chain Management. Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt, opfylder dine behov.

## <a name="licensing"></a>Licensering

Omkostningsregnskabstjenesten er givet i licens sammen med standardfunktionerne i lagerregnskabet, der er tilgængelige for Supply Chain Management. Du behøver ikke at købe en ekstra licens for at bruge tjenesten til omkostningsregnskab.

## <a name="install-the-add-in"></a>Installer tilføjelsesprogrammet

> [!IMPORTANT]
> Hvis du vil bruge omkostningsregnskabstjenesten, skal du have et LCS-aktiveret miljø med høj tilgængelighed (ikke et OneBox-miljø), og du skal køre Dynamics 365 Supply Chain Management version 10.0.11 eller senere.

Hvis du vil bruge omkostningsregnskabstjenesten, skal du installere tilføjelsesprogrammet med omkostningsregnskabstjenesten til Supply Chain Management som beskrevet i følgende procedure.

1. Log på LCS.

1. Gå til **Styring af prøveversionsfunktion**.

1. Vælg plustegnet (**+**).

1. I feltet **Kode** skal du angive betanøglen til tilføjelsesprogrammet for omkostningsregnskabstjenesten. (Du skal have modtaget din nøgle pr. mail).

1. Vælg **Ophæv blokering**.

1. Åbn det LCS-miljø, hvor du vil tilføje tjenesten.

1. Gå til **Alle detaljer**.

1. Rul ned til oversigtspanelet **Tilføjelsesprogrammer for miljø**.

1. Vælg **Installer et nyt tilføjelsesprogram**.

1. Vælg **Omkostningsregnskabstjeneste**.

1. Følg installationsvejledningen, og accepter vilkårene og betingelserne.

1. Vælg **Installer**.

1. I oversigtspanelet **Miljøtilføjelsesprogrammer** kan du se, at tjenesten til omkostningsregnskab er ved at blive installeret. Efter nogle få minutter skal status ændres fra **Installerer** til **Installeret**. (Du skal muligvis opdatere siden for at se ændringen). På dette tidspunkt er omkostningsregnskabstjenesten klar til brug.

## <a name="set-up-the-integration"></a>Konfigurere integrationen

Sådan konfigurerer du integrationen mellem omkostningsregnskabstjenesten og Dynamics 365 Supply Chain Management:

1. Gå til **Systemadministration > Funktionsstyring**.

1. Vælg **Søg efter opdateringer**.

1. Åbn fanen **Alle**, og søg efter funktionen ved navn *Omkostningsregnskabstjeneste*.

1. Vælg **Aktiver nu**.

1. Gå til **Omkostningsstyring > Omkostningsregnskabstjeneste > Opsætning > Parametre for omkostningsregnskabstjeneste > Integrationsparametre**.

1. I feltet **Program-id** skal du angive følgende kode:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. I feltet **Datatjenesteslutpunkt** skal du angive følgende URL-adresse:<br>https://operationsdataservice.operations365.dynamics.com/

1. I feltet **Slutpunkt for omkostningsregnskabstjeneste** skal du angive følgende URL-adresse:<br>https://costaccountingservice.operations365.dynamics.com/

1. Omkostningsregnskabstjenesten er nu klar til brug.

## <a name="related-resources"></a>Tilknyttede ressourcer

[Startside for omkostningsregnskabstjeneste](cost-accounting-service-home.md)
