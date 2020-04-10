---
title: Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)
description: Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e02e76cd5762fc683290eeee49d23c9fed8d4503
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150510"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Beregne en stykliste ved hjælp af en enkelt struktur (februar 2016)

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på enkeltniveau, der er baseret på efterkalkulationsarket. Det er den sjette opgave i styklisteberegningsserien. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.

1. Gå til Frigivne produkter.
2. Find og vælg den ønskede post på listen.
    * Vælg produktet BOM_1.  
3. Klik på Administrer omkostninger i handlingsruden.
4. Klik på Varepris.
5. Klik på Beregn varens kostpris.
    * Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.  
6. Klik på rullelisten i feltet Efterkalkulationsversion for at åbne opslaget.
    * I dette eksempel skal du vælge 10. Dette er den samme efterkalkulationsversion, som bruges til at føje kostprisen til komponenterne.  
7. Klik på OK.
8. Klik på Vis beregningsoplysninger.
    * Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.    Her er kompositionen af omkostningerne: *    10 er afledt af ITEM_A, 10 fra ITEM_B, 10 fra BOM_2. Der er i dette tilfælde ingen oplysninger om BOM_2, fordi den blev angivet som en standardomkostning på 10, men ikke blev angivet gennem beregning.  *    7 afledes fra opstillingstiden, der er en konstant omkostning, og yderligere 7 afledes fra procestidshandlingen (proces).  *    Der findes også andre beløb, der svarer til indirekte omkostninger.  
9. @SysTaskRecorder:_RequestClose

