---
title: ER-funktionen CHAR
description: Dette emne indeholder oplysninger om, hvordan funktionen CHAR til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746429"
---
# <a name="char-er-function"></a><span data-ttu-id="26778-103">ER-funktionen CHAR</span><span class="sxs-lookup"><span data-stu-id="26778-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26778-104">Funktionen `CHAR` returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="26778-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="26778-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="26778-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="26778-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="26778-106">Arguments</span></span>

<span data-ttu-id="26778-107">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="26778-107">`number`: *Integer*</span></span>

<span data-ttu-id="26778-108">Et tal, der svarer til et forventet enkelt tegn.</span><span class="sxs-lookup"><span data-stu-id="26778-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="26778-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="26778-109">Return values</span></span>

<span data-ttu-id="26778-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="26778-110">*String*</span></span>

<span data-ttu-id="26778-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="26778-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26778-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="26778-112">Usage notes</span></span>

<span data-ttu-id="26778-113">Den streng, som denne funktion returnerer, afhænger af den kodning, der er valgt i det overordnede **FIL**-formatelement.</span><span class="sxs-lookup"><span data-stu-id="26778-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="26778-114">Du kan finde en liste over understøttede kodninger under [Kodningsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="26778-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="26778-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="26778-115">Example</span></span>

<span data-ttu-id="26778-116">`CHAR (255)` returnerer **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="26778-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26778-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="26778-117">Additional resources</span></span>

[<span data-ttu-id="26778-118">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="26778-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]