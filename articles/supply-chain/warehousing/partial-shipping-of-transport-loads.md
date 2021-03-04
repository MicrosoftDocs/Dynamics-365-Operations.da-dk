---
title: Delvis forsendelse af en transportlast
description: Dette emne forklarer, hvordan du kan afsende en last delvist og udskyde planlægning af kapaciteten for lasten.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424510"
---
# <a name="partial-shipment-of-a-transport-load"></a>Delvis forsendelse af en transportlast

[!include[banner](../includes/banner.md)]

Ved at oprette en delvis lastforsendelse kan du håndtere laster, hvor kapaciteten ikke kan fastslås, før alle de salgslinjer er føjet til en last. Processen kan derefter afsluttes, når det nøjagtige palleantal er kendt. Du behøver derfor ikke beslutte, hvilke paller der tildeles hvilken transport, indtil det øjeblik hvor en transport lastes fysisk fra det midlertidige lager.

Denne funktion giver et alternativ til overholdelsen af en strengere struktur, hvor du skal bestemme, hvilke paller der tildeles hvilken transport, før pluk- eller lastningsarbejdet kan oprettes. I stedet kan brugere konfigurere individuelle laster til bekræftelse af en dellevering. Transportens lastningsprocesser for disse laster kan derefter udføres. Derfor kan afdelingen for fragtplanlægning planlægge laster uden at overveje kapaciteten for de enkelte transporter.

På lastningstidspunktet kan arbejdere definere en ny transportlast, som en palle kan lastes til. De kan også identificere en eksisterende transportlast. Disse data kan registreres via en mobilenhed. Derfor kan flere lagermedarbejdere laste lagervarer fra samme laster eller forskellige laster på samme lastbil. Lasterne kan derefter blive leveret helt eller delvist.

> [!NOTE] 
> For at laste lager fra en last til en bestemt transportlast og delvist levere lasten, skal arbejdet genereres ved hjælp af en lastningsklasse i en arbejdsskabelon. Almindeligt plukarbejde af typen **Pluk** lastes til en transportlast som f.eks. en lastbil.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Konfigurere transportlast til delvis levering

Opsætningen af delleveringer af laster består af følgende to procedurer.

### <a name="set-the-loading-strategy"></a>Konfigurere lastningsstrategi

Du skal aktivere delvis lastning ved at angive lastningsstrategien. Når du har oprettet lastningsstrategien, efter du har oprettet en last.

1. Vælg **Lokationsstyring** \> **Laster** \> **Alle laster**.
2. Vælg en last, og klik derefter på **Hoved**.
3. I feltet **Lastningsstrategi** skal du vælge **Afsendelse af delvis last er tilladt**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Oprette et menupunkt til lastning af transportlaster

Du skal oprette et nyt menupunkt, der muliggør lastning af transportlaster. En transportlast gør det muligt at gruppere arbejdslinjer fra en eller flere laster. Alt, der føjes til transportlasten, kan derefter afsendes ved hjælp af en mobil scanner.

1. Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.
2. Vælg **Ny**, og i feltet **Tilstand** skal du derefter vælge **Arbejde**.
3. Angiv indstillingen **Brug eksisterende arbejde** til **Ja**.
4. På fanen **Generelt** i feltet **Ledet af** skal du vælge **Lastning af transport**.
5. For at muliggøre bekræftelse af en forsendelse på en mobil scanner skal du åbne feltet **Tilladt type for bekræftelse af afsendelse** og vælge **Transportlast**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Bekræfte afsendelse af en transportlast fra klienten

Denne opsætning gør det muligt at bekræfte en transportlast, der omfatter en fuld last eller en delvist lastet last, der skal afsendes.

1. Vælg **Lokationsstyring** \> **Laster** \> **Transportlaster**.
2. I handlingsruden på fanen **Lever og modtag**, i gruppen **Bekræft** skal du vælge **Transport**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]