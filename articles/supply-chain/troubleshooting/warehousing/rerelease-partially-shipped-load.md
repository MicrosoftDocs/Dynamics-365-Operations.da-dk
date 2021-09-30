---
title: Kan ikke gen-frigive en delvist leveret last til lagerstedet
description: I tidligere versioner kunne du ikke frigive en delvist afsendt belastning igen ved brug af visse funktioner med ufuldstændige reservationer. Dette er blevet løst.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475921"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Kan ikke gen-frigive en delvist leveret last til lagerstedet

## <a name="symptoms"></a>Symptomer

Du kan ikke frigive en delvist leveret last til lagerstedet. Når du foretager frigivelsen til lagerstedet, vises meddelelsen "Handlingen er fuldført", men der sker ingenting, og der oprettes ikke noget arbejde for det resterende antal. Dette problem opstår, når du bruger funktionaliteten til transport af last, og der er en ufuldstændig reservation.

## <a name="resolution"></a>Løsning

[KB-fejl 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Delvist leverede laster kan få ny bølge og genbehandles") er løst [version 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).