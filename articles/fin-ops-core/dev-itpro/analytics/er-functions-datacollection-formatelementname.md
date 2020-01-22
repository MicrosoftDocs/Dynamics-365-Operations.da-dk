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
ms.openlocfilehash: d66fed3815188fa7e31735e3523376ae4ea1cf46
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917666"
---
# <span data-ttu-id="f38e3-103"><a name="FORMATELEMENTNAME">ER-funktionen FORMATELEMENTNAME</a></span><span class="sxs-lookup"><span data-stu-id="f38e3-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f38e3-104">Funktionen `FORMATELEMENTNAME` returnerer en *Streng*-værdi, som repræsenterer navnet på det aktuelle element for elektronisk rapporteringsformat (ER).</span><span class="sxs-lookup"><span data-stu-id="f38e3-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38e3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f38e3-105">Syntax</span></span>

```
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="f38e3-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f38e3-106">Return values</span></span>

<span data-ttu-id="f38e3-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="f38e3-107">*String*</span></span>

<span data-ttu-id="f38e3-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="f38e3-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f38e3-109">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="f38e3-109">Usage notes</span></span>

<span data-ttu-id="f38e3-110">Denne funktion kan kaldes i ER-udtryk, som blev konfigureret for egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** til en ER-formatkomponent fra gruppen **Tekst**, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="f38e3-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="f38e3-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f38e3-111">Example</span></span>

<span data-ttu-id="f38e3-112">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="f38e3-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f38e3-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f38e3-113">Additional resources</span></span>

[<span data-ttu-id="f38e3-114">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f38e3-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
