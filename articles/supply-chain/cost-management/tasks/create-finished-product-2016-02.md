--- 
title: "Oprette et færdigt produkt (kun februar 2016)"
description: "Denne opgave drejer sig om oprettelse af et færdigt produkt."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f1cfd25f44182650330e0ff927c2e660f27f134d
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="aee74-103">Oprette et færdigt produkt (kun februar 2016)</span><span class="sxs-lookup"><span data-stu-id="aee74-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aee74-104">Denne opgave drejer sig om oprettelse af et færdigt produkt.</span><span class="sxs-lookup"><span data-stu-id="aee74-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="aee74-105">Det er den første opgave i styklisteberegningsserien.</span><span class="sxs-lookup"><span data-stu-id="aee74-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="aee74-106">Det demodatafirma, der bruges til at oprette denne opgave, er USMF.</span><span class="sxs-lookup"><span data-stu-id="aee74-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="aee74-107">Gå til Administration af produktoplysninger > Produkter > Frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="aee74-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="aee74-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="aee74-108">Click New.</span></span>
3. <span data-ttu-id="aee74-109">Skriv en værdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="aee74-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="aee74-110">Skriv BOM_1 i demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="aee74-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="aee74-111">Indtast eller vælg en værdi i feltet Varemodelgruppe.</span><span class="sxs-lookup"><span data-stu-id="aee74-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-112">Vælg STD.</span><span class="sxs-lookup"><span data-stu-id="aee74-112">Select STD.</span></span> <span data-ttu-id="aee74-113">STD står for standardomkostninger og er den mest almindeligt anvendte model, når du arbejder med omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="aee74-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="aee74-114">Indtast eller vælg en værdi i feltet Varegruppe.</span><span class="sxs-lookup"><span data-stu-id="aee74-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-115">Vælg f.eks. Lyd.</span><span class="sxs-lookup"><span data-stu-id="aee74-115">For example, select Audio.</span></span> <span data-ttu-id="aee74-116">Dette har ingen indflydelse på omkostningsberegninger.</span><span class="sxs-lookup"><span data-stu-id="aee74-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="aee74-117">Indtast eller vælg en værdi i feltet Lagringsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="aee74-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-118">Vælg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="aee74-118">Select SiteWH.</span></span> <span data-ttu-id="aee74-119">Kun lokation og lagersted bruges til demonstrationen.</span><span class="sxs-lookup"><span data-stu-id="aee74-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="aee74-120">Indtast eller vælg en værdi i feltet Sporingsdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="aee74-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-121">Sporingsdimensioner bliver ikke brugt i dette eksempel. Vælg Ingen.</span><span class="sxs-lookup"><span data-stu-id="aee74-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="aee74-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="aee74-122">Click OK.</span></span>
9. <span data-ttu-id="aee74-123">Klik på Styr lager i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="aee74-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="aee74-124">Klik på Standardindstillinger for ordre.</span><span class="sxs-lookup"><span data-stu-id="aee74-124">Click Default order settings.</span></span>
11. <span data-ttu-id="aee74-125">Vælg en indstilling i feltet Produktion.</span><span class="sxs-lookup"><span data-stu-id="aee74-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="aee74-126">Da dette er et færdigt produkt, der skal produceres, skal du vælge Produktion.</span><span class="sxs-lookup"><span data-stu-id="aee74-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="aee74-127">Indtast eller vælg en værdi i feltet Købssted.</span><span class="sxs-lookup"><span data-stu-id="aee74-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-128">Vælg Sted 1 i demonstrationen</span><span class="sxs-lookup"><span data-stu-id="aee74-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="aee74-129">Indtast eller vælg en værdi i feltet Sted for lager.</span><span class="sxs-lookup"><span data-stu-id="aee74-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-130">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="aee74-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="aee74-131">Indtast eller vælg en værdi i feltet Salgssted.</span><span class="sxs-lookup"><span data-stu-id="aee74-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="aee74-132">I dette eksempel skal du vælge Sted 1.</span><span class="sxs-lookup"><span data-stu-id="aee74-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="aee74-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aee74-133">Close the page.</span></span>


