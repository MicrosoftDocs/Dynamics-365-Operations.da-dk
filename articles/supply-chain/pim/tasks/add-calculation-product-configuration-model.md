---
title: Tilføje en beregning til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f8fcfdafb2d5fb5a4d4800221fabf4b2111f86
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150257"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Tilføje en beregning til en produktkonfigurationsmodel

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel. Den viser, hvordan du kan oprette et logisk udtryk ved at bruge operatoren "Hvis" til at indstille en højttalerhøjde til 10 for hvide højttalere og 15 til ethvert andet kabinetfinish. Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.


## <a name="add-a-calculation"></a>Tilføje en beregning

## <a name="create-calculation-expression"></a>Oprette et beregningsudtryk
1. Klik på udtrykket Rediger.
2. I feltet ConstraintBody skal du angive 'If[CabinetFinish == "Hvid", 10, 15]'.
3. Klik på Valider.
4. Klik på Luk.
5. Klik på OK.

