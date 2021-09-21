---
title: Den lagerbeholdning, der ikke tages i betragtning som "batch over" varer
description: I nogle skabeloner til allokering kan der ikke være aktuelle lagerbeholdninger for varer, der ligger "batch over". Batch- eller serienummeret skal angives på behovsordren.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475904"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>I nogle skabeloner til allokering kan der ikke være aktuelle lagerbeholdninger for varer, der ligger "batch over"

## <a name="symptoms"></a>Symptomer

Allokeringsskabeloner med *Overvej beholdning* som kriterium tager ikke den aktuelle disponible lagerbeholdning i betragtning for *batch over*-varer. De tager kun højde for det, hvis batchnummeret er angivet på salgsordrelinjen.

Men når du bruger *batch under*-varer, anses den aktuelle lagerbeholdning for at være forventet.

Du kan finde flere oplysninger under [Lagerstedsallokering](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Løsning

Hovedet til allokeringsskabelonen kan defineres for behovsstrategien *Bestilt*, *Reserveret* eller *Frigivet*. I strategien *Bestilt* gælder de samme reservationshierarkikrav, der gælder for reservation eller frigivelse til lagerprocesser. Derfor skal der for *batch over*- og *serie under*-reservationshierarkier angives batch- eller serienummer på behovsordren (salg eller flytning).

Du kan også bruge behovsstrategien *Reserveret* til at vælge batch- eller serienummer, før der genereres behov for lagerstedsallokering.
