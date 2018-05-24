---
title: Sende returvarer videre til inspektion
description: "Når du registrerer en returvare, skal du bestemme, at en vare skal sendes til inspektion, før den returneres til lageret eller bortskaffes på anden vis."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a60e6635e3bb1723ced7aba1a71135116b53272
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

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


