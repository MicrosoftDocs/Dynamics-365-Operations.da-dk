---
title: Liste over ER-funktioner i containerkategorien
description: Dette emne indeholder oplysninger om de containerfunktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561752"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="3fa3f-103">Liste over ER-funktioner i containerkategorien</span><span class="sxs-lookup"><span data-stu-id="3fa3f-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fa3f-104">Container-[funktioner](er-formula-language.md#functions) til [elektronisk rapportering (ER)](general-electronic-reporting.md) kan bruges til at udføre handlinger på datakilder af datatypen *Container*.</span><span class="sxs-lookup"><span data-stu-id="3fa3f-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="3fa3f-105">Disse operationer finder sted, når behandlingsdata repræsenterer en samling binære data i BLOB-format (binært stort objekt).</span><span class="sxs-lookup"><span data-stu-id="3fa3f-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="3fa3f-106">Dette emne indeholder en oversigt over disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="3fa3f-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="3fa3f-107">Liste med understøttede funktioner</span><span class="sxs-lookup"><span data-stu-id="3fa3f-107">List of supported functions</span></span>

| <span data-ttu-id="3fa3f-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="3fa3f-108">Function</span></span> | <span data-ttu-id="3fa3f-109">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="3fa3f-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="3fa3f-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="3fa3f-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="3fa3f-111">Denne funktion returnerer en *Container*-værdi, der består af binært indhold, der er afkodet fra den angivne ASCII-streng, som repræsenterer en Base64-gruppe af binær til tekst-kodningsskemaer.</span><span class="sxs-lookup"><span data-stu-id="3fa3f-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="3fa3f-112">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3fa3f-112">Additional resources</span></span>

[<span data-ttu-id="3fa3f-113">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3fa3f-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="3fa3f-114">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3fa3f-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="3fa3f-115">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="3fa3f-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]