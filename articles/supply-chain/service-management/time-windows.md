---
title: Tidsvinduer
description: "Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: b7268870aa9065e4e52d936e819107094bad3663
ms.contentlocale: da-dk
ms.lasthandoff: 02/20/2018

---

# <a name="time-windows"></a>Tidsvinduer  

[!INCLUDE [banner](../includes/banner.md)]

Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer. Du kan konfigurere systemet, så der automatisk oprettes serviceordrer. Baseret på de kriterier, der er angivet af et tidsvindue, kan du forbinde så mange serviceordrelinjer som muligt med så få serviceordrer som muligt.

I tidsvinduer specificeres det, hvor langt en serviceordrelinje kan flyttes fra dens beregnede dato. Den beregnede dato er den dato, hvor serviceordrelinjen var planlagt til at forekomme. Datoen er baseret på dens intervalindstilling og den serviceperiode, som du har defineret på siden **Oprette serviceordrer**. Du definerer et tidsvindue ved at bruge værdierne i følgende tabel:

| metode | Betegnelse                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uge   | Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme uge som den oprindeligt beregnede dato.                                                                                                                                                                                    |
| Måned  | Den dato, hvor serviceordrelinjen kan flyttes til en hvilken som helst åben dag i samme måned som den oprindeligt beregnede dato. For eksempel er den beregnede dato for en serviceordrelinje 15. februar 2017. Serviceordrelinjen kan planlægges for en ugedag mellem 1. februar og 28. februar 2017. |
| Manuelt | Du definerer det højeste antal dage, som serviceordrelinjen kan flyttes frem og tilbage i forhold til den oprindeligt beregnede dato.                                                                                                                                                                           |

Hvis du ikke specificerer et tidsvindue til en serviceaftalelinje, skal den serviceordrelinje, der er afledt af serviceaftalen, være på præcis samme dato, som den oprindeligt var planlagt til.

## <a name="related-topics"></a>Relaterede emner

[Oprette tidsvinduer](create-time-windows.md)


