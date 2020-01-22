---
title: ER-funktionen COUNTIF
description: Dette emne indeholder oplysninger om, hvordan funktionen COUNTIF til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917689"
---
# <span data-ttu-id="a5525-103"><a name="COUNTIF">ER-funktionen COUNTIF</a></span><span class="sxs-lookup"><span data-stu-id="a5525-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5525-104">Funktionen `COUNTIF` returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="a5525-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a5525-105">Betingelsen består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a5525-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5525-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="a5525-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="a5525-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="a5525-107">Arguments</span></span>

<span data-ttu-id="a5525-108">`condition range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="a5525-108">`condition range`: *String*</span></span>

<span data-ttu-id="a5525-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i formatet elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="a5525-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="a5525-110">`condition value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="a5525-110">`condition value`: *String*</span></span>

<span data-ttu-id="a5525-111">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="a5525-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5525-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="a5525-112">Return values</span></span>

<span data-ttu-id="a5525-113">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="a5525-113">*Integer*</span></span>

<span data-ttu-id="a5525-114">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="a5525-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a5525-115">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="a5525-115">Usage notes</span></span>

<span data-ttu-id="a5525-116">Egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** kan konfigureres til komponenten **Sekvens** eller til komponenten **XML-element** i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a5525-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a5525-117">Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="a5525-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="a5525-118">I argumentet `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="a5525-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="a5525-119">I argumentet `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="a5525-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="a5525-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a5525-120">Example</span></span>

<span data-ttu-id="a5525-121">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="a5525-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5525-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a5525-122">Additional resources</span></span>

[<span data-ttu-id="a5525-123">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="a5525-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
