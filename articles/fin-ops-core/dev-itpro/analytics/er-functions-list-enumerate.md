---
title: ER-funktionen ENUMERATE
description: Dette emne indeholder oplysninger om, hvordan funktionen ENUMERATE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916217"
---
# <span data-ttu-id="c18d4-103"><a name="ENUMERATE">ER-funktionen ENUMERATE</a></span><span class="sxs-lookup"><span data-stu-id="c18d4-103"><a name="ENUMERATE">ENUMERATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c18d4-104">Funktionen `ENUMERATE` returnerer en ny *Postliste*-værdi, der består af optalte poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="c18d4-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c18d4-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c18d4-105">Syntax</span></span>

```
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="c18d4-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c18d4-106">Arguments</span></span>

<span data-ttu-id="c18d4-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="c18d4-107">`list`: *Record list*</span></span>

<span data-ttu-id="c18d4-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="c18d4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c18d4-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="c18d4-109">Return values</span></span>

<span data-ttu-id="c18d4-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="c18d4-110">*Record list*</span></span>

<span data-ttu-id="c18d4-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="c18d4-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c18d4-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="c18d4-112">Usage notes</span></span>

<span data-ttu-id="c18d4-113">Listen over optalte poster, der returneres, udsætter følgende yderligere elementer:</span><span class="sxs-lookup"><span data-stu-id="c18d4-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="c18d4-114">Feltposter (**Værdi**-komponent)</span><span class="sxs-lookup"><span data-stu-id="c18d4-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="c18d4-115">Det aktuelle postindeks (**Tal**-komponent)</span><span class="sxs-lookup"><span data-stu-id="c18d4-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="c18d4-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c18d4-116">Example</span></span>

<span data-ttu-id="c18d4-117">I følgende illustration er **Enumerated**-datakilden oprettet som en fasttekstliste over kreditorposter fra **Vendors**-datakilden, der henviser til VendTable-tabellen.</span><span class="sxs-lookup"><span data-stu-id="c18d4-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="c18d4-118">I følgende illustration vises formatet elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="c18d4-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="c18d4-119">I dette format oprettes databindinger for at generere outputtet i XML-format.</span><span class="sxs-lookup"><span data-stu-id="c18d4-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="c18d4-120">Dette output viser individuelle leverandører som optalte noder.</span><span class="sxs-lookup"><span data-stu-id="c18d4-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="c18d4-121">I følgende illustration vises resultatet, når det designede format køres.</span><span class="sxs-lookup"><span data-stu-id="c18d4-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="c18d4-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c18d4-122">Additional resources</span></span>

[<span data-ttu-id="c18d4-123">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="c18d4-123">List functions</span></span>](er-functions-category-list.md)
