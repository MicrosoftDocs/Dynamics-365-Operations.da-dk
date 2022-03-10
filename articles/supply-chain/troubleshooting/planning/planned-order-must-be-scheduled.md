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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777737"
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
