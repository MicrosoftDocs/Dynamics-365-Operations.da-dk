---
title: Forskelle mellem indbygget behovsplanlægning og planlægningsoptimering
description: Dette emne viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden for analyse af tilpasning af Planlægningsoptimering.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344948"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Forskelle mellem indbygget behovsplanlægning og planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Resultater af planlægningsoptimering kan være forskellige fra resultaterne af det indbyggede system til behovsplanlægning. Forskellene kan også skyldes ventende funktioner. Dette emne viser funktioner, som Planlægningsoptimering endnu ikke understøtter, og som ikke vises på siden **[Analyse af tilpasning af Planlægningsoptimering](planning-optimization-fit-analysis.md)]**.

| Funktion | Aktuel funktionsmåde i Planlægningsoptimering |
|---|---|
| Fastvægtprodukter | Fastvægtprodukter betragtes som almindelige produkter.|
| Dimensioner, der kan udvides | Dimensioner, der kan udvides, er tomme på ordreforslag, også selvom afkrydsningsfeltet **Dækningsplan efter dimension** er markeret på siden **Lagringsdimensionsgrupper** eller **Sporingsdimensionsgrupper**. |
| Filtrerede produktionskørsler | Yderligere oplysninger finder du i [Produktionsplanlægning – Filtre](production-planning.md#filters). |
| Hovedplanlægning | Budgetplanlægning understøttes ikke. Det anbefales, at du bruger behovsplanlægning, når der er knyttet en budgetmodel til behovsplanen. |
| Nummerserier for ordreforslag | Nummerserier for ordreforslag understøttes ikke. Ordreforslagsnumre genereres på tjenestesiden. |
| Plankopiering, sletning af plan og oprydning af planversion | <p>Følgende elementer deaktiveres under **Varedisponering \> Varedisponering \> Vedligeholdelse af planer** i navigationsruden:</p><ul><li>Plankopiering</li><li>Sletning af plan</li><li>Oprydning af planversion</li></ul> |
| Returordrer | Returordrer tages ikke i betragtning. |
| Planlægningsrelaterede funktioner | Nærmere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md#limitations). |
| Transportkalendere | Værdien i kolonnen **Transportkalender** på siden **Leveringsmåder** ignoreres. |

## <a name="additional-resources"></a>Yderligere ressourcer

- [Analyse af tilpasning af planlægningsoptimering](planning-optimization-fit-analysis.md)
- [Parametre, der ikke bruges af planlægningsoptimering](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
