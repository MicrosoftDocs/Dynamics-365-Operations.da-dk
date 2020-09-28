---
title: ER-funktionen FORMATELEMENTNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen FORMATELEMENTNAME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745627"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="6c09f-103">ER-funktionen FORMATELEMENTNAME</span><span class="sxs-lookup"><span data-stu-id="6c09f-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c09f-104">Funktionen `FORMATELEMENTNAME` returnerer en *Streng*-værdi, som repræsenterer navnet på det aktuelle element for elektronisk rapporteringsformat (ER).</span><span class="sxs-lookup"><span data-stu-id="6c09f-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c09f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="6c09f-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="6c09f-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="6c09f-106">Return values</span></span>

<span data-ttu-id="6c09f-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6c09f-107">*String*</span></span>

<span data-ttu-id="6c09f-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="6c09f-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6c09f-109">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="6c09f-109">Usage notes</span></span>

<span data-ttu-id="6c09f-110">Denne funktion kan kaldes i ER-udtryk, som blev konfigureret for egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** til en ER-formatkomponent fra gruppen **Tekst**, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="6c09f-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="6c09f-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6c09f-111">Example</span></span>

<span data-ttu-id="6c09f-112">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="6c09f-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c09f-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6c09f-113">Additional resources</span></span>

[<span data-ttu-id="6c09f-114">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="6c09f-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
