---
title: Oversigt over Dynamics 365 Commerce-prøveversionsmiljø
description: Dette emne indeholder en oversigt over prøveversionsmiljøet til Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024677"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>Oversigt over Dynamics 365 Commerce-prøveversionsmiljø


[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over prøveversionsmiljøet til Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversigt

Commerce-prøveversionsmiljøet er et valgfrit altomfattende prøveversionsmiljø til Dynamics 365 Commerce, som gør det muligt for potentielle kunder at afprøve Commerce-produktet før dets generelle offentlige udgivelse.

Bortset fra nogle mindre begrænsninger, der ikke påvirker funktioner eller funktionalitet, giver Commerce-prøveversionsmiljøet den komplette Commerce-oplevelse og kan bruges af kunder og implementeringspartnere til at evaluere produktet, give feedback og foretage fit-/GAP-analyse.

## <a name="limitations-of-the-commerce-preview-environment"></a>Begrænsninger i Commerce-prøveversionsmiljøet

Selvom Commerce-prøveversionsmiljøet indeholder det komplette sæt af Commerce-funktioner og -funktionalitet, er der nogle mindre begrænsninger:

- Selv om Commerce-prøveversionsmiljøet i sig selv ikke har nogen geografiske begrænsning, kan miljøets komponenter, såsom Retail Cloud Scale Unit (RCSU) og e-Commerce-programmer, kun klargøres i USA.
- Anvendelse af Commerce-prøveversionsmiljøet er begrænset til 30 dage fra datoen for klargøringen af e-Commerce.
- Commerce-prøveversionsmiljøet kan kun implementeres og initialiseres i et miljø, der bruger demotopologien, hvor alle komponenter i et miljø installeres i en enkelt virtuel maskine (VM). Den væsentligste begrænsning for denne VM-topologi med én boks er antallet af brugere, som prøveversionsmiljøet kan understøtte samtidig.
- Commerce-prøveversionsmiljøet kan kun evalueres indtil Commerce-produktet gøres generelt tilgængeligt (GA). Nye demo-miljøer vil være tilgængelige efter GA.

## <a name="get-started"></a>Introduktion

Hvis du vil klargør Commerce-prøveversionsmiljøet se [Klargøring af et Commerce-prøveversionsmiljø](provisioning-guide.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Klargøre et Dynamics 365 Commerce-prøveversionsmiljø](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø](cpe-post-provisioning.md)

[Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø](cpe-faq.md)
