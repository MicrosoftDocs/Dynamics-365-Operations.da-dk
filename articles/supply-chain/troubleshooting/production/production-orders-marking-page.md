---
title: Produktionsordrer vises ikke på siden Afmærkning
description: Nogle produktionsordrer vises ikke på siden Afmærkning. Dette emne indeholder en forklaring på de tre produktkonfigurationer, der ikke kan markeres.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475850"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Produktionsordrer vises ikke på siden Afmærkning

## <a name="symptoms"></a>Symptomer

Når der arbejdes med fremstilling, vises visse produktionsordrer ikke på **afmærkningssiden**.

## <a name="resolution"></a>Løsning

Produkter, der har følgende konfigurationer, er ikke tilgængelige til afmærkning. Derfor vil de ikke blive vist på siden **Afmærkning**:

- Produkterne defineres som produkter af typen *fastvægt*.
- De er aktiveret for de avancerede lagerprocesser.
- De konfigureres til at blive kontrolleret med *Standardomkostning*-princippet.
