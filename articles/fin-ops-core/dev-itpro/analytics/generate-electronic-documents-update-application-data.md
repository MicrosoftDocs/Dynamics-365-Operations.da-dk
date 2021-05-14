---
title: Generere elektroniske dokumenter og opdatere programdata ved brug af ER
description: Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet til at generere udgående elektroniske dokumenter.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944311"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="ac614-103">Generere elektroniske dokumenter og opdatere programdata ved brug af ER</span><span class="sxs-lookup"><span data-stu-id="ac614-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac614-104">Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet til at generere udgående elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ac614-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="ac614-105">Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="ac614-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="ac614-106">På denne måde kan et enkelt ER-format bruges til at generere udgående elektroniske dokumenter og derefter opdatere programdataene.</span><span class="sxs-lookup"><span data-stu-id="ac614-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="ac614-107">Denne funktion kan også anvendes i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="ac614-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="ac614-108">For at forhindre gentagen brug af programdata kan du markere et programs data i de efterfølgende processer med det samme, når dataene er brugt til at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ac614-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="ac614-109">For eksempel kan du markere betalingstransaktioner som allerede behandlet umiddelbart efter, at der er medtaget i en genereret betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="ac614-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="ac614-110">For at gemme behandlingsdetaljerne for elektroniske dokumenter, der er genereret ved hjælp af ER-logik.</span><span class="sxs-lookup"><span data-stu-id="ac614-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="ac614-111">F.eks. et entydigt betalingsmeddelelses-id, der genereres ved hjælp af ER-udtrykket.</span><span class="sxs-lookup"><span data-stu-id="ac614-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="ac614-112">Udtrykket er baseret på oplysninger, der er angivet i ER-dialogboksen, når ER-formatet køres for at oprette dokumenter.</span><span class="sxs-lookup"><span data-stu-id="ac614-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="ac614-113">Du kan få flere oplysninger om denne funktion ved at afspille sættet af opgaveguider Generere ER-dokumenter med opdatering af programdata (en del af 7.5.4.3 forretningsprocessen Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)), som fører dig gennem detaljerede oplysninger om Intrastat-rapportering og -arkivering.</span><span class="sxs-lookup"><span data-stu-id="ac614-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="ac614-114">Følgende filer kræves for at fuldføre bestemte trin i disse opgaveguider.</span><span class="sxs-lookup"><span data-stu-id="ac614-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="ac614-115">Hent og gem filerne til din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="ac614-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="ac614-116">Konfiguration af ER-datamodel: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="ac614-116">ER data model configuration: Intrastat (model)</span></span>](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [<span data-ttu-id="ac614-117">Konfiguration af model ER: Intrastat (tilknytning)</span><span class="sxs-lookup"><span data-stu-id="ac614-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [<span data-ttu-id="ac614-118">ER-formatkonfiguration: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="ac614-118">ER format configuration: Intrastat (format)</span></span>](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
