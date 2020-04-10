---
title: " Oprette produktpakker til indkøbsordrer"
description: Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b0084c6b4acbf14e3afec552575d5be26114237
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141355"
---
# <a name="create-product-packages-for-purchase-orders"></a> Oprette produktpakker til indkøbsordrer

[!include [banner](../includes/banner.md)]

Denne procedure gennemgår oprettelse af en produktpakke og brugen af den i en indkøbsordre. Indkøbsordren skal bruges til at oprette en ordre på et foruddefineret sæt produkter. Proceduren bruger USRT-demodatafirmaet.


## <a name="create-a-product-package"></a>Oprette en produktpakke
1. Gå til Retail og Commerce > Lagerstyring > Genopfyldning > Produktpakker.
2. Klik på Ny.
3. Skriv en værdi i feltet Pakkenummer.
4. Skriv en værdi i feltet Beskrivelse.
5. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
7. Klik på Tilføj.
8. I feltet Varenummer skal du skrive "0160".
9. Klik på rullelisten i feltet Størrelse for at åbne opslaget.
10. Klik op linket i den valgte række på listen.
11. Angiv et tal i feltet Antal.
12. Klik på Tilføj.
13. I feltet Varenummer skal du skrive "0160".
14. Klik på rullelisten i feltet Variantnummer for at åbne opslaget.
15. Klik op linket i den valgte række på listen.
16. Angiv et tal i feltet Antal.
17. Klik på Tilføj.
18. I feltet Varenummer skal du skrive "0175".
19. Angiv et tal i feltet Antal.
20. Klik på Gem.
21. Luk siden.

## <a name="add-package-to-purchase-order"></a>Føje pakke til indkøbsordre
1. Gå til Kreditor > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.
4. Vælg den samme leverandør, som produktpakken tidligere blev oprettet for, på listen, hvis der blev valgt en leverandør.
5. Slå udvidelsen af sektionen Generelt til/fra.
6. Klik på rullelisten i feltet Sted for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet Lagersted for at åbne opslaget.
9. Klik op linket i den valgte række på listen.
10. Klik på OK.
11. Slå udvidelsen af sektionen Linjedetaljer til/fra.
12. Klik på fanen Produktpakker.
13. Klik på Indkøbsordrelinje.
14. Klik på Opret linjer fra pakke.
15. Find og vælg på listen den produktpakke, der blev oprettet i forrige trin.
16. Angiv et tal i feltet Antal.
17. Klik på Opret.
18. Klik på Gem.

