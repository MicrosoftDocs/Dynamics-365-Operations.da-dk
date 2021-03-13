---
title: Introduktion til omkostningsregnskabstjenesten (privat visning)
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011841"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Introduktion til omkostningsregnskabstjenesten (privat visning)

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

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Sådan får du omkostningsregnskabstjenesten (privat visning)

> [!IMPORTANT]
> Hvis du vil bruge omkostningsregnskabstjenesten, skal du have et LCS-aktiveret miljø med høj tilgængelighed (ikke et OneBox-miljø), og du skal køre Dynamics 365 Supply Chain Management version 10.0.11 eller senere.

Hvis du vil tilmelde dig den private visning af omkostningsregnskabstjenesten, skal du sende dit LCS-miljø-ID med e-mail til [Omkostningsregnskabstjeneste (privat visning)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Når vi godkender dig til programmet, sender vi dig en opfølgnings-e-mail, der indeholder en betanøgle til omkostningsregnskabstjenesten. Når du modtager betanøglen, kan du fortsætte ved at [installere tilføjelsesprogrammet](#install).

## <a name="licensing"></a>Licensering

Omkostningsregnskabstjenesten er givet i licens sammen med standardfunktionerne i lagerregnskabet, der er tilgængelige for Supply Chain Management. Du behøver ikke at købe en ekstra licens for at bruge tjenesten til omkostningsregnskab.

## <a name="install-the-add-in"></a><a name="install"></a>Installer tilføjelsesprogrammet

Hvis du vil bruge omkostningsregnskabstjenesten, skal du installere tilføjelsesprogrammet med omkostningsregnskabstjenesten til Supply Chain Management som beskrevet i følgende procedure.

1. [Tilmeld dig](#sign-up) til omkostningsregnskabstjenesten (privat visning).

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
