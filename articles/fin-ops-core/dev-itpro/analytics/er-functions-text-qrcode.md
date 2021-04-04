---
title: ER-funktionen QRCODE
description: Dette emne indeholder oplysninger om, hvordan funktionen QRCODE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562655"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="af380-103">ER-funktionen QRCODE</span><span class="sxs-lookup"><span data-stu-id="af380-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af380-104">Funktionen `QRCODE` returnerer en *Container*-værdi, som viser QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format.</span><span class="sxs-lookup"><span data-stu-id="af380-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="af380-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="af380-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="af380-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="af380-106">Arguments</span></span>

<span data-ttu-id="af380-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="af380-107">`text`: *String*</span></span>

<span data-ttu-id="af380-108">En *Streng*-værdi, der repræsenterer den oprindelige tekst.</span><span class="sxs-lookup"><span data-stu-id="af380-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="af380-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="af380-109">Return values</span></span>

<span data-ttu-id="af380-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="af380-110">*Container*</span></span>

<span data-ttu-id="af380-111">Den resulterende binære strøm.</span><span class="sxs-lookup"><span data-stu-id="af380-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="af380-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="af380-112">Example</span></span>

<span data-ttu-id="af380-113">Du kan konfigurere et format til elektronisk rapportering (ER) til at generere et udgående dokument i Microsoft Office-format (Excel-projektmapper eller Word-dokumenter) ved hjælp af en foruddefineret skabelon.</span><span class="sxs-lookup"><span data-stu-id="af380-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="af380-114">Denne skabelon kan indeholde et **Billed**-objekt (Excel-projektmappe) eller et **Indholdskontrolelement (Picture Content Control)** (Word-dokument) som pladsholder for et QR-kodebillede.</span><span class="sxs-lookup"><span data-stu-id="af380-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="af380-115">Du skal føje et **Celle**-element, der skal bruges til at udfylde denne pladsholder, til det konfigurerede ER-format.</span><span class="sxs-lookup"><span data-stu-id="af380-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="af380-116">Hvis du vil angive, hvilke oplysninger der skal gemmes i en QR-kode, skal du definere en binding for dette **Celle**-element.</span><span class="sxs-lookup"><span data-stu-id="af380-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="af380-117">For eksempel kan du konfigurere en sådan binding til at indeholde følgende udtryk:</span><span class="sxs-lookup"><span data-stu-id="af380-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="af380-118">Når du kører det konfigurerede ER-format, vil tekstværdien i feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels** blive brugt til at generere et QR-kodebillede.</span><span class="sxs-lookup"><span data-stu-id="af380-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="af380-119">Dette billede erstatter en QR-kodebilledepladshol.der i dokumentskabelonen og bruges til at generere et udgående dokument.</span><span class="sxs-lookup"><span data-stu-id="af380-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="af380-120">Når dette billede af det genererede dokument scannes, returneres den tekst, der blev hentet fra feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels**.</span><span class="sxs-lookup"><span data-stu-id="af380-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="af380-121">Du kan finde flere oplysninger under [Integrer billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="af380-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af380-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="af380-122">Additional resources</span></span>

[<span data-ttu-id="af380-123">Tekstfunktioner</span><span class="sxs-lookup"><span data-stu-id="af380-123">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]