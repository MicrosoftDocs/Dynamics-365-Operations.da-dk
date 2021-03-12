---
title: Fragtgrupper
description: Dette emne beskriver, hvordan du konfigurerer data til fragtgrupper.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 14a2f4c7d8d053ffd7b4b5d090113e1d9c3294c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974104"
---
# <a name="carrier-groups"></a><span data-ttu-id="3fd5d-103">Fragtgrupper</span><span class="sxs-lookup"><span data-stu-id="3fd5d-103">Carrier groups</span></span>

<span data-ttu-id="3fd5d-104">En fragtgruppe er en samling fragtmænd og fragttjenester.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="3fd5d-105">Hver fragtmand angiver den foretrukne rækkefølge for de fragtmænd og fragttjenester, der tilhører den.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="3fd5d-106">Når der findes flere fragtmænd og fragttjenester for samme rutesegment, kan du angive en fragtgruppe i stedet for en bestemt fragtmand og fragttjeneste i ruteplanen eller rutevejledningen.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="3fd5d-107">Oprette en fragtgruppe</span><span class="sxs-lookup"><span data-stu-id="3fd5d-107">Create a carrier group</span></span>

1. <span data-ttu-id="3fd5d-108">Gå til **Transportstyring &gt; Opsætning &gt; Fragtmænd &gt; Fragtgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="3fd5d-109">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-109">Select **New**.</span></span>
1. <span data-ttu-id="3fd5d-110">Angiv et entydigt id for gruppen i feltet **Fragtgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="3fd5d-111">Angiv et sigende navn for gruppen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="3fd5d-112">Tilføj en række i oversigtspanelet **Detaljer**, og vælg en fragtmand og en fragttjeneste for den.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="3fd5d-113">Gentag dette trin, indtil du har tilføjet så mange fragtmænd, du skal bruge for gruppen.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="3fd5d-114">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3fd5d-114">Close the page.</span></span>
