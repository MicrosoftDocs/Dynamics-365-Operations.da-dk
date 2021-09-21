---
title: Du kan ikke slette et frigivet produkt
description: Du kan kun slette et frigivet produkt og alle dets varianter, hvis der ikke er relaterede transaktioner for det frigivne produkt.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475936"
---
# <a name="you-cant-delete-a-released-product"></a>Du kan ikke slette et frigivet produkt

## <a name="symptoms"></a>Symptomer

Du kan kun slette et frigivet produkt og alle dets varianter, hvis der ikke er relaterede transaktioner for det frigivne produkt.

## <a name="resolution"></a>Løsning

Udfør følgende trin for at slette en frigivet produkt eller produktmaster.

1. Luk alle åbne transaktioner for varerne.
1. Reducer lagerbeholdningen til 0 (nul).
1. Udfør lagerlukning.
1. Slet alle produktvarianter for den produktmaster, du vil slette.
