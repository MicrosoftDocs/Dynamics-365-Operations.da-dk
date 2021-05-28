---
title: Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer
description: Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026382"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomer

Feltet **Sidste testdato** opdateres ikke, når der oprettes flere kvalitetsordrer.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Den sidste testdato er ikke relateret til kvalitetsordrer. Den gemmer den dato, hvor de færdige varer blev købt eller produceret første gang. Denne dato bruges til at beregne hyldelevetidsvejledningsdatoen.
