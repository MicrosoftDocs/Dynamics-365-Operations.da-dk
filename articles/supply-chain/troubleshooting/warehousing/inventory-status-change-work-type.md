---
title: Kan ikke vælge ændring af lagerstatus i kolonnen Arbejdstype
description: Du kan ikke oprette en arbejdsskabelonlinje for ændring af lagerstatus, fordi arbejdstypen kun bruges af systemprocesser. Vælg en anden arbejdstype.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475938"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Kan ikke vælge ændring af lagerstatus i kolonnen Arbejdstype

## <a name="symptoms"></a>Symptomer

Når du konfigurerer Microsoft Dynamics 365 Supply Chain Management, vises der muligvis følgende fejlmeddelelse:

> Du kan ikke oprette en arbejdsskabelonlinje for ændring af lagerstatus, fordi arbejdstypen ikke er gyldig. Vælg en anden arbejdstype.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet. Arbejdstypen *Ændring af lagerstatus* bruges kun i forbindelse med systemprocesser. Den kan ikke konfigureres. Da listen over arbejdstyper er fastlagt som en fasttekst, kan de ekstra poster ikke filtreres fra rullemenuen **Arbejdstype**.
