---
title: ER-funktionen COUNTIFS
description: Dette emne indeholder oplysninger om, hvordan funktionen COUNTIFS til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 9627c7835c8f3f1b6aedc1f691470dc29a11d6b5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042544"
---
# <span data-ttu-id="5afeb-103"><a name="COUNTIFS">ER-funktionen COUNTIFS</a></span><span class="sxs-lookup"><span data-stu-id="5afeb-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5afeb-104">Funktionen `COUNTIFS` returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="5afeb-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="5afeb-105">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="5afeb-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afeb-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5afeb-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="5afeb-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5afeb-107">Arguments</span></span>

<span data-ttu-id="5afeb-108">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5afeb-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="5afeb-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i formatet elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="5afeb-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="5afeb-110">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="5afeb-110">This argument is mandatory.</span></span>

<span data-ttu-id="5afeb-111">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5afeb-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="5afeb-112">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="5afeb-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="5afeb-113">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="5afeb-113">This argument is mandatory.</span></span>

<span data-ttu-id="5afeb-114">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5afeb-114">`condition N range`: *String*</span></span>

<span data-ttu-id="5afeb-115">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="5afeb-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="5afeb-116">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="5afeb-116">These additional arguments are optional.</span></span>

<span data-ttu-id="5afeb-117">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5afeb-117">`condition N value`: *String*</span></span>

<span data-ttu-id="5afeb-118">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.</span><span class="sxs-lookup"><span data-stu-id="5afeb-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="5afeb-119">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="5afeb-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="5afeb-120">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5afeb-120">Return values</span></span>

<span data-ttu-id="5afeb-121">*Heltal*</span><span class="sxs-lookup"><span data-stu-id="5afeb-121">*Integer*</span></span>

<span data-ttu-id="5afeb-122">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="5afeb-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5afeb-123">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="5afeb-123">Usage notes</span></span>

<span data-ttu-id="5afeb-124">Egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** kan konfigureres til komponenten **Sekvens** eller til komponenten **XML-element** i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="5afeb-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="5afeb-125">Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="5afeb-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="5afeb-126">I `condition range` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="5afeb-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="5afeb-127">I `condition value` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="5afeb-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="5afeb-128">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5afeb-128">Example</span></span>

<span data-ttu-id="5afeb-129">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="5afeb-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5afeb-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5afeb-130">Additional resources</span></span>

[<span data-ttu-id="5afeb-131">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="5afeb-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
