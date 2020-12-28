---
title: Titres de recette i den offentlige sektor i Frankrig
description: Titres de recette bruges af direktøren til at underrette og autorisere bogholderen til at opkræve og deponere et specifikt beløb fra en anden enhed.
author: rschloma
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 19931
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0ccd613b4118bc7bada51fd8da84eb89b568c37
ms.sourcegitcommit: 102c1e998a591a295307c588dfe523cfa750d43c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665498"
---
# <a name="titres-de-recette-in-the-public-sector-in-france"></a><span data-ttu-id="b3bb7-103">Titres de recette i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="b3bb7-103">Titres de recette in the public sector in France</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3bb7-104">Direktøren bruger titres de recette til at underrette og autorisere bogholderen til at opkræve og deponere et specifikt beløb fra en anden enhed.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-104">The director uses the titre de recette to notify and authorize the accountant to collect and deposit a specific amount from another entity.</span></span> <span data-ttu-id="b3bb7-105">Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-105">The director or the accountant may delegate a representative to perform the task.</span></span> <span data-ttu-id="b3bb7-106">Ansvaret for hver opgave er dog stadig direktørens eller bogholderens.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-106">However, the responsibility for each task remains with the director or the accountant.</span></span> <span data-ttu-id="b3bb7-107">Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-107">The titre maintains the strict separation that is required between the director's operational role and the accountant's accounting role.</span></span>

<span data-ttu-id="b3bb7-108">I Dynamics 365 Finance tildeles hver titre en enkelt fritekstfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-108">In Dynamics 365 Finance, each titre is assigned a single free text invoice line.</span></span> <span data-ttu-id="b3bb7-109">Denne tildeling garanterer, at hver titre kun vedrører én debitor og indeholder kun én konto i budgettet.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-109">This assignment guarantees that each titre concerns only one debtor and includes only one budgetary account.</span></span> <span data-ttu-id="b3bb7-110">En gruppe af relaterede titres sammen med al understøttende dokumentation tildeles til en bordereau de titre for afsendelse til bogholderen.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-110">A group of related titres, together with all supporting documentation, are assigned to a bordereau de titre for submittal to the accountant.</span></span>

## <a name="directors-tasks"></a><span data-ttu-id="b3bb7-111">Direktørens opgaver</span><span class="sxs-lookup"><span data-stu-id="b3bb7-111">Director’s tasks</span></span>
<span data-ttu-id="b3bb7-112">Fra siden **Vedligehold titres de recette** kan direktøren udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="b3bb7-112">From the **Maintain titres de recette** page, the director can complete the following tasks:</span></span>

-   <span data-ttu-id="b3bb7-113">**Tildele fakturalinjer til et titre de recette.**</span><span class="sxs-lookup"><span data-stu-id="b3bb7-113">**Assign invoice lines to a titre de recette.**</span></span> <span data-ttu-id="b3bb7-114">Du kan finde de fakturalinjer, der endnu ikke er tildelt til et titre, ved at filtrere de hentede linjer efter kolonnen **Titre**.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-114">To find the invoice lines that haven’t yet been assigned to a titre, you can filter the retrieved lines by the **Titre** column.</span></span>
-   <span data-ttu-id="b3bb7-115">**Godkende opkrævning af fakturalinjer, der er tildelt til titres.**</span><span class="sxs-lookup"><span data-stu-id="b3bb7-115">**Authorize collection of invoice lines that are assigned to titres.**</span></span> <span data-ttu-id="b3bb7-116">Godkendelse kan også ske fra fanen **Titre de recette** på siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-116">Authorization can also be completed from the **Titre de recette** tab on the **Free text invoice** page.</span></span>
-   <span data-ttu-id="b3bb7-117">**Tildele titres to a bordereau de titre.**</span><span class="sxs-lookup"><span data-stu-id="b3bb7-117">**Assign titres to a bordereau de titre.**</span></span> <span data-ttu-id="b3bb7-118">Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de titre, ved at bruge kolonnen **Bordereau de titre** til at filtrere de hentede linjer.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-118">To find the invoice lines that haven’t yet been assigned to a bordereau de titre, use the **Bordereau de titre** column to filter the retrieved lines.</span></span>

<span data-ttu-id="b3bb7-119">Hvis du vil sende titres til bogholderen til indbetaling, indsamler direktøren de udskrevne titres og relateret dokumentation under en borderau de titre.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-119">To submit titres to the accountant for deposit, the director collects the printed titres and their related documentation under a borderau de titre.</span></span>

-   <span data-ttu-id="b3bb7-120">Udskriv titres, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Titre de recette rapport**.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-120">Print the titres assigned to a bordereau from the **Records to include** FastTab on the **Titre de recette report** page.</span></span>
-   <span data-ttu-id="b3bb7-121">Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de titre rapport**.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-121">Print the bordereau from the **Records to include** FastTab on the **Bordereau de titre report** page.</span></span>

## <a name="accountants-tasks"></a><span data-ttu-id="b3bb7-122">Bogholderens opgaver</span><span class="sxs-lookup"><span data-stu-id="b3bb7-122">Accountant’s tasks</span></span>
<span data-ttu-id="b3bb7-123">Fra siden **Vedligehold titres de recette** eller fra fanen **Titre de recette** på fritekstfakturasiden kan bogholderen acceptere, afvise eller spærre titeren.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-123">From the **Maintain titres de recette** page or from the **Titre de recette** tab on the free text invoice page, the accountant can accept, reject, or hold titres.</span></span> <span data-ttu-id="b3bb7-124">Når et titre afvises, ændres direktørstatus til Ikke gennemset.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-124">When a titre is rejected, the director status changes to Not reviewed.</span></span> <span data-ttu-id="b3bb7-125">Tal for titre og bordereau de titre ryddes.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-125">The titre and bordereau de titre numbers are cleared.</span></span>

## <a name="using-the-database-inquiry-page"></a><span data-ttu-id="b3bb7-126">Brug af Database-forespørgselssiden</span><span class="sxs-lookup"><span data-stu-id="b3bb7-126">Using the Database inquiry page</span></span>
<span data-ttu-id="b3bb7-127">Du kan åbne siden **Databaseforespørgsel** fra siden **Vedligehold titres de recette** ved at angive, hvilke datoer du vil vælge fakturaer fra.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-127">To open the **Database inquiry** page from the **Maintain titres de recette** page, specify the range of dates you want to select invoices from.</span></span> <span data-ttu-id="b3bb7-128">Klik derefter på **Hent linjer**.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-128">Then click **Retrieve lines**.</span></span> <span data-ttu-id="b3bb7-129">Siden **Databaseforespørgsel** åbnes, og her kan du angive kriterierne for de fakturalinjer, du vil hente.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-129">Thhe **Database inquiry** page opens and you can specify the criteria for the invoice lines you want to retrieve.</span></span> <span data-ttu-id="b3bb7-130">Når du lukker siden, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-130">When you close the page, all the invoice lines that meet the selected criteria are retrieved into the grid.</span></span> <span data-ttu-id="b3bb7-131">Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-131">Lines from the invoices that are being edited will not be retrieved.</span></span> 

<span data-ttu-id="b3bb7-132">Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-132">Use the following criteria in the database inquiry page to retrieve lines.</span></span>

- <span data-ttu-id="b3bb7-133">Fakturalinjer, der ikke er gennemset af direktøren.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-133">Invoice lines that have not been reviewed by the director.</span></span>

  | <span data-ttu-id="b3bb7-134">Tabellen</span><span class="sxs-lookup"><span data-stu-id="b3bb7-134">Table</span></span> | <span data-ttu-id="b3bb7-135">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="b3bb7-135">Derived table</span></span> |             <span data-ttu-id="b3bb7-136">Felt</span><span class="sxs-lookup"><span data-stu-id="b3bb7-136">Field</span></span>             |    <span data-ttu-id="b3bb7-137">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="b3bb7-137">Criteria</span></span>    |
  |-------|---------------|-------------------------------|----------------|
  | <span data-ttu-id="b3bb7-138">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-138">Titre</span></span> |     <span data-ttu-id="b3bb7-139">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-139">Titre</span></span>     | <span data-ttu-id="b3bb7-140">Status for direktørgodkendelse</span><span class="sxs-lookup"><span data-stu-id="b3bb7-140">Director authorization status</span></span> | <span data-ttu-id="b3bb7-141">"Ikke gennemset"</span><span class="sxs-lookup"><span data-stu-id="b3bb7-141">"Not reviewed"</span></span> |


- <span data-ttu-id="b3bb7-142">Fakturalinjer fra titres, der er godkendt til opkrævning af direktøren, men endnu ikke godkendt af bogholderen.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-142">Invoice lines from titres that have been authorized for collection by the director, but not yet approved by the accountant.</span></span>

  | <span data-ttu-id="b3bb7-143">Tabellen</span><span class="sxs-lookup"><span data-stu-id="b3bb7-143">Table</span></span> | <span data-ttu-id="b3bb7-144">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="b3bb7-144">Derived table</span></span> |             <span data-ttu-id="b3bb7-145">Felt</span><span class="sxs-lookup"><span data-stu-id="b3bb7-145">Field</span></span>             |    <span data-ttu-id="b3bb7-146">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="b3bb7-146">Criteria</span></span>    |
  |-------|---------------|-------------------------------|----------------|
  | <span data-ttu-id="b3bb7-147">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-147">Titre</span></span> |     <span data-ttu-id="b3bb7-148">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-148">Titre</span></span>     | <span data-ttu-id="b3bb7-149">Status for direktørgodkendelse</span><span class="sxs-lookup"><span data-stu-id="b3bb7-149">Director authorization status</span></span> |  <span data-ttu-id="b3bb7-150">"Godkendt"</span><span class="sxs-lookup"><span data-stu-id="b3bb7-150">"Authorized"</span></span>  |
  | <span data-ttu-id="b3bb7-151">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-151">Titre</span></span> |     <span data-ttu-id="b3bb7-152">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-152">Titre</span></span>     | <span data-ttu-id="b3bb7-153">Bogholders acceptstatus</span><span class="sxs-lookup"><span data-stu-id="b3bb7-153">Accountant acceptance status</span></span>  | <span data-ttu-id="b3bb7-154">"Ikke gennemset"</span><span class="sxs-lookup"><span data-stu-id="b3bb7-154">"Not reviewed"</span></span> |


- <span data-ttu-id="b3bb7-155">Fakturalinjer fra titres, der er afvist af bogholderen.</span><span class="sxs-lookup"><span data-stu-id="b3bb7-155">Invoice lines from titres that were rejected by the accountant.</span></span>

  | <span data-ttu-id="b3bb7-156">Tabellen</span><span class="sxs-lookup"><span data-stu-id="b3bb7-156">Table</span></span> | <span data-ttu-id="b3bb7-157">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="b3bb7-157">Derived table</span></span> | <span data-ttu-id="b3bb7-158">Felt</span><span class="sxs-lookup"><span data-stu-id="b3bb7-158">Field</span></span>                        | <span data-ttu-id="b3bb7-159">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="b3bb7-159">Criteria</span></span>   |
  |-------|---------------|------------------------------|------------|
  | <span data-ttu-id="b3bb7-160">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-160">Titre</span></span> | <span data-ttu-id="b3bb7-161">Titre</span><span class="sxs-lookup"><span data-stu-id="b3bb7-161">Titre</span></span>         | <span data-ttu-id="b3bb7-162">Bogholders acceptstatus</span><span class="sxs-lookup"><span data-stu-id="b3bb7-162">Accountant acceptance status</span></span> | <span data-ttu-id="b3bb7-163">"Afvist"</span><span class="sxs-lookup"><span data-stu-id="b3bb7-163">"Rejected"</span></span> |





