---
title: ER-funktionen SPLIT
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLIT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c99ee5e8129ed45253893dc83acdef99b4ce2c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745587"
---
# <a name="split-er-function"></a><span data-ttu-id="75aab-103">ER-funktionen SPLIT</span><span class="sxs-lookup"><span data-stu-id="75aab-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75aab-104">Funktionen `SPLIT` opdeler den angivne inputstreng i understrenge og returnerer resultatet som en ny *Postliste*-værdi.</span><span class="sxs-lookup"><span data-stu-id="75aab-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="75aab-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="75aab-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="75aab-106">Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge, som hver især har den angivne længde.</span><span class="sxs-lookup"><span data-stu-id="75aab-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="75aab-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="75aab-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="75aab-108">Denne syntaks anvendes til at opdele den angivne inputstreng i understrenge baseret på den angivne afgrænser.</span><span class="sxs-lookup"><span data-stu-id="75aab-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="75aab-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="75aab-109">Arguments</span></span>

<span data-ttu-id="75aab-110">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="75aab-110">`input`: *String*</span></span>

<span data-ttu-id="75aab-111">Den tekst du vil dele op.</span><span class="sxs-lookup"><span data-stu-id="75aab-111">The text to split.</span></span>

<span data-ttu-id="75aab-112">`length`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="75aab-112">`length`: *Integer*</span></span>

<span data-ttu-id="75aab-113">Den maksimale længde på en enkelt understreng.</span><span class="sxs-lookup"><span data-stu-id="75aab-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="75aab-114">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="75aab-114">`delimiter`: *String*</span></span>

<span data-ttu-id="75aab-115">En afgrænser, der bruges til at adskille understrenge.</span><span class="sxs-lookup"><span data-stu-id="75aab-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="75aab-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="75aab-116">Return values</span></span>

<span data-ttu-id="75aab-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="75aab-117">*Record list*</span></span>

<span data-ttu-id="75aab-118">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="75aab-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="75aab-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="75aab-119">Usage notes</span></span>

<span data-ttu-id="75aab-120">Poststrukturen for den returnerede liste består af feltet **Værdi** af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="75aab-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="75aab-121">Alle poster på listen, der returneres, indeholder genererede understrenge i dette felt.</span><span class="sxs-lookup"><span data-stu-id="75aab-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="75aab-122">Hvis argumentet `delimiter` er tomt, vil den nye liste, der returneres, bestå af én post, der har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="75aab-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="75aab-123">Dette felt indeholder inputteksten.</span><span class="sxs-lookup"><span data-stu-id="75aab-123">This field contains the input text.</span></span>

<span data-ttu-id="75aab-124">Hvis `input`-argumentet er tomt, returneres en ny tom liste.</span><span class="sxs-lookup"><span data-stu-id="75aab-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="75aab-125">Hvis hverken `input`- eller `delimiter`-argumentet er angivet (nul), opstår der en programundtagelse.</span><span class="sxs-lookup"><span data-stu-id="75aab-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="75aab-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="75aab-126">Example 1</span></span>

<span data-ttu-id="75aab-127">`SPLIT ("abcd", 3)` returnerer en ny liste, der består af to poster, som har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="75aab-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="75aab-128">Feltet **Værdi** i den første post indeholder teksten **"abc"**, og feltet **Værdi** i den anden post indeholder teksten **"d"**.</span><span class="sxs-lookup"><span data-stu-id="75aab-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="75aab-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="75aab-129">Example 2</span></span>

<span data-ttu-id="75aab-130">`SPLIT ("XAb aBy", "aB")` returnerer en ny liste, der består af tre poster, som har et **Værdi**-felt af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="75aab-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="75aab-131">Feltet **Værdi** i den første post indeholder teksten **"X"**, feltet **Værdi** i den anden post indeholder teksten **"&nbsp;"**, og feltet **Værdi** i den tredje post indeholder teksten **"y"**.</span><span class="sxs-lookup"><span data-stu-id="75aab-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="75aab-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="75aab-132">Additional resources</span></span>

[<span data-ttu-id="75aab-133">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="75aab-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]