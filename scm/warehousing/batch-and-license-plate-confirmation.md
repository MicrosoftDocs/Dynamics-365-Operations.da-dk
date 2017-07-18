---
title: "Bekræftelse af batch og nummerplade"
description: "I dette emne beskrives, hvordan du kan konfigurere og anvende batch- og id-bekræftelse fra en mobilenhed."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 70a8c18560f0cfc7a44625520f2f035a6004618a
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017


---

# <a name="batch-and-license-plate-confirmation"></a>Bekræftelse af batch og nummerplade

[!include[banner](../includes/banner.md)]

Med batchbekræftelse kan du bekræfte, at den korrekte batch plukkes fra mobilenheden. Ved det oprindelige pluk af arbejde for varer af typen batch over alene, hvor *batch over* angiver, at batch rangerer højere end sted i søgehierarkiet, skal du kontrollere, svarer det batch, der plukkes, svarer til batchen på arbejdslinjen. 

Med id-bekræftelse kan du bekræfte, at det korrekte id plukkes fra mobilenheden. Ved pluk af arbejde fra et sted i et stadie, skal du kontrollere, at det id, der plukkes, svarer til det id, der er knyttet til arbejdet. Hvis arbejdet startes ved at scanne et id, springes dette bekræftelsestrin over.

## <a name="where-it-applies"></a>Hvor det er relevant
Bekræftelsen anvendes i følgende scenarier:

- Batchbekræftelse gælder for de første pluk af arbejde for varer af typen batch over.
- Bekræftelse af id gælder for pluk fra steder i stadier.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Konfigurere bekræftelse af batch og id
Du kan konfigurere batch- og id-bekræftelse fra mobilenhedens menupunkter.  
1.  Angiv opsætningen af arbejdsbekræftelsen fra menupunkterne på mobilenheden.  
2.  Vælg indstillingen for batch- eller id-bekræftelse. Begge indstillinger er tilgængelige for pluk af arbejdstypen, hvor automatisk bekræftelse ikke er aktiveret.  
