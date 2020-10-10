---
title: ER-funktionen GETENUMVALUEBYNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen GETENUMVALUEBYNAME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885221"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="b709a-103">ER-funktionen GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="b709a-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b709a-104">Funktionen `GETENUMVALUEBYNAME` søger efter en bestemt *Fasttekst*-værdi i den angivne fasttekstdatakilde ved hjælp af det fasttekstnavn, der er angivet som en *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="b709a-105">Hvis *Fasttekst*-værdien findes, returnerer funktionen den.</span><span class="sxs-lookup"><span data-stu-id="b709a-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="b709a-106">Ellers returnerer funktionen **nul** i fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b709a-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b709a-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="b709a-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b709a-108">Arguments</span></span>

<span data-ttu-id="b709a-109">`enumeration data source path`: *Fasttekst*</span><span class="sxs-lookup"><span data-stu-id="b709a-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="b709a-110">Den gyldige sti til en datakilde for en af følgende fastteksttyper:</span><span class="sxs-lookup"><span data-stu-id="b709a-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="b709a-111">Modelfasttekst til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="b709a-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="b709a-112">ER-formatfasttekst</span><span class="sxs-lookup"><span data-stu-id="b709a-112">ER format enumeration</span></span>
- <span data-ttu-id="b709a-113">Microsoft Dynamics 365 Finance-fasttekst</span><span class="sxs-lookup"><span data-stu-id="b709a-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="b709a-114">`enumeration value text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="b709a-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="b709a-115">En strengværdi, der repræsenterer navnet på en enkelt fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="b709a-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b709a-116">Return values</span></span>

<span data-ttu-id="b709a-117">*Enum* kan være nul</span><span class="sxs-lookup"><span data-stu-id="b709a-117">Nullable *Enum*</span></span>

<span data-ttu-id="b709a-118">Den returnerede fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b709a-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="b709a-119">Usage notes</span></span>

<span data-ttu-id="b709a-120">Der udløses ingen undtagelse, hvis der ikke findes en *Enum*-værdi ved hjælp af navnet på den fasttekstværdi, der er angivet som en *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b709a-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b709a-121">Example 1</span></span>

<span data-ttu-id="b709a-122">I følgende illustration introduceres fastteksten **ReportDirection** i en datamodel.</span><span class="sxs-lookup"><span data-stu-id="b709a-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="b709a-123">Bemærk, at der er defineret etiketter for fasttekstværdierne.</span><span class="sxs-lookup"><span data-stu-id="b709a-123">Notice that labels are defined for the enumeration values.</span></span>

![Tilgængelige værdier for en datamodelfasttekst](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="b709a-125">Følgende illustration viser disse detaljer:</span><span class="sxs-lookup"><span data-stu-id="b709a-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="b709a-126">Datakilden **$Retning** er konfigureret i en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="b709a-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="b709a-127">Denne datakilde konfigureres på basis af modelfastteksten **RapportRetning**.</span><span class="sxs-lookup"><span data-stu-id="b709a-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="b709a-128">Udtrykket `$IsArrivals` er designet til at bruge den modelfasttekstbaserede datakilde **$Retning** som parameter for denne funktion.</span><span class="sxs-lookup"><span data-stu-id="b709a-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="b709a-129">Værdien af denne sammenligning er **SAND**.</span><span class="sxs-lookup"><span data-stu-id="b709a-129">The value of this comparison expression is **TRUE**.</span></span>

![Eksempel på en datamodelfasttekst](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="b709a-131">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b709a-131">Example 2</span></span>

<span data-ttu-id="b709a-132">Funktionerne `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) giver dig mulighed for at hente værdier og etiketter på understøttet fasttekst som tekstværdier.</span><span class="sxs-lookup"><span data-stu-id="b709a-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="b709a-133">(Den understøttede fasttekst er programfasttekst, datamodelfasttekst og formatfasttekst).</span><span class="sxs-lookup"><span data-stu-id="b709a-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="b709a-134">I følgende illustration introduceres datakilden **TransType** i en modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="b709a-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="b709a-135">Denne datakilde refererer til programfastteksten **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="b709a-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Datakilde for en modeltilknytning, der refererer til en programfasttekst](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="b709a-137">Følgende illustration viser datakilden **TransTypeList**, der er konfigureret i en modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="b709a-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="b709a-138">Denne datakilde konfigureres på basis af programfastteksten **TransType**.</span><span class="sxs-lookup"><span data-stu-id="b709a-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="b709a-139">Funktionen `LISTOFFIELDS` bruges til at returnere alle fasttekstværdier som en liste over poster, der indeholder felter.</span><span class="sxs-lookup"><span data-stu-id="b709a-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="b709a-140">På denne måde vises detaljerne for alle fasttekstværdier.</span><span class="sxs-lookup"><span data-stu-id="b709a-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="b709a-141">Feltet **EnumValue** er konfigureret for datakilden **TransTypeList** ved hjælp af udtrykket `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="b709a-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="b709a-142">Dette felt returnerer en fasttekstværdi for hver post på denne liste.</span><span class="sxs-lookup"><span data-stu-id="b709a-142">This field returns an enumeration value for every record in this list.</span></span>

![Datakilde for en modeltilknytning, der returnerer alle fasttekstværdier for en valgt fasttekst som en liste over poster](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="b709a-144">Følgende illustration viser datakilden **VendTrans**, der er konfigureret i en modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="b709a-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="b709a-145">Denne datakilde returnerer kreditorposteringer fra programtabellen **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="b709a-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="b709a-146">Finanstypen for hver postering defineres af værdien i feltet **TransType**.</span><span class="sxs-lookup"><span data-stu-id="b709a-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="b709a-147">Feltet **TransTypeTitle** er konfigureret for datakilden **VendTrans** ved hjælp af udtrykket `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="b709a-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="b709a-148">I dette felt returneres etiketten for en fasttekstværdi for den aktuelle postering som tekst, hvis denne fasttekstværdi er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="b709a-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="b709a-149">Ellers returneres en tom strengværdi.</span><span class="sxs-lookup"><span data-stu-id="b709a-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="b709a-150">Feltet **TransTypeTitle** er knyttet til feltet **LedgerType** i en datamodel, der gør det muligt at bruge disse oplysninger i hvert ER-format, der bruger datamodellen som en datakilde.</span><span class="sxs-lookup"><span data-stu-id="b709a-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Datakilde for en modeltilknytning, der returnerer kreditorposteringer](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="b709a-152">I følgende illustration vises, hvordan du kan bruge [datakildefejlfindingen](er-debug-data-sources.md) til at teste den konfigurerede modeltilknytning.</span><span class="sxs-lookup"><span data-stu-id="b709a-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Bruge datakildefejlfindingen til at teste den konfigurerede modeltilknytning](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="b709a-154">Feltet **LedgerType** i en datamodel viser etiketter af posteringstyperne som forventet.</span><span class="sxs-lookup"><span data-stu-id="b709a-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="b709a-155">Hvis du planlægger at bruge denne fremgangsmåde til en stor mængde transaktionsdata, skal du overveje kørselsydeevnen.</span><span class="sxs-lookup"><span data-stu-id="b709a-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="b709a-156">Du kan finde flere oplysninger i [Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="b709a-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b709a-157">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b709a-157">Additional resources</span></span>

[<span data-ttu-id="b709a-158">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="b709a-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="b709a-159">Spore kørslen af ER-formater til fejlfinding af problemer med ydeevnen</span><span class="sxs-lookup"><span data-stu-id="b709a-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="b709a-160">ER-funktionen LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="b709a-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="b709a-161">ER-funktionen FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="b709a-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="b709a-162">ER-funktionen WHERE</span><span class="sxs-lookup"><span data-stu-id="b709a-162">WHERE ER function</span></span>](er-functions-list-where.md)
