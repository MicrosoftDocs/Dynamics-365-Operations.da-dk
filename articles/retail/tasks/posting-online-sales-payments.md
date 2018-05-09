--- 
title: " Bogføre onlinesalg og -betalinger"
description: "Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 463a68e73e04990a99323f9f77d9936f586a575c
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="0c899-103"> Bogføre onlinesalg og -betalinger</span><span class="sxs-lookup"><span data-stu-id="0c899-103">Post online sales and payments</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0c899-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="0c899-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="0c899-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="0c899-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0c899-106">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="0c899-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="0c899-107">Kik på Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="0c899-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="0c899-108">Vælg "Detailbutikker efter område" i feltet Organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="0c899-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="0c899-109">Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="0c899-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="0c899-110">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="0c899-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="0c899-111">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="0c899-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="0c899-112">Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="0c899-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="0c899-113">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="0c899-113">Click Recurrence.</span></span>
7. <span data-ttu-id="0c899-114">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="0c899-114">Select the No end date option.</span></span>
8. <span data-ttu-id="0c899-115">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0c899-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="0c899-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0c899-116">Click OK.</span></span>
10. <span data-ttu-id="0c899-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0c899-117">Click OK.</span></span>


