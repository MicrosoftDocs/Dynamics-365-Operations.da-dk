---
title: Oprette en indkøbsordre til en engangsleverandør
description: Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836306"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Oprette en indkøbsordre til en engangsleverandør

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en indkøbsordre for en engangsleverandør. Leverandøren oprettes automatisk sammen med indkøbsordren, så du skal ikke oprette kreditorkontoen manuelt. Indkøbsordrer oprettes typisk af en indkøbsagent. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Det er en forudsætning, at der er konfigureret en engangsleverandør på siden Kreditorparametre.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Oprette en indkøbsordre til en engangsleverandør
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Vælg Ja i feltet Engangsleverandør.
    * Der oprettes automatisk en kreditorkonto, som og tildeles til købsordren. Kreditorkontoen oprettes ud fra den skabelon, der er angivet under fanen Generelt på siden Kreditorparametre.  
4. Skriv et navn til leverandørne i feltet Navn.
5. Klik på OK.
    * Indkøbsordren kan nu udfyldes og behandles som enhver anden ordre. Der er ingen særlige kendetegn for, hvordan dette gøres. Fakturaen medregner en transaktion på den kreditorkonto, der blev oprettet til ordren, og betalingen vil derefter blive behandlet. Når dette er udført, kan kreditorkontoen slettes. Dette gøres typisk i kreditorafdelingen.  

