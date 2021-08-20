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
ms.openlocfilehash: 94d569684a0bfa2398e98147b9b85531954f8d56748894034a048fa627230ef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775501"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Indkøbsordreforslag oprettes, når der findes et indkøb i negative dage

KB-nummer: 4614298

## <a name="symptoms"></a>Symptomer

Hvis disponeringskoden er *Min./maks.*, opretter planlægningsoptimering et indkøbsordreforslag, når der er et indkøb inden for negative dage.

## <a name="resolution"></a>Løsning

Planlægningsoptimering understøtter ikke negative dage. Men funktionen sikrer altid, at ordreforslag ikke planlægges inden for leveringstiden i forhold til dags dato. Leveringstiden for indkøbet er f.eks. 10 dage, og en indkøbsordre forventes at ankomme otte dage fra dags dato. I dette tilfælde bruges indkøbsordren som levering for efterspørgsel, der ligger fem dage fra i dag.

Det anbefales derfor, at du justerer leveringstiderne for at være dækket ind i alle (eller næsten alle) situationer.
