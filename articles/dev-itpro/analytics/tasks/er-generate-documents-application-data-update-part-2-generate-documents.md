--- 
title: Designe konfigurationer for at generere dokumenter med programdata
description: "For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Generere dokumenter med opdatering til programdata (Del 1 - Importere konfigurationer)."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ad5508ea5807f505b29f2e60a1459c9c22552694
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="design-configurations-to-generate-documents-with-application-data"></a><span data-ttu-id="55b2a-103">Designe konfigurationer for at generere dokumenter med programdata</span><span class="sxs-lookup"><span data-stu-id="55b2a-103">Design configurations to generate documents with application data</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55b2a-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Generere dokumenter med opdatering til programdata (Del 1: Importere konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="55b2a-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="55b2a-105">I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="55b2a-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="55b2a-106">I denne procedure skal du køre den ER-importerede formatkonfiguration, der er oprettet for eksempelfirmaet, Litware Inc., for at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="55b2a-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="55b2a-107">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="55b2a-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="55b2a-108">Disse trin kan udføres ved hjælp af DEMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="55b2a-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="55b2a-109">Før du begynder, skal du ændre landekonteksten for DEMF firmaet fra DEU (Tyskland) til BEL (Belgien).</span><span class="sxs-lookup"><span data-stu-id="55b2a-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="55b2a-110">Klik på Virksomhedsadministration > Organisationer > Juridiske enheder for at opdatere landekoden i den primære adresse for den juridiske enhed DEMF.</span><span class="sxs-lookup"><span data-stu-id="55b2a-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="55b2a-111">Genstart programmet.</span><span class="sxs-lookup"><span data-stu-id="55b2a-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="55b2a-112">Kør det importerede ER format</span><span class="sxs-lookup"><span data-stu-id="55b2a-112">Run imported ER format</span></span>
1. <span data-ttu-id="55b2a-113">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="55b2a-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="55b2a-114">Udvid 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="55b2a-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="55b2a-115">Vælg 'Intrastat (model)\Intrastat (format)' i træet.</span><span class="sxs-lookup"><span data-stu-id="55b2a-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="55b2a-116">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="55b2a-116">Click Run.</span></span>
    * <span data-ttu-id="55b2a-117">Kør kladdeversionen af ER-formatkonfigurationen for at generere Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="55b2a-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="55b2a-118">Skriv 'intrastat.xml' i feltet Angiv filnavn.</span><span class="sxs-lookup"><span data-stu-id="55b2a-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="55b2a-119">Angiv navnet på filen.</span><span class="sxs-lookup"><span data-stu-id="55b2a-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="55b2a-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="55b2a-120">Click OK.</span></span>
    * <span data-ttu-id="55b2a-121">Gennemse den genererede XML-fil.</span><span class="sxs-lookup"><span data-stu-id="55b2a-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="55b2a-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55b2a-122">Close the page.</span></span>
8. <span data-ttu-id="55b2a-123">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="55b2a-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="55b2a-124">Åbn denne formular for at få vist Intrastat-posteringer, der er medtaget i det genererede elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="55b2a-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="55b2a-125">Klik på Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="55b2a-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="55b2a-126">Da det udførte ER-format ikke indeholder nogen indstillinger for opdatering af programdata, er detaljerne for den fuldførte Intrastat-rapport ikke blevet arkiveret.</span><span class="sxs-lookup"><span data-stu-id="55b2a-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="55b2a-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55b2a-127">Close the page.</span></span>
11. <span data-ttu-id="55b2a-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="55b2a-128">Close the page.</span></span>


