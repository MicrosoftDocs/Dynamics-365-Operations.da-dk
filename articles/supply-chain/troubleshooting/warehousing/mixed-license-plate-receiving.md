---
title: Modtagelse af blandede id'er fungerer ikke for alle dispositionskoder
description: Når Handling-feltet for en dispositionskode er sat til Kredit eller Kasseres, kan du kun bruge menupunktet Modtagelse af blandede id'er til at behandle returvarer.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475929"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Modtagelse af blandede id'er fungerer ikke for nogen dispositionskode med Kredit

## <a name="symptoms"></a>Symptomer

Når **Handling**-feltet for en dispositionskode er sat til *Kredit* eller *Kasseres*, kan du kun bruge menupunktet [Modtagelse af blandede id'er](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) til at behandle returvarer.

## <a name="resolution"></a>Løsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. Aktuelt er det kun [dispositionskoder](/dynamics365/supply-chain/service-management/set-up-disposition-codes), hvor feltet **Handling** er indstillet til *Kredit* eller *Kasseres*, der understøttes til modtagelse af blandede id'er.
