---
title: Oprette en indkøbsordre til en engangsleverandør
description: Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ffb6515d8f24df68efbce265d98ed4e64e8d6b07
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677416"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Oprette en indkøbsordre til en engangsleverandør

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør. Leverandøren oprettes automatisk sammen med indkøbsordren, så du skal ikke oprette kreditorkontoen manuelt. Indkøbsordrer oprettes typisk af en indkøbsagent. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Det er en forudsætning, at der er konfigureret en engangsleverandør på siden Kreditorparametre.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Oprette en indkøbsordre til en engangsleverandør
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Vælg Ja i feltet Engangsleverandør.
    * Der oprettes automatisk en kreditorkonto, som og tildeles til købsordren. Kreditorkontoen oprettes ud fra den skabelon, der er angivet under fanen Generelt på siden Kreditorparametre.  
4. Skriv et navn til leverandørne i feltet Navn.
5. Klik på OK.
    * Indkøbsordren kan nu udfyldes og behandles som enhver anden ordre. Der er ingen særlige kendetegn for, hvordan dette gøres. Fakturaen medregner en transaktion på den kreditorkonto, der blev oprettet til ordren, og betalingen vil derefter blive behandlet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]