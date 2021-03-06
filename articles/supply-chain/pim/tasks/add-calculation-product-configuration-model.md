---
title: Tilføje en beregning til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812663"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]