---
title: "Generere elektroniske dokumenter og opdatere programdata ved hjælp af værktøjet Elektronisk rapportering"
description: "Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet Finans and Operations til at generere udgående elektroniske dokumenter. Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7378c1d205b9a9cd61044dc33fc52ff75c6b94b7
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="fdbfe-104">Generere elektroniske dokumenter og opdatere programdata ved hjælp af værktøjet Elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="fdbfe-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

<span data-ttu-id="fdbfe-105">Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet Finans and Operations til at generere udgående elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="fdbfe-106">Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="fdbfe-107">På denne måde kan et enkelt ER-format bruges til at generere udgående elektroniske dokumenter og derefter opdatere programdataene.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="fdbfe-108">Denne funktion kan også anvendes i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="fdbfe-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="fdbfe-109">For at forhindre gentagen brug af programdata kan du markere et programs data i de efterfølgende processer med det samme, når dataene er brugt til at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="fdbfe-110">For eksempel kan du markere betalingstransaktioner som allerede behandlet umiddelbart efter, at der er medtaget i en genereret betalingsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="fdbfe-111">For at gemme behandlingsdetaljerne for elektroniske dokumenter, der er genereret ved hjælp af ER-logik.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="fdbfe-112">F.eks. et entydigt betalingsmeddelelses-id, der genereres ved hjælp af ER-udtrykket.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="fdbfe-113">Udtrykket er baseret på oplysninger, der er angivet i ER-dialogboksen, når ER-formatet køres for at oprette dokumenter.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="fdbfe-114">Du kan få flere oplysninger om denne funktion ved at afspille sættet af opgaveguider Generere ER-dokumenter med opdatering af programdata (en del af 7.5.4.3 forretningsprocessen Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)), som fører dig gennem detaljerede oplysninger om Intrastat-rapportering og -arkivering.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="fdbfe-115">Følgende filer kræves for at fuldføre bestemte trin i disse opgaveguider.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="fdbfe-116">Hent og gem filerne til din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="fdbfe-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="fdbfe-117">Konfiguration af ER-datamodel: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="fdbfe-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="fdbfe-118">Konfiguration af model ER: Intrastat (tilknytning)</span><span class="sxs-lookup"><span data-stu-id="fdbfe-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="fdbfe-119">ER-formatkonfiguration: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="fdbfe-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
