---
title: Oprette en indkøbsordre til en engangsleverandør
description: Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812366"
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