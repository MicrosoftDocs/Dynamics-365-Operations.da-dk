---
title: Liste over ER-funktioner i kategorien dataindsamling
description: Dette emne indeholder oplysninger om de dataindsamlingsfunktioner, der understøttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: b318945c9cd10b237843d26cfdc46fc08e84e268
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917804"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="a02ef-103">Liste over ER-funktioner i kategorien dataindsamling</span><span class="sxs-lookup"><span data-stu-id="a02ef-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a02ef-104">Dataindsamlingsfunktionerne til elektronisk rapportering (ER) bruges til at tælle og opsummere i et ER-format, der køres, og som er baseret på data fra det output, der allerede er genereret i formatet **Tekst** eller **XML**.</span><span class="sxs-lookup"><span data-stu-id="a02ef-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="a02ef-105">Denne fremgangsmåde bruges til at forbedre ydeevnen i et ER-format, der køres, til at angive værdier for fortløbende totaler i genererede dokumenter og til andre formål.</span><span class="sxs-lookup"><span data-stu-id="a02ef-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="a02ef-106">Dette emne indeholder en oversigt over disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="a02ef-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a02ef-107">Liste med understøttede funktioner</span><span class="sxs-lookup"><span data-stu-id="a02ef-107">List of supported functions</span></span>

| <span data-ttu-id="a02ef-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="a02ef-108">Function</span></span> | <span data-ttu-id="a02ef-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a02ef-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a02ef-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="a02ef-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="a02ef-111">Denne funktion returnerer en *Postliste*-værdi, der indeholder listen over værdier, der blev returneret af egenskaben **Indsamlet datanøgleværdi** for formatelementer og indsamles, når formateringselementerne blev brugt til at generere et udgående dokument under format kørslen, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="a02ef-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a02ef-112">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a02ef-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a02ef-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="a02ef-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="a02ef-114">Denne funktion returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="a02ef-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a02ef-115">Betingelsen består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a02ef-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a02ef-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="a02ef-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="a02ef-117">Denne funktion returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="a02ef-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a02ef-118">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a02ef-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a02ef-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="a02ef-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="a02ef-120">Denne funktion returnerer en værdi i form af en *Streng*, som repræsenterer navnet på det aktuelle ER-formatelement.</span><span class="sxs-lookup"><span data-stu-id="a02ef-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="a02ef-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="a02ef-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="a02ef-122">Denne funktion returnerer en værdi bestående af *Reelle tal*, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse.</span><span class="sxs-lookup"><span data-stu-id="a02ef-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a02ef-123">Betingelsen består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a02ef-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a02ef-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="a02ef-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="a02ef-125">Denne funktion returnerer en værdi bestående af *Reelle tal*, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser.</span><span class="sxs-lookup"><span data-stu-id="a02ef-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a02ef-126">Hver betingelse består af et nøgleområde og en nøgleværdi.</span><span class="sxs-lookup"><span data-stu-id="a02ef-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a02ef-127">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a02ef-127">Additional resources</span></span>

[<span data-ttu-id="a02ef-128">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a02ef-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a02ef-129">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a02ef-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a02ef-130">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a02ef-130">Electronic reporting formula language</span></span>](er-formula-language.md)
