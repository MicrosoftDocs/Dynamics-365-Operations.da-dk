---
title: Analysere indgående dokumenter i Excel-format
description: Dette emne indeholder oplysninger om design af elektronisk rapporteringsformater (ER) for at analysere indhold af indgående Microsoft Excel-filer.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755174"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="c2a01-103">Analysere indgående dokumenter i Excel-format</span><span class="sxs-lookup"><span data-stu-id="c2a01-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c2a01-104">Du kan designe ER-formater for at analysere indgående Microsoft Excel-filer, der repræsenterer data i Microsoft Excel-projektmapper (filer i XLSX format).</span><span class="sxs-lookup"><span data-stu-id="c2a01-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="c2a01-105">Derefter kan du bruge indholdet fra disse filer til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="c2a01-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="c2a01-106">Dette er nyttigt, hvis du:</span><span class="sxs-lookup"><span data-stu-id="c2a01-106">This is useful if you:</span></span>

- <span data-ttu-id="c2a01-107">Designer en ny model og formaterer og vil teste den under kørsel.</span><span class="sxs-lookup"><span data-stu-id="c2a01-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="c2a01-108">I så fald simulerer Excel faktiske programdata.</span><span class="sxs-lookup"><span data-stu-id="c2a01-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="c2a01-109">Administrer andre data end dit program i Excel og ønsker at importere dataene for at sende en bestemt rapport.</span><span class="sxs-lookup"><span data-stu-id="c2a01-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="c2a01-110">Du kan finde oplysninger om denne funktion ved at afspiller opgaveguiderne **ER Import af data fra en Microsoft Excel-fil (del 1: Designformat)** og **ER Import af data fra en Microsoft Excel-fil (del 2: Importere data)** (dele af 7.5.4.3 Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)).</span><span class="sxs-lookup"><span data-stu-id="c2a01-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="c2a01-111">Disse opgaveguider gennemgår, hvordan den indgående Excel-filen kan analyseres ved hjælp af ER-formatet for at importere oplysninger fra indgående dokumenter og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="c2a01-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="c2a01-112">Du kan hente filerne med opgaveguiderne i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="c2a01-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="c2a01-113">Hent følgende filer for at fuldføre opgaveguiderne nævnt ovenfor.</span><span class="sxs-lookup"><span data-stu-id="c2a01-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="c2a01-114">Indholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c2a01-114">Content description</span></span>                         | <span data-ttu-id="c2a01-115">Filer</span><span class="sxs-lookup"><span data-stu-id="c2a01-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c2a01-116">Indgående fil i . XLSX-format - skabelon</span><span class="sxs-lookup"><span data-stu-id="c2a01-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="c2a01-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="c2a01-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="c2a01-118">Indgående fil i . XLSX-format - eksempeldata</span><span class="sxs-lookup"><span data-stu-id="c2a01-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="c2a01-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="c2a01-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="c2a01-120">Hvis du endnu ikke har afspillet følgende opgaveguide, [ER Oprette nødvendige konfigurationer for at importere data fra en ekstern fil](./tasks/er-required-configurations-import-data.md) i det aktuelle Finance and Operations-program, kan du downloade følgende fil.</span><span class="sxs-lookup"><span data-stu-id="c2a01-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="c2a01-121">Indholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c2a01-121">Content description</span></span>    | <span data-ttu-id="c2a01-122">Filer</span><span class="sxs-lookup"><span data-stu-id="c2a01-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c2a01-123">ER-modelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c2a01-123">ER model configuration</span></span> | [<span data-ttu-id="c2a01-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="c2a01-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]