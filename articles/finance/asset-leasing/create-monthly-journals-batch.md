---
title: Oprette månedlige kladdeposter i en batch
description: Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881198"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="5b231-103">Oprette månedlige kladdeposter i en batch</span><span class="sxs-lookup"><span data-stu-id="5b231-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b231-104">Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres.</span><span class="sxs-lookup"><span data-stu-id="5b231-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="5b231-105">Batchafvikling kan bruges til at oprette kladdeposter fra flere tidsplaner.</span><span class="sxs-lookup"><span data-stu-id="5b231-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="5b231-106">Disse kladdeposteringer kan omfatte leasingbetalinger, passiv afskrivning, brugsretaktiv (ROU) afskrivning af aktiver og udgifter til udført omkostning.</span><span class="sxs-lookup"><span data-stu-id="5b231-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="5b231-107">Du kan også bruge batchbehandling til at udføre den første anerkendelse af flere leasingaftaler samtidigt eller til at oprette overgangsjusteringer for flere leasingaftaler på samme tid.</span><span class="sxs-lookup"><span data-stu-id="5b231-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="5b231-108">Hvis du vil oprette et batchjob eller behandle betalingsfakturaer, afskrivninger eller renter for flere leasingaftaler skal du gå til **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**.</span><span class="sxs-lookup"><span data-stu-id="5b231-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="5b231-109">I den dialogboks, der vises, kan du vælge den plan, som kladdeposterne skal oprettes ud fra.</span><span class="sxs-lookup"><span data-stu-id="5b231-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="5b231-110">Du kan også angive, om batchprocessen skal køres for bestemte enheder, leasinggrupper eller leasingkartoteker.</span><span class="sxs-lookup"><span data-stu-id="5b231-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="5b231-111">Efterfølgende posteringer, f. eks. planer for amortisering af passiver, betalinger, afskrivning og udgifter, bogføres først, når den første godkendelse af de tilsvarende leasingaftaler er bogført.</span><span class="sxs-lookup"><span data-stu-id="5b231-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="5b231-112">Kladdeposterne oprettes, men de bogføres ikke, før du vælger kommandoen **Kør**.</span><span class="sxs-lookup"><span data-stu-id="5b231-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
