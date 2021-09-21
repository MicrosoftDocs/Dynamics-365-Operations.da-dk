---
title: Tekst overskrives, når en vare konfigureres på en salgsordrelinje
description: Når et produkt konfigureres på en salgsordrelinje, overskrives den tilpassede tekst med standardtekst. Ændre teksten, efter at du har konfigureret linjen, og ikke før.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475858"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Varetekst overskrives, når et produkt konfigureres på en salgsordrelinje

## <a name="symptoms"></a>Symptomer

Dette problem opstår, når du opretter en salgsordrelinje for en vare, der kan konfigureres, og derefter redigere vareteksten. Når du konfigurerer varen og derefter vælger **OK**, overskrives teksten med standardteksten.

## <a name="resolution"></a>Løsning

Denne funktionsmåde forventes. Tekstfeltet indeholder variantnavnet, som kun er udfyldt, når du har konfigureret linjen. Derfor skal du ændre teksten, efter at du har konfigureret linjen, og ikke før.
