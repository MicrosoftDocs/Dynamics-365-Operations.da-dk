---
title: Indkøbsordreforslag oprettes, når der findes et indkøb i negative dage
description: Hvis disponeringskoden er Min./maks., opretter planlægningsoptimering et indkøbsordreforslag, når der er et indkøb inden for negative dage.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026377"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Indkøbsordreforslag oprettes, når der findes et indkøb i negative dage

KB-nummer: 4614298

## <a name="symptoms"></a>Symptomer

Hvis disponeringskoden er *Min./maks.*, opretter planlægningsoptimering et indkøbsordreforslag, når der er et indkøb inden for negative dage.

## <a name="resolution"></a>Løsning

Planlægningsoptimering understøtter ikke negative dage. Men funktionen sikrer altid, at ordreforslag ikke planlægges inden for leveringstiden i forhold til dags dato. Leveringstiden for indkøbet er f.eks. 10 dage, og en indkøbsordre forventes at ankomme otte dage fra dags dato. I dette tilfælde bruges indkøbsordren som levering for efterspørgsel, der ligger fem dage fra i dag.

Det anbefales derfor, at du justerer leveringstiderne for at være dækket ind i alle (eller næsten alle) situationer.
