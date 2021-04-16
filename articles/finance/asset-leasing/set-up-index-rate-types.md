---
title: Konfigurere indekssatser
description: I dette emne forklares, hvordan du konfigurerer indekssatser. Der kræves indekssatser, hvis organisationen knytter leasingbetalinger til et sæt indekssatser.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823017"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="f9a23-104">Konfigurere indekssatser</span><span class="sxs-lookup"><span data-stu-id="f9a23-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9a23-105">Hvis leasingbetalingerne afhænger af et indeks, kan indekssatstyperne tilføjes og vedligeholdes i systemet.</span><span class="sxs-lookup"><span data-stu-id="f9a23-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="f9a23-106">Hvis du vil værdiregulere leasingbetalinger fra siden **Indekssatstype**, bruger processen til værdiregulering af indekssatsen den seneste indekssats fra datoen for værdiregulering.</span><span class="sxs-lookup"><span data-stu-id="f9a23-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="f9a23-107">Udfør følgende trin for at tilføje indekssatstyper og indekssatser.</span><span class="sxs-lookup"><span data-stu-id="f9a23-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="f9a23-108">Gå til **Aktivleasing \> Konfiguration \> Indekssatstype**.</span><span class="sxs-lookup"><span data-stu-id="f9a23-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="f9a23-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f9a23-109">Select **New**.</span></span>
3. <span data-ttu-id="f9a23-110">Angiv satstypen og navnet på indekssatsen i de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="f9a23-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="f9a23-111">Hvis du vil tilføje en ny indekssatsværdi, skal du vælge indekssatstypen og derefter vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f9a23-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="f9a23-112">Vælg satsens gældende startdato, og vælg satsværdien.</span><span class="sxs-lookup"><span data-stu-id="f9a23-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="f9a23-113">Du skal vælge enten **Differenceværdi for indekssats** eller **Værdi for indekssats** for indekssatsmetode.</span><span class="sxs-lookup"><span data-stu-id="f9a23-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="f9a23-114">Vælg metoden **Værdiforskel for indekssats** for at beregne en ny leasingbetaling, baseret på forskellen mellem indekssatsen på startdatoen og den seneste indekssats.</span><span class="sxs-lookup"><span data-stu-id="f9a23-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="f9a23-115">Indekssatsen defineres i feltet **Indekssats (%)**.</span><span class="sxs-lookup"><span data-stu-id="f9a23-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="f9a23-116">Vælg metoden **Værdi af indekssats** for at beregne leasingbetaling ved hjælp af den procentdel, der er angivet i feltet **Indekssats (%)**.</span><span class="sxs-lookup"><span data-stu-id="f9a23-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]