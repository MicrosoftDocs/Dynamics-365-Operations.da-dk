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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742022"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Feltet Sidste testdato opdateres ikke, når der oprettes flere kvalitetsordrer

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomer

Feltet **Sidste testdato** opdateres ikke, når der oprettes flere kvalitetsordrer.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Den sidste testdato er ikke relateret til kvalitetsordrer. Den gemmer den dato, hvor de færdige varer blev købt eller produceret første gang. Denne dato bruges til at beregne hyldelevetidsvejledningsdatoen.
