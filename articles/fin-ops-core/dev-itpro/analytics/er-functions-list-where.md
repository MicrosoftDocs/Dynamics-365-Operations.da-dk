---
title: ER-funktionen WHERE
description: Dette emne indeholder oplysninger om, hvordan funktionen WHERE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: bdf5c658fda83399c7bcffeaaf07005164c53f8a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745491"
---
# <a name="where-er-function"></a><span data-ttu-id="1c13a-103">ER-funktionen WHERE</span><span class="sxs-lookup"><span data-stu-id="1c13a-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c13a-104">Funktionen `WHERE` returnerer den angivne liste som en *Postliste*-værdi, efter at den er blevet filtreret i henhold til den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="1c13a-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c13a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1c13a-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="1c13a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1c13a-106">Arguments</span></span>

<span data-ttu-id="1c13a-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="1c13a-107">`list`: *Record list*</span></span>

<span data-ttu-id="1c13a-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="1c13a-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1c13a-109">`condition`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="1c13a-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="1c13a-110">Et gyldigt betinget udtryk, der bruges til at filtrere poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="1c13a-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c13a-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="1c13a-111">Return values</span></span>

<span data-ttu-id="1c13a-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="1c13a-112">*Record list*</span></span>

<span data-ttu-id="1c13a-113">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="1c13a-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c13a-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="1c13a-114">Usage notes</span></span>

<span data-ttu-id="1c13a-115">Denne funktion adskiller sig fra funktionen [FILTER](er-functions-list-filter.md), fordi den angivne betingelse anvendes på enhver elektronisk rapporteringsdatakilde (ER-datakilde) af typen *Postliste*, som er tilgængelige i hukommelsen.</span><span class="sxs-lookup"><span data-stu-id="1c13a-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="1c13a-116">Hvis de argumenter, der er konfigureret for denne funktion (`list` og `condition`), tillader, at denne anmodning oversættes til det direkte SQL-kald, bliver der udløst en advarsel på designtidspunktet.</span><span class="sxs-lookup"><span data-stu-id="1c13a-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="1c13a-117">Denne meddelelse informerer brugeren om, at ydeevnen kan blive forbedret, hvis funktionen [FILTER](er-functions-list-filter.md) bruges i stedet for `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="1c13a-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c13a-118">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1c13a-118">Example 1</span></span>

<span data-ttu-id="1c13a-119">Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil udtrykket `WHERE (Vendors, Vendors.VendGroup = "40")` alene returnere en liste over de leverandører, der tilhører leverandørgruppe 40.</span><span class="sxs-lookup"><span data-stu-id="1c13a-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c13a-120">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1c13a-120">Example 2</span></span>

<span data-ttu-id="1c13a-121">Hvis du angiver datakilden **DS** af typen *Beregnet felt*, og den indeholder udtrykket `SPLIT ("A|B|C", "|")`, returnerer udtrykket `WHERE( DS, DS.Value = "B")` en liste med blot én post, som indeholder teksten **"B"** i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="1c13a-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c13a-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1c13a-122">Additional resources</span></span>

[<span data-ttu-id="1c13a-123">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="1c13a-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]