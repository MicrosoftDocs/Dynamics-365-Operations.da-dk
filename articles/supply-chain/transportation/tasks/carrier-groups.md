---
title: Fragtgrupper
description: Dette emne beskriver, hvordan du konfigurerer data til fragtgrupper.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9fe95ee9a0b6d69544f35ac6bc9cdf3dd00db291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809056"
---
# <a name="carrier-groups"></a><span data-ttu-id="65967-103">Fragtgrupper</span><span class="sxs-lookup"><span data-stu-id="65967-103">Carrier groups</span></span>

<span data-ttu-id="65967-104">En fragtgruppe er en samling fragtmænd og fragttjenester.</span><span class="sxs-lookup"><span data-stu-id="65967-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="65967-105">Hver fragtmand angiver den foretrukne rækkefølge for de fragtmænd og fragttjenester, der tilhører den.</span><span class="sxs-lookup"><span data-stu-id="65967-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="65967-106">Når der findes flere fragtmænd og fragttjenester for samme rutesegment, kan du angive en fragtgruppe i stedet for en bestemt fragtmand og fragttjeneste i ruteplanen eller rutevejledningen.</span><span class="sxs-lookup"><span data-stu-id="65967-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="65967-107">Oprette en fragtgruppe</span><span class="sxs-lookup"><span data-stu-id="65967-107">Create a carrier group</span></span>

1. <span data-ttu-id="65967-108">Gå til **Transportstyring &gt; Opsætning &gt; Fragtmænd &gt; Fragtgruppe**.</span><span class="sxs-lookup"><span data-stu-id="65967-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="65967-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="65967-109">Select **New**.</span></span>
1. <span data-ttu-id="65967-110">Angiv et entydigt id for gruppen i feltet **Fragtgruppe**.</span><span class="sxs-lookup"><span data-stu-id="65967-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="65967-111">Angiv et sigende navn for gruppen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="65967-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="65967-112">Tilføj en række i oversigtspanelet **Detaljer**, og vælg en fragtmand og en fragttjeneste for den.</span><span class="sxs-lookup"><span data-stu-id="65967-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="65967-113">Gentag dette trin, indtil du har tilføjet så mange fragtmænd, du skal bruge for gruppen.</span><span class="sxs-lookup"><span data-stu-id="65967-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="65967-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="65967-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]