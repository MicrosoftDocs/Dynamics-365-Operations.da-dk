--- 
title: Oprette kriterier for valg af salgspris
description: Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ce805b0bf43c931ebca13720d43754c18094fc85
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="cec75-103">Oprette kriterier for valg af salgspris</span><span class="sxs-lookup"><span data-stu-id="cec75-103">Create sales price selection criteria</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cec75-104">Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.</span><span class="sxs-lookup"><span data-stu-id="cec75-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="cec75-105">Denne procedure kræver, at der er mindst én tilgængelig salgspris.</span><span class="sxs-lookup"><span data-stu-id="cec75-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="cec75-106">I dette eksempel bruges prismodellen for salgsprismodellen for højttalerløsningen i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="cec75-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="cec75-107">Normalt bruger en produktchef denne procedure.</span><span class="sxs-lookup"><span data-stu-id="cec75-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="cec75-108">Tilføj et nyt kriterium for en eksisterende salgsprismodel</span><span class="sxs-lookup"><span data-stu-id="cec75-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="cec75-109">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="cec75-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="cec75-110">Klik på Produktkonfigurationsmodeller.</span><span class="sxs-lookup"><span data-stu-id="cec75-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="cec75-111">På listen skal du vælge rækken for produktmodellen for højttalerløsningen, men ikke klikke på linket for modelnavnet.</span><span class="sxs-lookup"><span data-stu-id="cec75-111">In the list, select the row for the Speaker solution product model, but don’t click the link for the model name.</span></span>
4. <span data-ttu-id="cec75-112">Klik på Model i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cec75-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="cec75-113">Klik på Prismodelkriterier.</span><span class="sxs-lookup"><span data-stu-id="cec75-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="cec75-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="cec75-114">Click New.</span></span>
7. <span data-ttu-id="cec75-115">Skriv "Kundegruppe 10" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cec75-115">In the Name field, type ‘Customer group 10’.</span></span>
    * <span data-ttu-id="cec75-116">Navnet på prismodelkriteriet bruges til at identificere de underliggende udvælgelseskriterier.</span><span class="sxs-lookup"><span data-stu-id="cec75-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="cec75-117">Indtast eller vælg en værdi i feltet Prismodel.</span><span class="sxs-lookup"><span data-stu-id="cec75-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="cec75-118">I feltet Ordretype skal du vælge "Salgsordre".</span><span class="sxs-lookup"><span data-stu-id="cec75-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="cec75-119">Ordretypen bestemmer de databasefelter, der er tilgængelige for valgforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="cec75-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="cec75-120">Indtast en dato i feltet Gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="cec75-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="cec75-121">Angiv en dato i feltet Udløber senest.</span><span class="sxs-lookup"><span data-stu-id="cec75-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="cec75-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cec75-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="cec75-123">Opret forespørgslen for udvælgelseskriterierne</span><span class="sxs-lookup"><span data-stu-id="cec75-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="cec75-124">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cec75-124">Click Edit.</span></span>
2. <span data-ttu-id="cec75-125">Vælg Kunder i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="cec75-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="cec75-126">Vælg Kundegruppe i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="cec75-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="cec75-127">I dette eksempel bruger vi en specifik kundegruppe til udvælgelseskriterierne.</span><span class="sxs-lookup"><span data-stu-id="cec75-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="cec75-128">Vælg Kundegruppe 10 i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="cec75-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="cec75-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cec75-129">Click OK.</span></span>


