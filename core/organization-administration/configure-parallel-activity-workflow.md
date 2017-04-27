---
title: Konfigurere en parallel aktivitet i en arbejdsgang
description: "Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurere en parallel aktivitet i en arbejdsgang

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
    | **Bemærk! **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Grenenes rækkefølge betyder ikke noget, fordi alle grenene i en parallel aktivitet kører samtidigt. |

3.  Hvis du vil konfigurere hver gren, skal du se [Konfigurere en parallel gren](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




