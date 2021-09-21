---
title: Rettelse af leveringsnote kan ikke behandles
description: Hvis du prøver at rette en leveringsnota, efter at den er bogført, får du vist en fejl. Denne side forklarer, hvordan bogførte følgesedler korrigeres for varer, der er aktiveret for WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475930"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Rettelse af leveringsnote kan ikke behandles

## <a name="symptoms"></a>Symptomer

Når du har bogført en følgeseddel, kan du ikke annullere den, fordi knappen **Annuller** ikke er tilgængelig. Du kan heller ikke rette følgesedlen. Hvis du prøver, modtager du følgende fejlmeddelelse:

> Rettelse af leveringsnote kan ikke behandles. Følgeseddel indeholder kun varer, der er underlagt warehouse management-processer, da disse ikke understøttes af korrektion af følgeseddel.

## <a name="resolution"></a>Løsning

Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for avanceret Warehouse Management (WMS), skal bogføringen ske fra lasten, ikke direkte fra ordren.
