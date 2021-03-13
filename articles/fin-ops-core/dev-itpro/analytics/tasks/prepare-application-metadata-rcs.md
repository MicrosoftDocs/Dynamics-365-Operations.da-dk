---
title: Klargøre programmetadata, der skal bruges i RCS
description: Dette emne beskriver, hvordan du opretter en ny rapporteringskonfiguration, der indeholder applikationsmetadata.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5f55d089a88642cb2bda70274472ad0f0e45cd7
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094234"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="661bf-103">Klargøre programmetadata, der skal bruges i RCS</span><span class="sxs-lookup"><span data-stu-id="661bf-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="661bf-104">Følgende trin forklarer, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan oprette en ny elektronisk rapporteringskonfiguration (ER), der indeholder programmetadata til udformning af ER-modeltilknytningskonfigurationer i RCS (Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="661bf-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="661bf-105">Denne konfiguration bruges til udformning af en eksempel-ER-modeltilknytningskonfiguration for at få adgang til udenlandske handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="661bf-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="661bf-106">I dette eksempel skal du oprette en konfiguration til eksempelfirmaet Litware, Inc. Denne fremgangsmåde kan udføres i enhver virksomhed.</span><span class="sxs-lookup"><span data-stu-id="661bf-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="661bf-107">For at fuldføre disse trin skal du først fuldføre trinnene i emnet [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="661bf-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="661bf-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="661bf-108">Prerequisites</span></span>
1.    <span data-ttu-id="661bf-109">Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="661bf-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="661bf-110">Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="661bf-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="661bf-111">Hvis du ikke kan se denne konfigurationsudbyder, skal du fuldføre trinnene i proceduren [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="661bf-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="661bf-112">Klik på **Konfiguration af metadata**.</span><span class="sxs-lookup"><span data-stu-id="661bf-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="661bf-113">Antag, at RCS bruges til at designe en ER-løsning for et Finance and Operation-program, der vil generere elektroniske dokumenter, der indeholder oplysninger om forretningsdomæe til udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="661bf-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="661bf-114">Hvis du vil angive tilknytningen mellem ER-datamodellen og kilderne til de påkrævede data, har vi behov for at få adgang til Finance and Operations i RCS.</span><span class="sxs-lookup"><span data-stu-id="661bf-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="661bf-115">Som en del af designet af ER-løsningen konfigurerer vi en ny ER-metadatakonfiguration, der indeholder alle de metadata, der i øjeblikket er påkrævet for at generere ER-rapporter for det valgte forretningsdomæne.</span><span class="sxs-lookup"><span data-stu-id="661bf-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="661bf-116">Tilføj konfiguration af metadata</span><span class="sxs-lookup"><span data-stu-id="661bf-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="661bf-117">Klik på **Opret konfiguration** for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="661bf-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="661bf-118">Skriv 'Udenrigshandelmetadata' i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="661bf-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="661bf-119">Klik på **Opret konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="661bf-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="661bf-120">Klik på **Designer**.</span><span class="sxs-lookup"><span data-stu-id="661bf-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="661bf-121">Klik på **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="661bf-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="661bf-122">Du kan enten vælge alle metadata for hele programmet eller for udvalgte modeller eller moduler.</span><span class="sxs-lookup"><span data-stu-id="661bf-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="661bf-123">Bemærk i dette tilfælde, at følgende metadata vil blive tilføjet automatisk: tabeller over poster, fasttekster og udvidede datatyper (EDT'er).</span><span class="sxs-lookup"><span data-stu-id="661bf-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="661bf-124">Når der kræves flere typer metadata, skal de tilføjes manuelt.</span><span class="sxs-lookup"><span data-stu-id="661bf-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="661bf-125">Vi har nogle metadata, der er relateret til udenlandske handelstransaktioner, ved at vælge metadataelementer manuelt.</span><span class="sxs-lookup"><span data-stu-id="661bf-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="661bf-126">Klik på **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="661bf-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="661bf-127">Klik på **Tabelposter**.</span><span class="sxs-lookup"><span data-stu-id="661bf-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="661bf-128">Brug Quick Filter til at filtre på feltet **Navn** med værdien "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="661bf-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="661bf-129">Vælg **Intrastat** -tabelposten.</span><span class="sxs-lookup"><span data-stu-id="661bf-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="661bf-130">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="661bf-130">Click **OK**.</span></span>
  
<span data-ttu-id="661bf-131">Vi har tilføjet metadataoplysninger om Intrastat-tabellen med poster.</span><span class="sxs-lookup"><span data-stu-id="661bf-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="661bf-132">Gå til træet, og udvid **Tabelposter Intrastat**\>**Relationer**.</span><span class="sxs-lookup"><span data-stu-id="661bf-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="661bf-133">I træet skal du vælge **Tabelposter Intrastat**\>**Relationer\IntrastatCommodity (Tabelposter for EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="661bf-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="661bf-134">Klik på **Tilføj metadata**.</span><span class="sxs-lookup"><span data-stu-id="661bf-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="661bf-135">Metadata om nødvendige relationer for den valgte tabel med poster skal tilføjes manuelt.</span><span class="sxs-lookup"><span data-stu-id="661bf-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="661bf-136">Klik på **Tilføj datakilde**.</span><span class="sxs-lookup"><span data-stu-id="661bf-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="661bf-137">Klik på **Fasttekst**.</span><span class="sxs-lookup"><span data-stu-id="661bf-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="661bf-138">Brug Quick Filter til at filtre på feltet **Navn** med værdien "IntrastatDirection".</span><span class="sxs-lookup"><span data-stu-id="661bf-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="661bf-139">Vælg posten **IntrastatDirection-fasttekst**.</span><span class="sxs-lookup"><span data-stu-id="661bf-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="661bf-140">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="661bf-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="661bf-141">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="661bf-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="661bf-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="661bf-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="661bf-143">Fuldfør kladdeversionen af metadatakonfigurationen</span><span class="sxs-lookup"><span data-stu-id="661bf-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="661bf-144">Klik på **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="661bf-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="661bf-145">Klik på **Fuldfør**.</span><span class="sxs-lookup"><span data-stu-id="661bf-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="661bf-146">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="661bf-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="661bf-147">Vælg den fuldførte version **1**.</span><span class="sxs-lookup"><span data-stu-id="661bf-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="661bf-148">Eksportér den fuldførte version af metadatakonfiguration fra program som en XML-fil</span><span class="sxs-lookup"><span data-stu-id="661bf-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="661bf-149">Klik på **Udveksling**.</span><span class="sxs-lookup"><span data-stu-id="661bf-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="661bf-150">Klik på **Eksporter som XML-fil**.</span><span class="sxs-lookup"><span data-stu-id="661bf-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="661bf-151">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="661bf-151">Click **OK**.</span></span> 
    
<span data-ttu-id="661bf-152">Den oprettede metadatakonfiguration er blevet gemt som en XML-fil, der kan importeres til RCS og bruges som kilden til oplysninger om metadata til forretningsdomænet for udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="661bf-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="661bf-153">Baseret på disse oplysninger kan vi angive tilknytningen mellem programmetadata og ER-datamodel.</span><span class="sxs-lookup"><span data-stu-id="661bf-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
