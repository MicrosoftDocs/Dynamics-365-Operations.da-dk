---
title: Konventioner i aktivleasing
description: Dette emne beskriver konventionerne leasingaktiver.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881802"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="d6edc-103">Konventioner i aktivleasing</span><span class="sxs-lookup"><span data-stu-id="d6edc-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d6edc-104">Dette emne beskriver konventionerne leasingaktiver.</span><span class="sxs-lookup"><span data-stu-id="d6edc-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="d6edc-105">Leasingkonventioner bruges til at bestemme startdatoen for leasingkartoteket.</span><span class="sxs-lookup"><span data-stu-id="d6edc-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="d6edc-106">Hvis leasingaftalen er angivet til **Ingen**, er startdatoen den samme som startdatoen for leasingaftalen (det vil sige værdien af feltet **Startdato for leasingaftalen**).</span><span class="sxs-lookup"><span data-stu-id="d6edc-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="d6edc-107">Hvis leasingaftalen er angivet til **Fuld måned**, er udløbsdatoen den første dag i måneden, hvor startdatoen for leasingaftalen ligger.</span><span class="sxs-lookup"><span data-stu-id="d6edc-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="d6edc-108">Datoen for tilskrivningen bestemmer startdatoen for perioden for passiv-amortisering og afskrivningsplaner for aktiver.</span><span class="sxs-lookup"><span data-stu-id="d6edc-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="d6edc-109">Renteudgifter og afskrivningsudgifter bogføres på periodens slutdato for de tilsvarende planer.</span><span class="sxs-lookup"><span data-stu-id="d6edc-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="d6edc-110">Den første registrering af genkendelse og kladdeposten til justering bogføres på ikrafttrædelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="d6edc-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="d6edc-111">Funktionen til leasingkonventioner kan aktiveres via Funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="d6edc-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="d6edc-112">I arbejdsområdet i **Funktionsstyring** skal du finde og vælge den funktion, der hedder **Leasingkonvention for leasingfunktionen**, og derefter vælge **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="d6edc-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="d6edc-113">Leasingkonventioner knyttes til opsætningen af et leasinganlægskartotek.</span><span class="sxs-lookup"><span data-stu-id="d6edc-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="d6edc-114">Benyt følgende fremgangsmåde for at få vist eller angive leasingkonventionen.</span><span class="sxs-lookup"><span data-stu-id="d6edc-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="d6edc-115">Gå til **Aktivleasing \> Konfiguration \> Leasingkartotek**.</span><span class="sxs-lookup"><span data-stu-id="d6edc-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="d6edc-116">Vælg en af følgende værdier i feltet **Leasingkonvention**.</span><span class="sxs-lookup"><span data-stu-id="d6edc-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="d6edc-117">Leasingkonvention</span><span class="sxs-lookup"><span data-stu-id="d6edc-117">Leasing convention</span></span> | <span data-ttu-id="d6edc-118">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d6edc-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="d6edc-119">None</span><span class="sxs-lookup"><span data-stu-id="d6edc-119">None</span></span>               | <span data-ttu-id="d6edc-120">Amortisations- og afskrivningsplaner for aktiver træder i gang på startdatoen for leasingaftalen, da startdatoen for afskrivningen er lig med startdatoen for leasingaftalen.</span><span class="sxs-lookup"><span data-stu-id="d6edc-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="d6edc-121">Slutdatoen er én måned senere.</span><span class="sxs-lookup"><span data-stu-id="d6edc-121">The end date is one month later.</span></span> <span data-ttu-id="d6edc-122">Denne leasingkonvention garanterer ikke, at renten vil blive bogført den sidste dag i hver måned.</span><span class="sxs-lookup"><span data-stu-id="d6edc-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="d6edc-123">Hel måned</span><span class="sxs-lookup"><span data-stu-id="d6edc-123">Full month</span></span>         | <span data-ttu-id="d6edc-124">For leasingaftaler, der har en startdato, der finder sted på et vilkårligt tidspunkt i løbet af måneden, starter amortisations- og afskrivningsplanerne for aktiver for at periodisere udgifter den første dag i den pågældende måned.</span><span class="sxs-lookup"><span data-stu-id="d6edc-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="d6edc-125">Denne leasingkonvention sikrer, at der påløber renter på den sidste dag i hver måned for hele måneden.</span><span class="sxs-lookup"><span data-stu-id="d6edc-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="d6edc-126">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="d6edc-126">Select **Save**.</span></span>

<span data-ttu-id="d6edc-127">Når en leasingaftale oprettes, angives startdatoen for hvert kartotek automatisk på baggrund af den startdato, der er angivet for lejen, og den leasingkonvention, der er angivet i kartoteket.</span><span class="sxs-lookup"><span data-stu-id="d6edc-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
