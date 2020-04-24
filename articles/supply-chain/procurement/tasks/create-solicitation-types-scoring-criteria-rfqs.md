---
title: Oprette anmodningstyper og scorekriterier for tilbudsanmodninger
description: Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204671"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="a9142-103">Oprette anmodningstyper og scorekriterier for tilbudsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a9142-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9142-104">Denne vejledning viser dig, hvordan du opretter en anmodningstype og knytter det til en scoremetode.</span><span class="sxs-lookup"><span data-stu-id="a9142-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="a9142-105">Den viser også, hvordan du bruger anmodningstypen på en tilbudsanmodninger, som derefter angiver standardscoremetoden.</span><span class="sxs-lookup"><span data-stu-id="a9142-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="a9142-106">Disse opgaver udføres normalt af en indkøbschef.</span><span class="sxs-lookup"><span data-stu-id="a9142-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="a9142-107">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="a9142-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a9142-108">Du skal have en scoremetode tilgængelig, før du starter.</span><span class="sxs-lookup"><span data-stu-id="a9142-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="a9142-109">Oprette en anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a9142-109">Create a solicitation type</span></span>
1. <span data-ttu-id="a9142-110">Gå til Indkøb og forsyning > Opsætning > Tilbudsanmodning > Anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a9142-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="a9142-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a9142-111">Click New.</span></span>
3. <span data-ttu-id="a9142-112">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a9142-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a9142-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a9142-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a9142-114">Vælg i feltet Scoremetode den scoremetode, du vil bruge for denne anmodningstype.</span><span class="sxs-lookup"><span data-stu-id="a9142-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="a9142-115">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a9142-115">Click Save.</span></span>
7. <span data-ttu-id="a9142-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a9142-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="a9142-117">Brug anmodningstypen</span><span class="sxs-lookup"><span data-stu-id="a9142-117">Use the solicitation type</span></span>
1. <span data-ttu-id="a9142-118">Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="a9142-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="a9142-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="a9142-119">Click New.</span></span>
3. <span data-ttu-id="a9142-120">I feltet Anmodningstype skal du vælge den anmodningstype, som du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a9142-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="a9142-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a9142-121">Click OK.</span></span>
5. <span data-ttu-id="a9142-122">Klik på Scorekriterier.</span><span class="sxs-lookup"><span data-stu-id="a9142-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="a9142-123">De scorekriterier, der vises, er dem fra scoremetoden, som du har knyttet til anmodningstypen.</span><span class="sxs-lookup"><span data-stu-id="a9142-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="a9142-124">Du kan vælge at tilføje eller slette kriterierne på denne side.</span><span class="sxs-lookup"><span data-stu-id="a9142-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="a9142-125">Det er også muligt at tilføje nye kriterier ved at kopiere dem fra andre scoremetoder.</span><span class="sxs-lookup"><span data-stu-id="a9142-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="a9142-126">Klik på Kopiér kriterier.</span><span class="sxs-lookup"><span data-stu-id="a9142-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="a9142-127">Indtast eller vælg en værdi i feltet Scoremetode.</span><span class="sxs-lookup"><span data-stu-id="a9142-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="a9142-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a9142-128">Click OK.</span></span>
9. <span data-ttu-id="a9142-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a9142-129">Close the page.</span></span>

