---
title: ER-funktionen IF
description: Dette emne indeholder oplysninger om, hvordan funktionen IF til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565898"
---
# <a name="if-er-function"></a><span data-ttu-id="dc0fd-103">ER-funktionen IF</span><span class="sxs-lookup"><span data-stu-id="dc0fd-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0fd-104">Funktionen `IF` returnerer den først angivne værdi, hvis den angivne betingelse er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="dc0fd-105">Ellers returneres den anden angivne værdi.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="dc0fd-106">Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0fd-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="dc0fd-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="dc0fd-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="dc0fd-108">Arguments</span></span>

<span data-ttu-id="dc0fd-109">`condition`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="dc0fd-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="dc0fd-110">Et gyldigt betinget udtryk, der skal afprøves.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="dc0fd-111">`first value`: *Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="dc0fd-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="dc0fd-112">Det resultat, der returneres, hvis betingelsen er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="dc0fd-113">`second value`: *Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="dc0fd-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="dc0fd-114">Det resultat, der returneres, hvis betingelsen ikke er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc0fd-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="dc0fd-115">Return values</span></span>

<span data-ttu-id="dc0fd-116">*Alle understøttede datatyper*</span><span class="sxs-lookup"><span data-stu-id="dc0fd-116">*Any of the supported data types*</span></span>

<span data-ttu-id="dc0fd-117">Den resulterende værdi af en af de understøttede datatyper.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dc0fd-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="dc0fd-118">Usage notes</span></span>

<span data-ttu-id="dc0fd-119">Argumenterne `first value` og `second value` skal angives ved hjælp af den samme datatype.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="dc0fd-120">Der udløses en undtagelse på designtidspunktet, hvis datatyperne for de konfigurerede værdier ikke matcher.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="dc0fd-121">Hvis den første og den anden resultatværdi er værdier af datatypen *Container (post)* eller *Postliste*, indeholder resultatet kun de felter, der findes i begge værdier.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="dc0fd-122">Eksempel</span><span class="sxs-lookup"><span data-stu-id="dc0fd-122">Example</span></span>

<span data-ttu-id="dc0fd-123">`IF (1=2, "condition is met", "condition is not met")` returnerer strengen **betingelsen er ikke opfyldt**.</span><span class="sxs-lookup"><span data-stu-id="dc0fd-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc0fd-124">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dc0fd-124">Additional resources</span></span>

[<span data-ttu-id="dc0fd-125">Logiske funktioner</span><span class="sxs-lookup"><span data-stu-id="dc0fd-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]