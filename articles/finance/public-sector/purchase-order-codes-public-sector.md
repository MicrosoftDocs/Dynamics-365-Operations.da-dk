---
title: Indkøbsordrekoder i den offentlige sektor
description: Dette emne indeholder oplysninger om koder og særlige meddelelser, der kan bruges til bekræftelse af indkøbsordrer.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConfirmingPOCodes, PurchTableListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 27291
ms.assetid: 65032886-4dc6-4411-98c8-8969287fd7df
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07dddec6e9cf9c949b2798808fdf36d092e7925b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984704"
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