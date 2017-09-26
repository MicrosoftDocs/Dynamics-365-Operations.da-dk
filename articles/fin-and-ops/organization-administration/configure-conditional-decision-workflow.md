---
title: Konfigurere en betinget beslutning i en arbejdsgang
description: "Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurere en betinget beslutning i en arbejdsgang

[!include[banner](../includes/banner.md)]


Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning.

En betinget beslutning er et punkt, hvor en arbejdsgang opdeles i to forgreninger. Hvis du vil konfigurere en betinget beslutning i arbejdsgangseditoren, skal du højreklikke på den betingede beslutning og derefter klikke på **Egenskaber** for at åbne formen **Egenskaber**.

## <a name="name-a-decision"></a>Navngive en beslutning
Benyt denne fremgangsmåde til at angive et navn på den betingede beslutning.
1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Angiv et entydigt navn på den betingede beslutning i feltet **Navn**.

## <a name="set-conditions"></a> Angive betingelser
Systemet bestemmer, hvilken forgrening der skal bruges, ved at evaluere det sendte dokument for at afgøre, om det opfylder bestemte betingelser.
1.  Klik på **Grundlæggende indstillinger** i venstre rude.
2.  Klik på **Tilføj betingelse**.
3.  Angiv en betingelse.
4.  Angiv supplerende betingelser, hvis det er påkrævet.
5.  Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du udføre følgende trin:
    1.  Klik på **Test** for at åbne formen **Test betingelse for arbejdsgang**.
    2.  Vælg en post i området **Valider betingelse** i formen.
    3.  Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.
    4.  Klik på **OK** eller **Annuller** for at vende tilbage til formen **Egenskaber**.






