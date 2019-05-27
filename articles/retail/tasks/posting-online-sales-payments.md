---
title: Bogføring af onlinesalg og betalinger
description: Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.
author: jashanno
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
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550202"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="7722d-103">Bogføring af onlinesalg og betalinger</span><span class="sxs-lookup"><span data-stu-id="7722d-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7722d-104">Denne procedure hjælper med at konfigurere og køre et tilbagevendende batchjob for at oprette salgsordrer og betalinger for transaktioner i onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="7722d-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="7722d-105">Denne procedure bruger USRT-firmaets demodata.</span><span class="sxs-lookup"><span data-stu-id="7722d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="7722d-106">Gå til Alle arbejdsområder > Detailbutiksregnskab.</span><span class="sxs-lookup"><span data-stu-id="7722d-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="7722d-107">Kik på Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="7722d-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="7722d-108">Vælg "Detailbutikker efter område" i feltet Organisationshierarki.</span><span class="sxs-lookup"><span data-stu-id="7722d-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="7722d-109">Vælg enten en bestemt onlinebutik, eller vælg en node, hvis du vil oprette batchjobbet for en gruppe butikker.</span><span class="sxs-lookup"><span data-stu-id="7722d-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="7722d-110">Klik på pilen for at føje dit valg.</span><span class="sxs-lookup"><span data-stu-id="7722d-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="7722d-111">Klik på fanen Kør i baggrunden.</span><span class="sxs-lookup"><span data-stu-id="7722d-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="7722d-112">Markér eller fjern markeringen af afkrydsningsfeltet Batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="7722d-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="7722d-113">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="7722d-113">Click Recurrence.</span></span>
7. <span data-ttu-id="7722d-114">Vælg indstillingen Slutdato mangler.</span><span class="sxs-lookup"><span data-stu-id="7722d-114">Select the No end date option.</span></span>
8. <span data-ttu-id="7722d-115">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="7722d-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="7722d-116">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7722d-116">Click OK.</span></span>
10. <span data-ttu-id="7722d-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7722d-117">Click OK.</span></span>

