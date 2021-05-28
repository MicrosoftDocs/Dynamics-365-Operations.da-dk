---
title: Tilbageførsel af færdigmeldingen opretter en uventet åben postering
description: Tilbageførsel af færdigmelding med afmærkning opretter en åben postering, hvor det tilbageførte antal har samme lagerdimensioner som den tilbageførte postering.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026383"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Tilbageførsel af færdigmeldingen opretter en uventet åben postering

KB-nummer: 4612469

## <a name="symptoms"></a>Symptomer

Hvis du tilbagefører færdigmelding med afmærkning, opretter systemet en åben postering, hvor det tilbageførte antal har samme lagerdimensioner som den postering, der blev tilbageført.

## <a name="resolution"></a>Løsning

Når du tilbagefører en færdigmeldingshandling, initialiseres lagerdimensionen fra produktionskladden. Den får derfor batchnummeret. På grund af afmærkningen arver salgsordretransaktionerne batchnummeret.

Dimensionen kan nulstilles, når færdigmeldingen er bogført.
