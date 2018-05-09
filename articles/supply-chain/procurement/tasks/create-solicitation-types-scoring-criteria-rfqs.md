--- 
title: Oprette anmodningstyper og scorekriterier for tilbudsanmodninger
description: Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode.
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6876f8ed0f69ec5a34c4c9671081c76245945b1e
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="a3bc7-103">Oprette anmodningstyper og scorekriterier for tilbudsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a3bc7-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3bc7-104">Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="a3bc7-105">Den viser også, hvordan du bruger anmodningstypen på en tilbudsanmodninger, som derefter angiver standardscoremetoden.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="a3bc7-106">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="a3bc7-107">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a3bc7-108">Du skal have en scoremetode tilgængelig, før du starter.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="a3bc7-109">Oprette en anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-109">Create a solicitation type</span></span>
1. <span data-ttu-id="a3bc7-110">Gå til Indkøb og forsyning > Opsætning > Tilbudsanmodning > Anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="a3bc7-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-111">Click New.</span></span>
3. <span data-ttu-id="a3bc7-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a3bc7-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a3bc7-114">Vælg i feltet Scoremetode den scoremetode, du vil bruge for denne anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="a3bc7-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-115">Click Save.</span></span>
7. <span data-ttu-id="a3bc7-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="a3bc7-117">Brug anmodningstypen</span><span class="sxs-lookup"><span data-stu-id="a3bc7-117">Use the solicitation type</span></span>
1. <span data-ttu-id="a3bc7-118">Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="a3bc7-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-119">Click New.</span></span>
3. <span data-ttu-id="a3bc7-120">I feltet Anmodningstype skal du vælge den anmodningstype, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="a3bc7-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-121">Click OK.</span></span>
5. <span data-ttu-id="a3bc7-122">Klik på Scorekriterier.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="a3bc7-123">De scorekriterier, der vises, er dem fra scoremetoden, som du har knyttet til anmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="a3bc7-124">Du kan vælge at tilføje eller slette kriterierne på denne side.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="a3bc7-125">Det er også muligt at tilføje nye kriterier ved at kopiere dem fra andre scoremetoder.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="a3bc7-126">Klik på Kopiér kriterier.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="a3bc7-127">Indtast eller vælg en værdi i feltet Scoremetode.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="a3bc7-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-128">Click OK.</span></span>
9. <span data-ttu-id="a3bc7-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a3bc7-129">Close the page.</span></span>


