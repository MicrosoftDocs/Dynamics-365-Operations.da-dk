---
title: ER-funktionen COLLECTEDLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen COLLECTEDLIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
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
ms.openlocfilehash: 494fb0fa1000abe8d0234d512e41926103c56f05
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755318"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="f9025-103">ER-funktionen COLLECTEDLIST</span><span class="sxs-lookup"><span data-stu-id="f9025-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9025-104">Funktionen `COLLECTEDLIST` returnerer en *Postliste*-værdi, der indeholder listen over værdier, der blev returneret af egenskaben **Indsamlet datanøgleværdi** for formatelementer og indsamles, når formateringselementerne blev brugt til at generere udgående dokumenter under format kørslen, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="f9025-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="f9025-105">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="f9025-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9025-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f9025-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="f9025-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f9025-107">Arguments</span></span>

<span data-ttu-id="f9025-108">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f9025-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="f9025-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i formatet elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="f9025-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="f9025-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="f9025-110">This argument is mandatory.</span></span>

<span data-ttu-id="f9025-111">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f9025-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="f9025-112">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="f9025-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f9025-113">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="f9025-113">This argument is mandatory.</span></span>

<span data-ttu-id="f9025-114">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f9025-114">`condition N range`: *String*</span></span>

<span data-ttu-id="f9025-115">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="f9025-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="f9025-116">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="f9025-116">These additional arguments are optional.</span></span>

<span data-ttu-id="f9025-117">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="f9025-117">`condition N value`: *String*</span></span>

<span data-ttu-id="f9025-118">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="f9025-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f9025-119">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="f9025-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9025-120">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="f9025-120">Return values</span></span>

<span data-ttu-id="f9025-121">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="f9025-121">*Record list*</span></span>

<span data-ttu-id="f9025-122">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="f9025-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f9025-123">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="f9025-123">Usage notes</span></span>

<span data-ttu-id="f9025-124">Egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** kan konfigureres til komponenten **Sekvens** eller til komponenten **XML-element** i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="f9025-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="f9025-125">Denne funktion returnerer en tom liste, når indstillingen **Detaljer om indsamlingsoutput** for komponenten **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="f9025-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="f9025-126">I `condition range` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="f9025-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="f9025-127">I `condition value` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="f9025-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="f9025-128">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f9025-128">Example</span></span>

<span data-ttu-id="f9025-129">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="f9025-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9025-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f9025-130">Additional resources</span></span>

[<span data-ttu-id="f9025-131">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="f9025-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]