---
title: Bekræftelse af batch og nummerplade
description: I dette emne beskrives, hvordan du kan konfigurere og anvende batch- og id-bekræftelse fra en mobilenhed.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13e246f9a496dcc38829eef788d09c50300c99fb95daffad134012733341e4af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726531"
---
# <a name="batch-and-license-plate-confirmation"></a>Bekræftelse af batch og nummerplade

[!include [banner](../includes/banner.md)]

Med batchbekræftelse kan du bekræfte, at den korrekte batch plukkes fra mobilenheden. Ved det oprindelige pluk af arbejde kun for varerne *Batch over\[lokation\]*, hvor batch over angiver, at batch placeres højere end lokation i søgehierarkiet, skal du kontrollere, at det batch, der plukkes, svarer til batchen på arbejdslinjen.

Med id-bekræftelse kan du bekræfte, at det korrekte id plukkes fra mobilenheden. Ved pluk af arbejde fra et sted i et stadie, skal du kontrollere, at det id, der plukkes, svarer til det id, der er knyttet til arbejdet. Hvis arbejdet startes ved at scanne et id, springes dette bekræftelsestrin over.

## <a name="where-it-applies"></a>Hvor det er relevant

Bekræftelsen anvendes i følgende scenarier:

- Batchbekræftelse gælder for de første pluk af arbejde for varer af typen batch over.
- Bekræftelse af id gælder for pluk fra steder i stadier.

> [!IMPORTANT]
> Genopfyldning understøttes ikke for bekræftelse af id. Når der udføres genopfyldningsarbejde, oprettes der intet bekræftelsestrin for id.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Konfigurere bekræftelse af batch og id

Du kan konfigurere batch- og id-bekræftelse fra mobilenhedens menupunkter.

1. Angiv opsætningen af arbejdsbekræftelsen fra menupunkterne på mobilenheden.  
1. Vælg indstillingen for batch- eller id-bekræftelse. Begge indstillinger er tilgængelige for pluk af arbejdstypen, hvor automatisk bekræftelse ikke er aktiveret.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
