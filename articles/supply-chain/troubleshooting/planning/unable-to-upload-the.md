---
title: Du kan ikke opdatere de budgetterede enhedsomkostninger, når du importerer behovsprognoseposter
description: Når du bruger dataenheder til at importere behovsprognoseposter, opdateres kostprisen for eksisterende poster ikke, så den svarer til de importerede data.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765364"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Du kan ikke opdatere de budgetterede enhedsomkostninger, når du importerer behovsprognoseposter

KB-nummer: 4614109

## <a name="symptoms"></a>Symptomer

Når du bruger dataenheder til at importere behovsprognoseposter, opdateres værdien i **Budgetteret enhedsomkostning** for eksisterende poster ikke, så den svarer til de importerede data.

## <a name="cause"></a>Årsag

**Budgetteret enhedsomkostning** er et skrivebeskyttet felt. Værdien er baseret på produktenhedens kostpris og kan ikke angives direkte via import.

## <a name="resolution"></a>Løsning

Da feltet er skrivebeskyttet, kan du ikke importere værdier for det. Værdien beregnes i overensstemmelse med den eksisterende forretningslogik.
