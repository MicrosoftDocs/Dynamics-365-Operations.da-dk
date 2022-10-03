---
title: Indkøbsordrekoder i den offentlige sektor
description: Denne artikel indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer.
author: velofog
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: velofog
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27291
ms.assetid: 65032886-4dc6-4411-98c8-8969287fd7df
ms.search.industry: Public sector
ms.search.form: ConfirmingPOCodes, PurchTableListPage
ms.openlocfilehash: 9ad1a59fb0ae0be9f0d40ed8fb5919c71b27c180
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573123"
---
# <a name="purchase-order-codes-in-the-public-sector"></a>Indkøbsordrekoder i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer. En bekræftende indkøbsordre omgår den typiske indkøbsproces.

I denne artikel beskrives funktionerne i de indkøbsordrekoder, der er tilgængelige for den offentlige sektor. Du skal først afgøre, hvad din koder og meddelelser skal være. Du kan bruge siden **Bekræfter koder til indkøbsordrer** for at oprette koder og specielle meddelelser, der kan bruges til bekræftelse af indkøbsordrer (POs). En bekræftende indkøbsordre omgår den typiske indkøbsproces. For eksempel skal du tillade en ikke-planlagt ordre ved hjælp af et PO-nummer på tidspunktet for et køb i stedet for ved hjælp af et dokument, der er leveret, før varen er påkrævet. 

Når du har oprettet koderne, kan du tildele koderne til indkøbsordrer på siden **Alle indkøbsordrer**. 

Hvis du tildeler en bekræftende PO-kode til en indkøbsordre på oversigtspanelet **Ikke-planlagt køb** (for eksempel, når du opretter en ny indkøbsordre), bliver den meddelelse, der er knyttet til den bekræftende PO-kode, udskrevet øverst på indkøbsordren.

## <a name="tips"></a>Tip!
-   Hvis du ændrer en bekræftende PO-kode, der allerede er tildelt til en indkøbsordre, erstatter den nye kode den gamle. Denne ændring påvirker både nye indkøbsordrer og produktionsordrer, der er bogført. En indkøbsordre havde f.eks. en bekræftende PO-kode for **Bekræfter**, da den blev bogført, men den pågældende kode er senere ændret til **Nødstilfælde**. I dette tilfælde vil hver indkøbsordre, der havde koden **Bekræfter**, nu have koden **Nødstilfælde** i stedet.
-   Du kan oprette meddelelser på forskellige sprog. Denne funktion kan være en hjælp, når du køber fra handlende i andre lande/områder. Organisationen har f.eks. hjemsted i et engelsktalende land eller område, og du vil oprette en spansk meddelelse for bekræftende indkøbsordrer, som har en bekræftende PO-kode **Bekræfter**.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
