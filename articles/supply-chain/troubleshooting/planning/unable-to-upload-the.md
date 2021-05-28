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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026375"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="2d96c-103">Du kan ikke opdatere de budgetterede enhedsomkostninger, når du importerer behovsprognoseposter</span><span class="sxs-lookup"><span data-stu-id="2d96c-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="2d96c-104">KB-nummer: 4614109</span><span class="sxs-lookup"><span data-stu-id="2d96c-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="2d96c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="2d96c-105">Symptoms</span></span>

<span data-ttu-id="2d96c-106">Når du bruger dataenheder til at importere behovsprognoseposter, opdateres værdien i **Budgetteret enhedsomkostning** for eksisterende poster ikke, så den svarer til de importerede data.</span><span class="sxs-lookup"><span data-stu-id="2d96c-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="2d96c-107">Årsag</span><span class="sxs-lookup"><span data-stu-id="2d96c-107">Cause</span></span>

<span data-ttu-id="2d96c-108">**Budgetteret enhedsomkostning** er et skrivebeskyttet felt.</span><span class="sxs-lookup"><span data-stu-id="2d96c-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="2d96c-109">Værdien er baseret på produktenhedens kostpris og kan ikke angives direkte via import.</span><span class="sxs-lookup"><span data-stu-id="2d96c-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="2d96c-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="2d96c-110">Resolution</span></span>

<span data-ttu-id="2d96c-111">Da feltet er skrivebeskyttet, kan du ikke importere værdier for det.</span><span class="sxs-lookup"><span data-stu-id="2d96c-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="2d96c-112">Værdien beregnes i overensstemmelse med den eksisterende forretningslogik.</span><span class="sxs-lookup"><span data-stu-id="2d96c-112">The value will be calculated according to the existing business logic.</span></span>
