--- 
title: " Konfigurere og køre et job for at beregne opgørelser"
description: "Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 329da4ebe56a3f975ad65474068e3548c23405b4
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="6ad53-103"> Konfigurere og køre et job for at beregne opgørelser</span><span class="sxs-lookup"><span data-stu-id="6ad53-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6ad53-104">Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.</span><span class="sxs-lookup"><span data-stu-id="6ad53-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="6ad53-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="6ad53-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6ad53-106">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="6ad53-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="6ad53-107">Klik på Beregn opgørelser.</span><span class="sxs-lookup"><span data-stu-id="6ad53-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="6ad53-108">Vælg enten en bestemt butik eller en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="6ad53-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="6ad53-109">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="6ad53-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="6ad53-110">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="6ad53-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="6ad53-111">Vælg "Ja" under batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="6ad53-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="6ad53-112">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="6ad53-112">Click Recurrence.</span></span>
6. <span data-ttu-id="6ad53-113">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="6ad53-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="6ad53-114">Angiv et tidspunkt i feltet Starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="6ad53-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="6ad53-115">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="6ad53-115">Select the No end date option.</span></span>
9. <span data-ttu-id="6ad53-116">Angiv "Dage" i feltet PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="6ad53-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="6ad53-117">Angiv et tal i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="6ad53-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="6ad53-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ad53-118">Click OK.</span></span>
12. <span data-ttu-id="6ad53-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6ad53-119">Click OK.</span></span>


