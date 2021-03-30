---
title: Referencer til oprindelige fakturaer på kreditnotaer
description: Dette emne indeholder en forklaring på, hvordan du opretter og udskriver de oprindelige fakturanumre i relaterede kreditnotaer.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207345"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="81588-103">Referencer til oprindelige fakturaer på kreditnotaer</span><span class="sxs-lookup"><span data-stu-id="81588-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="81588-104">I nogle lande og områder er der et juridisk krav om, at udskrevne kreditnotaer skal indeholde referencer til de oprindelige fakturaer.</span><span class="sxs-lookup"><span data-stu-id="81588-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="81588-105">Dette emne indeholder en forklaring på, hvordan du opretter og udskriver de oprindelige fakturanumre i relaterede kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="81588-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="81588-106">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="81588-106">Prerequisites</span></span>

- <span data-ttu-id="81588-107">Brug arbejdsområdet **Funktionsstyring** til at aktivere funktionen **Layout til fakturakreditering i salgs- og projektfakturarapporter**.</span><span class="sxs-lookup"><span data-stu-id="81588-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="81588-108">Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="81588-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="81588-109">De formater til krævede dokumenter, der kan udskrives, skal konfigureres i Udskriftsstyring.</span><span class="sxs-lookup"><span data-stu-id="81588-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="81588-110">De funktioner, der er beskrevet i dette emne, gælder for følgende dokumenter:</span><span class="sxs-lookup"><span data-stu-id="81588-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="81588-111">**Debitor**</span><span class="sxs-lookup"><span data-stu-id="81588-111">**Accounts receivable**</span></span>

- <span data-ttu-id="81588-112">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="81588-112">Free text credit note</span></span>
- <span data-ttu-id="81588-113">Kreditnota til kunden</span><span class="sxs-lookup"><span data-stu-id="81588-113">Customer credit note</span></span>

<span data-ttu-id="81588-114">**Projektstyring og regnskab**</span><span class="sxs-lookup"><span data-stu-id="81588-114">**Project management and accounting**</span></span>

- <span data-ttu-id="81588-115">Projektkreditnota</span><span class="sxs-lookup"><span data-stu-id="81588-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="81588-116">Konfigurere debitorparametre</span><span class="sxs-lookup"><span data-stu-id="81588-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="81588-117">Benyt følgende fremgangsmåde for at angive den parameter, der styrer, om referencer til de oprindelige fakturaer udskrives på relaterede kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="81588-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="81588-118">Gå til **Debitor** \> **Konfiguration** \> **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="81588-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="81588-119">Under fanen **Opdateringer** i oversigtspanelet **Faktura** skal du angive indstillingen **Anvend layoutet for fakturakreditering i rapporter for salgs- og projektfakturaer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="81588-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Konfigurere debitorparametre](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="81588-121">Definere referencer til oprindelige fakturaer</span><span class="sxs-lookup"><span data-stu-id="81588-121">Define references to original invoices</span></span>

<span data-ttu-id="81588-122">Benyt følgende procedurer til at definere referencer til oprindelige fakturaer på basis af dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="81588-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="81588-123">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="81588-123">Free text credit note</span></span>

1. <span data-ttu-id="81588-124">Gå til **Debitor** \> **Fakturaer** \> **Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="81588-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="81588-125">Opret en ny kreditnota, eller vælg en eksisterende kreditnota.</span><span class="sxs-lookup"><span data-stu-id="81588-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="81588-126">Åbn fakturaen.</span><span class="sxs-lookup"><span data-stu-id="81588-126">Open the invoice.</span></span>
4. <span data-ttu-id="81588-127">Vælg **Kreditfaktura** i gruppen **Funktioner** under fanen **Faktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81588-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="81588-128">Angiv referencen til den oprindelige faktura, og vælg årsagen til rettelsen.</span><span class="sxs-lookup"><span data-stu-id="81588-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Definere referencen til en fritekstfaktura](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="81588-130">Kreditnota til kunden</span><span class="sxs-lookup"><span data-stu-id="81588-130">Customer credit note</span></span>

1. <span data-ttu-id="81588-131">Gå til **Debitor** \> **Ordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="81588-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="81588-132">Vælg og åbn den fakturerede salgsordre, der skal rettes.</span><span class="sxs-lookup"><span data-stu-id="81588-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="81588-133">Klik på **Kreditnota** i gruppen **Kreditnota** under fanen **Sælg** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81588-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="81588-134">Angiv årsagen til rettelsen.</span><span class="sxs-lookup"><span data-stu-id="81588-134">Enter the reason for the correction.</span></span> <span data-ttu-id="81588-135">Referencen til den oprindelige faktura oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="81588-135">The reference to the original invoice is automatically established.</span></span>

![Definere referencen til en salgsordre](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="81588-137">Projektkreditnota</span><span class="sxs-lookup"><span data-stu-id="81588-137">Project credit note</span></span>

1. <span data-ttu-id="81588-138">Gå til **Projektstyring og regnskab** \> **Projektfakturaer** \> **Projektfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="81588-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="81588-139">Vælg og åbn den projektfaktura, der skal rettes.</span><span class="sxs-lookup"><span data-stu-id="81588-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="81588-140">Vælg **Vælg til kreditfaktura** i gruppen **Funktioner** under fanen **Projektfaktura** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="81588-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="81588-141">Vælg **Kreditfaktura**.</span><span class="sxs-lookup"><span data-stu-id="81588-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="81588-142">Angiv årsagen til rettelsen.</span><span class="sxs-lookup"><span data-stu-id="81588-142">Enter the reason for the correction.</span></span> <span data-ttu-id="81588-143">Referencen til den oprindelige faktura oprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="81588-143">The reference to the original invoice is automatically established.</span></span>

![Definere referencen til en projektfaktura](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="81588-145">Udskrive kreditnotaer</span><span class="sxs-lookup"><span data-stu-id="81588-145">Printing credit notes</span></span>

<span data-ttu-id="81588-146">Når du udskriver fritekst-, debitor- og projektkreditnotaer, omfatter de referencen til den oprindelige faktura og årsagen til rettelsen.</span><span class="sxs-lookup"><span data-stu-id="81588-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Udskrevet kreditnota](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="81588-148">Kontroller, at dokumenternes formater, der kan udskrives, er konfigureret korrekt, efter at det antages, at referencer til oprindelige fakturaer vil blive udskrevet.</span><span class="sxs-lookup"><span data-stu-id="81588-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]