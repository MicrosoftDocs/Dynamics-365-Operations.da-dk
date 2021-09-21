---
title: Lagerkladden er låst, og arbejdsgangens batchjob fungerer ikke
description: En af lagerkladderne er låst af en eller anden handling, og den frigives ikke
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475877"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Lagerkladden er låst, og arbejdsgangens batchjob fungerer ikke

## <a name="symptoms"></a>Symptomer

En af lagerkladderne er låst af en eller anden handling, og den frigives ikke. Hvis der f.eks. opstår en ukendt fejl under bogføring (som er en systemlåshandling), kan kladden stadig have statussen systemlåst. I dette tilfælde viser arbejdsgangsopgavehandleren en fejl under låsevalidering.

## <a name="resolution"></a>Løsning

Log på SQL Server-forekomsten for Supply Chain Management, og kontrollér, om **InventJournalTable.SystemBlocked** er angivet til *1*. Hvis det er tilfældet, skal du sørge for, at kladden ikke er i låst status og derefter nulstille **InventJournalTable.SystemBlocked** til *0*.
