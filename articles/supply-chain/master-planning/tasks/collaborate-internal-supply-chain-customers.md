---
title: Samarbejde med intern forsyningskædes kunder
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
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84c42e550d51e40b7f777c3da67ed765519ddfd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424650"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="39703-103">Samarbejde med intern forsyningskædes kunder</span><span class="sxs-lookup"><span data-stu-id="39703-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39703-104">Denne fremgangsmåde viser, hvordan du får vist alle forslag, der opfyldes af en intern kreditor.</span><span class="sxs-lookup"><span data-stu-id="39703-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="39703-105">Det demodatafirma, der bruges til at oprette denne procedure, er DEMF.</span><span class="sxs-lookup"><span data-stu-id="39703-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="39703-106">Klik på Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="39703-106">Click Master planning.</span></span>
2. <span data-ttu-id="39703-107">Indtast eller vælg en værdi i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="39703-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="39703-108">Vælg plan 10 i feltet Plan.</span><span class="sxs-lookup"><span data-stu-id="39703-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="39703-109">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="39703-109">Click Run.</span></span>
4. <span data-ttu-id="39703-110">Indtast et antal i feltet Antal tråde.</span><span class="sxs-lookup"><span data-stu-id="39703-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="39703-111">Dette repræsenterer antallet af parallelle tråde, der skal bruges til behovsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="39703-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="39703-112">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="39703-112">Click OK.</span></span>
    * <span data-ttu-id="39703-113">Det kan tage et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="39703-113">This may take a while.</span></span>  
6. <span data-ttu-id="39703-114">Klik på Planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="39703-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="39703-115">Klik på Udgående planlagt intern efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="39703-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="39703-116">Denne side indeholder en oversigt over alle planlagte behov, der opfyldes af en intern leverandør i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="39703-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="39703-117">Udvid sektionen Upstream detaljer om efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="39703-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="39703-118">I dette afsnit finder du oplysninger om, hvordan behovet opfyldes.</span><span class="sxs-lookup"><span data-stu-id="39703-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="39703-119">Du skal måske vente på, at varedisponering kører i forsyningsfirmaet, før du kan se yderligere oplysninger her.</span><span class="sxs-lookup"><span data-stu-id="39703-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

