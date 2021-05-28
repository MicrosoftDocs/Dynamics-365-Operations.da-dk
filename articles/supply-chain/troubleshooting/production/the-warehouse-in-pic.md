---
title: Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje.
description: Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026362"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomer

Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Hvis der oprettes en pluklistekladdelinje, der har en reference (via parti-id'et) til en produktionsstyklistelinje, opdateres lagerstedet på produktionsstyklistelinjen ikke, hvis lagerstedsdimensionen på pluklistelinjen for produktionen ændres senere.
