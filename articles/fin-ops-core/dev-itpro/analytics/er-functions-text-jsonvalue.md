---
title: ER-funktionen JSONVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen JSONVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 75f20632074cb4dead98991fd6522ab9b20b9965
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041207"
---
# <span data-ttu-id="db8c3-103"><a name="JSONVALUE">ER-funktionen JSONVALUE</a></span><span class="sxs-lookup"><span data-stu-id="db8c3-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db8c3-104">Funktionen `JSONVALUE` opdeler data i JavaScript Object Notation (JSON)-format, som tilgås via den angivne sti og udtrækker en skalarværdi, der indeholder det angivne ID.</span><span class="sxs-lookup"><span data-stu-id="db8c3-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="db8c3-105">Derefter returneres den udpakkede skalarværdi som en *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="db8c3-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8c3-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="db8c3-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="db8c3-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="db8c3-107">Arguments</span></span>

<span data-ttu-id="db8c3-108">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="db8c3-108">`input`: *String*</span></span>

<span data-ttu-id="db8c3-109">Den gyldige sti til en datakilde af typen *Streng*, som indeholder JSON-data.</span><span class="sxs-lookup"><span data-stu-id="db8c3-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="db8c3-110">`path`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="db8c3-110">`path`: *String*</span></span>

<span data-ttu-id="db8c3-111">Identifikatoren for en skalarværdi af JSON-data.</span><span class="sxs-lookup"><span data-stu-id="db8c3-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="db8c3-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="db8c3-112">Return values</span></span>

<span data-ttu-id="db8c3-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="db8c3-113">*String*</span></span>

<span data-ttu-id="db8c3-114">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="db8c3-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="db8c3-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="db8c3-115">Example</span></span>

<span data-ttu-id="db8c3-116">Datakilden **$JsonField** indeholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="db8c3-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="db8c3-117">I dette tilfælde returnerer `JSONVALUE (JsonField, "BuildNumber")`-udtrykket følgende værdi af datatypen *Streng*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="db8c3-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db8c3-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="db8c3-118">Additional resources</span></span>

[<span data-ttu-id="db8c3-119">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="db8c3-119">Text functions</span></span>](er-functions-category-text.md)
