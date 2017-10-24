---
title: Faktorafskrivning
description: Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="factor-depreciation"></a>Faktorafskrivning

[!include[banner](../includes/banner.md)]


Denne artikel indeholder en oversigt over faktorafskrivningsmetoden.

Faktorer er de procentsatser, der bruges til afskrivning på aktiver. Når du opretter en afskrivningsprofil for anlægsaktiver og vælger **Faktor** i feltet **Metode** på siden **Afskrivningsprofiler**, kan du oprette progressiv, degressiv eller lineær afskrivning:

-   Ved progressiv afskrivning øges afskrivningsbeløbet for hver afskrivningsperiode.
-   Ved degressiv afskrivning mindskes afskrivningsbeløbet for hver afskrivningsperiode.
-   Ved lineær afskrivning er afskrivningsbeløbet det samme i hver afskrivningsperiode.

Reglerne og eksemplerne, der følger nedenfor angiver, hvordan du kan oprette faktorer til de forskellige afskrivningstyper. 

> [!NOTE] 
> Når du vælger **Faktor** i feltet **Metode**, vises felterne **Faktor** og **Interval**.

## <a name="progressive-depreciation"></a>Progressiv afskrivning
Værdien i feltet **Faktor** er større end **50**.

### <a name="example"></a>Eksempel

Anskaffelsesprisen er 100.000, faktoren er 70, levetiden er 10 år, og afskrivningen starter 1. januar. Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.

| År | Periode      | Afskrivningsbeløb | Bogført nettoværdi – beløb |
|------|-------------|---------------------|-----------------------|
| 1    | 31. december | 307,69              | 99.692,31             |
| 2    | 31. december | 1.447,21            | 98.245,10             |
| 3    | 31. december | 3.104,50            | 95.140,60             |
| 4    | 31. december | 5.150,21            | 89.990,39             |
| 5    | 31. december | 7.522,95            | 82.467,44             |
| 6    | 31. december | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Degressiv afskrivning
Værdien i feltet **Faktor** er mindre end **50**.

### <a name="example"></a>Eksempel

Anskaffelsesprisen er 100.000, faktoren er 20, levetiden er 10 år, og afskrivningen starter 1. januar. Afskrivningsbeløbene og værdien af den bogførte nettoværdi vises kun for de første seks år af levetiden.

| År | Periode      | Afskrivningsbeløb | Bogført nettoværdi – beløb |
|------|-------------|---------------------|-----------------------|
| 1    | 31. december | 56.080,43           | 43.919,57             |
| 2    | 31. december | 10.665,70           | 33.253,87             |
| 3    | 31. december | 7.156,22            | 26.097,65             |
| 4    | 31. december | 5.538,06            | 20.559,59             |
| 5    | 31. december | 4.579,89            | 15.979,70             |
| 6    | 31. december | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Lineær afskrivning
Værdien i feltet **Faktor** er lig med **50**. I dette tilfælde er afskrivningen den samme i hver periode, og derfor skal du overveje konsekvensen af de værdier, du har angivet i andre felter, som beskrevet i [Lineær afskrivning for levetiden](straight-line-service-life-depreciation.md).




