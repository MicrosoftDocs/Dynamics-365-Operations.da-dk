---
title: Titres de recette i den offentlige sektor i Frankrig
description: Titre de recette bruges af direktøren for at underrette bogholderen om, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed, og til at godkende, at bogholderen indbetaler beløbet. Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver hos direktøren eller bogholderen. Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.
author: rschloma
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 19931
ms.search.region: France
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cb556ebec7070f6291df019b1215a5fcacf6967
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1513117"
---
# <a name="titres-de-recette-in-the-public-sector-in-france"></a><span data-ttu-id="a3187-105">Titres de recette i den offentlige sektor i Frankrig</span><span class="sxs-lookup"><span data-stu-id="a3187-105">Titres de recette in the public sector in France</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3187-106">Titre de recette bruges af direktøren for at underrette bogholderen om, at organisationen er berettiget til at indsamle et bestemt beløb fra en anden enhed, og til at godkende, at bogholderen indbetaler beløbet.</span><span class="sxs-lookup"><span data-stu-id="a3187-106">The titre de recette is used by the director to notify the accountant that the organization is entitled to collect a specific amount from another entity, and to authorize the accountant to deposit that amount.</span></span> <span data-ttu-id="a3187-107">Direktøren eller bogholderen kan delegere en repræsentant til at udføre opgaven, men ansvaret for hver opgave forbliver hos direktøren eller bogholderen.</span><span class="sxs-lookup"><span data-stu-id="a3187-107">The director or the accountant may delegate a representative to perform the task, but the responsibility for each task remains with the director or the accountant.</span></span> <span data-ttu-id="a3187-108">Titre opretholder en nødvendig stram adskillelse mellem direktørens operationelle rolle og bogholderens regnskabsrolle.</span><span class="sxs-lookup"><span data-stu-id="a3187-108">The titre maintains the strict separation that is required between the operational role of the director and the accounting role of the accountant.</span></span>

<span data-ttu-id="a3187-109">I Microsoft Dynamics 365 for Finance and Operations tildeles hver titre en enkelt fritekstfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="a3187-109">In Microsoft Dynamics 365 for Finance and Operations, each titre is assigned a single free text invoice line.</span></span> <span data-ttu-id="a3187-110">Dette garanterer, at hver titre kun vedrører én debitor og indeholder kun én konto i budgettet.</span><span class="sxs-lookup"><span data-stu-id="a3187-110">This guarantees that each titre concerns only one debtor and includes only one budgetary account.</span></span> <span data-ttu-id="a3187-111">En gruppe af relaterede titres sammen med al understøttende dokumentation tildeles til en bordereau de titre for afsendelse til bogholderen.</span><span class="sxs-lookup"><span data-stu-id="a3187-111">A group of related titres, together with all supporting documentation, are assigned to a bordereau de titre for submittal to the accountant.</span></span>

## <a name="directors-tasks"></a><span data-ttu-id="a3187-112">Direktørens opgaver</span><span class="sxs-lookup"><span data-stu-id="a3187-112">Director’s tasks</span></span>
<span data-ttu-id="a3187-113">Fra siden **Vedligehold titres de recette** kan direktøren udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="a3187-113">From the **Maintain titres de recette** page, the director can complete the following tasks:</span></span>

-   <span data-ttu-id="a3187-114">**Tildele fakturalinjer til et titre de recette.**</span><span class="sxs-lookup"><span data-stu-id="a3187-114">**Assign invoice lines to a titre de recette.**</span></span> <span data-ttu-id="a3187-115">Du kan finde de fakturalinjer, der endnu ikke er tildelt til et titre, ved at filtrere de hentede linjer efter kolonnen **Titre**.</span><span class="sxs-lookup"><span data-stu-id="a3187-115">To find the invoice lines that haven’t yet been assigned to a titre, you can filter the retrieved lines by the **Titre** column.</span></span>
-   <span data-ttu-id="a3187-116">**Godkende opkrævning af fakturalinjer, der er tildelt til titres.**</span><span class="sxs-lookup"><span data-stu-id="a3187-116">**Authorize collection of invoice lines that are assigned to titres.**</span></span> <span data-ttu-id="a3187-117">Dette kan også gøres fra fanen **Titre de recette** på fritekstfakturasiden.</span><span class="sxs-lookup"><span data-stu-id="a3187-117">This can also be done from the **Titre de recette** tab on the free text invoice page.</span></span>
-   <span data-ttu-id="a3187-118">**Tildele titres to a bordereau de titre.**</span><span class="sxs-lookup"><span data-stu-id="a3187-118">**Assign titres to a bordereau de titre.**</span></span> <span data-ttu-id="a3187-119">Du kan finde de fakturalinjer, der endnu ikke er tildelt til et Bordereau de titre, ved at filtrere de hentede linjer efter kolonnen **Bordereau de titre**.</span><span class="sxs-lookup"><span data-stu-id="a3187-119">To find the invoice lines that haven’t yet been assigned to a bordereau de titre, you can filter the retrieved lines by the **Bordereau de titre** column.</span></span>

<span data-ttu-id="a3187-120">Hvis du vil sende titres til bogholderen til indbetaling, indsamler direktøren de udskrevne titres og relateret dokumentation under en borderau de titre.</span><span class="sxs-lookup"><span data-stu-id="a3187-120">To submit titres to the accountant for deposit, the director collects the printed titres and their related documentation under a borderau de titre.</span></span>

-   <span data-ttu-id="a3187-121">Udskriv titres, der er tildelt til en bordereau, fra oversigtspanelet **Poster, der skal indgå** på siden **Titre de recette rapport**.</span><span class="sxs-lookup"><span data-stu-id="a3187-121">Print the titres assigned to a bordereau from the **Records to include** FastTab on the **Titre de recette report** page.</span></span>
-   <span data-ttu-id="a3187-122">Udskriv bordereau fra oversigtspanelet **Poster, der skal indgå** på siden **Bordereau de titre rapport**.</span><span class="sxs-lookup"><span data-stu-id="a3187-122">Print the bordereau from the **Records to include** FastTab on the **Bordereau de titre report** page.</span></span>

## <a name="accountants-tasks"></a><span data-ttu-id="a3187-123">Bogholderens opgaver</span><span class="sxs-lookup"><span data-stu-id="a3187-123">Accountant’s tasks</span></span>
<span data-ttu-id="a3187-124">Fra siden **Vedligehold titres de recette** eller fra fanen **Titre de recette** på fritekstfakturasiden kan bogholderen acceptere, afvise eller spærre titeren.</span><span class="sxs-lookup"><span data-stu-id="a3187-124">From the **Maintain titres de recette** page or from the **Titre de recette** tab on the free text invoice page, the accountant can accept, reject, or hold titres.</span></span> <span data-ttu-id="a3187-125">Når et titre er blevet afvist, ændres direktørstatus til Ikke gennemset, og titre- og bordereau de titre-numre fjernes.</span><span class="sxs-lookup"><span data-stu-id="a3187-125">When a titre is rejected, the director status changes to Not reviewed, and the titre and bordereau de titre numbers are cleared.</span></span>

## <a name="using-the-database-inquiry-page"></a><span data-ttu-id="a3187-126">Brug af databaseforespørgselssiden</span><span class="sxs-lookup"><span data-stu-id="a3187-126">Using the database inquiry page</span></span>
<span data-ttu-id="a3187-127">Du kan åbne databaseforespørgselssiden på siden **Vedligehold titres de recette** ved at angive, hvilke datoer du vil vælge fakturaer fra.</span><span class="sxs-lookup"><span data-stu-id="a3187-127">To open the database inquiry page on the **Maintain titres de recette** page, specify the range of dates you want to select invoices from.</span></span> <span data-ttu-id="a3187-128">Klik derefter på **Hent linjer**.</span><span class="sxs-lookup"><span data-stu-id="a3187-128">Then click **Retrieve lines**.</span></span> <span data-ttu-id="a3187-129">Dette åbner databaseforespørgselssiden, hvor du kan angive kriterierne for de fakturalinjer, du vil hente.</span><span class="sxs-lookup"><span data-stu-id="a3187-129">This opens the database inquiry page where you can specify the criteria for the invoice lines you want to retrieve.</span></span> <span data-ttu-id="a3187-130">Når du lukker formularen, hentes alle fakturalinjer, der opfylder de kriterier, der er valgt, til gitteret.</span><span class="sxs-lookup"><span data-stu-id="a3187-130">When you close the form, all the invoice lines that meet the selected criteria are retrieved into the grid.</span></span> <span data-ttu-id="a3187-131">Linjer fra fakturaer, der er ved at blive redigeret, kan ikke hentes.</span><span class="sxs-lookup"><span data-stu-id="a3187-131">Lines from the invoices that are being edited will not be retrieved.</span></span> <span data-ttu-id="a3187-132">**Tip**! Brug følgende kriterier på databaseforespørgselssiden for at hente linjerne.</span><span class="sxs-lookup"><span data-stu-id="a3187-132">**Tip**: Use the following criteria in the database inquiry page to retrieve lines.</span></span>

- <span data-ttu-id="a3187-133">Fakturalinjer, der ikke er gennemset af direktøren.</span><span class="sxs-lookup"><span data-stu-id="a3187-133">Invoice lines that have not been reviewed by the director.</span></span>

  | <span data-ttu-id="a3187-134">Tabellen</span><span class="sxs-lookup"><span data-stu-id="a3187-134">Table</span></span> | <span data-ttu-id="a3187-135">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="a3187-135">Derived table</span></span> |             <span data-ttu-id="a3187-136">Felt</span><span class="sxs-lookup"><span data-stu-id="a3187-136">Field</span></span>             |    <span data-ttu-id="a3187-137">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="a3187-137">Criteria</span></span>    |
  |-------|---------------|-------------------------------|----------------|
  | <span data-ttu-id="a3187-138">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-138">Titre</span></span> |     <span data-ttu-id="a3187-139">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-139">Titre</span></span>     | <span data-ttu-id="a3187-140">Status for direktørgodkendelse</span><span class="sxs-lookup"><span data-stu-id="a3187-140">Director authorization status</span></span> | <span data-ttu-id="a3187-141">"Ikke gennemset"</span><span class="sxs-lookup"><span data-stu-id="a3187-141">"Not reviewed"</span></span> |


- <span data-ttu-id="a3187-142">Fakturalinjer fra titres, der er godkendt til opkrævning af direktøren, men endnu ikke godkendt af bogholderen.</span><span class="sxs-lookup"><span data-stu-id="a3187-142">Invoice lines from titres that have been authorized for collection by the director, but not yet approved by the accountant.</span></span>

  | <span data-ttu-id="a3187-143">Tabellen</span><span class="sxs-lookup"><span data-stu-id="a3187-143">Table</span></span> | <span data-ttu-id="a3187-144">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="a3187-144">Derived table</span></span> |             <span data-ttu-id="a3187-145">Felt</span><span class="sxs-lookup"><span data-stu-id="a3187-145">Field</span></span>             |    <span data-ttu-id="a3187-146">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="a3187-146">Criteria</span></span>    |
  |-------|---------------|-------------------------------|----------------|
  | <span data-ttu-id="a3187-147">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-147">Titre</span></span> |     <span data-ttu-id="a3187-148">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-148">Titre</span></span>     | <span data-ttu-id="a3187-149">Status for direktørgodkendelse</span><span class="sxs-lookup"><span data-stu-id="a3187-149">Director authorization status</span></span> |  <span data-ttu-id="a3187-150">"Godkendt"</span><span class="sxs-lookup"><span data-stu-id="a3187-150">"Authorized"</span></span>  |
  | <span data-ttu-id="a3187-151">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-151">Titre</span></span> |     <span data-ttu-id="a3187-152">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-152">Titre</span></span>     | <span data-ttu-id="a3187-153">Bogholders acceptstatus</span><span class="sxs-lookup"><span data-stu-id="a3187-153">Accountant acceptance status</span></span>  | <span data-ttu-id="a3187-154">"Ikke gennemset"</span><span class="sxs-lookup"><span data-stu-id="a3187-154">"Not reviewed"</span></span> |


- <span data-ttu-id="a3187-155">Fakturalinjer fra titres, der er afvist af bogholderen.</span><span class="sxs-lookup"><span data-stu-id="a3187-155">Invoice lines from titres that were rejected by the accountant.</span></span>

  | <span data-ttu-id="a3187-156">Tabellen</span><span class="sxs-lookup"><span data-stu-id="a3187-156">Table</span></span> | <span data-ttu-id="a3187-157">Afledt tabel</span><span class="sxs-lookup"><span data-stu-id="a3187-157">Derived table</span></span> | <span data-ttu-id="a3187-158">Felt</span><span class="sxs-lookup"><span data-stu-id="a3187-158">Field</span></span>                        | <span data-ttu-id="a3187-159">Afgrænsning</span><span class="sxs-lookup"><span data-stu-id="a3187-159">Criteria</span></span>   |
  |-------|---------------|------------------------------|------------|
  | <span data-ttu-id="a3187-160">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-160">Titre</span></span> | <span data-ttu-id="a3187-161">Titre</span><span class="sxs-lookup"><span data-stu-id="a3187-161">Titre</span></span>         | <span data-ttu-id="a3187-162">Bogholders acceptstatus</span><span class="sxs-lookup"><span data-stu-id="a3187-162">Accountant acceptance status</span></span> | <span data-ttu-id="a3187-163">"Afvist"</span><span class="sxs-lookup"><span data-stu-id="a3187-163">"Rejected"</span></span> |





