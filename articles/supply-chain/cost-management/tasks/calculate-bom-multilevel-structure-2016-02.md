---
title: Beregne en stykliste ved hjælp af en struktur for flere niveauer (februar 2016)
description: Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0834baf42ed6aa10acec6529513e44ff52ab754
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845636"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Beregne en stykliste ved hjælp af en struktur for flere niveauer (februar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan omkostningerne for et færdigt produkt beregnes ved hjælp af udfoldning på flere niveauer, der er baseret på efterkalkulationsarket. Det er den syvende opgave i styklisteberegningsserien. Det demodatafirma, der bruges til at oprette denne opgave, er USMF.

1. Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.
2. Find og vælg den ønskede post på listen.
    * Vælg produktet BOM_1.  
3. Klik på Administrer omkostninger i handlingsruden.
4. Klik på Varepris.
5. Klik på Beregn varens kostpris.
    * Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.  
6. Indtast eller vælg en værdi i feltet Efterkalkulationsversion.
    * Vælg Efterkalkulationsversion 20, fordi omkostningstypen er Planlagt, og udfoldningstilstanden er Flere niveauer.   Udfoldningstilstanden Flere niveauer er for planlagte omkostninger og simuleringer. Den bruges ikke til standardomkostninger.  
7. Klik på OK.
8. Klik på Vis beregningsoplysninger.
    * Du skal måske klikke på ellipseknappen (...) for at se denne indstilling i den øverste menu.  Bemærk i dette tilfælde, hvordan BOM_2 er blevet beregnet under hensyntagen til råvare, proces samt faste omkostninger med en total på 29,40 i stedet for standardkostprisen på 10, der blev aktiveret i den indledende opgaveguide i denne serie.  
9. Klik på arkfanen Efterkalkulation.
    * Hvis du flytter til fanen Efterkalkulation, er totalerne pr. omkostningsgruppe forskellige sammenlignet med den beregning, der er udført i forrige opgaveguide.  
10. Vælg "Flere" i feltet Niveau.
    * Når du vælger Flere, klassificeres omkostningerne efter sammensætningen af BOM_2, hvor 10 er afledt af omkostningsgruppen M1 (ITEM_C), og 15,60 er afledt af dens produktion, hvor omkostningsgruppen er L2. Indirekte omkostninger varierer også.  
11. Luk siden.
12. Luk siden.

