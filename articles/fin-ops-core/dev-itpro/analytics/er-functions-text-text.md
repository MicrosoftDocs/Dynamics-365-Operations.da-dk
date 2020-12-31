---
title: ER-funktionen TEXT
description: Dette emne indeholder oplysninger om, hvordan funktionen TEXT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682889"
---
# <a name="text-er-function"></a><span data-ttu-id="a0782-103">ER-funktionen TEXT</span><span class="sxs-lookup"><span data-stu-id="a0782-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0782-104">Funktionen `TEXT` returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="a0782-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0782-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a0782-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="a0782-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a0782-106">Arguments</span></span>

<span data-ttu-id="a0782-107">`number`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="a0782-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="a0782-108">Et tal, der skal konverteres til en tekststreng.</span><span class="sxs-lookup"><span data-stu-id="a0782-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0782-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="a0782-109">Return values</span></span>

<span data-ttu-id="a0782-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a0782-110">*String*</span></span>

<span data-ttu-id="a0782-111">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="a0782-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a0782-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="a0782-112">Usage notes</span></span>

<span data-ttu-id="a0782-113">For værdier af typen *Reel* er strengkonverteringen begrænset til to decimaler.</span><span class="sxs-lookup"><span data-stu-id="a0782-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="a0782-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a0782-114">Example</span></span>

<span data-ttu-id="a0782-115">Hvis serverens landestandard for Microsoft Dynamics 365 Finance-forekomsten er defineret som **EN-US**, returnerer `TEXT (NOW ())` den aktuelle Finance-sessionsdato, 17. december 2015, som tekststrengen **"17/12/2015 07:59:23"**.</span><span class="sxs-lookup"><span data-stu-id="a0782-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="a0782-116">`TEXT (1/3)` returnerer **"0,33"**.</span><span class="sxs-lookup"><span data-stu-id="a0782-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0782-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a0782-117">Additional resources</span></span>

[<span data-ttu-id="a0782-118">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="a0782-118">Text functions</span></span>](er-functions-category-text.md)
