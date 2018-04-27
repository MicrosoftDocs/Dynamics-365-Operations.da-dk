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
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Konfigurere en betinget beslutning i en arbejdsgang

[!INCLUDE [banner](../includes/banner.md)]

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






