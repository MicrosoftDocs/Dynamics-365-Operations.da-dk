---
title: Oprette en leasinggruppe
description: I dette emne forklares, hvordan du konfigurerer leasinggrupper. Der kræves leasinggrupper for at oprette nye leasingaftaler.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 88a49e4db868078fd05875df33ca5727363aaa18
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881222"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="2d38c-104">Oprette en leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="2d38c-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d38c-105">I dette emne forklares, hvordan du konfigurerer leasinggrupper.</span><span class="sxs-lookup"><span data-stu-id="2d38c-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="2d38c-106">Der kræves leasinggrupper for at oprette nye leasingaftaler.</span><span class="sxs-lookup"><span data-stu-id="2d38c-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="2d38c-107">Leasingkartoteker knyttes til hver leasinggruppe.</span><span class="sxs-lookup"><span data-stu-id="2d38c-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="2d38c-108">Leasingkartoteker bestemmer, hvilke standardprofiler der skal oprettes for hver leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="2d38c-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="2d38c-109">Du kan knytte bestemte konti til en leasinggruppe på siden **Leasingbogføringsparametre**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="2d38c-110">Oprette en leasingprofil og tilføje en leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="2d38c-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="2d38c-111">Gå til **Aktivleasing \> Konfiguration \> Leasinggrupper**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="2d38c-112">Vælg **Ny** i handlingsruden for at tilføje en leasinggruppe.</span><span class="sxs-lookup"><span data-stu-id="2d38c-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="2d38c-113">Der føjes en linje til gitteret.</span><span class="sxs-lookup"><span data-stu-id="2d38c-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="2d38c-114">Angiv en værdi i feltet **Leasinggruppe**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="2d38c-115">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="2d38c-116">De oplysninger, du netop har angivet, føjes til feltet **Leasinggruppe** på siden **Tilføj leasingaftale**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="2d38c-117">Knytte et kartotek til en leasinggruppe</span><span class="sxs-lookup"><span data-stu-id="2d38c-117">Associate a book with a lease group</span></span>

<span data-ttu-id="2d38c-118">Når du har oprettet leasinggrupper, kan du knytte kartoteker til hver gruppe.</span><span class="sxs-lookup"><span data-stu-id="2d38c-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="2d38c-119">Når du opretter en leasingaftale og tildeler den til en leasinggruppe, opretter systemet et sæt planer for hvert enkelt kartotek, der er knyttet til leasinggruppen.</span><span class="sxs-lookup"><span data-stu-id="2d38c-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="2d38c-120">Kartoteker skal konfigureres, før de kan tildeles en leasinggruppe.</span><span class="sxs-lookup"><span data-stu-id="2d38c-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="2d38c-121">Gå til **Aktivleasing \> Konfiguration \> Leasinggruppe**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="2d38c-122">Vælg en leasinggruppe, og vælg derefter **Kartoteker**.</span><span class="sxs-lookup"><span data-stu-id="2d38c-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="2d38c-123">Vælg **Ny**, og vælg derefter feltet **Kartotekstype**, der skal knyttes til leasinggruppen.</span><span class="sxs-lookup"><span data-stu-id="2d38c-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="2d38c-124">Du kan tildele flere kartoteker til en leasinggruppe, hvis en leasingaftalen skal redegøres for på forskellige måder.</span><span class="sxs-lookup"><span data-stu-id="2d38c-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
