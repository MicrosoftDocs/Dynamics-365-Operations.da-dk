---
title: Genklassificere den kortfristede del af leasingforpligtelse
description: I dette emne forklares det, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet.
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
ms.openlocfilehash: 7d98d66b5fe9d32a86eb75d937fedfdca6773ac4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823089"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="20b40-103">Genklassificere den kortfristede del af leasingforpligtelsen</span><span class="sxs-lookup"><span data-stu-id="20b40-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20b40-104">I dette emne forklares det, hvordan du opretter en måneds kladdepost, så en del af leasingforpligtelsen klassificeres som kortfristet.</span><span class="sxs-lookup"><span data-stu-id="20b40-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="20b40-105">Når den plan, der er valgt i batchprocessen, er **Kortsigtet omposteringsleasingforpligtelse**, oprettes der en kladdepost.</span><span class="sxs-lookup"><span data-stu-id="20b40-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="20b40-106">Denne post bruges til bogføring af den aktuelle del af en leasingforpligtelse på den sidste dag i måneden.</span><span class="sxs-lookup"><span data-stu-id="20b40-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="20b40-107">På samme tid, bogføres en post for tilbageførsel pr. den første dag i den næste måned.</span><span class="sxs-lookup"><span data-stu-id="20b40-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="20b40-108">Den kortfristede del af leasingforpligtelsen vises i planen for leasingamortisering.</span><span class="sxs-lookup"><span data-stu-id="20b40-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="20b40-109">Når kladdeposten er bogført, bliver kolonnen **Kladde, der er oprettet for passiv** tilgængelig, og kladde-id'et angives også i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="20b40-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="20b40-110">Udfør følgende trin for at oprette og bogføre den kortfristede passiv-omposteringskladde.</span><span class="sxs-lookup"><span data-stu-id="20b40-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="20b40-111">Gå til det **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**.</span><span class="sxs-lookup"><span data-stu-id="20b40-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="20b40-112">I dialogboksen **Oprettelse af batchkladde** i feltet **Vælg tidsplan** kan du vælge **Kortfristet leasingforpligtelse**.</span><span class="sxs-lookup"><span data-stu-id="20b40-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="20b40-113">Vælg en leasinggruppe i feltet **Leasinggruppe**.</span><span class="sxs-lookup"><span data-stu-id="20b40-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="20b40-114">Alternativt kan du vælge Kartotek-id i feltet **Kartotek-id**.</span><span class="sxs-lookup"><span data-stu-id="20b40-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="20b40-115">Aktiver parameteren **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="20b40-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="20b40-116">Alternativt, hvis posten skal oprettes men ikke bogføres, skal denne parameter være deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="20b40-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="20b40-117">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="20b40-117">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
