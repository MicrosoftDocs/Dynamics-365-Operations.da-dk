---
title: ER-funktionen ALLITEMSQUERY
description: Dette emne indeholder oplysninger om, hvordan funktionen ALLITEMSQUERY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745363"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="d9ee1-103">ER-funktionen ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="d9ee1-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9ee1-104">Funktionen `ALLITEMSQUERY` kører som en sammenkædet SQL-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="d9ee1-105">Den returnerer en ny fladtrykt *Postliste*-værdi, som består af en liste over poster, som repræsenterer alle elementer, der svarer til den angivne sti.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ee1-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d9ee1-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="d9ee1-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d9ee1-107">Arguments</span></span>

<span data-ttu-id="d9ee1-108">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="d9ee1-108">`path`: *Record list*</span></span>

<span data-ttu-id="d9ee1-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="d9ee1-110">Den skal indeholde mindst én relation.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9ee1-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="d9ee1-111">Return values</span></span>

<span data-ttu-id="d9ee1-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="d9ee1-112">*Record list*</span></span>

<span data-ttu-id="d9ee1-113">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d9ee1-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="d9ee1-114">Usage notes</span></span>

<span data-ttu-id="d9ee1-115">Den angivne sti skal defineres som en gyldig datakildesti for et datakildeelement af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="d9ee1-116">Den skal endvidere indeholde mindst én relation.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-116">It must also contain at least one relation.</span></span> <span data-ttu-id="d9ee1-117">Dataelementer som stiens *Streng* og *Dato* bør udløse en fejl i designfasen i udtryksgenerator til den elektroniske rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="d9ee1-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="d9ee1-118">Når denne funktion anvendes på datakilder af datatypen *Postliste*, der refererer til et programobjekt, der kan kaldes direkte ved hjælp af SQL (f.eks. en tabel, en enhed eller en forespørgsel), køres den som en sammenkædet SQL-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="d9ee1-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="d9ee1-119">Ellers kører den i hukommelsen som funktionen [ALLITEM](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="d9ee1-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="d9ee1-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d9ee1-120">Example</span></span>

<span data-ttu-id="d9ee1-121">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="d9ee1-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="d9ee1-122">En **CustInv** datakilde af typen *Tabelposter*, som refererer til tabellen CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="d9ee1-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="d9ee1-123">En **FilteredInv**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="d9ee1-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="d9ee1-124">En **JourLines** af typen *Beregnet felt*, der indeholder udtrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="d9ee1-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="d9ee1-125">Når du kører modeltilknytningen for at kalde datakilden **JourLines**, udføres følgende SQL-sætning:</span><span class="sxs-lookup"><span data-stu-id="d9ee1-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="d9ee1-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d9ee1-126">Additional resources</span></span>

[<span data-ttu-id="d9ee1-127">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="d9ee1-127">List functions</span></span>](er-functions-category-list.md)
