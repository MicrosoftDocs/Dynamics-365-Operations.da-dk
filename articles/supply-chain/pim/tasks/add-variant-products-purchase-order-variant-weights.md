---
title: Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt
description: Denne procedure gennemgår trinnene for brug af variantvægte til automatisk udfyldning af indkøbsordrelinjer for hver variant af et produkt.
author: t-benebo
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f9523410447c102481dd2c709b1fa3dd69d03e8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565636"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Tilføje variantprodukter til indkøbsordrer ved hjælp af varianters vægt

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]