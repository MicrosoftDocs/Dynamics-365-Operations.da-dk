---
title: Foretage fejlfinding i procesproduktion
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med procesproduktion.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966174"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="1b551-103">Foretage fejlfinding i procesproduktion</span><span class="sxs-lookup"><span data-stu-id="1b551-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="1b551-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med procesproduktion.</span><span class="sxs-lookup"><span data-stu-id="1b551-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="1b551-105">Når jeg bruger jobkortenheden til at rapportere en delmængde på det sidste job i en produktionsordre, vil alle tidligere job på den ordre, der har status som igangværende, automatisk blive afsluttet.</span><span class="sxs-lookup"><span data-stu-id="1b551-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="1b551-106">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="1b551-106">This behavior is by design.</span></span> <span data-ttu-id="1b551-107">På siden **Produktionsordrestandarder** under fanen **Færdigmelding** er der en indstilling med navnet **Slutmarker rute**.</span><span class="sxs-lookup"><span data-stu-id="1b551-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="1b551-108">Hvis dette emne er angivet til *Ja*, bogføres en rutekortkladde, når en arbejder bruger jobkortenheden eller jobkortterminalen til at rapportere den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="1b551-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="1b551-109">I denne kladde markeres alle operationer som fuldført, og alle produktionsjob afsluttes.</span><span class="sxs-lookup"><span data-stu-id="1b551-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="1b551-110">Når indstillingen **Slutmarker rute** er angivet til *Ja*, betragter systemet ikke den jobstatus, som arbejderen valgte, da denne rapporterede den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="1b551-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="1b551-111">Systemet overvejer heller ikke, om arbejderen rapporterer en fuld eller delvis mængde.</span><span class="sxs-lookup"><span data-stu-id="1b551-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="1b551-112">Når jeg forsøger på lagerlukning, får jeg vist følgende advarselsmeddelelse: "Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning".</span><span class="sxs-lookup"><span data-stu-id="1b551-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="1b551-113">Hvis du i versioner før 10.0.13 ikke bruger omkostningsforløbet for lean produktionsflow, får du vist følgende fejlmeddelelse under lagerlukningen:</span><span class="sxs-lookup"><span data-stu-id="1b551-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="1b551-114">Du er ved at udføre en lagerlukning med datoen %1.</span><span class="sxs-lookup"><span data-stu-id="1b551-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="1b551-115">Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning.</span><span class="sxs-lookup"><span data-stu-id="1b551-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="1b551-116">Husk at udføre beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning.</span><span class="sxs-lookup"><span data-stu-id="1b551-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="1b551-117">Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i Reskontro eller Finans, før dette er udført.</span><span class="sxs-lookup"><span data-stu-id="1b551-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="1b551-118">Dette problem er løst i version 10.0.13 og senere.</span><span class="sxs-lookup"><span data-stu-id="1b551-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="1b551-119">Du kan finde flere oplysninger i [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="1b551-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
