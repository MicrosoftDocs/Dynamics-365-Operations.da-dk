---
title: ER-funktionen SUMIF
description: Dette emne indeholder oplysninger om, hvordan funktionen SUMIF til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916424"
---
# <span data-ttu-id="33ec8-103"><a name="SUMIF">ER-funktionen SUMIF</a></span><span class="sxs-lookup"><span data-stu-id="33ec8-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33ec8-104">Funktionen `SUMIF` returnerer en *Reel* værdi, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="33ec8-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="33ec8-105">Betingelsen består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="33ec8-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ec8-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="33ec8-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="33ec8-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="33ec8-107">Arguments</span></span>

<span data-ttu-id="33ec8-108">`key name for summing`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="33ec8-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="33ec8-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for formatkomponenten til elektronisk rapportering (ER), for hvilken værdien af bindingen skal bruges til opsummerende formål.</span><span class="sxs-lookup"><span data-stu-id="33ec8-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="33ec8-110">Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="33ec8-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="33ec8-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="33ec8-111">Return values</span></span>

<span data-ttu-id="33ec8-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="33ec8-112">*Real*</span></span>

<span data-ttu-id="33ec8-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="33ec8-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="33ec8-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="33ec8-114">Usage notes</span></span>

<span data-ttu-id="33ec8-115">Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="33ec8-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="33ec8-116">I argumentet `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="33ec8-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="33ec8-117">I argumentet `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="33ec8-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="33ec8-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="33ec8-118">Example</span></span>

<span data-ttu-id="33ec8-119">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="33ec8-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33ec8-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="33ec8-120">Additional resources</span></span>

[<span data-ttu-id="33ec8-121">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="33ec8-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
