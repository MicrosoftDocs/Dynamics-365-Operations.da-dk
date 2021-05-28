---
title: Når et fastvægtantal opdeles, bruges minimumantallet i stedet for det nominelle antal
description: Når et fastvægtantal opdeles i batches, bruger feltet Plukantal det minimumantal, der er angivet for varen, og ikke det nominelle antal.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026380"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Når et fastvægtantal opdeles, bruges minimumantallet i stedet for det nominelle antal

KB-nummer: 4612073

## <a name="symptoms"></a>Symptomer

Når et fastvægtantal opdeles i batches, bruger feltet **Plukantal** det minimumantal, der er angivet for varen, og ikke det nominelle antal.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Systemet bruger den enkelte varens opsætning for minimumantal til plukning.
