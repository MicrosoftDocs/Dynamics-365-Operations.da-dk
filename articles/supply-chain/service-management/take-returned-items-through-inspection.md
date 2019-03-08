---
title: Føre returvarer gennem inspektion
description: Føre returvarer gennem inspektion.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82d94e055326e598113822b8d7c4852b7dcb0c4e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "356478"
---
# <a name="take-returned-items-through-inspection"></a>Føre returvarer gennem inspektion 

[!include [banner](../includes/banner.md)]


1.  Klik på **Lagerstyring** \> **Periodisk** \> **Kvalitetsstyring** \> **Karantæneordrer**.

2.  Find den ordrelinje, der svarer til den returnerede vare, du undersøger.

    > [!NOTE]
    > <P>En karantæneordre kan kun knyttes til et enkelt varenummer. Hvis der returneres ti varer med forskellige varenumre i en enkelt forsendelse, og de sendes i karantæne, oprettes der ti forskellige karantæneordrer.</P>

3.  Når varen er undersøgt, skal du foretage et valg i feltet **Dispositionskode** for at angive, hvad der skal ske med varen, og hvordan den relaterede økonomiske transaktion skal håndteres. Varen kan f.eks. returneres til lager, samtidig med at kunden refunderes, varen kan kasseres, samtidig med at der sendes en erstatning til kunden, eller varen kan returneres til kunden uden kredit.
    
    > [!NOTE]
    > <P>Hvis flere varer i en enkelt varenummerbatch ikke kan knyttes til samme dispositionskode, skal du opdele karantæneordren (<STRONG>Funktioner</STRONG> &gt; <STRONG>Opdel</STRONG>) for at tildele en anden dispositionskode til de enkelte underbatch.</P>


4.  Når du er færdig med inspektionen, skal du klikke på **Færdigmeld** for at frigive de returnerede varer og oprette en varemodtagelseskladdepostering. Den person eller afdeling, der modtager varerne, skal behandle kladden for de varer, som skal returneres til lageret.
    
    eller
    
    Afslut karantæneordren, og flyt varerne tilbage til lageret direkte ved hjælp af en af funktionerne for **Lager**.

5.  Luk formen for at gemme ændringerne.

## <a name="see-also"></a>Se også

[Angive, hvordan returvarer skal kasseres](specify-how-to-dispose-of-returned-items.md)

  


