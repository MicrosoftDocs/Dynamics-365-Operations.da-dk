---
title: Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt
description: Denne procedure gennemgår trinnene for brug af variantvægte til automatisk udfyldning af indkøbsordrelinjer for hver variant af et produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "345484"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure gennemgår trinnene for brug af variantvægte til automatisk udfyldning af indkøbsordrelinjer for hver variant af et produkt. Når du vælger mængden af produktet, du vil købe, oprettes der indkøbsordrelinjer for alle varianter af produktet med foreslåede mængder, der er baseret på de vægte, der er konfigureret i produktvarianterne. Denne procedure omfatter ikke trin til at konfigurere vægtværdier for produktdimensioner og produktvarianter. Denne procedure bruger USRT-firmaets demodata.

1. Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Slå udvidelsen af sektionen Generelt til/fra.
6. Klik på rullelisten i feltet Sted for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Klik på OK.
12. Slå udvidelsen af sektionen Linjedetaljer til/fra.
13. Klik på fanen Varianter.
14. Klik på Tilføj linje.
15. Markér den valgte række på listen.
16. I feltet Varenummer skal du skrive "0140".
17. Angiv antallet til '1000'.
18. Klik på Gem.

