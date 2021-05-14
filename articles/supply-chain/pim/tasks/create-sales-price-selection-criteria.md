---
title: Oprette kriterier for valg af salgspris
description: Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920525"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="494f6-103">Oprette kriterier for valg af salgspris</span><span class="sxs-lookup"><span data-stu-id="494f6-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="494f6-104">Denne procedure viser, hvordan du opretter et valgkriterium for salgspris til attributbaserede salgsprismodeller.</span><span class="sxs-lookup"><span data-stu-id="494f6-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="494f6-105">Denne procedure kræver, at der er mindst én tilgængelig salgspris.</span><span class="sxs-lookup"><span data-stu-id="494f6-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="494f6-106">I dette eksempel bruges prismodellen for salgsprismodellen for højttalerløsningen i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="494f6-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="494f6-107">Normalt bruger en produktchef denne procedure.</span><span class="sxs-lookup"><span data-stu-id="494f6-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="494f6-108">Tilføj et nyt kriterium for en eksisterende salgsprismodel</span><span class="sxs-lookup"><span data-stu-id="494f6-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="494f6-109">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="494f6-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="494f6-110">På listen skal du vælge rækken for produktmodellen for højttalerløsning, men ikke vælge linket for modelnavnet.</span><span class="sxs-lookup"><span data-stu-id="494f6-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="494f6-111">Vælg **Model** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="494f6-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="494f6-112">Vælg **Prismodelkriterier**.</span><span class="sxs-lookup"><span data-stu-id="494f6-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="494f6-113">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="494f6-113">Select **New**.</span></span>
1. <span data-ttu-id="494f6-114">Skriv 'Kundegruppe 10' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="494f6-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="494f6-115">Navnet på prismodelkriteriet bruges til at identificere de underliggende udvælgelseskriterier.</span><span class="sxs-lookup"><span data-stu-id="494f6-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="494f6-116">Indtast eller vælg en værdi i feltet **Prismodel**.</span><span class="sxs-lookup"><span data-stu-id="494f6-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="494f6-117">I feltet **Ordretype** skal du vælge *Salgsordre*.</span><span class="sxs-lookup"><span data-stu-id="494f6-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="494f6-118">Ordretypen bestemmer de databasefelter, der er tilgængelige for valgforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="494f6-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="494f6-119">Indtast en dato i feltet **Gyldig fra**.</span><span class="sxs-lookup"><span data-stu-id="494f6-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="494f6-120">Angiv en dato i feltet **Udløber senest**.</span><span class="sxs-lookup"><span data-stu-id="494f6-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="494f6-121">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="494f6-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="494f6-122">Opret forespørgslen for udvælgelseskriterierne</span><span class="sxs-lookup"><span data-stu-id="494f6-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="494f6-123">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="494f6-123">Select **Edit**.</span></span>
2. <span data-ttu-id="494f6-124">Vælg *Kunder* i feltet **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="494f6-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="494f6-125">Vælg *Kundegruppe* i feltet **Felt**.</span><span class="sxs-lookup"><span data-stu-id="494f6-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="494f6-126">I dette eksempel bruger vi en specifik kundegruppe til udvælgelseskriterierne.</span><span class="sxs-lookup"><span data-stu-id="494f6-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="494f6-127">Vælg *Kundegruppe 10* i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="494f6-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="494f6-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="494f6-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]