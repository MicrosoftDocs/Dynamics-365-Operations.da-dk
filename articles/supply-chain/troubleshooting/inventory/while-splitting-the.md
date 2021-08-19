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
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723449"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Når et fastvægtantal opdeles, bruges minimumantallet i stedet for det nominelle antal

KB-nummer: 4612073

## <a name="symptoms"></a>Symptomer

Når et fastvægtantal opdeles i batches, bruger feltet **Plukantal** det minimumantal, der er angivet for varen, og ikke det nominelle antal.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Systemet bruger den enkelte varens opsætning for minimumantal til plukning.
