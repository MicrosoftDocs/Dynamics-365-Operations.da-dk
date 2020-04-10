---
title: Konfigurer og kør jobbet for at beregne opgørelser
description: Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141194"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="fe9c6-103">Konfigurer og kør jobbet for at beregne opgørelser</span><span class="sxs-lookup"><span data-stu-id="fe9c6-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe9c6-104">Denne procedure hjælper med at konfigurere og køre tilbagevendende batchjob for at oprette og beregne opgørelser for en valgt butik eller butiksgruppe.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="fe9c6-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="fe9c6-106">Gå til Alle arbejdsområder > Butiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="fe9c6-107">Klik på Beregn opgørelser.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="fe9c6-108">Vælg enten en bestemt butik eller en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="fe9c6-109">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="fe9c6-110">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="fe9c6-111">Vælg "Ja" under batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="fe9c6-112">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-112">Click Recurrence.</span></span>
6. <span data-ttu-id="fe9c6-113">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="fe9c6-114">Angiv et tidspunkt i feltet Starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="fe9c6-115">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-115">Select the No end date option.</span></span>
9. <span data-ttu-id="fe9c6-116">Angiv "Dage" i feltet PatternUnit.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="fe9c6-117">Angiv et tal i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="fe9c6-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-118">Click OK.</span></span>
12. <span data-ttu-id="fe9c6-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="fe9c6-119">Click OK.</span></span>

