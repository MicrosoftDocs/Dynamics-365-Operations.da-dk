---
title: "Opdele genererede XML-filer ud fra filstørrelse og indholdsmængde"
description: "Dette emne indeholder oplysninger om, hvordan du opdeler genererede filer baseret på filstørrelsen og antallet af indholdselementer."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.contentlocale: da-dk
ms.lasthandoff: 08/13/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="053b7-103">Opdele genererede XML-filer ud fra filstørrelse og indholdsmængde</span><span class="sxs-lookup"><span data-stu-id="053b7-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="053b7-104">Du kan designe ER-formater for at oprette udgående dokumenter i XML-format.</span><span class="sxs-lookup"><span data-stu-id="053b7-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="053b7-105">Nogle gange kan disse dokumenterne kun accepteres, når de opfylder bestemte kriterier, f.eks. en maksimal filstørrelse eller et maksimalt antal af bestemte XML-noder.</span><span class="sxs-lookup"><span data-stu-id="053b7-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="053b7-106">Du kan designe ER-formater for at generere elektroniske dokumenter, der opfylder de krav, som modtagerne af disse dokumenter angiver.</span><span class="sxs-lookup"><span data-stu-id="053b7-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="053b7-107">For FILE-formatelementet kan du definere en grænse for filens størrelse som et ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="053b7-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="053b7-108">Hvis den angivne grænse overskrides, når der oprettes en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.</span><span class="sxs-lookup"><span data-stu-id="053b7-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="053b7-109">For XML ELEMENT-formater kan du definere en grænse for antal elementer som et ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="053b7-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="053b7-110">Hvis antallet af XML-noder i den fil, der genereres, overskrider den angivne grænse, når der køres en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.</span><span class="sxs-lookup"><span data-stu-id="053b7-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="053b7-111">For XML SEQUENCE-formatelementer kan du definere en grænse for antal underordnede elementer som et ER-udtryk.</span><span class="sxs-lookup"><span data-stu-id="053b7-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="053b7-112">Hvis antallet af indlejrede XML-noder i formatelementet i den genererede fil overskrider den angivne grænse, når der køres en ER-rapport, afslutter ER oprettelsen af den aktuelle fil og fortsætter derefter med at oprette den næste fil.</span><span class="sxs-lookup"><span data-stu-id="053b7-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="053b7-113">Du kan markere ethvert XML ELEMENT-format, som non-breakable.</span><span class="sxs-lookup"><span data-stu-id="053b7-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="053b7-114">På denne måde kan du organisere de indlejrede elementer i XML-noder, der genereres under formatelementet, i en enkelt genereret fil.</span><span class="sxs-lookup"><span data-stu-id="053b7-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="053b7-115">Ud over at bruge XML ELEMENT- og XML SEQUENCE-formatelementer til at føje XML-noder til den oprettede fil, kan du bruge RAW XML-formatelementet.</span><span class="sxs-lookup"><span data-stu-id="053b7-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="053b7-116">Noder, som du tilføjer ved hjælp af det RAW XML-formatelementet, tages ikke i betragtning, når antallet af noder, beregnes for at vurdere grænserne for antallet af elementer.</span><span class="sxs-lookup"><span data-stu-id="053b7-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="053b7-117">Hvis du har konfigureret fildestinationer for et FILE-formatelement, der er konfigureret til at opdele det genererede output, når bestemte grænseværdier overskrides, sendes hvert enkelt genererede output til den konfigurerede fildestination som en individuel fil.</span><span class="sxs-lookup"><span data-stu-id="053b7-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="053b7-118">For entydigt at identificere de filer, der oprettes ved at opdele outputtet, skal du konfigurere et ER-udtryk for FILE-formatelementet.</span><span class="sxs-lookup"><span data-stu-id="053b7-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="053b7-119">Hvis du medtager en ER-datakilde af typen NUMBER SEQUENCE, øges nummerserien trinvist for hver enkelt del af det opdelte output.</span><span class="sxs-lookup"><span data-stu-id="053b7-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="053b7-120">Hvis du vil vide mere om denne funktion, kan du afspille opgaveguiden **ER Opdele XML-filer baseret på filstørrelsen eller antallet af indholdselementer**, som er en del af forretningsprocessen **7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)**, og som kan hentes fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="053b7-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="053b7-121">Denne opgaveguide gennemgår konfigurationen af et ER-format for at opdele genererede filer baseret på begrænsninger i filstørrelsen og antallet af indholdselementer.</span><span class="sxs-lookup"><span data-stu-id="053b7-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="053b7-122">Du skal hente følgende filer for at fuldføre opgaveguiden:</span><span class="sxs-lookup"><span data-stu-id="053b7-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="053b7-123">ER-modelkonfiguration - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="053b7-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="053b7-124">ER-formatkonfiguration - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="053b7-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="053b7-125">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="053b7-125">Additional resources</span></span>
[<span data-ttu-id="053b7-126">Destinationer for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="053b7-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="053b7-127">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="053b7-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

