---
title: Konfigurere betingede beslutninger i en arbejdsgang
description: Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36c4ff32a4cb6d10e363a1522cb48823c4f491dabe2845d390147b42cdfcec4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712237"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Konfigurere betingede beslutninger i en arbejdsgang

[!include [banner](../includes/banner.md)]

Brug følgende procedure for at konfigurere egenskaberne for den betingede beslutning.

En betinget beslutning er et punkt, hvor en arbejdsgang opdeles i to forgreninger. Hvis du vil konfigurere en betinget beslutning i arbejdsgangseditoren, skal du højreklikke på den betingede beslutning og derefter klikke på **Egenskaber** for at åbne formen **Egenskaber**.

## <a name="name-a-decision"></a>Navngive en beslutning

Benyt denne fremgangsmåde til at angive et navn på den betingede beslutning.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Angiv et entydigt navn på den betingede beslutning i feltet **Navn**.

## <a name="set-conditions"></a>Angive betingelser

Systemet bestemmer, hvilken forgrening der skal bruges, ved at evaluere det sendte dokument for at afgøre, om det opfylder bestemte betingelser.

1. Klik på **Grundlæggende indstillinger** i venstre rude.
2. Klik på **Tilføj betingelse**.
3. Angiv en betingelse.
4. Angiv supplerende betingelser, hvis det er påkrævet.
5. Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du udføre følgende trin:

    1. Klik på **Test** for at åbne formen **Test betingelse for arbejdsgang**.
    2. Vælg en post i området **Valider betingelse** i formen.
    3. Klik på **Test**. Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.
    4. Klik på **OK** eller **Annuller** for at vende tilbage til formen **Egenskaber**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]