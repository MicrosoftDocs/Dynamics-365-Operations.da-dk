---
title: Vægt skal være positiv
description: Vægt skal være positiv
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924297"
---
# <a name="weight-must-be-positive"></a>Vægt skal være positiv

Fejlkode: WeightMustBePositive

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Vægt skal være positiv.

## <a name="cause"></a>Årsag

Feltet **Bruttovægt** er angivet til *0* (nul) eller en negativ værdi.

## <a name="resolution"></a>Løsning

Hvis du vil angive en vægt, skal du benytte en af følgende fremgangsmåder:

- Angiv en værdii feltet **Bruttovægt**. Vælg derefter en enhed på rullelisten.
- Vælg **Hent systemvægt** til beregning af værdien for **Bruttovægt**.
