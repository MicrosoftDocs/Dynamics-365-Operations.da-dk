--- 
title: "Konfigurere attributbaseret prissætning for konfigurerbare produkter"
description: Denne procedure viser, hvordan du opretter attributbaserede priser.
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurere attributbaseret prissætning for konfigurerbare produkter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter attributbaserede priser. Som en forudsætning skal du have en produktkonfigurationsmodel, der har en eller flere komponenter og attributter. I dette eksempel bruges Højttaler af topkvalitet-modellen i demodatafirmaet USMF. Normalt bruger en produktchef denne procedure.


## <a name="create-a-new-price-model"></a>Opret en ny prismodel
1. Klik på Definition af produktvariantmodel.
2. Klik på Produktkonfigurationsmodeller.
3. På listen skal du vælge linjen Højttaler af topkvalitet, men ikke klikke på linket for navnet.
4. Klik på Model i handlingsruden.
5. Klik på Prismodeller.
6. Klik på Ny.
7. Angiv en værdi i feltet Prismodel.
    * Brug et navn, der gør det nemt at identificere modellen.  
8. Skriv en værdi i feltet Beskrivelse.
9. Klik på Gem.

## <a name="add-price-elements"></a>Tilføj priselementer
1. Klik på Rediger.
    * Hver komponent i en produktmodel kan have et basispriselement og et vilkårligt antal prisudtryksregler. Du kan også tilføje priser i forskellige valutaer.  
2. Indtast en værdi i feltet Basisprisudtryk.
    * Skriv for eksempel 100.   En basisprisudtryk kan være en numerisk værdi, eller det kan bestå af en matematisk beregning, der omfatter en eller flere attributter.  
3. Klik på Tilføj.
4. Skriv 'Rosewood' i feltet Navn.
    * Navnet på prisudtrykket hjælper med at identificere, hvad priselementet repræsenterer. I dette eksempel opretter vi priselementet for indstillingen Kabinetfinish til Rosewood-højttaler.  
5. Klik på Rediger betingelse.
    * En prisbetingelse hjælper med at sikre, at prisudtrykselementet kun er inkluderet i salgsprisen, hvis der findes en bestemt kombination af attributter.  
6. I feltet ConstraintBody skal du angive 'CabinetFinish=="Rosewood"'.
7. Klik på OK.
8. Skriv en værdi i feltet Udtryk.
    * Skriv for eksempel 50.  
9. Luk siden.
10. Luk siden.


