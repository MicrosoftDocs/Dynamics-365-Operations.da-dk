---
title: Oprette månedlige kladdeposter i en batch
description: Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971322"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="007b7-103">Oprette månedlige kladdeposter i en batch</span><span class="sxs-lookup"><span data-stu-id="007b7-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="007b7-104">Dette emne forklarer, hvordan du opretter kladdeposteringer i en batch for at øge effektiviteten, når de månedlige leasingudgifter registreres.</span><span class="sxs-lookup"><span data-stu-id="007b7-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="007b7-105">Batchafvikling kan bruges til at oprette kladdeposter fra flere tidsplaner.</span><span class="sxs-lookup"><span data-stu-id="007b7-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="007b7-106">Disse kladdeposteringer kan omfatte leasingbetalinger, passiv afskrivning, brugsretaktiv (ROU) afskrivning af aktiver og udgifter til udført omkostning.</span><span class="sxs-lookup"><span data-stu-id="007b7-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="007b7-107">Du kan også bruge batchbehandling til at udføre den første anerkendelse af flere leasingaftaler samtidigt eller til at oprette overgangsjusteringer for flere leasingaftaler på samme tid.</span><span class="sxs-lookup"><span data-stu-id="007b7-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="007b7-108">Hvis du vil oprette et batchjob eller behandle betalingsfakturaer, afskrivninger eller renter for flere leasingaftaler skal du gå til **Aktivleasing \> Periodisk \> Oprettelse af batchkladde**.</span><span class="sxs-lookup"><span data-stu-id="007b7-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="007b7-109">I den dialogboks, der vises, kan du vælge den plan, som kladdeposterne skal oprettes ud fra.</span><span class="sxs-lookup"><span data-stu-id="007b7-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="007b7-110">Du kan også angive, om batchprocessen skal køres for bestemte enheder, leasinggrupper eller leasingkartoteker.</span><span class="sxs-lookup"><span data-stu-id="007b7-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="007b7-111">Efterfølgende posteringer, f. eks. planer for amortisering af passiver, betalinger, afskrivning og udgifter, bogføres først, når den første godkendelse af de tilsvarende leasingaftaler er bogført.</span><span class="sxs-lookup"><span data-stu-id="007b7-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="007b7-112">Kladdeposterne oprettes, men de bogføres ikke, før du vælger kommandoen **Kør**.</span><span class="sxs-lookup"><span data-stu-id="007b7-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>
