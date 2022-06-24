---
title: Generere en begrænset plan
description: Denne artikel forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger.
author: t-benebo
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65884d556724cd6132fe328e95a5bec78885c174
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904008"
---
# <a name="generate-a-constrained-plan"></a>Generere en begrænset plan

[!include [banner](../../includes/banner.md)]

Denne artikel forklarer, hvordan du opretter en plan, der tager højde for både materiale- og kapacitetsbegrænsninger. Planen sikrer, at produktion ikke starter, før materialer er tilgængelige, og ressourcer overbookes ikke. 

Det demodatafirma, der bruges til at oprette denne procedure, er USMF. Denne procedure er beregnet til produktionsplanlæggeren.


## <a name="set-up-a-constrained-plan"></a>Konfigurer en begrænset plan
1. Vælg arbejdsområdet til **Varedisponering** på startsiden.
2. Vælg **Behovsplaner** på listen over links længst til højre i arbejdsområdet.
3. Find og vælg den ønskede post på listen. Eksempel: **StaticPlan**  
4. Vælg **Ja** i feltet **Kapacitetsbegrænsning**.
5. Angiv `30` i feltet **Tidshorisont for kapacitetsbegrænsning**.
6. Udvid sektionen **Tidshorisonter i dage**.
7. Vælg **Ja** i feltet **Kapacitet**.
8. Angiv et tal i feltet **Tidshorisont for kapacitetsplanlægning (dage)**. Eksempel: `60`  
9. Vælg **Ja** i feltet **Beregnede forsinkelser**.
10. Angiv et tal i feltet **Tidshorisont for beregning af forsinkelser (dage)**. Eksempel: `60` 
11. Udvid sektionen **Beregnede forsinkelser**.
12. Vælg **Ja** i feltet **Tilføj den beregnede forsinkelse til behovsdatoen**.
13. Luk siden.

## <a name="create-a-constrained-plan"></a>Opret en begrænset plan
1. Vælg **Kør**.
2. Angiv eller vælg den plan, du har defineret betingelser for, i feltet **Behovsplan**.  
3. Vælg **OK**.
4. Vælg **Ordreforslag**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]