---
title: Inspicere varers kvalitet
description: Denne procedure viser, hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545399"
---
# <a name="inspect-the-quality-of-goods"></a>Inspicere varers kvalitet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du behandler en kvalitetsordre. Du kan køre denne guide i USMF-demodatafirmaet. Inden du begynder denne eksempelprocedure, skal du bekræfte indkøbsordren "000016" og bogføre en produktkvittering. Dette vil automatisk oprette en kvalitetsordre. Kvalitetskontroller foretages normalt af en kvalitetsmedarbejder.


## <a name="select-a-quality-order"></a>Vælg en kvalitetsordre
1. Gå til Lagerstyring > Periodiske opgaver > Kvalitetsstyring > Kvalitetsordrer.
2. Markér den valgte række på listen.
    * Vælg den kvalitetsordre, der blev oprettet, før du startede denne procedure.  

## <a name="record-test-results"></a>Registrere testresultater
1. Klik på Resultater.
2. Klik på Rediger.
3. Skriv et tal i feltet Antalsresultat.
4. Markér den valgte række på listen.
5. Klik på rullelisten i feltet Udfald for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
    * I dette eksempel er resultatet baseret på et foruddefineret udfald. Normalt ville du registrere et mere specifikt testresultat, for eksempel en størrelse eller anden dimension.  
7. Klik op linket i den valgte række på listen.
8. Klik på Gem.
9. Luk siden.

## <a name="validate-the-quality-order"></a>Valider kvalitetsordren
1. Klik på Valider.
2. Klik på rullelisten i feltet Valideret af for at åbne opslaget.
    * Vælg den bruger, der udfører kvalitetskontrollen.  
3. Klik op linket i den valgte række på listen.
4. Klik på Vælg.
5. Klik på OK.
6. Luk siden.

