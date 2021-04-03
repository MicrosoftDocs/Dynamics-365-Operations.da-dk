---
title: Liste over ER-funktioner af kategorien typekonvertering
description: Dette emne indeholder oplysninger om de konverteringsfunktioner, der understøttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561512"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="9adb9-103">Liste over ER-funktioner af kategorien typekonvertering</span><span class="sxs-lookup"><span data-stu-id="9adb9-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9adb9-104">Typekonverteringsfunktioner til elektronisk rapportering (ER) kan bruges til at konvertere værdier mellem typer.</span><span class="sxs-lookup"><span data-stu-id="9adb9-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="9adb9-105">Dette emne indeholder en oversigt over disse funktioner.</span><span class="sxs-lookup"><span data-stu-id="9adb9-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="9adb9-106">Typekonverteringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="9adb9-106">Type conversion functions</span></span>

| <span data-ttu-id="9adb9-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb9-107">Function</span></span> | <span data-ttu-id="9adb9-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9adb9-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9adb9-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="9adb9-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="9adb9-110">Denne funktion returnerer en *Int64*-værdi, der repræsenterer den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="9adb9-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9adb9-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="9adb9-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="9adb9-112">Denne funktion returnerer en *Int*-værdi, der repræsenterer den angivne streng.</span><span class="sxs-lookup"><span data-stu-id="9adb9-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9adb9-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="9adb9-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="9adb9-114">Denne funktion returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="9adb9-115">Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning.</span><span class="sxs-lookup"><span data-stu-id="9adb9-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="9adb9-116">Værdi</span><span class="sxs-lookup"><span data-stu-id="9adb9-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="9adb9-117">Denne funktion returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="9adb9-118">Typekonverteringsfunktioner i containerkategorien</span><span class="sxs-lookup"><span data-stu-id="9adb9-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="9adb9-119">I følgende tabel beskrives typekonverteringsfunktionerne i kategorien [container](er-functions-category-container.md).</span><span class="sxs-lookup"><span data-stu-id="9adb9-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="9adb9-120">Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb9-120">Function</span></span> | <span data-ttu-id="9adb9-121">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9adb9-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9adb9-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="9adb9-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="9adb9-123">Denne funktion konverterer det angivne input af typen *Streng* til et dataelement af typen *Container*.</span><span class="sxs-lookup"><span data-stu-id="9adb9-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="9adb9-124">Typekonverteringsfunktioner i kategorien dato og klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="9adb9-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="9adb9-125">I følgende tabel beskrives typekonverteringsfunktionerne i [kategorien dato og klokkeslæt](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="9adb9-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="9adb9-126">Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb9-126">Function</span></span> | <span data-ttu-id="9adb9-127">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9adb9-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9adb9-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="9adb9-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="9adb9-129">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given *Streng*-værdi i det angivne format og i en eventuelt angivet kultur til en dato-/klokkeslætsværdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="9adb9-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="9adb9-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="9adb9-131">Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given *Dato*-værdi til en dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="9adb9-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="9adb9-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="9adb9-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="9adb9-133">Denne funktion returnerer en værdi i form af en *Dato*, som er konverteret fra en given *Streng*-værdi i det angivne format og i en eventuelt angivet kultur til en datoværdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="9adb9-134">Typekonverteringsfunktioner i listekategorien</span><span class="sxs-lookup"><span data-stu-id="9adb9-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="9adb9-135">I følgende tabel beskrives typekonverteringsfunktionerne i [listekategorien](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="9adb9-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="9adb9-136">Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb9-136">Function</span></span> | <span data-ttu-id="9adb9-137">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9adb9-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9adb9-138">Liste</span><span class="sxs-lookup"><span data-stu-id="9adb9-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="9adb9-139">Denne funktion returnerer en ny *Postliste*-værdi som en ny liste, der er oprettet på grundlag af de angivne argumenter af typen *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="9adb9-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="9adb9-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="9adb9-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="9adb9-141">Denne funktion returnerer en *Postliste*-værdi, der er oprettet på baggrund af strukturen af et angivet argument af typen *Optælling* eller *Container (post)*.</span><span class="sxs-lookup"><span data-stu-id="9adb9-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="9adb9-142">Opdel</span><span class="sxs-lookup"><span data-stu-id="9adb9-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="9adb9-143">Denne funktion opdeler den angivne *Streng*-værdi i understrenge og returnerer resultatet som en ny *Postliste*-værdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="9adb9-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="9adb9-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="9adb9-145">Denne funktion returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne *Postliste*-værdi.</span><span class="sxs-lookup"><span data-stu-id="9adb9-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="9adb9-146">Værdierne kan være adskilt af et angivet separatortegn.</span><span class="sxs-lookup"><span data-stu-id="9adb9-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="9adb9-147">Typekonverteringsfunktioner i tekstkategorien</span><span class="sxs-lookup"><span data-stu-id="9adb9-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="9adb9-148">I følgende tabel beskrives typekonverteringsfunktionerne i [tekstkategorien](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="9adb9-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="9adb9-149">Funktion</span><span class="sxs-lookup"><span data-stu-id="9adb9-149">Function</span></span> | <span data-ttu-id="9adb9-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9adb9-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9adb9-151">Char</span><span class="sxs-lookup"><span data-stu-id="9adb9-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="9adb9-152">Denne funktion returnerer en *Streng*-værdi, som repræsenterer et enkelt tegn, der refereres til af det angivne Unicode-nummer.</span><span class="sxs-lookup"><span data-stu-id="9adb9-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="9adb9-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="9adb9-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="9adb9-154">Denne funktion konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*.</span><span class="sxs-lookup"><span data-stu-id="9adb9-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="9adb9-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="9adb9-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="9adb9-156">Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne tal i det angivne format og i en eventuelt angivet kultur.</span><span class="sxs-lookup"><span data-stu-id="9adb9-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="9adb9-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="9adb9-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="9adb9-158">Denne funktion returnerer en *Container*-værdi, som præsenterer QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format.</span><span class="sxs-lookup"><span data-stu-id="9adb9-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="9adb9-159">Tekst</span><span class="sxs-lookup"><span data-stu-id="9adb9-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="9adb9-160">Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne tal, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst.</span><span class="sxs-lookup"><span data-stu-id="9adb9-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9adb9-161">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9adb9-161">Additional resources</span></span>

[<span data-ttu-id="9adb9-162">Oversigt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="9adb9-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9adb9-163">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="9adb9-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="9adb9-164">Formelsprog i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="9adb9-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]