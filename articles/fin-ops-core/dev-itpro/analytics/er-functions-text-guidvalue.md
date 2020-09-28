---
title: ER-funktionen GUIDVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen GUIDVALUE til elektronisk rapportering (ER) skal anvendes.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b4c65063cd22b5370ca6000a32c6fd1cc9ce6b6
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743825"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="7dca4-103">ER-funktionen GUIDVALUE</span><span class="sxs-lookup"><span data-stu-id="7dca4-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dca4-104">Funktionen `GUIDVALUE` konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*.</span><span class="sxs-lookup"><span data-stu-id="7dca4-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dca4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7dca4-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="7dca4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7dca4-106">Arguments</span></span>

<span data-ttu-id="7dca4-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="7dca4-107">`input`: *String*</span></span>

<span data-ttu-id="7dca4-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="7dca4-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7dca4-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7dca4-109">Return values</span></span>

<span data-ttu-id="7dca4-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7dca4-110">*GUID*</span></span>

<span data-ttu-id="7dca4-111">Den resulterende GUID-værdi (globalt entydigt identifikator).</span><span class="sxs-lookup"><span data-stu-id="7dca4-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7dca4-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="7dca4-112">Usage notes</span></span>

<span data-ttu-id="7dca4-113">For at omregne i modsat retning (dvs. konvertering til et angivet input af datatypen *GUID* til et dataelement af datatypen *Streng*) kan du bruge funktionen [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="7dca4-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="7dca4-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7dca4-114">Example</span></span>

<span data-ttu-id="7dca4-115">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="7dca4-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="7dca4-116">En **mitID**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="7dca4-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="7dca4-117">En **Brugere**-datakilde af typen *Tabelposter*, som refererer til tabellen BrugerInfo</span><span class="sxs-lookup"><span data-stu-id="7dca4-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="7dca4-118">Du kan derefter bruge et udtryk såsom `FILTER (Users, Users.objectId = myID)` til at filtrere tabellen BrugeInfo efter feltet **ObjektID** af datatypen *GUID*.</span><span class="sxs-lookup"><span data-stu-id="7dca4-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dca4-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7dca4-119">Additional resources</span></span>

[<span data-ttu-id="7dca4-120">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="7dca4-120">Text functions</span></span>](er-functions-category-text.md)
