---
title: ER-funktionen VALUEINLARGE
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUEINLARGE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1e35c695d697e0d0f42baeaf568548273f9d205b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565802"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="4ec5d-103">ER-funktionen VALUEINLARGE</span><span class="sxs-lookup"><span data-stu-id="4ec5d-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ec5d-104">Funktionen `VALUEINLARGE` afgør, om det angivne input af typen *Int64* eller *Heltal* svarer til en værdi for et angivet element på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="4ec5d-105">Funktionen returnerer en *Boolesk* værdi som værende **SAND**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="4ec5d-106">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="4ec5d-107">Hvis du vil forstå forskellen med `VALUEIN`-funktionen, skal du se afsnittet [Bemærkninger til brug](#usage_note) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec5d-108">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4ec5d-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="4ec5d-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4ec5d-109">Arguments</span></span>

<span data-ttu-id="4ec5d-110">`input`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="4ec5d-110">`input`: *Field*</span></span>

<span data-ttu-id="4ec5d-111">Den gyldige sti til et datakildeelement af typen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="4ec5d-112">Værdien af dette element bliver sammenlignet.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-112">The value of this item will be matched.</span></span>

<span data-ttu-id="4ec5d-113">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4ec5d-113">`list`: *Record list*</span></span>

<span data-ttu-id="4ec5d-114">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="4ec5d-115">`list item expression`: *Betingelse*</span><span class="sxs-lookup"><span data-stu-id="4ec5d-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="4ec5d-116">Et gyldigt betinget udtryk, der enten peger på eller indeholder et enkelt felt fra den angivne liste, som skal bruges til sammenligningen.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ec5d-117">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="4ec5d-117">Return values</span></span>

<span data-ttu-id="4ec5d-118">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="4ec5d-118">*Boolean*</span></span>

<span data-ttu-id="4ec5d-119">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="4ec5d-120"><a name="usage_note">Bemærkninger til brug</a></span><span class="sxs-lookup"><span data-stu-id="4ec5d-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="4ec5d-121">Når det angivne input repræsenterer en *Int64*- eller *Heltal*-type for et datakildeelement, vil det kald, der kan oversættes til en direkte SQL-sætning, blive konverteret til en midlertidig SQL-tabel, og matchning udføres i databasen ved at udføre en enkelt `EXISTS JOIN`-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="4ec5d-122">Ellers virker denne funktion som funktionen [`VALUEIN`](er-functions-logical-valuein.md).</span><span class="sxs-lookup"><span data-stu-id="4ec5d-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="4ec5d-123">Når det angivne input repræsenterer et datakildeelement, der er designet som et andet element end *Int64*- og *Heltal*-typen, opstår der en fejl, på designtidspunktet om, at `VALUEINLARGE`-funktionen ikke kan anvendes til det konfigurerede ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="4ec5d-124">Når `VALUEINLARGE`-funktionsudtrykket udføres, og der bruges mere end én midlertidig tabel i området for denne udførelse, opstår der en kørselsfejl.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="4ec5d-125">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4ec5d-125">Example</span></span>

<span data-ttu-id="4ec5d-126">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="4ec5d-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="4ec5d-127">Datakilden **In** for typen *Tabelpost*.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="4ec5d-128">Denne datakilde refererer til **Intrastat**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="4ec5d-129">Indstillingen **På tværs af firma** er angivet til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="4ec5d-130">Datakilden **InMemory** af typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="4ec5d-131">Denne datakilde indeholder udtrykket `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="4ec5d-132">Datakilden **InFiltered** af typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="4ec5d-133">Denne datakilde indeholder udtrykket `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="4ec5d-134">Når datakilden **InFiltered** kaldes i konteksten af firmaet **DEMF**, oprettes der en ny midlertidig tabel i programdatabasen, den indsamlede liste over postidentifikationskoder i hukommelsen indsættes i denne tabel, og følgende SQL-sætning genereres for at returnere filtrerede poster i **Intrastat**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4ec5d-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="4ec5d-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4ec5d-135">Additional resources</span></span>

[<span data-ttu-id="4ec5d-136">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="4ec5d-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="4ec5d-137">VALUEIN-funktioner</span><span class="sxs-lookup"><span data-stu-id="4ec5d-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]