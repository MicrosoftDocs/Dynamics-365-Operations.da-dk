--- 
title: Generere dokumenter med opdatering af programdata til elektronisk rapportering (ER)
description: "For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren \"ER Generere dokumenter med opdatering til programdata (Del 4 - Redigere format)\"."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b2844621bf50a385ad1a4770c0df2d97623dc77a
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="e1684-103">Generere dokumenter med opdatering af programdata til elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e1684-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1684-104">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren "ER Generere dokumenter med opdatering til programdata (Del 4: Redigere format)".</span><span class="sxs-lookup"><span data-stu-id="e1684-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="e1684-105">I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument og opdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="e1684-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="e1684-106">Du kan udføre ER-formatkonfigurationen for at generere Intrastat-rapporten og opdatere programdata for at arkivere oplysninger om rapporteringsprocessen i denne procedure.</span><span class="sxs-lookup"><span data-stu-id="e1684-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="e1684-107">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="e1684-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e1684-108">Disse trin kan udføres ved hjælp af DEMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="e1684-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="e1684-109">Før du begynder, skal du sørge for, at landekonteksten for DEMF-firmaet er BEL (Belgien).</span><span class="sxs-lookup"><span data-stu-id="e1684-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="e1684-110">Konfigurer udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="e1684-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="e1684-111">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="e1684-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="e1684-112">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="e1684-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="e1684-113">For at arkivere oplysninger om Intrastat-rapporteringsproces skal vi kunne identificere poster for hvert arkiv, vi har oprettet.</span><span class="sxs-lookup"><span data-stu-id="e1684-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="e1684-114">I den forbindelse skal der konfigureres en særlig nummerserie.</span><span class="sxs-lookup"><span data-stu-id="e1684-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="e1684-115">Vælg referencen, der er 'Id for Intrastat-arkiv'.</span><span class="sxs-lookup"><span data-stu-id="e1684-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="e1684-116">Skriv en værdi i feltet Nummerseriekode.</span><span class="sxs-lookup"><span data-stu-id="e1684-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="e1684-117">Skriv eller vælg værdien 'Fore_2' i feltet 'Nummerseriekode'.</span><span class="sxs-lookup"><span data-stu-id="e1684-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="e1684-118">Nummerseriekoden ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="e1684-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="e1684-119">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e1684-119">Click Save.</span></span>
7. <span data-ttu-id="e1684-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e1684-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="e1684-121">Kør ændret ER format</span><span class="sxs-lookup"><span data-stu-id="e1684-121">Run modified ER format</span></span>
1. <span data-ttu-id="e1684-122">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e1684-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e1684-123">Udvid 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e1684-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="e1684-124">Vælg 'Intrastat (model)\Intrastat (format)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e1684-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="e1684-125">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="e1684-125">Click Run.</span></span>
5. <span data-ttu-id="e1684-126">Skriv 'intrastat2.xml' i feltet Angiv filnavn.</span><span class="sxs-lookup"><span data-stu-id="e1684-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="e1684-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="e1684-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="e1684-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e1684-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="e1684-129">Gennemse resultaterne af udførelse af ER-format</span><span class="sxs-lookup"><span data-stu-id="e1684-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="e1684-130">Gennemse den genererede XML-fil.</span><span class="sxs-lookup"><span data-stu-id="e1684-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="e1684-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e1684-131">Close the page.</span></span>
2. <span data-ttu-id="e1684-132">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e1684-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="e1684-133">Åbn denne formular, der indeholder Intrastat-posteringer, der er medtaget i det genererede elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="e1684-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="e1684-134">Klik på Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="e1684-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="e1684-135">Da det udførte ER-format nu indeholder indstillinger for opdatering af programdata, er detaljerne for den fuldførte Intrastat-rapportering blevet arkiveret.</span><span class="sxs-lookup"><span data-stu-id="e1684-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="e1684-136">I denne formular kan du se overskriftsposten for det oprettede arkiv.</span><span class="sxs-lookup"><span data-stu-id="e1684-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="e1684-137">Klik på Detaljer.</span><span class="sxs-lookup"><span data-stu-id="e1684-137">Click Details.</span></span>
    * <span data-ttu-id="e1684-138">I denne formular kan du se oplysninger om det oprettede arkiv.</span><span class="sxs-lookup"><span data-stu-id="e1684-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="e1684-139">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e1684-139">Close the page.</span></span>
6. <span data-ttu-id="e1684-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e1684-140">Close the page.</span></span>
7. <span data-ttu-id="e1684-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e1684-141">Close the page.</span></span>


