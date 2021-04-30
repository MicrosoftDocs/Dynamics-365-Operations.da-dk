---
title: Overføre reskontro til Finans
description: Dette emne beskriver egenskaber i Microsoft Dynamics 365 Finance, der er relateret til processen for overførsel af reskontro i finansmodulet.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897498"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="4475c-103">Overføre reskontro til Finans</span><span class="sxs-lookup"><span data-stu-id="4475c-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4475c-104">Dette emne indeholder en beskrivelse af de egenskaber i Microsoft Dynamics 365 Finance, der er knyttet til reglerne for overførsel af batches for kladdeposteringer af reskontro.</span><span class="sxs-lookup"><span data-stu-id="4475c-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="4475c-105">I version 8.1 blev der foretaget ændringer for at tillade overførsel af regler, der udfasede den **synkrone** indstilling.</span><span class="sxs-lookup"><span data-stu-id="4475c-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="4475c-106">Du kan finde flere oplysninger under [Fjernede eller udfasede funktioner for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="4475c-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="4475c-107">Følgende indstillinger er tilgængelige for overførsel af reskontrobatches.</span><span class="sxs-lookup"><span data-stu-id="4475c-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="4475c-108">Asynkron – Denne indstilling planlægger straks overførslen af reskontroregnskabsposter til Finans.</span><span class="sxs-lookup"><span data-stu-id="4475c-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="4475c-109">Finansbilaget registreres, så snart ressourcer der er ledige ressourcer til at behandle denne anmodning på serveren.</span><span class="sxs-lookup"><span data-stu-id="4475c-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="4475c-110">Planlagt batch – Denne indstilling vil tilføje de reskontroregnskabsposter, der overføres til behandlingskøen i finansmodulet, hvor posterne skal behandles i den modtagne ordre.</span><span class="sxs-lookup"><span data-stu-id="4475c-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="4475c-111">Finansbilaget registreres på det planlagte tidspunkt, hvis der er ledige ressourcer til at behandle dette batchjob på serveren.</span><span class="sxs-lookup"><span data-stu-id="4475c-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="4475c-112">I version 10.0.8 er der sket forbedringer af ydeevnen for indstillingen Asynkron.</span><span class="sxs-lookup"><span data-stu-id="4475c-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="4475c-113">Denne funktion er aktiveret under funktionsnavnet **Overførsel af reskontro til Finans med performance-optimering**.</span><span class="sxs-lookup"><span data-stu-id="4475c-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="4475c-114">Denne funktionalitet forbedrer overførslen af data fra reskontro til Finans.</span><span class="sxs-lookup"><span data-stu-id="4475c-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="4475c-115">Processen kan være mere effektiv, og den grupperer sæt med mindre transaktioner, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="4475c-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="4475c-116">Det giver en mere effektiv brug af batchserveren.</span><span class="sxs-lookup"><span data-stu-id="4475c-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="4475c-117">Denne funktionalitet kræver, at batchserveren konfigureres, er online og fungerer, for at den asynkrone overførselsindstilling kan fungere.</span><span class="sxs-lookup"><span data-stu-id="4475c-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]