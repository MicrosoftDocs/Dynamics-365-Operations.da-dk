---
title: Produktbekræftelse for klyngepluk
description: I dette emne beskrives, hvordan du opretter varebekræftelse sammen med klyngepluk.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367286"
---
# <a name="product-confirmation-for-cluster-picking"></a>Produktbekræftelse for klyngepluk

[!include [banner](../includes/banner.md)]

Med pluk af klyngen kan du plukke varer til flere ordrer samtidig. Når der anvendes en klyngepluk, er varebekræftelse afgørende for kontrol af de varer, der føjes til klynger. Du kan kontrollere varer i klyngepluk under klyngeplukprocessen.

## <a name="where-it-applies"></a>Hvor det er relevant

Varekontrol for klyngepluk fungerer på samme måde, som når du kontrollerer varer i en ikke-klynge plukproces. Opsætningen er baseret på opsætningen af produktets stregkode.

## <a name="set-up-item-verification-with-cluster-picking"></a>Konfigurer varekontrol med klyngepluk

1. I menupunktet på en mobilenhed skal du åbne opsætningsformularen for arbejdsbekræftelse: **Lokationsstyring** > **Lokationsstyring** > **Opsætning** > **Mobilenhed** > **Menupunkter i mobilenhed**.
1. Åbn **Konfiguration af arbejdsbekræftelse** fra menupunktet på mobilenheden.

|        Indstilling        |                                    Betegnelse                                    |
|----------------------|-----------------------------------------------------------------------------------|
| Bekræftelse af produkt | Gør det muligt for dig at kontrollere hver enkelt vare på lageret fra mobilenheden, når den scannes. |
