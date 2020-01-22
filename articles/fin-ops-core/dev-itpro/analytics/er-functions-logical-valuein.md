---
title: ER-funktionen VALUEIN
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUEIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915964"
---
# <span data-ttu-id="1b780-103"><a name="VALUEIN">ER-funktionen VALUEIN</a></span><span class="sxs-lookup"><span data-stu-id="1b780-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b780-104">Funktionen `VALUEIN` afgør, hvorvidt det angivne input svarer til en værdi for et angivet element på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="1b780-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="1b780-105">Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="1b780-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="1b780-106">Ellers returneres en *Boolesk* værdi på **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="1b780-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b780-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1b780-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="1b780-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1b780-108">Arguments</span></span>

<span data-ttu-id="1b780-109">`input`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="1b780-109">`input`: *Field*</span></span>

<span data-ttu-id="1b780-110">Den gyldige sti til et element i en datakilde af typen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="1b780-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="1b780-111">Værdien af dette element bliver sammenlignet.</span><span class="sxs-lookup"><span data-stu-id="1b780-111">The value of this item will be matched.</span></span>

<span data-ttu-id="1b780-112">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="1b780-112">`list`: *Record list*</span></span>

<span data-ttu-id="1b780-113">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="1b780-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1b780-114">`list item expression`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="1b780-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="1b780-115">Et gyldigt betinget udtryk, der enten peger på eller indeholder et enkelt felt fra den angivne liste, som skal bruges til sammenligningen.</span><span class="sxs-lookup"><span data-stu-id="1b780-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b780-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="1b780-116">Return values</span></span>

<span data-ttu-id="1b780-117">*Boolesk*</span><span class="sxs-lookup"><span data-stu-id="1b780-117">*Boolean*</span></span>

<span data-ttu-id="1b780-118">Den resulterende *Booleske* værdi.</span><span class="sxs-lookup"><span data-stu-id="1b780-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1b780-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="1b780-119">Usage notes</span></span>

<span data-ttu-id="1b780-120">Generelt set oversættes funktionen `VALUEIN` til et sæt **ELLER**-betingelser.</span><span class="sxs-lookup"><span data-stu-id="1b780-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="1b780-121">I nogle tilfælde kan den oversættes til en SQL-database-sætning ved hjælp af operatøren `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="1b780-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="1b780-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1b780-122">Example 1</span></span>

<span data-ttu-id="1b780-123">Du kan i din modeltilknytning definere datakilden **Liste** af typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="1b780-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="1b780-124">Denne datakilde indeholder udtrykket `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="1b780-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="1b780-125">Når en datakilde kaldes, og hvis den er konfigureret som udtrykket `VALUEIN ("B", List, List.Value)`, returneres **SANDT**.</span><span class="sxs-lookup"><span data-stu-id="1b780-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="1b780-126">I dette tilfælde oversættes funktionen `VALUEIN` til følgende sæt betingelser: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, når `("B" = "b")` er **SAND**.</span><span class="sxs-lookup"><span data-stu-id="1b780-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="1b780-127">Når en datakilde kaldes, og hvis den er konfigureret som udtrykket `VALUEIN ("B", List, LEFT(List.Value, 0))`, returneres **FALSK**.</span><span class="sxs-lookup"><span data-stu-id="1b780-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="1b780-128">I dette tilfælde oversættes funktionen `VALUEIN` til følgende betingelse: `("B" = "")`, som ikke er lig med **SAND**.</span><span class="sxs-lookup"><span data-stu-id="1b780-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="1b780-129">Den øvre grænse for antallet af tegn i teksten i en sådan betingelse er 32.768 tegn.</span><span class="sxs-lookup"><span data-stu-id="1b780-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="1b780-130">Du skal derfor ikke oprette datakilder, der kan overskride denne grænse på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="1b780-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="1b780-131">Hvis grænsen overskrides, stopper programmet med at køre, og der udløses en undtagelse.</span><span class="sxs-lookup"><span data-stu-id="1b780-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="1b780-132">For eksempel kan denne situation opstå, hvis datakilden er konfigureret som `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, og listerne **Liste1** samt **Liste2** indeholder en stor mængde poster.</span><span class="sxs-lookup"><span data-stu-id="1b780-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="1b780-133">I nogle tilfælde kan funktionen `VALUEIN` oversættes til en databasesætning ved hjælp af operatøren `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="1b780-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="1b780-134">Dette problem opstår, når funktionen [FILTER](er-functions-list-filter.md) anvendes, og følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="1b780-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="1b780-135">Indstillingen **Spørg efter forespørgsel** er deaktiveret for datakilden til funktionen `VALUEIN`, der refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="1b780-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="1b780-136">Der bliver ikke anvendt yderligere betingelser på denne datakilde på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="1b780-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="1b780-137">Ingen indlejrede udtryk konfigureres for datakilden til den `VALUEIN`-funktion, der refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="1b780-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="1b780-138">Et listeelement i `VALUEIN`-funktionen refererer til et felt i den angivne datakilde og ikke til et udtryk eller en metode i den angivne datakilde.</span><span class="sxs-lookup"><span data-stu-id="1b780-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="1b780-139">Overvej at bruge denne indstilling i stedet for funktionen [WHERE](er-functions-list-where.md), som er beskrevet tidligere i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="1b780-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="1b780-140">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1b780-140">Example 2</span></span>

<span data-ttu-id="1b780-141">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="1b780-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="1b780-142">Datakilden **In** for typen *Tabelpost*.</span><span class="sxs-lookup"><span data-stu-id="1b780-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="1b780-143">Denne datakilde refererer til Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="1b780-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="1b780-144">Datakilden **Port** for typen *Tabelpost*.</span><span class="sxs-lookup"><span data-stu-id="1b780-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="1b780-145">Denne datakilde refererer til IntrastatPort-tabellen.</span><span class="sxs-lookup"><span data-stu-id="1b780-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="1b780-146">Når en datakilde bliver kaldt, der konfigureret som udtrykket `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, genereres følgende SQL-sætning for at returnere filtrerede poster fra tabellen Intrastat.</span><span class="sxs-lookup"><span data-stu-id="1b780-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="1b780-147">For felterne **dataAreaId** genereres den endelige SQL-sætning ved hjælp af `IN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="1b780-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="1b780-148">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="1b780-148">Example 3</span></span>

<span data-ttu-id="1b780-149">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="1b780-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="1b780-150">Datakilden **Le** for typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="1b780-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="1b780-151">Denne datakilde indeholder udtrykket `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="1b780-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="1b780-152">Datakilden **In** for typen *Tabelpost*.</span><span class="sxs-lookup"><span data-stu-id="1b780-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="1b780-153">Denne datakilde refererer til Intrastat-tabellen, og indstillingen **På tværs af virksomheden** er aktiveret for den.</span><span class="sxs-lookup"><span data-stu-id="1b780-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="1b780-154">Når en datakilde, der er blevet konfigureret som udtrykket `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, kaldes, indeholder den endelige SQL-sætning følgende betingelse.</span><span class="sxs-lookup"><span data-stu-id="1b780-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="1b780-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1b780-155">Additional resources</span></span>

[<span data-ttu-id="1b780-156">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="1b780-156">Logical functions</span></span>](er-functions-category-logical.md)
