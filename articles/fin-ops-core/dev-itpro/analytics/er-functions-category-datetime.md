---
title: Liste over ER-funktioner i kategorien Dato og klokkeslæt
description: Dette emne indeholder oplysninger om funktionerne dato og klokkeslæt, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 52b84f9b611f703fd390eca58c1364a4992bece2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561704"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="79b36-103">Liste over ER-funktioner i kategorien Dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="79b36-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79b36-104">Funktionerne dato og klokkeslæt for elektronisk rapportering (ER) kan bruges til at udtrække oplysninger fra dato- og klokkeslætsværdier og til at udføre handlinger på dem.</span><span class="sxs-lookup"><span data-stu-id="79b36-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="79b36-105">Dette emne indeholder en oversigt over disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="79b36-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="79b36-106">Liste med understøttede funktioner</span><span class="sxs-lookup"><span data-stu-id="79b36-106">List of supported functions</span></span>

| <span data-ttu-id="79b36-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="79b36-107">Function</span></span> | <span data-ttu-id="79b36-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="79b36-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="79b36-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="79b36-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="79b36-110">Denne funktion returnerer en værdi med *DatoKlokkeslæt*, der er det angivne antal dage før eller efter en angivet startdato.</span><span class="sxs-lookup"><span data-stu-id="79b36-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="79b36-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="79b36-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="79b36-112">Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet kultur.</span><span class="sxs-lookup"><span data-stu-id="79b36-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="79b36-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="79b36-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="79b36-114">Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer en given dato-/klokkeslætsværdi som tekst i det angivne format og i en eventuelt angivet kultur.</span><span class="sxs-lookup"><span data-stu-id="79b36-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="79b36-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="79b36-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="79b36-116">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="79b36-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="79b36-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="79b36-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="79b36-118">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean \[time\]GMT).</span><span class="sxs-lookup"><span data-stu-id="79b36-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="79b36-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="79b36-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="79b36-120">Denne funktion returnerer en værdi i form af en *Dato*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en datoværdi.</span><span class="sxs-lookup"><span data-stu-id="79b36-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="79b36-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="79b36-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="79b36-122">Denne funktion returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="79b36-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="79b36-123">Dage</span><span class="sxs-lookup"><span data-stu-id="79b36-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="79b36-124">Denne funktion returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem to angivne datoer.</span><span class="sxs-lookup"><span data-stu-id="79b36-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="79b36-125">Now</span><span class="sxs-lookup"><span data-stu-id="79b36-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="79b36-126">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer den aktuelle dato og klokkeslæt for den aktuelle programserver.</span><span class="sxs-lookup"><span data-stu-id="79b36-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="79b36-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="79b36-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="79b36-128">Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="79b36-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="79b36-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="79b36-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="79b36-130">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato-/klokkeslætsværdien **nul** (1. januar 1900) i UTC-tid (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="79b36-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="79b36-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="79b36-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="79b36-132">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato og klokkeslæt for den aktuelle programsession.</span><span class="sxs-lookup"><span data-stu-id="79b36-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="79b36-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="79b36-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="79b36-134">Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programsession.</span><span class="sxs-lookup"><span data-stu-id="79b36-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="79b36-135">I dag</span><span class="sxs-lookup"><span data-stu-id="79b36-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="79b36-136">Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programserver.</span><span class="sxs-lookup"><span data-stu-id="79b36-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="79b36-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="79b36-137">Additional resources</span></span>

[<span data-ttu-id="79b36-138">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="79b36-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="79b36-139">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="79b36-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="79b36-140">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="79b36-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]