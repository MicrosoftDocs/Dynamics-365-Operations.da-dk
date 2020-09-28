---
title: ER-funktionen SUMIFS
description: Dette emne indeholder oplysninger om, hvordan funktionen SUMIFS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: a6815a8c9f4141649532f9cd56ac3bc442b48686
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743321"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="2378c-103">ER-funktionen SUMIFS</span><span class="sxs-lookup"><span data-stu-id="2378c-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2378c-104">Funktionen `SUMIFS` returnerer en *Reel* værdi, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="2378c-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2378c-105">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="2378c-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2378c-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2378c-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="2378c-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2378c-107">Arguments</span></span>

<span data-ttu-id="2378c-108">`key name for summing`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2378c-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="2378c-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for formatkomponenten til elektronisk rapportering (ER), for hvilken værdien af bindingen skal bruges til opsummerende formål.</span><span class="sxs-lookup"><span data-stu-id="2378c-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="2378c-110">Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Numerisk** komponent eller en **Streng**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2378c-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2378c-111">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2378c-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="2378c-112">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="2378c-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="2378c-113">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="2378c-113">This argument is mandatory.</span></span>

<span data-ttu-id="2378c-114">Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2378c-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2378c-115">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2378c-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="2378c-116">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="2378c-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2378c-117">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="2378c-117">This argument is mandatory.</span></span>

<span data-ttu-id="2378c-118">Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2378c-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2378c-119">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2378c-119">`condition N range`: *String*</span></span>

<span data-ttu-id="2378c-120">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="2378c-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="2378c-121">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="2378c-121">These additional arguments are optional.</span></span>

<span data-ttu-id="2378c-122">Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2378c-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2378c-123">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2378c-123">`condition N value`: *String*</span></span>

<span data-ttu-id="2378c-124">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="2378c-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2378c-125">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="2378c-125">These additional arguments are optional.</span></span>

<span data-ttu-id="2378c-126">Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2378c-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="2378c-127">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="2378c-127">Return values</span></span>

<span data-ttu-id="2378c-128">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="2378c-128">*Real*</span></span>

<span data-ttu-id="2378c-129">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="2378c-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2378c-130">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="2378c-130">Usage notes</span></span>

<span data-ttu-id="2378c-131">Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="2378c-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="2378c-132">I argumenterne `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="2378c-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="2378c-133">I argumenterne `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="2378c-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="2378c-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2378c-134">Example</span></span>

<span data-ttu-id="2378c-135">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="2378c-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2378c-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2378c-136">Additional resources</span></span>

[<span data-ttu-id="2378c-137">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="2378c-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
