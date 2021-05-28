---
title: Batchnummeret fjernes, når der vælges et nyt parti-id
description: Når du gennemser en pluklistekladdelinje, ryddes værdien i feltet Batchnummer, hvis du vælger en ny værdi i feltet Parti-id.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026356"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Batchnummeret fjernes, når der vælges et nyt parti-id

KB-nummer: 4613107

## <a name="symptoms"></a>Symptomer

Når du gennemser en pluklistekladdelinje, ryddes værdien i feltet **Batchnummer**, hvis du vælger en ny værdi i feltet **Parti-id**.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Hvis du ændrer parti-id'et, skal du ændre varekonteksten. Derfor nulstilles batchnummeret.

Hvis du vil knytte batchnummeret til et parti-id, skal du angive parti-id'et først.
