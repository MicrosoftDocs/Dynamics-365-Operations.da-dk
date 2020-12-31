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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed21252fbbe3d4adad106625062e10e3de712bb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687738"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="5233d-103">ER-funktionen ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="5233d-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5233d-104">Funktionen `ALLITEMSQUERY` kører som en sammenkædet SQL-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="5233d-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="5233d-105">Den returnerer en ny fladtrykt *Postliste*-værdi, som består af en liste over poster, som repræsenterer alle elementer, der svarer til den angivne sti.</span><span class="sxs-lookup"><span data-stu-id="5233d-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="5233d-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5233d-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="5233d-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5233d-107">Arguments</span></span>

<span data-ttu-id="5233d-108">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="5233d-108">`path`: *Record list*</span></span>

<span data-ttu-id="5233d-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="5233d-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="5233d-110">Den skal indeholde mindst én relation.</span><span class="sxs-lookup"><span data-stu-id="5233d-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="5233d-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5233d-111">Return values</span></span>

<span data-ttu-id="5233d-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="5233d-112">*Record list*</span></span>

<span data-ttu-id="5233d-113">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="5233d-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5233d-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="5233d-114">Usage notes</span></span>

<span data-ttu-id="5233d-115">Den angivne sti skal defineres som en gyldig datakildesti for et datakildeelement af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="5233d-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="5233d-116">Den skal endvidere indeholde mindst én relation.</span><span class="sxs-lookup"><span data-stu-id="5233d-116">It must also contain at least one relation.</span></span> <span data-ttu-id="5233d-117">Dataelementer som stiens *Streng* og *Dato* bør udløse en fejl i designfasen i udtryksgenerator til den elektroniske rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="5233d-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="5233d-118">Når denne funktion anvendes på datakilder af datatypen *Postliste*, der refererer til et programobjekt, der kan kaldes direkte ved hjælp af SQL (f.eks. en tabel, en enhed eller en forespørgsel), køres den som en sammenkædet SQL-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="5233d-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="5233d-119">Ellers kører den i hukommelsen som funktionen [ALLITEM](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="5233d-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="5233d-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5233d-120">Example</span></span>

<span data-ttu-id="5233d-121">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="5233d-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="5233d-122">En **CustInv** datakilde af typen *Tabelposter*, som refererer til tabellen CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="5233d-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="5233d-123">En **FilteredInv**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="5233d-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="5233d-124">En **JourLines** af typen *Beregnet felt*, der indeholder udtrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="5233d-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="5233d-125">Når du kører modeltilknytningen for at kalde datakilden **JourLines**, udføres følgende SQL-sætning:</span><span class="sxs-lookup"><span data-stu-id="5233d-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="5233d-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5233d-126">Additional resources</span></span>

[<span data-ttu-id="5233d-127">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="5233d-127">List functions</span></span>](er-functions-category-list.md)
