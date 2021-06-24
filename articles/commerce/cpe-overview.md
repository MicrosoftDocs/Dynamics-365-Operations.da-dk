---
title: Konfigurere en Dynamics 365 Commerce-oversigt
description: Dette emne indeholder en oversigt over evalueringsmiljøet til Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c890d7c49b6607ab0cbad536bbf8a3649465a7c1
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193486"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Konfigurere en Dynamics 365 Commerce-oversigt

[!include [banner](includes/banner.md)]

Dette emne indeholder en oversigt over evalueringsmiljøet til Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Miljøer til Commerce-evaluering er ikke generelt tilgængelige og tildeles til partnere og kunder efter anmodning. Du kan få flere oplysninger ved at rette henvendelse til din kontakt hos din Microsoft-partner.

Commerce-evalueringsmiljøet er et valgfrit altomfattende miljø til Dynamics 365 Commerce, som gør det muligt for partnere og potentielle kunder at afprøve Commerce-produktet.

Evalueringsmiljøer er delvist forudkonfigureret for at reducere de krævede trin efter klargøring.

Bortset fra nogle mindre begrænsninger, der ikke påvirker funktioner eller funktionalitet, giver Commerce-evalueringsmiljøet den komplette Commerce-oplevelse og kan bruges af kunder og implementeringspartnere til at evaluere produktet, give feedback og foretage fit-/GAP-analyse.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Begrænsninger i Commerce-evalueringsmiljøet

Selvom Commerce-evalueringsmiljøet indeholder det komplette sæt af Commerce-funktioner og -funktionalitet, er der nogle mindre begrænsninger:

- Selv om Commerce-evalueringsmiljøet i sig selv ikke har nogen geografiske begrænsninger, skal miljøets komponenter, såsom Retail Cloud Scale Unit (RCSU) og e-Commerce-programmer, klargøres i USA.
- Anvendelse af Commerce-evalueringsmiljøet er begrænset til 30 dage fra datoen for klargøringen af e-Commerce.
- Commerce-evalueringsmiljøet kan kun implementeres og initialiseres i et miljø, der bruger demotopologien, hvor alle komponenter i et miljø installeres i en enkelt skybaseret virtuel maskine (VM). Den væsentligste begrænsning for denne topologi er antallet af brugere, som miljøet kan understøtte samtidig.

## <a name="get-started"></a>Introduktion

Sådan klargør du Commerce-evalueringsmiljøet se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Klargøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md)

[Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md)

[Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø](cpe-bopis.md)

[Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø](cpe-optional-features.md)

[Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
