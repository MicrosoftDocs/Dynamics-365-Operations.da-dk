---
title: Inspicere varers kvalitet
description: Dette emne forklarer, hvordan du behandler en kvalitetsordre.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424889"
---
# <a name="inspect-the-quality-of-goods"></a>Inspicere varers kvalitet

[!include [banner](../../includes/banner.md)]

Dette emne forklarer, hvordan du behandler en kvalitetsordre. Du kan køre denne guide i USMF-demodatafirmaet. Inden du begynder denne eksempelprocedure, skal du bekræfte indkøbsordren "000016" og bogføre en produktkvittering. Dette vil automatisk oprette en kvalitetsordre. Kvalitetskontroller foretages normalt af en kvalitetsmedarbejder.


## <a name="select-a-quality-order"></a>Vælg en kvalitetsordre
1. I navigationsruden skal du gå til **Moduler > Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.**
2. Vælg den kvalitetsordre, der blev oprettet, før du startede denne procedure.  

## <a name="record-test-results"></a>Registrere testresultater
1. Vælg **Resultater**.
2. Vælg **Rediger**.
3. I feltet **Antal resultater** skal du skrive et tal.
4. I feltet **Udfald** skal du vælge den ønskede post i rullemenuen.  
- I dette eksempel er resultatet baseret på et foruddefineret udfald. Normalt ville du registrere et mere specifikt testresultat, for eksempel en størrelse eller anden dimension.  
5. Vælg **Gem**.
6. Luk siden.

## <a name="validate-the-quality-order"></a>Valider kvalitetsordren
1. Vælg **Valider**.
2. I feltet **Valideret af** skal du i rullemenuen vælge den bruger, som udfører inspektionen.  
3. Klik på **Vælg**.
4. Vælg **OK**.
5. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]