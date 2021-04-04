---
title: Funktionen LISTDISTINCT ER
description: Dette emne indeholder oplysninger om, hvordan funktionen til elektronisk LISTDISTINCT-rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563818"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="be508-103">Funktionen LISTDISTINCT ER</span><span class="sxs-lookup"><span data-stu-id="be508-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="be508-104">Funktionen `LISTDISTINCT` beregner det angivne udtryk som en vælger for hver post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="be508-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="be508-105">Den returnerer en ny værdi for *Postliste*, som indeholder en enkelt post for hver entydig vælgerværdi.</span><span class="sxs-lookup"><span data-stu-id="be508-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="be508-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="be508-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="be508-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="be508-107">Arguments</span></span>

<span data-ttu-id="be508-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="be508-108">`list`: *Record list*</span></span>

<span data-ttu-id="be508-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="be508-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="be508-110">`selector`: *Primitiv datatype*</span><span class="sxs-lookup"><span data-stu-id="be508-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="be508-111">Et gyldigt udtryk, der bruges til at beregne en vælgerværdi for hver post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="be508-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="be508-112">Følgende datatyper understøttes for denne parameter:</span><span class="sxs-lookup"><span data-stu-id="be508-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="be508-113">Boolesk</span><span class="sxs-lookup"><span data-stu-id="be508-113">Boolean</span></span>
- <span data-ttu-id="be508-114">Dato</span><span class="sxs-lookup"><span data-stu-id="be508-114">Date</span></span>
- <span data-ttu-id="be508-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="be508-115">DateTime</span></span>
- <span data-ttu-id="be508-116">Guid</span><span class="sxs-lookup"><span data-stu-id="be508-116">GUID</span></span>
- <span data-ttu-id="be508-117">Heltal</span><span class="sxs-lookup"><span data-stu-id="be508-117">Integer</span></span>
- <span data-ttu-id="be508-118">Int64</span><span class="sxs-lookup"><span data-stu-id="be508-118">Int64</span></span>
- <span data-ttu-id="be508-119">Kommatal</span><span class="sxs-lookup"><span data-stu-id="be508-119">Real</span></span>
- <span data-ttu-id="be508-120">Streng</span><span class="sxs-lookup"><span data-stu-id="be508-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="be508-121">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="be508-121">Return values</span></span>

<span data-ttu-id="be508-122">*Liste over poster*</span><span class="sxs-lookup"><span data-stu-id="be508-122">*Record list*</span></span>

<span data-ttu-id="be508-123">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="be508-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be508-124">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="be508-124">Usage notes</span></span>

<span data-ttu-id="be508-125">Strukturen på den liste, der oprettes, svarer til strukturen i den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="be508-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="be508-126">Den samme vælgerværdi kan beregnes for flere poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="be508-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="be508-127">I dette tilfælde svarer feltværdierne for den tilsvarende post på den oprettede liste til værdierne i den første post fra den angivne liste, som vælgerværdien beregnes for.</span><span class="sxs-lookup"><span data-stu-id="be508-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="be508-128">Udførelsen af denne funktion udføres for enhver datakilde for [Elektronisk rapportering (ER)](general-electronic-reporting.md) for den type af *Postliste*, der findes i hukommelsen.</span><span class="sxs-lookup"><span data-stu-id="be508-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="be508-129">Datakilden **GROUPBY** kan også bruges til at generere den liste over poster, som den vælger, der har bestemte værdier, beregnes for.</span><span class="sxs-lookup"><span data-stu-id="be508-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="be508-130">Set ud fra ydeevne og hukommelse i forbruget er det imidlertid bedre at bruge funktionen `LISTDISTINCT` end datakilden **GROUPBY**, da udførelsen af funktionen udføres i hukommelsen.</span><span class="sxs-lookup"><span data-stu-id="be508-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="be508-131">Eksempel</span><span class="sxs-lookup"><span data-stu-id="be508-131">Example</span></span>

<span data-ttu-id="be508-132">I følgende eksempel vises det, hvordan du kan få vist en liste over entydige kundekontonumre, som mindst én salgsfaktura eller projektfaktura er blevet udstedt til i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="be508-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="be508-133">Angiv datakilden **SalesInvoice** for den type af `Record list`, der refererer til programtabellen **CustInvoiceJour** og filtrerer salgsfakturaer for bestemte perioder.</span><span class="sxs-lookup"><span data-stu-id="be508-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="be508-134">Feltet `InvoiceAccount` i denne datakilde returnerer kontonummeret for en faktureret kunde.</span><span class="sxs-lookup"><span data-stu-id="be508-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="be508-135">Angiv datakilden **ProjectInvoice** for den type af `Record list`, der refererer til programtabellen **ProjInvoiceJour** og filtrerer projektfakturaer for bestemte perioder.</span><span class="sxs-lookup"><span data-stu-id="be508-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="be508-136">Feltet `InvoiceAccount` i denne datakilde returnerer kontonummeret for en faktureret kunde.</span><span class="sxs-lookup"><span data-stu-id="be508-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="be508-137">Konfigurer datakilden **AllInvoices** af typen `Calculated field`, der indeholder udtrykket `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="be508-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="be508-138">Denne datakilde returnerer den joinforbundne liste over salgsfakturaer og projektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="be508-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="be508-139">Konfigurer datakilden **InvoicedCustomer** af typen `Record list`, der indeholder udtrykket `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="be508-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="be508-140">Denne datakilde returnerer en ny liste, der indeholder en enkelt post for hver entydig kunde, der er faktureret i den angivne periode.</span><span class="sxs-lookup"><span data-stu-id="be508-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="be508-141">Feltet `InvoiceAccount` på denne liste indeholder et kundekontonummer.</span><span class="sxs-lookup"><span data-stu-id="be508-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be508-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="be508-142">Additional resources</span></span>

[<span data-ttu-id="be508-143">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="be508-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]