--- 
title: "Konfigurere attributbaseret prissætning for konfigurerbare produkter"
description: Denne procedure viser, hvordan du opretter attributbaserede priser.
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 88402bef6fd5dad38a74795cd31a4046085d6db7
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Konfigurere attributbaseret prissætning for konfigurerbare produkter

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


