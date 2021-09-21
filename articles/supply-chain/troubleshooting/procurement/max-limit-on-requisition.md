---
title: Maksimumgrænsen for købsaftalen gælder ikke for en indkøbsrekvisition
description: Maksimumgrænsen for købsaftalen gælder ikke for en indkøbsrekvisition
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475882"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Maksimumgrænsen for købsaftalen gælder ikke for en indkøbsrekvisition

## <a name="symptoms"></a>Symptomer

Når en indkøbsrekvisition er knyttet til en købsaftale, er maksimumgrænsen fra købsaftalen ikke gældende i indkøbsrekvisitionen. Standardprisoplysningerne angives korrekt, men mere end maksimumgrænsen fra købsaftalen kan bestilles i indkøbsrekvisitionen.

## <a name="resolution"></a>Løsning

Denne funktionsmåde forventes. Da rekvisitioner ikke altid er godkendt, bør et antal eller beløb ikke reserveres på købsaftalen. Derfor når du ikke maksimumgrænsen fra købsaftalen.
