---
title: ER-funktionen ALLITEMS
description: Dette emne indeholder oplysninger om, hvordan funktionen ALLITEMS til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 47113d52e15d3d61f00b3c54229e286eb0f1a8d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745387"
---
# <a name="allitems-er-function"></a><span data-ttu-id="694d7-103">ER-funktionen ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="694d7-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="694d7-104">Funktionen `ALLITEMS` kører som en markering i hukommelsen og returnerer en ny flad *Postliste*-værdi som en liste over poster, der repræsenterer alle elementer, der svarer til den angivne sti.</span><span class="sxs-lookup"><span data-stu-id="694d7-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="694d7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="694d7-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="694d7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="694d7-106">Arguments</span></span>

<span data-ttu-id="694d7-107">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="694d7-107">`path`: *Record list*</span></span>

<span data-ttu-id="694d7-108">Den gyldige sti til en datakilde af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="694d7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="694d7-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="694d7-109">Return values</span></span>

<span data-ttu-id="694d7-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="694d7-110">*Record list*</span></span>

<span data-ttu-id="694d7-111">Den resulterende liste over poster.</span><span class="sxs-lookup"><span data-stu-id="694d7-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="694d7-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="694d7-112">Usage notes</span></span>

<span data-ttu-id="694d7-113">Stien skal defineres som en gyldig datakildesti for et datakildeelement af datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="694d7-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="694d7-114">Dataelementer som strengen til stien og datoen bør udløse en fejl i designfasen i udtryksgenerator til den elektroniske rapportering (ER).</span><span class="sxs-lookup"><span data-stu-id="694d7-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="694d7-115">Vi anbefaler ikke, at du bruger denne funktion til transaktionsdatakilder, der kan indeholde en stor mængde data.</span><span class="sxs-lookup"><span data-stu-id="694d7-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="694d7-116">Overvej i stedet at bruge funktionen [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="694d7-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="694d7-117">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="694d7-117">Example 1</span></span>

<span data-ttu-id="694d7-118">Hvis du indtaster `SPLIT("abcdef" , 2)` som datakilde **DS**, returnerer `COUNT( ALLITEMS (DS))` udtrykket **3**.</span><span class="sxs-lookup"><span data-stu-id="694d7-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="694d7-119">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="694d7-119">Example 2</span></span>

<span data-ttu-id="694d7-120">Hvis du indtaster **Vend** som datakilde for datatypen *Postliste*, der refererer til programtabellen VendTable, returnerer udtrykket `ALLITEMS (Vend.'<Relations'.ContactPerson)` en flad liste over poster, der har tabelstrukturen **Kontaktperson**, og som indeholder alle kontaktpersoner, der kan tilgås ved hjælp af relationen **ContactPerson.ContactForParty == VendTable.Party**, og som er tilgængelig for alle leverandører fra den refererede leverandørtabel.</span><span class="sxs-lookup"><span data-stu-id="694d7-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="694d7-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="694d7-121">Additional resources</span></span>

[<span data-ttu-id="694d7-122">Listefunktioner</span><span class="sxs-lookup"><span data-stu-id="694d7-122">List functions</span></span>](er-functions-category-list.md)
