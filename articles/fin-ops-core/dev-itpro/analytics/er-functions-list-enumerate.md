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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745243"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="6bb4a-103">ER-funktionen ENUMERATE</span><span class="sxs-lookup"><span data-stu-id="6bb4a-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bb4a-104">Funktionen `ENUMERATE` returnerer en ny *Postliste*-værdi, der består af optalte poster på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb4a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="6bb4a-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="6bb4a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="6bb4a-106">Arguments</span></span>

<span data-ttu-id="6bb4a-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="6bb4a-107">`list`: *Record list*</span></span>

<span data-ttu-id="6bb4a-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="6bb4a-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="6bb4a-109">Return values</span></span>

<span data-ttu-id="6bb4a-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="6bb4a-110">*Record list*</span></span>

<span data-ttu-id="6bb4a-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6bb4a-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="6bb4a-112">Usage notes</span></span>

<span data-ttu-id="6bb4a-113">Listen over optalte poster, der returneres, udsætter følgende yderligere elementer:</span><span class="sxs-lookup"><span data-stu-id="6bb4a-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="6bb4a-114">Feltposter (**Værdi**-komponent)</span><span class="sxs-lookup"><span data-stu-id="6bb4a-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="6bb4a-115">Det aktuelle postindeks (**Tal**-komponent)</span><span class="sxs-lookup"><span data-stu-id="6bb4a-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="6bb4a-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="6bb4a-116">Example</span></span>

<span data-ttu-id="6bb4a-117">I følgende illustration er **Enumerated**-datakilden oprettet som en fasttekstliste over kreditorposter fra **Vendors**-datakilden, der henviser til VendTable-tabellen.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="6bb4a-118">I følgende illustration vises formatet elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="6bb4a-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="6bb4a-119">I dette format oprettes databindinger for at generere outputtet i XML-format.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="6bb4a-120">Dette output viser individuelle leverandører som optalte noder.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="6bb4a-121">I følgende illustration vises resultatet, når det designede format køres.</span><span class="sxs-lookup"><span data-stu-id="6bb4a-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="6bb4a-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6bb4a-122">Additional resources</span></span>

[<span data-ttu-id="6bb4a-123">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="6bb4a-123">List functions</span></span>](er-functions-category-list.md)
