--- 
title: "Generere en begrænset plan"
description: "Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>Generere en begrænset plan

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger. Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke. 

Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til produktionsplanlæggeren.


## <a name="set-up-a-constrained-plan"></a>Konfigurer en begrænset plan
1. Klik på Varedisponering.
2. Klik på Behovsplaner.
3. Find og vælg den ønskede post på listen.
    * Eksempel: StaticPlan  
4. Vælg Ja i feltet Kapacitetsbegrænsning.
5. Angiv "30" i feltet Tidshorisont for kapacitetsbegrænsning.
6. Udvid sektionen Tidshorisonter i dage.
7. Vælg Ja i feltet Kapacitet.
8. Angiv et tal i feltet Tidshorisont for kapacitetsplanlægning (dage).
    * Eksempel: 60  
9. Vælg Ja i feltet Beregnede forsinkelser.
10. Angiv et tal i feltet Tidshorisont for beregning af forsinkelser (dage).
    * Eksempel: 60  
11. Udvid sektionen Beregnede forsinkelser.
12. Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.
13. Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.
14. Vælg Ja i feltet Tilføj den beregnede forsinkelse til behovsdatoen.
15. Luk siden.

## <a name="create-a-constrained-plan"></a>Opret en begrænset plan
1. Klik på Kør.
2. Indtast eller vælg en værdi i feltet Behovsplan.
    * Vælg den plan, som du har konfigureret begrænsninger for.  
3. Klik på OK.
    * Det kan tage et stykke tid.  
4. Klik på Ordreforslag.


