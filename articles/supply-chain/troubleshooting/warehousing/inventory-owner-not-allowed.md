---
title: Lagerejeren er ikke tilladt ved behandling af bevægelser
description: Du kan få vist fejlen, "Lagerejeren %1 er ikke tilladt". I øjeblikket understøtter processerne i lagerstedsstyring kun det lager, der ejes af den juridiske enhed.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475880"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Lagerejeren er ikke tilladt ved behandling af bevægelser i lagerstedsappen

## <a name="symptoms"></a>Symptomer

Du får vist denne fejlmeddelelse i mobilappen Warehouse Management, når du scanner et nummerplade-id.

> Lagerejeren %1 er ikke tilladt i denne proces.

## <a name="cause"></a>Årsag

Sporingsdimensionen **Ejer** mangler, når mobilappen Warehouse management bruges til at foretage bevægelser. En almindelig lageroverførselskladde fra Supply Chain Management-klienten ser ud til at fungere efter hensigten og kan kun bogføres, hvis dimensionen **Ejer** er udfyldt.

## <a name="resolution"></a>Løsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. I øjeblikket understøtter lagerstyringsprocesser kun det lager, der ejes af den juridiske enhed.
