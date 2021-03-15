---
title: Tilføje en beregning til en produktkonfigurationsmodel
description: Denne procedure viser, hvordan du kan føje en ny beregning til en produktkonfigurationsmodel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987048"
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