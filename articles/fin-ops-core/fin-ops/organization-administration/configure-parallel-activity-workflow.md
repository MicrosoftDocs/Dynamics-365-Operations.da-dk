---
title: Konfigurere parallelle aktiviteter i en arbejdsgang
description: Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0bc97f401ad9e097248dfd5afb0baa8edbb6b3c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350664"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Konfigurere parallelle aktiviteter i en arbejdsgang

[!include [banner](../includes/banner.md)]

Udfør følgende procedurer i arbejdsgangseditoren, hvis du vil konfigurere en parallel aktivitet.

En parallel aktivitet består af grene i en arbejdsgang, der kører samtidigt.

## <a name="name-a-parallel-activity"></a>Navnet på en parallel aktivitet

Udfør følgende trin for at angive et navn på den parallelle aktivitet.

1. Højreklik på den parallelle aktivitet, og klik derefter på **Egenskaber** for at åbne formen **Egenskaber**.
2. Klik på **Grundlæggende indstillinger** i venstre rude.
3. Angiv et entydigt navn på den parallelle aktivitet i feltet **Nanv**.
4. Klik på **Luk**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurere grenene i den parallelle aktivitet

Udfør følgende trin for at tilføje og konfigurere grenene i den parallelle aktivitet.

1. Dobbeltklik på den parallelle aktivitet for at få vist grenene i den parallelle aktivitet.
2. Du kan tilføje en gren ved at trække elementet **Gren** fra området **Arbejdsgangselementer** til et indsættelsespunkt på lærredet. I følgende illustration vises et indsættelsespunkt.

    ![Indsættelsespunkt.](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Grenenes rækkefølge betyder ikke noget, fordi alle grenene i en parallel aktivitet kører samtidigt.

3. Hvis du vil konfigurere hver gren, skal du se [Konfigurer parallelle grene i en arbejdsgang](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]