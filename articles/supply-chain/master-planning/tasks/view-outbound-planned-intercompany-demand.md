---
title: Vise udgående planlagt intern efterspørgsel
description: Denne fremgangsmåde viser, hvordan du får vist alle forslag, der opfyldes af en intern kreditor.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd24e2e19e3e7257f37ebc0becb8af2fdf82b546
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208587"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="be78e-103">Vise udgående planlagt intern efterspørgsel</span><span class="sxs-lookup"><span data-stu-id="be78e-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be78e-104">Denne fremgangsmåde viser, hvordan du får vist alle forslag, der opfyldes af en intern kreditor.</span><span class="sxs-lookup"><span data-stu-id="be78e-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="be78e-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="be78e-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="be78e-106">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="be78e-106">Click Master planning.</span></span>
2. <span data-ttu-id="be78e-107">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="be78e-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="be78e-108">Vælg plan 10 i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="be78e-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="be78e-109">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="be78e-109">Click Run.</span></span>
4. <span data-ttu-id="be78e-110">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="be78e-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="be78e-111">Dette repræsenterer antallet af parallelle tråde, der skal bruges til behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="be78e-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="be78e-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="be78e-112">Click OK.</span></span>
    * <span data-ttu-id="be78e-113">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="be78e-113">This may take a while.</span></span>  
6. <span data-ttu-id="be78e-114">Klik på Planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="be78e-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="be78e-115">Klik på Udgående planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="be78e-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="be78e-116">Denne side indeholder en oversigt over alle planlagte behov, der opfyldes af en intern leverandør i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="be78e-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="be78e-117">Udvid sektionen Upstream detaljer om efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="be78e-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="be78e-118">I dette afsnit finder du oplysninger om, hvordan behovet opfyldes.</span><span class="sxs-lookup"><span data-stu-id="be78e-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="be78e-119">Du skal måske vente på, at varedisponering kører i forsyningsfirmaet, før du kan se yderligere oplysninger her.</span><span class="sxs-lookup"><span data-stu-id="be78e-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

