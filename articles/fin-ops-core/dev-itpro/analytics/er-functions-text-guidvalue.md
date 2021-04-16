---
title: ER-funktionen GUIDVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen GUIDVALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746381"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="e1ebe-103">ER-funktionen GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="e1ebe-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1ebe-104">Funktionen `GUIDVALUE` konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ebe-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e1ebe-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="e1ebe-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e1ebe-106">Arguments</span></span>

<span data-ttu-id="e1ebe-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e1ebe-107">`input`: *String*</span></span>

<span data-ttu-id="e1ebe-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1ebe-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="e1ebe-109">Return values</span></span>

<span data-ttu-id="e1ebe-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e1ebe-110">*GUID*</span></span>

<span data-ttu-id="e1ebe-111">Den resulterende GUID-værdi (globalt entydigt identifikator).</span><span class="sxs-lookup"><span data-stu-id="e1ebe-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e1ebe-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="e1ebe-112">Usage notes</span></span>

<span data-ttu-id="e1ebe-113">For at omregne i modsat retning (dvs. konvertering til et angivet input af datatypen *GUID* til et dataelement af datatypen *Streng*) kan du bruge funktionen [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="e1ebe-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="e1ebe-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e1ebe-114">Example</span></span>

<span data-ttu-id="e1ebe-115">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="e1ebe-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="e1ebe-116">En **mitID**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="e1ebe-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="e1ebe-117">En **Brugere**-datakilde af typen *Tabelposter*, som refererer til tabellen BrugerInfo</span><span class="sxs-lookup"><span data-stu-id="e1ebe-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="e1ebe-118">Du kan derefter bruge et udtryk såsom `FILTER (Users, Users.objectId = myID)` til at filtrere tabellen BrugeInfo efter feltet **ObjektID** af datatypen *GUID*.</span><span class="sxs-lookup"><span data-stu-id="e1ebe-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1ebe-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e1ebe-119">Additional resources</span></span>

[<span data-ttu-id="e1ebe-120">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="e1ebe-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]