---
title: Sende returvarer videre til inspektion
description: Når du registrerer en returvare, skal du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c7c238536ead603b11d4c97e98289ab157ad86db
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578770"
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]