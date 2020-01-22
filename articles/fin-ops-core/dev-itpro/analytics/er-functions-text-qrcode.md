---
title: ER-funktionen QRCODE
description: Dette emne indeholder oplysninger om, hvordan funktionen QRCODE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916746"
---
# <span data-ttu-id="0a958-103"><a name="QRCODE">ER-funktionen QRCODE</a></span><span class="sxs-lookup"><span data-stu-id="0a958-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a958-104">Funktionen `QRCODE` returnerer en *Container*-værdi, som viser QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format.</span><span class="sxs-lookup"><span data-stu-id="0a958-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a958-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0a958-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="0a958-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0a958-106">Arguments</span></span>

<span data-ttu-id="0a958-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="0a958-107">`text`: *String*</span></span>

<span data-ttu-id="0a958-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="0a958-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0a958-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="0a958-109">Return values</span></span>

<span data-ttu-id="0a958-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="0a958-110">*Container*</span></span>

<span data-ttu-id="0a958-111">Den resulterende binære strøm.</span><span class="sxs-lookup"><span data-stu-id="0a958-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="0a958-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0a958-112">Example</span></span>

<span data-ttu-id="0a958-113">Du kan konfigurere et format til elektronisk rapportering (ER) til at generere et udgående dokument i Microsoft Office-format (Excel-projektmapper eller Word-dokumenter) ved hjælp af en foruddefineret skabelon.</span><span class="sxs-lookup"><span data-stu-id="0a958-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="0a958-114">Denne skabelon kan indeholde et **Billed**-objekt (Excel-projektmappe) eller et **Indholdskontrolelement (Picture Content Control)** (Word-dokument) som pladsholder for et QR-kodebillede.</span><span class="sxs-lookup"><span data-stu-id="0a958-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="0a958-115">Du skal føje et **Celle**-element, der skal bruges til at udfylde denne pladsholder, til det konfigurerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="0a958-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="0a958-116">Hvis du vil angive, hvilke oplysninger der skal gemmes i en QR-kode, skal du definere en binding for dette **Celle**-element.</span><span class="sxs-lookup"><span data-stu-id="0a958-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="0a958-117">For eksempel kan du konfigurere en sådan binding til at indeholde følgende udtryk:</span><span class="sxs-lookup"><span data-stu-id="0a958-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="0a958-118">Når du kører det konfigurerede ER-format, vil tekstværdien i feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels** blive brugt til at generere et QR-kodebillede.</span><span class="sxs-lookup"><span data-stu-id="0a958-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="0a958-119">Dette billede erstatter en QR-kodebilledepladshol.der i dokumentskabelonen og bruges til at generere et udgående dokument.</span><span class="sxs-lookup"><span data-stu-id="0a958-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="0a958-120">Når dette billede af det genererede dokument scannes, returneres den tekst, der blev hentet fra feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="0a958-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="0a958-121">Du kan finde flere oplysninger under [Integrer billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="0a958-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a958-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0a958-122">Additional resources</span></span>

[<span data-ttu-id="0a958-123">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="0a958-123">Text functions</span></span>](er-functions-category-text.md)
