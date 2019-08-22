---
title: Generere en begrænset plan
description: Denne procedure viser, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845281"
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

