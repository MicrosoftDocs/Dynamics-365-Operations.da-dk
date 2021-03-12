---
title: Sende returvarer videre til inspektion
description: Når du registrerer en returvare, skal du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7207c54a88b8a7fc6c38db50c4916d1fc16b5ec4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006665"
---
# <a name="pass-returned-items-on-to-inspection"></a>Sende returvarer videre til inspektion 

[!include [banner](../includes/banner.md)]


Når du registrerer en returvare, kan du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.

1.  Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Varemodtagelse**.
    
    \-eller-
    
    Klik på **Lagerstyring** \> **Kladder** \> **Varemodtagelse** \> **Produktionsindlagring**.

2.  Registrer modtagelsen af en vare som sædvanligt i formularen **Lokationskladde**.
    

    > [!NOTE]
    > <P>Du kan finde oplysninger om registrering af modtagelsen af returnerede varer under <A href="register-the-receipt-of-returned-items.md">Registrere modtagelsen af returvarer</A></P>



3.  Under fanen **Standardværdier** i området **Håndteringsmåde** skal du markere feltet **Karantænestyring**.

Dette betyder, at systemet vil oprette en karantæneordre, og den person eller afdeling, der udfører inspektionerne, vil svare på denne ordre ved hjælp af formularen **Karantæneordre**.

## <a name="see-also"></a>Se også

[Føre returvarer gennem inspektion](take-returned-items-through-inspection.md)

[Angive, hvordan returvarer skal kasseres](specify-how-to-dispose-of-returned-items.md)

