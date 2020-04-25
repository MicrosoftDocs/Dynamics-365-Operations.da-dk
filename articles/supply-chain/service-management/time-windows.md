---
title: Tidsvinduer
description: Du kan bruge tidsvinduer til at optimere planlægningen af serviceordrelinjer.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63a166806c2c8ac84cc1d71d6ec84fcb28033feb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206513"
---
# <a name="time-windows"></a>Tidsvinduer  

[!include [banner](../includes/banner.md)]

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

