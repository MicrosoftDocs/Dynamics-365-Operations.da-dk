---
title: Frigive en produktionsordre
description: Denne procedure viser, hvordan du frigiver en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: beef850e7e58fb58db545c0be5990b52619070d3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424324"
---
# <a name="release-a-production-order"></a><span data-ttu-id="6fdff-103">Frigive en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="6fdff-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fdff-104">Denne procedure viser, hvordan du frigiver en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="6fdff-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="6fdff-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="6fdff-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6fdff-106">Dette er den fjerde procedure ud af syv, der beskriver produktionsordrens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="6fdff-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="6fdff-107">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="6fdff-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="6fdff-108">Vælg en produktionsordre med status Planlagt i gitteret.</span><span class="sxs-lookup"><span data-stu-id="6fdff-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="6fdff-109">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6fdff-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="6fdff-110">Klik på Frigiv.</span><span class="sxs-lookup"><span data-stu-id="6fdff-110">Click Release.</span></span>
    * <span data-ttu-id="6fdff-111">På denne side kan du bekræfte frigivelsen af det markerede område af produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="6fdff-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="6fdff-112">Klik på Vælg, hvis du vil tilføje ordrer.</span><span class="sxs-lookup"><span data-stu-id="6fdff-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="6fdff-113">Trinnet Frigiv angiver, hvornår produktionsordren er frigivet til produktionen, så operatører i produktionen kan rapportere status for produktionsjob.</span><span class="sxs-lookup"><span data-stu-id="6fdff-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="6fdff-114">Der kan udstedes produktionspapirer, der indeholder relevante oplysninger om behandling af job.</span><span class="sxs-lookup"><span data-stu-id="6fdff-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="6fdff-115">Lagerstedsarbejde til pluk af råvarer genereres for de varer, der er defineret for lagerstedsprocessen.</span><span class="sxs-lookup"><span data-stu-id="6fdff-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="6fdff-116">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="6fdff-116">Click the General tab.</span></span>
    * <span data-ttu-id="6fdff-117">Vælg, hvilke produktionsrapporter der skal udskrives.</span><span class="sxs-lookup"><span data-stu-id="6fdff-117">Select which production reports should be printed.</span></span> <span data-ttu-id="6fdff-118">Jobkortrapporten udskriver en side for hvert planlagt job og kræver, at produktionsordren planlægges på jobniveau.</span><span class="sxs-lookup"><span data-stu-id="6fdff-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="6fdff-119">Rapporten indeholder oplysninger om planlagt start- og sluttidspunkt, antallet, der skal produceres, og hvilken ressource der behandler jobbet.</span><span class="sxs-lookup"><span data-stu-id="6fdff-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="6fdff-120">Rapporten Rutejob indsamler de samme oplysninger på den samme side, men udskriver ikke en side for hvert job.</span><span class="sxs-lookup"><span data-stu-id="6fdff-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="6fdff-121">Rapporten Rutekort viser kun handlingerne, men ikke jobbene.</span><span class="sxs-lookup"><span data-stu-id="6fdff-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="6fdff-122">Derfor kræver denne rapport ikke finplanlægning, men kan bruges, når produktionsordrer planlægges på driftsniveau.</span><span class="sxs-lookup"><span data-stu-id="6fdff-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="6fdff-123">Markér afkrydsningsfeltet Udskriv rutekort.</span><span class="sxs-lookup"><span data-stu-id="6fdff-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="6fdff-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6fdff-124">Click OK.</span></span>
7. <span data-ttu-id="6fdff-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6fdff-125">Close the page.</span></span>

