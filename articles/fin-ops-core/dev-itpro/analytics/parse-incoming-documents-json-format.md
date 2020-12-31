---
title: Analysere indgående dokumenter i JSON-format
description: Dette emne forklarer, hvordan du opretter ER-formater (Electronic reporting) til at parse indgående dokumenter i JSON-format (JavaScript Object Notation).
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b4ed81bb5527ea8e02caaa1262a57960dd7cdf29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685757"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="d5655-103">Analysere indgående dokumenter i JSON-format</span><span class="sxs-lookup"><span data-stu-id="d5655-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d5655-104">Du kan designe ER-formater (Electronic reporting) til at parse indgående elektroniske dokumenter, der repræsenterer data i et tekstformat, der er baseret på JavaScript (med andre ord filer i \[JSON\]-formatet (JavaScript Object Notation)).</span><span class="sxs-lookup"><span data-stu-id="d5655-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="d5655-105">Hvis du vil vide mere om denne funktion, skal du hente filerne i følgende tabel og derefter afspille ER-konfigurationen Opret et format fra en ekstern JSON-filopgaveguide.</span><span class="sxs-lookup"><span data-stu-id="d5655-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="d5655-106">I denne opgaveguide viser, hvordan et ER-format kan bruges til at analysere en indgående JSON-fil for at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="d5655-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="d5655-107">Stilling</span><span class="sxs-lookup"><span data-stu-id="d5655-107">Title</span></span>                                  | <span data-ttu-id="d5655-108">Filnavn</span><span class="sxs-lookup"><span data-stu-id="d5655-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="d5655-109">Konfiguration af ER-format</span><span class="sxs-lookup"><span data-stu-id="d5655-109">ER format configuration</span></span>                | [<span data-ttu-id="d5655-110">Format til import af kreditorers trans_JSON.xml</span><span class="sxs-lookup"><span data-stu-id="d5655-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="d5655-111">Eksempel på indgående fil i .csv-format</span><span class="sxs-lookup"><span data-stu-id="d5655-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="d5655-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="d5655-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="d5655-113">Behov</span><span class="sxs-lookup"><span data-stu-id="d5655-113">Requirements</span></span>

<span data-ttu-id="d5655-114">Før du fuldfører ER-konfigurationen Opret et format for at importere data fra en ekstern JSON-filopgaveguide, skal følgende krav opfyldes:</span><span class="sxs-lookup"><span data-stu-id="d5655-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="d5655-115">Overordnede elementer i JSON-filen kan kun være objektelementer.</span><span class="sxs-lookup"><span data-stu-id="d5655-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="d5655-116">Indlejrede elementer for et objekt skal være egenskabselementer, så der oprettes en gyldig JSON-struktur.</span><span class="sxs-lookup"><span data-stu-id="d5655-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="d5655-117">JSON-arrays kan kun være indlejrede elementer for et objekts egenskabselementer.</span><span class="sxs-lookup"><span data-stu-id="d5655-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="d5655-118">JSON-arrays kan kun indeholde JSON-objekter.</span><span class="sxs-lookup"><span data-stu-id="d5655-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="d5655-119">De må ikke indeholde direkte strengværdier/numeriske værdier og indlejrede arrays.</span><span class="sxs-lookup"><span data-stu-id="d5655-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="d5655-120">Elementerne i disse arrays parses i den rækkefølge, de er angivet i i formatet.</span><span class="sxs-lookup"><span data-stu-id="d5655-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="d5655-121">Indstillingerne for multiplicitet på alle JSON-objekter vil blive taget i betragtning.</span><span class="sxs-lookup"><span data-stu-id="d5655-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="d5655-122">Derudover skal du fuldføre opgaveguiden [Opret de krævede konfigurationer til import af data fra en ekstern fil](tasks/er-required-configurations-import-data.md), hvis du ikke allerede har fuldført den.</span><span class="sxs-lookup"><span data-stu-id="d5655-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="d5655-123">Hent følgende fil for at fuldføre opgaveguiden.</span><span class="sxs-lookup"><span data-stu-id="d5655-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="d5655-124">Stilling</span><span class="sxs-lookup"><span data-stu-id="d5655-124">Title</span></span>                  | <span data-ttu-id="d5655-125">Filnavn</span><span class="sxs-lookup"><span data-stu-id="d5655-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="d5655-126">ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d5655-126">ER model configuration</span></span> | [<span data-ttu-id="d5655-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="d5655-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
