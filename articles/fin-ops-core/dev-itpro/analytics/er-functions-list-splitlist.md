---
title: ER-funktionen SPLITLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLITLIST til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745563"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="b0cb1-103">ER-funktionen SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="b0cb1-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0cb1-104">Funktionen `SPLITLIST` opdeler den angivne liste i underlister (eller batches), som hver især indeholder det angivne antal poster.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="b0cb1-105">Derefter returneres resultatet som en ny *Postliste*-værdi, der består af batches.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b0cb1-106">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="b0cb1-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="b0cb1-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="b0cb1-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="b0cb1-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b0cb1-108">Arguments</span></span>

<span data-ttu-id="b0cb1-109">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-109">`list`: *Record list*</span></span>

<span data-ttu-id="b0cb1-110">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b0cb1-111">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-111">`number`: *Integer*</span></span>

<span data-ttu-id="b0cb1-112">Det højeste antal viste poster per batch.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="b0cb1-113">`on-demand reading flag`: *Boolesk*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="b0cb1-114">En *boolesk* værdi, der angiver, om elementer i underlister skal genereres efter behov.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0cb1-115">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="b0cb1-115">Return values</span></span>

<span data-ttu-id="b0cb1-116">*Liste over poster*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-116">*Record list*</span></span>

<span data-ttu-id="b0cb1-117">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b0cb1-118">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="b0cb1-118">Usage notes</span></span>

<span data-ttu-id="b0cb1-119">Den returnerede batchliste indeholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="b0cb1-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="b0cb1-120">**Værdi:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-120">**Value:** *List*</span></span>

    <span data-ttu-id="b0cb1-121">Listen over poster, der tilhører den aktuelle batch.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="b0cb1-122">**Batchnumber:** *Heltal*</span><span class="sxs-lookup"><span data-stu-id="b0cb1-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="b0cb1-123">Antallet af aktuelle batches på den returnerede liste.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="b0cb1-124">Når aflæsningsflaget efter behov angives til **Sand**, genereres der underlister ved anmodning, hvilket gør det muligt at reducere forbruget af hukommelse, men det kan medføre nedsat ydeevne, hvis elementer ikke bruges sekventielt.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="b0cb1-125">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b0cb1-125">Example</span></span>

<span data-ttu-id="b0cb1-126">I følgende illustration er der oprettet en **Linjer**-datakilde som en postliste, der har mere end tre poster.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="b0cb1-127">Denne liste er opdelt i bundter, som hver indeholder op til to poster.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="b0cb1-128">I følgende illustration vises det designede formatlayout.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="b0cb1-129">I dette formatlayout er bindinger til datakilden **Linjer** oprettet for at generere outputtet i XML-format.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="b0cb1-130">Dette output viser individuelle noder for hvert parti og posterne i det.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="b0cb1-131">I følgende illustration vises resultatet, når det designede format køres.</span><span class="sxs-lookup"><span data-stu-id="b0cb1-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="b0cb1-132">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b0cb1-132">Additional resources</span></span>

[<span data-ttu-id="b0cb1-133">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="b0cb1-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
