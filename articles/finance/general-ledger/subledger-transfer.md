---
title: Overføre reskontro til Finans
description: Dette emne beskriver egenskaber i Microsoft Dynamics 365 Finance, der er relateret til processen for overførsel af reskontro i finansmodulet.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000441"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="e9208-103">Overføre reskontro til Finans</span><span class="sxs-lookup"><span data-stu-id="e9208-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9208-104">Dette emne indeholder en beskrivelse af de egenskaber i Microsoft Dynamics 365 Finance, der er knyttet til reglerne for overførsel af batches for kladdeposteringer af reskontro.</span><span class="sxs-lookup"><span data-stu-id="e9208-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="e9208-105">I version 8.1 blev der foretaget ændringer for at tillade overførsel af regler, der udfasede den synkrone indstilling.</span><span class="sxs-lookup"><span data-stu-id="e9208-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="e9208-106">Du kan finde flere oplysninger under [Fjernede eller udfasede funktioner for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="e9208-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="e9208-107">Følgende indstillinger er tilgængelige for overførsel af reskontrobatches.</span><span class="sxs-lookup"><span data-stu-id="e9208-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="e9208-108">Asynkron – Denne indstilling planlægger straks overførslen af reskontroregnskabsposter til Finans.</span><span class="sxs-lookup"><span data-stu-id="e9208-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="e9208-109">Finansbilaget registreres, så snart ressourcer der er ledige ressourcer til at behandle denne anmodning på serveren.</span><span class="sxs-lookup"><span data-stu-id="e9208-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="e9208-110">Planlagt batch – Denne indstilling vil tilføje de reskontroregnskabsposter, der overføres til behandlingskøen i finansmodulet, hvor posterne skal behandles i den modtagne ordre.</span><span class="sxs-lookup"><span data-stu-id="e9208-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="e9208-111">Finansbilaget registreres på det planlagte tidspunkt, hvis der er ledige ressourcer til at behandle dette batchjob på serveren.</span><span class="sxs-lookup"><span data-stu-id="e9208-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="e9208-112">I version 10.0.8 er der sket forbedringer af ydeevnen for indstillingen Asynkron.</span><span class="sxs-lookup"><span data-stu-id="e9208-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="e9208-113">Denne funktion er aktiveret under funktionsnavnet **Overførsel af reskontro til Finans med performance-optimering**.</span><span class="sxs-lookup"><span data-stu-id="e9208-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="e9208-114">Denne funktionalitet forbedrer overførslen af data fra reskontro til Finans.</span><span class="sxs-lookup"><span data-stu-id="e9208-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="e9208-115">Processen kan være mere effektiv, og den grupperer sæt med mindre transaktioner, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="e9208-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="e9208-116">Det giver en mere effektiv brug af batchserveren.</span><span class="sxs-lookup"><span data-stu-id="e9208-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="e9208-117">Denne funktionalitet kræver, at batchserveren konfigureres, er online og fungerer, for at den asynkrone overførselsindstilling kan fungere.</span><span class="sxs-lookup"><span data-stu-id="e9208-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 
