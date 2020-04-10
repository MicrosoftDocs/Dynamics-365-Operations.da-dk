---
title: Samarbejde med intern forsyningskædes kunder
description: Denne fremgangsmåde viser, hvordan du får vist alle forslag, der opfyldes af en intern kreditor.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2746534cc808dc61e54aa55c1030422bb37e8984
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148141"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="3d754-103">Samarbejde med intern forsyningskædes kunder</span><span class="sxs-lookup"><span data-stu-id="3d754-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d754-104">Denne fremgangsmåde viser, hvordan du får vist alle forslag, der opfyldes af en intern kreditor.</span><span class="sxs-lookup"><span data-stu-id="3d754-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="3d754-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="3d754-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="3d754-106">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="3d754-106">Click Master planning.</span></span>
2. <span data-ttu-id="3d754-107">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="3d754-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="3d754-108">Vælg plan 10 i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="3d754-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="3d754-109">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="3d754-109">Click Run.</span></span>
4. <span data-ttu-id="3d754-110">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="3d754-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="3d754-111">Dette repræsenterer antallet af parallelle tråde, der skal bruges til behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="3d754-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="3d754-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3d754-112">Click OK.</span></span>
    * <span data-ttu-id="3d754-113">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="3d754-113">This may take a while.</span></span>  
6. <span data-ttu-id="3d754-114">Klik på Planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="3d754-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="3d754-115">Klik på Udgående planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="3d754-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="3d754-116">Denne side indeholder en oversigt over alle planlagte behov, der opfyldes af en intern leverandør i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="3d754-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="3d754-117">Udvid sektionen Upstream detaljer om efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="3d754-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="3d754-118">I dette afsnit finder du oplysninger om, hvordan behovet opfyldes.</span><span class="sxs-lookup"><span data-stu-id="3d754-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="3d754-119">Du skal måske vente på, at varedisponering kører i forsyningsfirmaet, før du kan se yderligere oplysninger her.</span><span class="sxs-lookup"><span data-stu-id="3d754-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

