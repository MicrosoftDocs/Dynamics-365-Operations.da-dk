---
title: ER-funktionen DATETODATETIME
description: Dette emne indeholder oplysninger om, hvordan funktionen DATETODATETIME til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5ad1d304f0914a9ddbca951cdb7419dbcc1f46
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682433"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="5020f-103">ER-funktionen DATETODATETIME</span><span class="sxs-lookup"><span data-stu-id="5020f-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5020f-104">Funktionen `DATETODATETIME` returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given datoværdi til en dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="5020f-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="5020f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5020f-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="5020f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5020f-106">Arguments</span></span>

<span data-ttu-id="5020f-107">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="5020f-107">`date`: *Date*</span></span>

<span data-ttu-id="5020f-108">En datoværdi, der repræsenterer den dato, der skal konverteres.</span><span class="sxs-lookup"><span data-stu-id="5020f-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="5020f-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="5020f-109">Return values</span></span>

<span data-ttu-id="5020f-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="5020f-110">*DateTime*</span></span>

<span data-ttu-id="5020f-111">Den returnerede dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="5020f-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="5020f-112">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="5020f-112">Example 1</span></span>

<span data-ttu-id="5020f-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returnerer datoen for den aktuelle Microsoft Dynamics 365 Finance-session, 24. december 2015, som **24/12/2015 12:00:00**.</span><span class="sxs-lookup"><span data-stu-id="5020f-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="5020f-114">I dette eksempel er **CompInfo** en datakilde til elektronisk rapportering (ER) af typen **Finance and Operations/tabel** og refererer til tabellen CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="5020f-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="5020f-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="5020f-115">Example 2</span></span>

<span data-ttu-id="5020f-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returnerer dato-/klokkeslætsværdien **12/11/2019 12:00:00**.</span><span class="sxs-lookup"><span data-stu-id="5020f-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5020f-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5020f-117">Additional resources</span></span>

[<span data-ttu-id="5020f-118">Dato- og klokkeslætsfunktioner</span><span class="sxs-lookup"><span data-stu-id="5020f-118">Date and time functions</span></span>](er-functions-category-datetime.md)
