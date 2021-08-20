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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776770"
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
