---
title: Vare RM kan ikke reserveres fuldt ud, når en produktionsordre frigives
description: 'Når du frigiver en produktionsordre, kan du få fejlen: "Vare RM kunne ikke reserveres fuldt ud." Sørg for, at hele mængden er til rådighed, eller reserver varer manuelt.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475931"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Vare RM kan ikke reserveres fuldt ud, når en produktionsordre frigives

## <a name="symptoms"></a>Symptomer

Hvis ikke alle styklistelinjevarer er fysisk tilgængelige, når en produktionsordre frigives til et lagersted, og **Frigiv til lagersted**-politikken er angivet til *Kræv fuld reservation* på produktionsordren, vises følgende fejlmeddelelse:

> Vare-RM kunne ikke reserveres fuldt ud. Sørg for, at hele antallet er tilgængeligt, eller reservér varerne manuelt, hvis feltet Reservation på styklistelinjen er angivet til Manuel eller Startet. Ordren kunne ikke frigives til lagersted, fordi nogle materialer ikke kunne reserveres.

## <a name="resolution"></a>Løsning

Denne funktionsmåde er tilsigtet og fungerer som forventet. Du kan løse dette problem ved at følge vejledningen i fejlmeddelelsen: "Sørg for, at det fulde antal er til rådighed, eller reserver varerne manuelt, hvis feltet Reservation på styklistelinjen er angivet til Manuel eller Startet."
