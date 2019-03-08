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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "343161"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Tilføje en beregning til en produktkonfigurationsmodel

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel. Den viser, hvordan du kan oprette et logisk udtryk ved at bruge operatoren "Hvis" til at indstille en højttalerhøjde til 10 for hvide højttalere og 15 til ethvert andet kabinetfinish. Proceduren bruger komponenten Højttaler af topkvalitet i demofirmaet USMF.


## <a name="add-a-calculation"></a>Tilføje en beregning

## <a name="create-calculation-expression"></a>Oprette et beregningsudtryk
1. Klik på udtrykket Rediger.
2. I feltet ConstraintBody skal du angive 'If[CabinetFinish == "Hvid", 10, 15]'.
3. Klik på Valider.
4. Klik på Luk.
5. Klik på OK.

