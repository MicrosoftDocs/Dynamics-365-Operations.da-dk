---
title: ER-funktionen SPLITLISTBYLIMIT
description: Dette emne indeholder oplysninger om, hvordan funktionen SPLITLISTBYLIMIT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745539"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="7659c-103">ER-funktionen SPLITLISTBYLIMIT</span><span class="sxs-lookup"><span data-stu-id="7659c-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7659c-104">Funktionen `SPLITLISTBYLIMIT` opdeler den angivne liste i en ny liste over underlister (batches).</span><span class="sxs-lookup"><span data-stu-id="7659c-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="7659c-105">Antallet af poster i hvert batch beregnes dynamisk.</span><span class="sxs-lookup"><span data-stu-id="7659c-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="7659c-106">Funktionen returnerer dernæst resultatet som en ny *Postliste*-værdi, der består af batches.</span><span class="sxs-lookup"><span data-stu-id="7659c-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="7659c-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="7659c-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="7659c-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="7659c-108">Arguments</span></span>

<span data-ttu-id="7659c-109">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="7659c-109">`list`: *Record list*</span></span>

<span data-ttu-id="7659c-110">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="7659c-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7659c-111">`limit value`: *Heltal* eller *Reel*</span><span class="sxs-lookup"><span data-stu-id="7659c-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="7659c-112">Maksimumværdien for den grænse, der bruges til at opdele den oprindelige liste i batches.</span><span class="sxs-lookup"><span data-stu-id="7659c-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="7659c-113">`limit source`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="7659c-113">`limit source`: *Field*</span></span>

<span data-ttu-id="7659c-114">Den gyldige sti til et felt af typen *Heltal* eller *Reel* på den angivne liste.</span><span class="sxs-lookup"><span data-stu-id="7659c-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="7659c-115">Værdien i dette felt definerer det trin, som den samlede sum forøges med.</span><span class="sxs-lookup"><span data-stu-id="7659c-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="7659c-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="7659c-116">Return values</span></span>

<span data-ttu-id="7659c-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="7659c-117">*Record list*</span></span>

<span data-ttu-id="7659c-118">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="7659c-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7659c-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="7659c-119">Usage notes</span></span>

<span data-ttu-id="7659c-120">Den returnerede batchliste indeholder følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="7659c-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="7659c-121">**Værdi**: *Liste*</span><span class="sxs-lookup"><span data-stu-id="7659c-121">**Value**: *List*</span></span>

    <span data-ttu-id="7659c-122">Listen over poster, der tilhører den aktuelle batch.</span><span class="sxs-lookup"><span data-stu-id="7659c-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="7659c-123">**Batchnumber**: *Heltal*</span><span class="sxs-lookup"><span data-stu-id="7659c-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="7659c-124">Antallet af aktuelle batches på den returnerede liste.</span><span class="sxs-lookup"><span data-stu-id="7659c-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="7659c-125">Grænsen anvendes ikke på et enkelt element på den oprindelige liste, hvis grænsekilden overskrider den angivne grænse.</span><span class="sxs-lookup"><span data-stu-id="7659c-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="7659c-126">Eksempel</span><span class="sxs-lookup"><span data-stu-id="7659c-126">Example</span></span>

<span data-ttu-id="7659c-127">I følgende illustration vises et format til elektronisk rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="7659c-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="7659c-128">Følgende illustration viser de datakilder, der bruges til formatet.</span><span class="sxs-lookup"><span data-stu-id="7659c-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="7659c-129">I følgende illustration vises resultatet, når formatet køres.</span><span class="sxs-lookup"><span data-stu-id="7659c-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="7659c-130">I så fald er outputtet en simpel liste over råvarer.</span><span class="sxs-lookup"><span data-stu-id="7659c-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="7659c-131">I de følgende illustrationer er det samme format blevet justeret, så den repræsenterer listen over varegoder i batches, hvis et enkelt batch skal indeholde goder, og den samlede vægt ikke må overstige en grænse 9.</span><span class="sxs-lookup"><span data-stu-id="7659c-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="7659c-132">I følgende illustration vises resultatet, når det justerede format køres.</span><span class="sxs-lookup"><span data-stu-id="7659c-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="7659c-133">Grænsen anvendes ikke på den sidste vare på den oprindelige liste, da værdien (**11**) af grænsekilden (**vægt**) overskrider den angivne grænse (**9**).</span><span class="sxs-lookup"><span data-stu-id="7659c-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="7659c-134">For at ignorere underordnede lister under oprettelse af rapporter skal du enten bruge funktionen `WHERE` eller udtrykket **Aktiveret** for det tilsvarende formatelement, du har brug for.</span><span class="sxs-lookup"><span data-stu-id="7659c-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7659c-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="7659c-135">Additional resources</span></span>

[<span data-ttu-id="7659c-136">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="7659c-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]