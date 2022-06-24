---
title: Global A-skat
description: Denne artikel indeholder oplysninger om den globale funktion for A-skat og opsætningen af den. Funktionen til global A-skat er forbedret for leverandør- og debitorposteringer, så A-skat beregnes på vareniveau.
author: kailiang
ms.date: 01/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "15721"
- intro-internal
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 49d5048b9df30e94d959cf9f22b8ae837b74abdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846822"
---
# <a name="global-withholding-tax"></a>Global A-skat

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om den globale funktion for A-skat og forklarer opsætningen af den. Den nye funktionalitet er tilgængelig i version 10.0.17 og nyere.

Funktionen til global A-skat er forbedret for leverandør- og debitorposteringer, så A-skat beregnes på vareniveau. Saldoen på kontoen for A-skat fra købsposteringer kan udlignes ved at køre betalingsjobbet for A-skat mod afregningskontoen for A-skat.

> [!NOTE]
> Global A-skat understøtter ikke funktionen **Vedligehold gebyrer** på indkøbsordre-, kreditorfaktura- og salgsordresiderne.

## <a name="turn-on-global-withholding-tax"></a>Aktivere global A-skat

1. I området **Funktionsstyring** skal du vælge **Global A-skat** og derefter **Aktivér nu**.
2. Gå til **Moms \> Opsætning \> Parametre \> Finansparametre**, og under fanen **A-skat** skal du angive **Ja** option to **Aktiver global A-skat**.
3. Vælg **Gem**.
4. Opdater siden i webbrowseren.

> [!NOTE]
> Funktioner for global A-skat kan ikke være aktiveret for lande/områder, hvor der allerede findes lokale løsninger for A-skat. Disse områder omfatter, men er ikke begrænset til Indien, Brasilien, Thailand, Saudi-Arabien, Irland, Storbritannien og USA.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
