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
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738813"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Batchnummeret fjernes, når der vælges et nyt parti-id

KB-nummer: 4613107

## <a name="symptoms"></a>Symptomer

Når du gennemser en pluklistekladdelinje, ryddes værdien i feltet **Batchnummer**, hvis du vælger en ny værdi i feltet **Parti-id**.

## <a name="resolution"></a>Løsning

Systemet fungerer som designet. Hvis du ændrer parti-id'et, skal du ændre varekonteksten. Derfor nulstilles batchnummeret.

Hvis du vil knytte batchnummeret til et parti-id, skal du angive parti-id'et først.
