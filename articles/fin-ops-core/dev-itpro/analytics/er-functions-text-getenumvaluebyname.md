---
title: ER-funktionen GETENUMVALUEBYNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen GETENUMVALUEBYNAME til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916838"
---
# <span data-ttu-id="97bdd-103"><a name="GETENUMVALUEBYNAME">ER-funktionen GETENUMVALUEBYNAME</a></span><span class="sxs-lookup"><span data-stu-id="97bdd-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97bdd-104">Funktionen `GETENUMVALUEBYNAME` søger efter en bestemt *Fasttekst*-værdi i den angivne fasttekstdatakilde ved hjælp af det fasttekstnavn, der er angivet som en *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="97bdd-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="97bdd-105">Hvis *Fasttekst*-værdien findes, returnerer funktionen den.</span><span class="sxs-lookup"><span data-stu-id="97bdd-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="97bdd-106">Ellers returnerer funktionen **nul** i fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="97bdd-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bdd-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="97bdd-107">Syntax</span></span>

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="97bdd-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="97bdd-108">Arguments</span></span>

<span data-ttu-id="97bdd-109">`enumeration data source path`: *Fasttekst*</span><span class="sxs-lookup"><span data-stu-id="97bdd-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="97bdd-110">Den gyldige sti til en datakilde for en af følgende fastteksttyper:</span><span class="sxs-lookup"><span data-stu-id="97bdd-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="97bdd-111">Modelfasttekst til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="97bdd-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="97bdd-112">ER-formatfasttekst</span><span class="sxs-lookup"><span data-stu-id="97bdd-112">ER format enumeration</span></span>
- <span data-ttu-id="97bdd-113">Microsoft Dynamics 365 Finance-fasttekst</span><span class="sxs-lookup"><span data-stu-id="97bdd-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="97bdd-114">`enumeration value text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="97bdd-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="97bdd-115">En strengværdi, der repræsenterer navnet på en enkelt fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="97bdd-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="97bdd-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="97bdd-116">Return values</span></span>

<span data-ttu-id="97bdd-117">*Enum* kan være nul</span><span class="sxs-lookup"><span data-stu-id="97bdd-117">Nullable *Enum*</span></span>

<span data-ttu-id="97bdd-118">Den returnerede fasttekstværdi.</span><span class="sxs-lookup"><span data-stu-id="97bdd-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97bdd-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="97bdd-119">Usage notes</span></span>

<span data-ttu-id="97bdd-120">Der udløses ingen undtagelse, hvis der ikke findes en *Enum*-værdi ved hjælp af navnet på den fasttekstværdi, der er angivet som en *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="97bdd-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="97bdd-121">Eksempel</span><span class="sxs-lookup"><span data-stu-id="97bdd-121">Example</span></span>

<span data-ttu-id="97bdd-122">I følgende illustration introduceres fastteksten **ReportDirection** i en datamodel.</span><span class="sxs-lookup"><span data-stu-id="97bdd-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="97bdd-123">Bemærk, at der er defineret etiketter for fasttekstværdierne.</span><span class="sxs-lookup"><span data-stu-id="97bdd-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="97bdd-124">Følgende illustration viser disse detaljer:</span><span class="sxs-lookup"><span data-stu-id="97bdd-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="97bdd-125">Datakilden **$Retning** er konfigureret i en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="97bdd-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="97bdd-126">Denne datakilde konfigureres på basis af modelfastteksten **RapportRetning**.</span><span class="sxs-lookup"><span data-stu-id="97bdd-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="97bdd-127">Udtrykket `$IsArrivals` er designet til at bruge den modelfasttekstbaserede datakilde **$Retning** som parameter for denne funktion.</span><span class="sxs-lookup"><span data-stu-id="97bdd-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="97bdd-128">Værdien af denne sammenligning er **SAND**.</span><span class="sxs-lookup"><span data-stu-id="97bdd-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="97bdd-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="97bdd-129">Additional resources</span></span>

[<span data-ttu-id="97bdd-130">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="97bdd-130">Text functions</span></span>](er-functions-category-text.md)
