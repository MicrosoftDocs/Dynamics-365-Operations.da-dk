---
title: Konfigurer og kør jobbet for at beregne opgørelser
description: Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11acedb719286cc6c9c79e22e8d0ceca2368baee
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802593"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="0253c-103">Konfigurer og kør jobbet for at beregne opgørelser</span><span class="sxs-lookup"><span data-stu-id="0253c-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0253c-104">Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.</span><span class="sxs-lookup"><span data-stu-id="0253c-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="0253c-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="0253c-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0253c-106">Gå til Alle arbejdsområder > Butiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="0253c-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="0253c-107">Klik på Beregn opgørelser.</span><span class="sxs-lookup"><span data-stu-id="0253c-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="0253c-108">Vælg enten en bestemt butik eller en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="0253c-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="0253c-109">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="0253c-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="0253c-110">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="0253c-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="0253c-111">Vælg "Ja" under batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="0253c-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="0253c-112">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="0253c-112">Click Recurrence.</span></span>
6. <span data-ttu-id="0253c-113">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="0253c-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="0253c-114">Angiv et tidspunkt i feltet Starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="0253c-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="0253c-115">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="0253c-115">Select the No end date option.</span></span>
9. <span data-ttu-id="0253c-116">Angiv "Dage" i feltet PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="0253c-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="0253c-117">Angiv et tal i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="0253c-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="0253c-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0253c-118">Click OK.</span></span>
12. <span data-ttu-id="0253c-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0253c-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]