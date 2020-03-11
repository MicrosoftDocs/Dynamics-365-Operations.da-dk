---
title: ER-funktionen FORMAT
description: Dette emne indeholder oplysninger om, hvordan funktionen FORMAT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 7ae688ef6b24f8d90c0354c8c6449adba1588bfa
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041072"
---
# <span data-ttu-id="13f6f-103"><a name="FORMAT">ER-funktionen FORMAT</a></span><span class="sxs-lookup"><span data-stu-id="13f6f-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13f6f-104">Funktionen `FORMAT` returnerer den angivne streng som en *Streng*-værdi, efter den er blevet formateret ved at erstatte alle forekomster af **%N** med det *N*'te argument.</span><span class="sxs-lookup"><span data-stu-id="13f6f-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f6f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="13f6f-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="13f6f-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="13f6f-106">Arguments</span></span>

<span data-ttu-id="13f6f-107">`string`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13f6f-107">`string`: *String*</span></span>

<span data-ttu-id="13f6f-108">En reference til en datakilde af datatypen *Streng*, som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="13f6f-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="13f6f-109">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="13f6f-109">This argument is required.</span></span>

<span data-ttu-id="13f6f-110">`argument 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13f6f-110">`argument 1`: *String*</span></span>

<span data-ttu-id="13f6f-111">Det første argument, der bruges til at erstatte forekomster af **%1**.</span><span class="sxs-lookup"><span data-stu-id="13f6f-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="13f6f-112">Dette argument skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="13f6f-112">This argument is required.</span></span>

<span data-ttu-id="13f6f-113">`argument N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="13f6f-113">`argument N`: *String*</span></span>

<span data-ttu-id="13f6f-114">Det *N*'te argument, der bruges til at erstatte forekomster af **%2**, **%3** osv.</span><span class="sxs-lookup"><span data-stu-id="13f6f-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="13f6f-115">Disse yderligere argumenter er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="13f6f-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="13f6f-116">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="13f6f-116">Return values</span></span>

<span data-ttu-id="13f6f-117">*Streng*</span><span class="sxs-lookup"><span data-stu-id="13f6f-117">*String*</span></span>

<span data-ttu-id="13f6f-118">Den returnerede tekstværdi.</span><span class="sxs-lookup"><span data-stu-id="13f6f-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13f6f-119">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="13f6f-119">Usage notes</span></span>

<span data-ttu-id="13f6f-120">Hvis et argument ikke er angivet for en parameter, bliver parameteren returneret som **"%N"** i strengen.</span><span class="sxs-lookup"><span data-stu-id="13f6f-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="13f6f-121">For værdier af typen *Reel* er standardstrengkonverteringen begrænset til to decimaler.</span><span class="sxs-lookup"><span data-stu-id="13f6f-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="13f6f-122">Eksempel</span><span class="sxs-lookup"><span data-stu-id="13f6f-122">Example</span></span>

<span data-ttu-id="13f6f-123">I følgende illustration returnerer datakilden **PaymentModel** en liste over kundeposter ved hjælp af komponenten **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="13f6f-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="13f6f-124">Den returnerer værdien for behandlingsdato ved hjælp af feltet **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="13f6f-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="13f6f-125">Datakilden **PaymentModel** i det elektroniske rapporteringsformat (ER-format) er designet til at generere en elektronisk fil til de valgte debitorer og er valgt som en datakilde, og den styrer procesforløbet.</span><span class="sxs-lookup"><span data-stu-id="13f6f-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="13f6f-126">En undtagelse opstår for at give brugeren besked, hvis en bestemt kunde er spærret for den dato, hvor rapporten behandles.</span><span class="sxs-lookup"><span data-stu-id="13f6f-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="13f6f-127">Den formel, der er udviklet til denne type behandlingskontrol, kan bruge følgende ressourcer:</span><span class="sxs-lookup"><span data-stu-id="13f6f-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="13f6f-128">Etiket SYS70894, som har følgende tekst:</span><span class="sxs-lookup"><span data-stu-id="13f6f-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="13f6f-129">**For det amerikanske sprog:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="13f6f-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="13f6f-130">**For det danske sprog:** "Intet at udskrive"</span><span class="sxs-lookup"><span data-stu-id="13f6f-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="13f6f-131">Etiket SYS18389, som har følgende tekst:</span><span class="sxs-lookup"><span data-stu-id="13f6f-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="13f6f-132">**For sproget EN-US:** "Kunde %1 er spærret for %2."</span><span class="sxs-lookup"><span data-stu-id="13f6f-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="13f6f-133">**For det tyske sprog:** "Debitor '%1' er spærret for %2."</span><span class="sxs-lookup"><span data-stu-id="13f6f-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="13f6f-134">Her er det udtryk, der kan designes.</span><span class="sxs-lookup"><span data-stu-id="13f6f-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="13f6f-135">Hvis en rapport behandles for debitoren **Litware Retail** den 17. december 2015 i den amerikanske kultur, **EN-US**, og på det amerikanske sprog, **EN-US**, returnerer denne formel følgende tekst, som kan præsenteres for slutbrugeren som en undtagelsesmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="13f6f-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="13f6f-136">*Intet at udskrive. Customer Litware Retail er stoppet for 17/12/2015.*</span><span class="sxs-lookup"><span data-stu-id="13f6f-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="13f6f-137">Hvis den samme rapport behandles den 17. december 2015 for kunden **Litware Retail** med dansk kultur **DA** og sproget **DA**, returnerer formlen følgende tekst, der bruger et andet datoformat:</span><span class="sxs-lookup"><span data-stu-id="13f6f-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="13f6f-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="13f6f-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="13f6f-139">Følgende syntaks er anvendt i ER-formler for etiketter:</span><span class="sxs-lookup"><span data-stu-id="13f6f-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="13f6f-140">**For etiketter fra ressourcer i Microsoft Dynamics 365 Finance-app:** **\@X**, hvor **X** er etiket-id'et i applikationsobjekttræet (AOT)</span><span class="sxs-lookup"><span data-stu-id="13f6f-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="13f6f-141">**For etiketter, der er placeret i ER-konfigurationer:** **@GER_LABEL:X"**, hvor **X** er etiket-ID'et i ER-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="13f6f-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13f6f-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="13f6f-142">Additional resources</span></span>

[<span data-ttu-id="13f6f-143">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="13f6f-143">Text functions</span></span>](er-functions-category-text.md)
