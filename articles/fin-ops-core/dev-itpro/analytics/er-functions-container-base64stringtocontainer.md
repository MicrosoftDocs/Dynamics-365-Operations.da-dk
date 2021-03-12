---
title: ER-funktionen Base64StringToContainer
description: Dette emne indeholder oplysninger om, hvordan funktionen Base64StringToContainer til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739065"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="904ee-103">ER-funktionen Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="904ee-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="904ee-104">Denne `BASE64STRINGTOCONTAINER`-[funktion](er-formula-language.md#functions) konverterer det angivne input af typen *Streng* til et dataelement af typen *[Container](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="904ee-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="904ee-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="904ee-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="904ee-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="904ee-106">Arguments</span></span>

<span data-ttu-id="904ee-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="904ee-107">`input`: *String*</span></span>

<span data-ttu-id="904ee-108">Den gyldige sti til en datakilde af typen *Streng*.</span><span class="sxs-lookup"><span data-stu-id="904ee-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="904ee-109">Returnerede værdier</span><span class="sxs-lookup"><span data-stu-id="904ee-109">Return values</span></span>

<span data-ttu-id="904ee-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="904ee-110">*Container*</span></span>

<span data-ttu-id="904ee-111">Den binære værdi, der bliver resultatet, i binært BLOB-format (binært stort objekt).</span><span class="sxs-lookup"><span data-stu-id="904ee-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="904ee-112">Bemærkninger til brug</span><span class="sxs-lookup"><span data-stu-id="904ee-112">Usage notes</span></span>

<span data-ttu-id="904ee-113">Undtagelsen "Parameter er ikke gyldig" vises, hvis inputstrengen ikke indeholder en korrekt Base64-gruppe af binær til tekst-kodningsskemaer.</span><span class="sxs-lookup"><span data-stu-id="904ee-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="904ee-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="904ee-114">Example</span></span>

<span data-ttu-id="904ee-115">Du definerer følgende datakilder i din modeltilknytning:</span><span class="sxs-lookup"><span data-stu-id="904ee-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="904ee-116">Roddatakilden **DocuTypeGroupEnum** for typen *Dynamics 365 for Operations / fasttekst*, der henviser til **DocuTypeGroup**-programfasttekst</span><span class="sxs-lookup"><span data-stu-id="904ee-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="904ee-117">Roddatakilden **Kunde** af typen *Dynamics 365 for Operations / Tabelposter*, som refererer til programtabellen **CustTable**</span><span class="sxs-lookup"><span data-stu-id="904ee-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="904ee-118">Datakilden **\#Medie** af typen *Beregnet felt*, der konfigureres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="904ee-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="904ee-119">Den er tilføjet som en underordnet datakilde for datakilden **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="904ee-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="904ee-120">Den indeholder udtrykket `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="904ee-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="904ee-121">Datakilden **\#MediaAsBase64String** af typen *Beregnet felt*, der konfigureres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="904ee-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="904ee-122">Den er tilføjet som en underordnet datakilde for datakilden **Kunde.'\#Medie'**.</span><span class="sxs-lookup"><span data-stu-id="904ee-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="904ee-123">Den indeholder udtrykket `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="904ee-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="904ee-124">Datakilden **\#BlobFomBase64** af typen *Beregnet felt*, der konfigureres på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="904ee-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="904ee-125">Den er tilføjet som en underordnet datakilde for datakilden **Kunde.'\#Medie'**.</span><span class="sxs-lookup"><span data-stu-id="904ee-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="904ee-126">Den indeholder udtrykket `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="904ee-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="904ee-127">I dette eksempel koder datakilden **\#MediaAsBase64String** det binære indhold af den aktuelle medietilknytning som tekst, der repræsenterer en Base64-gruppe af binær til tekst-kodningsskemaer.</span><span class="sxs-lookup"><span data-stu-id="904ee-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="904ee-128">Datakilden **\#BlobFomBase64** afkoder Base64-strengen og returnerer en binær værdi i BLOB-format.</span><span class="sxs-lookup"><span data-stu-id="904ee-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Eksempeldatakilder på designersiden for ER-modeltilknytning](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="904ee-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="904ee-130">Additional resources</span></span>

[<span data-ttu-id="904ee-131">Containerfunktioner</span><span class="sxs-lookup"><span data-stu-id="904ee-131">Container functions</span></span>](er-functions-category-container.md)
