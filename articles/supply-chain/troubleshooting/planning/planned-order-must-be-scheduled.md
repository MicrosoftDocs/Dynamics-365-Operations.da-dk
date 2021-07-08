---
title: Produktionsordreforslag skal planlægges, før det kan autoriseres
description: Når du forsøger at autorisere et ordreforslag, får du vist en fejlmeddelelse om, at ordren skal planlægges, før den kan autoriseres.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294042"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Produktionsordreforslag skal planlægges, før det kan autoriseres

Fejlkode: SYS309802

## <a name="symptoms"></a>Symptomer

Når du forsøger at autorisere et ordreforslag, får du vist følgende fejlmeddelelse:

> Den planlagte produktionsordre skal planlægges, inden den kan autoriseres.

## <a name="cause"></a>Årsag

De planlagte start- og slutdatoer må ikke være tomme.

## <a name="resolution"></a>Løsning

Benyt følgende fremgangsmåde for at angive start- og slutdatoer for ordreforslaget.

1. Gå til **Varedisponering \> Varedisponering \> Ordreforslag**.
1. Åbn det relevante ordreforslag.
1. Angiv datoer i felterne **Startdato** og **Slutdato** i sektionen **Planlagt** i oversigtspanelet **Generelt**.
