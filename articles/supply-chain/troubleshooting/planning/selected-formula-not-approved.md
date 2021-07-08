---
title: Det markerede formelnummer er ikke godkendt til en batchordre
description: Når du forsøger at autorisere et ordreforslag, modtager du en fejlmeddelelse om, at det valgte formelnummer ikke er godkendt til en batchordre.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294034"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Det markerede formelnummer er ikke godkendt til en batchordre

Fejlkode: PRO2614

## <a name="symptoms"></a>Symptomer

Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:

> Det valgte formelnummer er ikke godkendt for en batchordre.

## <a name="cause"></a>Årsag

Systemet validerer den autoriserede handling for at sikre, at der findes en godkendt formel til den aktive vare. Du skal sandsynligvis godkende formlen.

## <a name="resolution"></a>Løsning

Benyt følgende fremgangsmåde for at godkende en formel.

1. Gå til **Administration af produktoplysninger \> Styklister og formler \> Formler**.
1. Vælg den relevante formel.
1. Vælg **Godkend formel** i gruppen **Vedligehold** under fanen **Formel** i handlingsruden.
1. Vælg en godkender i dialogboksen **Godkend stykliste eller formel**, og vælg derefter **OK**.
