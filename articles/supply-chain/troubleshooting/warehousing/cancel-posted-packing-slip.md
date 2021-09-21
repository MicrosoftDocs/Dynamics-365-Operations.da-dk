---
title: Kan ikke annullere en følgeseddel, når den er bogført fra en salgsordre
description: Når pluk- og forsendelsesprocesser er aktiveret for WMS, kan du ikke annullere en følgeseddel, når den er bogført fra en salgsordre. På denne side kan du finde en løsning.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475957"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Kan ikke annullere en følgeseddel, når den er bogført fra en salgsordre

## <a name="symptoms"></a>Symptomer

Når pluk- og forsendelsesprocesser er aktiveret for avanceret Warehouse Management (WMS), kan du ikke annullere en følgeseddel, når den er bogført fra en salgsordre.

## <a name="resolution"></a>Løsning

Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for WMS, skal bogføringen ske fra lasten, ikke fra ordren. Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.  

Generelt kan en salgsordre, der er plukket og afsendt via warehouse management-processer, få opdateret følgeseddel fra lasen eller forsendelsen og selve salgsordredokumentet. Men hvis du opdaterer følgeseddel på salgsordren fra salgsordredokumentet, kan tilbageførslen af følgesedlen stadig ikke udføres fra last- eller salgsordren. Det anbefales derfor, at du bruger bogføring af følgesedlen fra lasten. I dette tilfælde vil tilbageførsel, der foretages fra lasten, blive aktiveret.
