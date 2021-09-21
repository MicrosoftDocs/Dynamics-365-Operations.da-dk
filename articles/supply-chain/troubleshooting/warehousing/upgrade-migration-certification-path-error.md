---
title: Fejl i certificeringssti ved opgradering eller overflytning til WMS
description: Hvis appen viser fejlen "Trust anker til certificeringsstien, der ikke blev fundet" ved opgradering eller overflytning til WMS, indeholder denne side oplysninger om, hvordan problemet kan afhjælpes.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475878"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Tillidsanker til certificeringsstien blev ikke fundet ved opdatering og overflytning til WMS

## <a name="symptoms"></a>Symptomer

Når du opgraderer og overflytninger til WMS (Advanced Warehouse Management), vises der muligvis følgende fejlmeddelelser i appen Lokationsstyring:

> java.security.cert.certPathValidatorException: Tillidsanker for certificeringsstien blev ikke fundet.

## <a name="cause"></a>Årsag

Det sker, fordi der ikke er tillid til selv underskrevne certifikater i Android 8+ i miljøer med det lokale miljø.

## <a name="resolution"></a>Løsning

Brug et eksternt (offentligt) nøglecenter. Der findes en rettelse til dette problem i version 1.9.0.0 af Warehouse Management-appen. Du kan finde flere oplysninger om dette problem, og hvordan du løser det, under [Trust-anker for certificeringsstien, der ikke blev fundet ved oprettelse af app-forbindelse](certification-path-app-connection-error.md).
