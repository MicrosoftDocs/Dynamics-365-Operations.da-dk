---
title: Konfigurere indekssatser
description: I dette emne forklares, hvordan du konfigurerer indekssatser. Der kræves indekssatser, hvis organisationen knytter leasingbetalinger til et sæt indekssatser.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40f230a9d69a142b18eb27a2d5e420dbadc600d2
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880954"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="843d5-104">Konfigurere indekssatser</span><span class="sxs-lookup"><span data-stu-id="843d5-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="843d5-105">Hvis leasingbetalingerne afhænger af et indeks, kan indekssatstyperne tilføjes og vedligeholdes i systemet.</span><span class="sxs-lookup"><span data-stu-id="843d5-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="843d5-106">Hvis du vil værdiregulere leasingbetalinger fra siden **Indekssatstype**, bruger processen til værdiregulering af indekssatsen den seneste indekssats fra datoen for værdiregulering.</span><span class="sxs-lookup"><span data-stu-id="843d5-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="843d5-107">Udfør følgende trin for at tilføje indekssatstyper og indekssatser.</span><span class="sxs-lookup"><span data-stu-id="843d5-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="843d5-108">Gå til **Aktivleasing \> Konfiguration \> Indekssatstype**.</span><span class="sxs-lookup"><span data-stu-id="843d5-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="843d5-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="843d5-109">Select **New**.</span></span>
3. <span data-ttu-id="843d5-110">Angiv satstypen og navnet på indekssatsen i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="843d5-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="843d5-111">Hvis du vil tilføje en ny indekssatsværdi, skal du vælge indekssatstypen og derefter vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="843d5-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="843d5-112">Vælg satsens gældende startdato, og vælg satsværdien.</span><span class="sxs-lookup"><span data-stu-id="843d5-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="843d5-113">Du skal vælge enten **Differenceværdi for indekssats** eller **Værdi for indekssats** for indekssatsmetode.</span><span class="sxs-lookup"><span data-stu-id="843d5-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="843d5-114">Vælg metoden **Værdiforskel for indekssats** for at beregne en ny leasingbetaling, baseret på forskellen mellem indekssatsen på startdatoen og den seneste indekssats.</span><span class="sxs-lookup"><span data-stu-id="843d5-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="843d5-115">Indekssatsen defineres i feltet **Indekssats (%)**.</span><span class="sxs-lookup"><span data-stu-id="843d5-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="843d5-116">Vælg metoden **Værdi af indekssats** for at beregne leasingbetaling ved hjælp af den procentdel, der er angivet i feltet **Indekssats (%)**.</span><span class="sxs-lookup"><span data-stu-id="843d5-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
