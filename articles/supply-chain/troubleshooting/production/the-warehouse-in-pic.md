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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740545"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomer

Lagerstedet i pluklistekladden opdateres ikke på en styklistelinje.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Hvis der oprettes en pluklistekladdelinje, der har en reference (via parti-id'et) til en produktionsstyklistelinje, opdateres lagerstedet på produktionsstyklistelinjen ikke, hvis lagerstedsdimensionen på pluklistelinjen for produktionen ændres senere.
