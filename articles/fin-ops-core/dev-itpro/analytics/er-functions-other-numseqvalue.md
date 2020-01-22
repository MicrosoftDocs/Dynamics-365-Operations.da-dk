---
title: ER-funktionen NUMSEQVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMSEQVALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915826"
---
# <span data-ttu-id="72c91-103"><a name="NUMSEQVALUE">ER-funktionen NUMSEQVALUE</a></span><span class="sxs-lookup"><span data-stu-id="72c91-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72c91-104">Funktionen `NUMSEQVALUE` returnerer en *Streng*-værdi, som repræsenterer den nye genererede værdi for en nummerserie, der er baseret på den angivne nummerserie, omfang og område-ID.</span><span class="sxs-lookup"><span data-stu-id="72c91-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="72c91-105">Område-ID'et er lig med den firmakode, der leveres af den kontekst, som det elektroniske rapporteringsformat (ER-format) køres under.</span><span class="sxs-lookup"><span data-stu-id="72c91-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="72c91-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="72c91-106">Syntax 1</span></span>

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="72c91-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="72c91-107">Syntax 2</span></span>

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="72c91-108">Syntaks 3</span><span class="sxs-lookup"><span data-stu-id="72c91-108">Syntax 3</span></span>

```
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="72c91-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="72c91-109">Arguments</span></span>

<span data-ttu-id="72c91-110">`number sequence code`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="72c91-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="72c91-111">En tekstværdi, der repræsenterer koden for den nummerserie, som en ny værdi kræves i.</span><span class="sxs-lookup"><span data-stu-id="72c91-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="72c91-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="72c91-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="72c91-113">En *Int64*-værdi, der repræsenterer post-ID'et for en post i tabellen NumberSequenceTable, som indeholder definitionen af den nummerserie, som en ny værdi kræves i.</span><span class="sxs-lookup"><span data-stu-id="72c91-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="72c91-114">`scope type`: *Fasttekstværdi*</span><span class="sxs-lookup"><span data-stu-id="72c91-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="72c91-115">En fasttekstværdi for fastteksten **ERExpressionNumberSequenceScopeType**, der definerer omfanget af den nummerserie, som en ny værdi kræves i.</span><span class="sxs-lookup"><span data-stu-id="72c91-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="72c91-116">De tilgængelige områdetyper er **Delte**, **Juridiske enheder** og **Firma**.</span><span class="sxs-lookup"><span data-stu-id="72c91-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="72c91-117">`scope ID`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="72c91-117">`scope ID`: *String*</span></span>

<span data-ttu-id="72c91-118">En *Streng*-værdi, der identificerer området baseret på den angivne områdetype.</span><span class="sxs-lookup"><span data-stu-id="72c91-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="72c91-119">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="72c91-119">Return values</span></span>

<span data-ttu-id="72c91-120">*Streng*</span><span class="sxs-lookup"><span data-stu-id="72c91-120">*String*</span></span>

<span data-ttu-id="72c91-121">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="72c91-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="72c91-122">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="72c91-122">Usage notes</span></span>

<span data-ttu-id="72c91-123">For områdetypen **Delt** skal du angive en tom streng som område-ID'et.</span><span class="sxs-lookup"><span data-stu-id="72c91-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="72c91-124">For områdetyperne **Firma** og **Juridisk enhed** skal du angive firmakoden som område-ID.</span><span class="sxs-lookup"><span data-stu-id="72c91-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="72c91-125">Hvis du angiver en tom streng som område-ID for disse områdetyper, bruges den aktuelle firmakode.</span><span class="sxs-lookup"><span data-stu-id="72c91-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="72c91-126">Når der bruges syntaks 1, anmodes nummerserien om områdetypen **Firma**, og firmakoden leveres af den kontekst, som ER-formatet køres under.</span><span class="sxs-lookup"><span data-stu-id="72c91-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="72c91-127">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="72c91-127">Example 1</span></span>

<span data-ttu-id="72c91-128">I dit ER-format definerer du datakilden **AskNumSeq** af typen *Brugerinputparameter*.</span><span class="sxs-lookup"><span data-stu-id="72c91-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="72c91-129">Denne datakilde refererer til den udvidede datatype (EDT) **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="72c91-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="72c91-130">Derefter skal du definere datakilden **NumSeq** af typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="72c91-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="72c91-131">Denne datakilde indeholder udtrykket `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="72c91-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="72c91-132">Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi for den nummerserie, der blev angivet ved kørslen, ved at indtaste dens kode i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="72c91-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="72c91-133">Der anmodes om nummerserien for områdetypen **Firma**.</span><span class="sxs-lookup"><span data-stu-id="72c91-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="72c91-134">Firmakoden leveres af den kontekst, som ER-formatet køres under.</span><span class="sxs-lookup"><span data-stu-id="72c91-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="72c91-135">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="72c91-135">Example 2</span></span>

<span data-ttu-id="72c91-136">De følgende datakilder er defineret i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="72c91-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="72c91-137">Datakilden **LedgerParms** for typen *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="72c91-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="72c91-138">Denne datakilde refererer til tabellen LedgerParameters.</span><span class="sxs-lookup"><span data-stu-id="72c91-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="72c91-139">Datakilden **NumSeq** for typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="72c91-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="72c91-140">Denne datakilde indeholder udtrykket `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="72c91-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="72c91-141">Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den nummerserie, der er konfigureret i Finans-parametrene for det firma, der leverer den kontekst, som ER-formatet køres under.</span><span class="sxs-lookup"><span data-stu-id="72c91-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="72c91-142">Denne nummerserie identificerer entydigt kladder og fungerer som et batchnummer, der knytter posteringerne sammen.</span><span class="sxs-lookup"><span data-stu-id="72c91-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="72c91-143">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="72c91-143">Example 3</span></span>

<span data-ttu-id="72c91-144">De følgende datakilder er defineret i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="72c91-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="72c91-145">Datakilden **enumScope** for Microsoft Dynamics 365 Finance *fasttekst*-typen.</span><span class="sxs-lookup"><span data-stu-id="72c91-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="72c91-146">Denne datakilde refererer til fastteksten **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="72c91-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="72c91-147">Datakilden **NumSeq** for typen *Beregnet felt*.</span><span class="sxs-lookup"><span data-stu-id="72c91-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="72c91-148">Denne datakilde indeholder udtrykket `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="72c91-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="72c91-149">Når datakilden **NumSeq** kaldes, returneres den nye genererede værdi af den **Gene\_1**-nummerserie, der er konfigureret for det firma, der leverer den kontekst, som ER-formatet køres under.</span><span class="sxs-lookup"><span data-stu-id="72c91-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72c91-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="72c91-150">Additional resources</span></span>

[<span data-ttu-id="72c91-151">Andre (forretningsdomænespecifikke) funktioner</span><span class="sxs-lookup"><span data-stu-id="72c91-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
