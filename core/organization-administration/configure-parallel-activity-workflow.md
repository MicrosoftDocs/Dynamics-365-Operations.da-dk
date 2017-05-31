---
title: Konfigurere en parallel aktivitet i en arbejdsgang
description: "Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c2f98803164d5c761d2089152c077cfb9e83c43
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurere en parallel aktivitet i en arbejdsgang

[!include[banner](../includes/banner.md)]


Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.

En parallel aktivitet består af grene i en arbejdsgang, der kører samtidigt.

## <a name="name-a-parallel-activity"></a>Navnet på en parallel aktivitet
Udfør følgende trin for at angive et navn på den parallelle aktivitet.
1.  Højreklik på den parallelle aktivitet, og klik derefter på **Egenskaber** for at åbne formen **Egenskaber**.
2.  Klik på **Grundlæggende indstillinger** i venstre rude.
3.  Angiv et entydigt navn på den parallelle aktivitet i feltet **Nanv**.
4.  Klik på **Luk**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurere grenene i den parallelle aktivitet
Udfør følgende trin for at tilføje og konfigurere grenene i den parallelle aktivitet.
1.  Dobbeltklik på den parallelle aktivitet for at få vist grenene i den parallelle aktivitet.
2.  Du kan tilføje en gren ved at trække elementet **Gren** fra området **Arbejdsgangselementer** til et indsættelsespunkt på lærredet. I følgende illustration vises et indsættelsespunkt.![Indsættelsespunkt](./media/workflow_insertionpoint.gif)
    | **Bemærk!**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Grenenes rækkefølge betyder ikke noget, fordi alle grenene i en parallel aktivitet kører samtidigt. |

3.  Hvis du vil konfigurere hver gren, skal du se [Konfigurere en parallel gren](configure-parallel-branch-workflow.md).






