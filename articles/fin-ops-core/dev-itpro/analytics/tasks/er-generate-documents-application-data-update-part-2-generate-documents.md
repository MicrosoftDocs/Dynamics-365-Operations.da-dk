---
title: Designe konfigurationer til at generere dokumenter, der har programdata
description: I dette emne forklares det, hvordan du designer konfigurationer af elektronisk rapportering (ER) for at generere et elektronisk dokument. (Del 1 – Importere konfigurationer).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751076"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="16d38-104">Designe konfigurationer til at generere dokumenter, der har programdata</span><span class="sxs-lookup"><span data-stu-id="16d38-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16d38-105">For at fuldføre trinnene i denne procedure skal du først fuldføre proceduren ER Generere dokumenter med opdatering til programdata (Del 1: Importere konfigurationer).</span><span class="sxs-lookup"><span data-stu-id="16d38-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="16d38-106">I denne procedure forklares det, hvordan du designer elektroniske rapportering (ER) konfigurationer for at generere et elektronisk dokument.</span><span class="sxs-lookup"><span data-stu-id="16d38-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="16d38-107">I denne procedure skal du køre den ER-importerede formatkonfiguration, der er oprettet for eksempelfirmaet, Litware Inc., for at generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="16d38-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="16d38-108">Denne procedure er til brugere, der er tildelt rollen som systemadministrator eller elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="16d38-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="16d38-109">Disse trin kan udføres ved hjælp af DEMF-datasættet.</span><span class="sxs-lookup"><span data-stu-id="16d38-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="16d38-110">Før du begynder, skal du ændre landekonteksten for DEMF firmaet fra DEU (Tyskland) til BEL (Belgien).</span><span class="sxs-lookup"><span data-stu-id="16d38-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="16d38-111">Klik på Virksomhedsadministration > Organisationer > Juridiske enheder for at opdatere landekoden i den primære adresse for den juridiske enhed DEMF.</span><span class="sxs-lookup"><span data-stu-id="16d38-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="16d38-112">Genstart programmet.</span><span class="sxs-lookup"><span data-stu-id="16d38-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="16d38-113">Kør det importerede ER format</span><span class="sxs-lookup"><span data-stu-id="16d38-113">Run imported ER format</span></span>
1. <span data-ttu-id="16d38-114">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="16d38-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="16d38-115">Udvid 'Intrastat (model)' i træet.</span><span class="sxs-lookup"><span data-stu-id="16d38-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="16d38-116">Vælg 'Intrastat (model)\Intrastat (format)' i træet.</span><span class="sxs-lookup"><span data-stu-id="16d38-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="16d38-117">Klik på Kør.</span><span class="sxs-lookup"><span data-stu-id="16d38-117">Click Run.</span></span>
    * <span data-ttu-id="16d38-118">Kør kladdeversionen af ER-formatkonfigurationen for at generere Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="16d38-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="16d38-119">Skriv 'intrastat.xml' i feltet Angiv filnavn.</span><span class="sxs-lookup"><span data-stu-id="16d38-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="16d38-120">Angiv navnet på filen.</span><span class="sxs-lookup"><span data-stu-id="16d38-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="16d38-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="16d38-121">Click OK.</span></span>
    * <span data-ttu-id="16d38-122">Gennemse den genererede XML-fil.</span><span class="sxs-lookup"><span data-stu-id="16d38-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="16d38-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16d38-123">Close the page.</span></span>
8. <span data-ttu-id="16d38-124">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="16d38-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="16d38-125">Åbn denne formular for at få vist Intrastat-posteringer, der er medtaget i det genererede elektroniske dokument.</span><span class="sxs-lookup"><span data-stu-id="16d38-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="16d38-126">Klik på Intrastat-arkiv.</span><span class="sxs-lookup"><span data-stu-id="16d38-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="16d38-127">Da det udførte ER-format ikke indeholder nogen indstillinger for opdatering af programdata, er detaljerne for den fuldførte Intrastat-rapport ikke blevet arkiveret.</span><span class="sxs-lookup"><span data-stu-id="16d38-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="16d38-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16d38-128">Close the page.</span></span>
11. <span data-ttu-id="16d38-129">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="16d38-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]