--- 
title: " Bogføre onlinesalg og -betalinger"
description: "Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e8c3f861a53a3f5c2de29248523ff4efd5e1d072
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="0fa4b-103"> Bogføre onlinesalg og -betalinger</span><span class="sxs-lookup"><span data-stu-id="0fa4b-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0fa4b-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="0fa4b-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0fa4b-106">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="0fa4b-107">Kik på Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="0fa4b-108">Vælg "Detailbutikker efter område" i feltet Organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="0fa4b-109">Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="0fa4b-110">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="0fa4b-111">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="0fa4b-112">Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="0fa4b-113">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-113">Click Recurrence.</span></span>
7. <span data-ttu-id="0fa4b-114">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-114">Select the No end date option.</span></span>
8. <span data-ttu-id="0fa4b-115">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="0fa4b-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-116">Click OK.</span></span>
10. <span data-ttu-id="0fa4b-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0fa4b-117">Click OK.</span></span>


