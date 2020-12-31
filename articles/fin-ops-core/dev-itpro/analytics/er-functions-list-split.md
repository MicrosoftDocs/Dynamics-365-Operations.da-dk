---
title: ER-funktionen SPLIT
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLIT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686386"
---
# <a name="split-er-function"></a><span data-ttu-id="89eca-103">ER-funktionen SPLIT</span><span class="sxs-lookup"><span data-stu-id="89eca-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89eca-104">Funktionen `SPLIT` opdeler den angivne inputstreng i understrenge og returnerer resultatet som en ny *Postliste*-værdi.</span><span class="sxs-lookup"><span data-stu-id="89eca-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="89eca-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="89eca-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="89eca-106">Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge, som hver især har den angivne længde.</span><span class="sxs-lookup"><span data-stu-id="89eca-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="89eca-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="89eca-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="89eca-108">Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge baseret på den angivne afgrænser.</span><span class="sxs-lookup"><span data-stu-id="89eca-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="89eca-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="89eca-109">Arguments</span></span>

<span data-ttu-id="89eca-110">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="89eca-110">`input`: *String*</span></span>

<span data-ttu-id="89eca-111">Den tekst du vil dele op.</span><span class="sxs-lookup"><span data-stu-id="89eca-111">The text to split.</span></span>

<span data-ttu-id="89eca-112">`length`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="89eca-112">`length`: *Integer*</span></span>

<span data-ttu-id="89eca-113">Den maksimale længde på en enkelt understreng.</span><span class="sxs-lookup"><span data-stu-id="89eca-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="89eca-114">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="89eca-114">`delimiter`: *String*</span></span>

<span data-ttu-id="89eca-115">En afgrænser, der bruges til at adskille understrenge.</span><span class="sxs-lookup"><span data-stu-id="89eca-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="89eca-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="89eca-116">Return values</span></span>

<span data-ttu-id="89eca-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="89eca-117">*Record list*</span></span>

<span data-ttu-id="89eca-118">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="89eca-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89eca-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="89eca-119">Usage notes</span></span>

<span data-ttu-id="89eca-120">Poststrukturen for den returnerede liste består af feltet **Værdi** af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="89eca-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="89eca-121">Alle poster på listen, der returneres, indeholder genererede understrenge i dette felt.</span><span class="sxs-lookup"><span data-stu-id="89eca-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="89eca-122">Hvis argumentet `delimiter` er tomt, vil den nye liste, der returneres, bestå af én post, der har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="89eca-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="89eca-123">Dette felt indeholder inputteksten.</span><span class="sxs-lookup"><span data-stu-id="89eca-123">This field contains the input text.</span></span>

<span data-ttu-id="89eca-124">Hvis `input`-argumentet er tomt, returneres en ny tom liste.</span><span class="sxs-lookup"><span data-stu-id="89eca-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="89eca-125">Hvis hverken `input`- eller `delimiter`-argumentet er angivet (nul), opstår der en programundtagelse.</span><span class="sxs-lookup"><span data-stu-id="89eca-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="89eca-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="89eca-126">Example 1</span></span>

<span data-ttu-id="89eca-127">`SPLIT ("abcd", 3)` returnerer en ny liste, der består af to poster, som har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="89eca-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="89eca-128">Feltet **Værdi** i den første post indeholder teksten **"abc"**, og feltet **Værdi** i den anden post indeholder teksten **"d"**.</span><span class="sxs-lookup"><span data-stu-id="89eca-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="89eca-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="89eca-129">Example 2</span></span>

<span data-ttu-id="89eca-130">`SPLIT ("XAb aBy", "aB")` returnerer en ny liste, der består af tre poster, som har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="89eca-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="89eca-131">Feltet **Værdi** i den første post indeholder teksten **"X"**, feltet **Værdi** i den anden post indeholder teksten **"&nbsp;"**, og feltet **Værdi** i den tredje post indeholder teksten **"y"**.</span><span class="sxs-lookup"><span data-stu-id="89eca-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="89eca-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="89eca-132">Additional resources</span></span>

[<span data-ttu-id="89eca-133">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="89eca-133">List functions</span></span>](er-functions-category-list.md)
