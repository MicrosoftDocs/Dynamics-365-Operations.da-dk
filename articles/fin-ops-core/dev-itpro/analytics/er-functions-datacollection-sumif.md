---
title: ER-funktionen SUMIF
description: Dette emne indeholder oplysninger om, hvordan funktionen SUMIF til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 6f5069d197abf2e38d09012defeb982a9e5e1234
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565958"
---
# <a name="sumif-er-function"></a><span data-ttu-id="9981d-103">ER-funktionen SUMIF</span><span class="sxs-lookup"><span data-stu-id="9981d-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9981d-104">Funktionen `SUMIF` returnerer en *Reel* værdi, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="9981d-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="9981d-105">Betingelsen består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="9981d-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9981d-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9981d-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="9981d-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9981d-107">Arguments</span></span>

<span data-ttu-id="9981d-108">`key name for summing`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="9981d-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="9981d-109">En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for formatkomponenten til elektronisk rapportering (ER), for hvilken værdien af bindingen skal bruges til opsummerende formål.</span><span class="sxs-lookup"><span data-stu-id="9981d-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="9981d-110">Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="9981d-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="9981d-111">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="9981d-111">Return values</span></span>

<span data-ttu-id="9981d-112">*Kommatal*</span><span class="sxs-lookup"><span data-stu-id="9981d-112">*Real*</span></span>

<span data-ttu-id="9981d-113">Den resulterende numeriske værdi.</span><span class="sxs-lookup"><span data-stu-id="9981d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9981d-114">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="9981d-114">Usage notes</span></span>

<span data-ttu-id="9981d-115">Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.</span><span class="sxs-lookup"><span data-stu-id="9981d-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="9981d-116">I argumentet `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="9981d-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="9981d-117">I argumentet `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="9981d-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="9981d-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9981d-118">Example</span></span>

<span data-ttu-id="9981d-119">Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="9981d-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="9981d-120">Yderligere oplysninger og eksempler på brug af denne funktion finder du under [Udskyde udførelse af sekvenselementer i ER-formater](er-defer-sequence-element.md#Example) og [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="9981d-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9981d-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9981d-121">Additional resources</span></span>

[<span data-ttu-id="9981d-122">Dataindsamlingsfunktioner</span><span class="sxs-lookup"><span data-stu-id="9981d-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]