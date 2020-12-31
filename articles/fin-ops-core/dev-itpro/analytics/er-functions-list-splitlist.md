---
title: ER-funktionen SPLITLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLITLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0f527dcf313a6a5e3b6601cac9a0f6495f66833
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680332"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="114d4-103">ER-funktionen SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="114d4-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="114d4-104">Funktionen `SPLITLIST` opdeler den angivne liste i underlister (eller batches), som hver især indeholder det angivne antal poster.</span><span class="sxs-lookup"><span data-stu-id="114d4-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="114d4-105">Derefter returneres resultatet som en ny *Postliste*-værdi, der består af batches.</span><span class="sxs-lookup"><span data-stu-id="114d4-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="114d4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="114d4-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="114d4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="114d4-107">Arguments</span></span>

<span data-ttu-id="114d4-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="114d4-108">`list`: *Record list*</span></span>

<span data-ttu-id="114d4-109">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="114d4-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="114d4-110">`number`: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="114d4-110">`number`: *Integer*</span></span>

<span data-ttu-id="114d4-111">Det højeste antal viste poster per batch.</span><span class="sxs-lookup"><span data-stu-id="114d4-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="114d4-112">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="114d4-112">Return values</span></span>

<span data-ttu-id="114d4-113">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="114d4-113">*Record list*</span></span>

<span data-ttu-id="114d4-114">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="114d4-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="114d4-115">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="114d4-115">Usage notes</span></span>

<span data-ttu-id="114d4-116">Den returnerede batchliste indeholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="114d4-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="114d4-117">**Værdi:** *Liste*</span><span class="sxs-lookup"><span data-stu-id="114d4-117">**Value:** *List*</span></span>

    <span data-ttu-id="114d4-118">Listen over poster, der tilhører den aktuelle batch.</span><span class="sxs-lookup"><span data-stu-id="114d4-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="114d4-119">**Batchnumber:** *Heltal*</span><span class="sxs-lookup"><span data-stu-id="114d4-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="114d4-120">Antallet af aktuelle batches på den returnerede liste.</span><span class="sxs-lookup"><span data-stu-id="114d4-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="114d4-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="114d4-121">Example</span></span>

<span data-ttu-id="114d4-122">I følgende illustration er der oprettet en **Linjer**-datakilde som en postliste, der har mere end tre poster.</span><span class="sxs-lookup"><span data-stu-id="114d4-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="114d4-123">Denne liste er opdelt i bundter, som hver indeholder op til to poster.</span><span class="sxs-lookup"><span data-stu-id="114d4-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="114d4-124">I følgende illustration vises det designede formatlayout.</span><span class="sxs-lookup"><span data-stu-id="114d4-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="114d4-125">I dette formatlayout er bindinger til datakilden **Linjer** oprettet for at generere outputtet i XML-format.</span><span class="sxs-lookup"><span data-stu-id="114d4-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="114d4-126">Dette output viser individuelle noder for hvert parti og posterne i det.</span><span class="sxs-lookup"><span data-stu-id="114d4-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="114d4-127">I følgende illustration vises resultatet, når det designede format køres.</span><span class="sxs-lookup"><span data-stu-id="114d4-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="114d4-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="114d4-128">Additional resources</span></span>

[<span data-ttu-id="114d4-129">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="114d4-129">List functions</span></span>](er-functions-category-list.md)
