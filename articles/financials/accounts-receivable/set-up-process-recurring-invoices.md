---
title: Oprette og behandle tilbagevendende fakturaer
description: I denne artikel beskrives det, hvordan du opretter og behandler tilbagevendende fakturaer. Du kan bruge tilbagevendende fakturaer, hvis du skal fakturere kunder for samme beløb med jævne mellemrum.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b443630d1612b5095fefa74b5ed6d057be534b7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843067"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="0c158-104">Oprette og behandle tilbagevendende fakturaer</span><span class="sxs-lookup"><span data-stu-id="0c158-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c158-105">I denne artikel beskrives det, hvordan du opretter og behandler tilbagevendende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c158-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="0c158-106">Du kan bruge tilbagevendende fakturaer, hvis du skal fakturere kunder for samme beløb med jævne mellemrum.</span><span class="sxs-lookup"><span data-stu-id="0c158-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="0c158-107">Oprette en skabelon til en tilbagevendende fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="0c158-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="0c158-108">Hvis du regelmæssigt skal fakturere kunder for de samme tjenester, kan du definere en skabelon til fritekstfakturaer, som kan genbruges til oprettelse af fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="0c158-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="0c158-109">Denne skabelon indeholder følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0c158-109">This template contains the following information:</span></span>

-   <span data-ttu-id="0c158-110">Hovedoplysninger, som momsgrupper, betalingsbetingelser og betalingsmåde</span><span class="sxs-lookup"><span data-stu-id="0c158-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="0c158-111">Linjeoplysninger som beskrivelse af tjenesten, indtægtskonti, enhedspris og fakturabeløb</span><span class="sxs-lookup"><span data-stu-id="0c158-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="0c158-112">Gebyrer for forsendelse eller håndtering</span><span class="sxs-lookup"><span data-stu-id="0c158-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="0c158-113">Regnskabsfordelinger samt økonomiske dimensionsoplysninger som bærere og virksomhedsenheder</span><span class="sxs-lookup"><span data-stu-id="0c158-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="0c158-114">Du opretter reelt en hel faktura og gemme den som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="0c158-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="0c158-115">Du kan konfigurere skabeloner ved hjælp af siden **Tilbagevendende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="0c158-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="0c158-116">Tildele en fritekstfakturaskabelon til en debitor, og angiv oplysninger om gentagelse</span><span class="sxs-lookup"><span data-stu-id="0c158-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="0c158-117">Når skabelonen er oprettet, skal du tildele skabelonen til de kunder, som du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="0c158-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="0c158-118">Derudover skal du angive, hvornår og hvor ofte fakturaen skal bruges.</span><span class="sxs-lookup"><span data-stu-id="0c158-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="0c158-119">Du kan tildele skabelonerne under fanen **Faktura** på siden **Kunder**.</span><span class="sxs-lookup"><span data-stu-id="0c158-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="0c158-120">Føj skabelonen til listen, og opdater følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="0c158-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="0c158-121">Startdatoen og eventuelt slutdatoen for den tilbagevendende fakturering.</span><span class="sxs-lookup"><span data-stu-id="0c158-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="0c158-122">Hyppigheden af den tilbagevendende fakturering (f.eks. hver dag eller en gang om måneden)</span><span class="sxs-lookup"><span data-stu-id="0c158-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="0c158-123">Det maksimale faktureringsbeløb (hvis disse oplysninger er påkrævet)</span><span class="sxs-lookup"><span data-stu-id="0c158-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="0c158-124">En kunde kan have flere skabeloner, der har forskellige frekvenser.</span><span class="sxs-lookup"><span data-stu-id="0c158-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="0c158-125">Oprette de tilbagevendende fakturaer</span><span class="sxs-lookup"><span data-stu-id="0c158-125">Generate the recurring invoices</span></span>
<span data-ttu-id="0c158-126">På siden **Tilbagevendende fakturaer** er der en opgave, der behandler skabeloner til tilbagevendende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c158-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="0c158-127">Du angiver fakturadatoen og skabelonen, som fakturaerne skal oprettes ud fra.</span><span class="sxs-lookup"><span data-stu-id="0c158-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="0c158-128">Fakturaer oprettes og tildeles et enkelt gentagelses-id for hver gruppe fakturaer, der er behandlet.</span><span class="sxs-lookup"><span data-stu-id="0c158-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="0c158-129">Bogføre tilbagevendende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="0c158-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="0c158-130">Når der er oprettet tilbagevendende fakturaer, vises fakturaens gentagelses-id'er i en bogføringsopgave på siden **Tilbagevendende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="0c158-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="0c158-131">Du kan få vist alle fakturaer for et gentagelses-id ved at klikke på linket.</span><span class="sxs-lookup"><span data-stu-id="0c158-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="0c158-132">Under din gennemgang af fakturaer for gentagelses-id'et kan du slette enkelte fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c158-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="0c158-133">Kundens indstillinger for gentagelse nulstilles for den pågældende skabelon, så den kan gendannes senere.</span><span class="sxs-lookup"><span data-stu-id="0c158-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="0c158-134">Du kan bogføre en, mange eller alle fakturaer for et gentagelses-id.</span><span class="sxs-lookup"><span data-stu-id="0c158-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="0c158-135">Hvis arbejdsgange er aktiveret, skal du klikke på **Send**, før du kan bogføre fakturaerne.</span><span class="sxs-lookup"><span data-stu-id="0c158-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="0c158-136">Udskriv tilbagevendende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="0c158-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="0c158-137">Når tilbagevendende fakturaer bogføres, kan du udskrive fakturaer fra listesiden med fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="0c158-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="0c158-138">Du kan udskrive de fakturaer, der er valgt, eller du kan vælge et interval af fakturaer, der skal udskrives.</span><span class="sxs-lookup"><span data-stu-id="0c158-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>



