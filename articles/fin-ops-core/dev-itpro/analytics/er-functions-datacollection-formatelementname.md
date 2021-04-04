---
title: ER-funktionen FORMATELEMENTNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen FORMATELEMENTNAME til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561296"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="31573-103">ER-funktionen FORMATELEMENTNAME</span><span class="sxs-lookup"><span data-stu-id="31573-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31573-104">Funktionen `FORMATELEMENTNAME` returnerer en *Streng*-værdi, som repræsenterer navnet på det aktuelle element for elektronisk rapporteringsformat (ER).</span><span class="sxs-lookup"><span data-stu-id="31573-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="31573-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="31573-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="31573-106">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="31573-106">Return values</span></span>

<span data-ttu-id="31573-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="31573-107">*String*</span></span>

<span data-ttu-id="31573-108">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="31573-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="31573-109">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="31573-109">Usage notes</span></span>

<span data-ttu-id="31573-110">Denne funktion kan kaldes i ER-udtryk, som blev konfigureret for egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** til en ER-formatkomponent fra gruppen **Tekst**, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="31573-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="31573-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="31573-111">Example</span></span>

<span data-ttu-id="31573-112">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="31573-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31573-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="31573-113">Additional resources</span></span>

[<span data-ttu-id="31573-114">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="31573-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]