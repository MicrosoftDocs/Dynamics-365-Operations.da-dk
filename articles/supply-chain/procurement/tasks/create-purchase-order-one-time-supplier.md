---
title: Oprette en indkøbsordre til en engangsleverandør
description: Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425024"
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