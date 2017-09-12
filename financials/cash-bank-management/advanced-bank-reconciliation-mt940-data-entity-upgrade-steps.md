---
title: "Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed"
description: "Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: da-dk
ms.lasthandoff: 07/18/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="045e1-103">Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed</span><span class="sxs-lookup"><span data-stu-id="045e1-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="045e1-104">Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940.</span><span class="sxs-lookup"><span data-stu-id="045e1-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="045e1-105">Brug følgende trin til at tilføje importenhed for bankkontoudtog, der understøtter formatet MT940.</span><span class="sxs-lookup"><span data-stu-id="045e1-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="045e1-106">Kompilerer og synkroniserer følgende:</span><span class="sxs-lookup"><span data-stu-id="045e1-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="045e1-107">Sammensat Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="045e1-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="045e1-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="045e1-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="045e1-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="045e1-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="045e1-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="045e1-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="045e1-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="045e1-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="045e1-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="045e1-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="045e1-113">Datastyring\\dataprojekter.</span><span class="sxs-lookup"><span data-stu-id="045e1-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="045e1-114">Indlæse MT940-importprojekter</span><span class="sxs-lookup"><span data-stu-id="045e1-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="045e1-115">Ændre XSLT.</span><span class="sxs-lookup"><span data-stu-id="045e1-115">Change XSLT.</span></span>
            -   <span data-ttu-id="045e1-116">Klik på **Vis tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="045e1-116">Click **View map**.</span></span>
            -   <span data-ttu-id="045e1-117">Klik på **Vis tilknytning** på bankkontoudtogets dokumentet.</span><span class="sxs-lookup"><span data-stu-id="045e1-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="045e1-118">Klik på **Transformationer**</span><span class="sxs-lookup"><span data-stu-id="045e1-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="045e1-119">Slet filen BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="045e1-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="045e1-120">Tilføj den nye version af BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="045e1-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="045e1-121">Vis **løbenummeret** på **kildedata**-layout.</span><span class="sxs-lookup"><span data-stu-id="045e1-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="045e1-122">Kildedataformat = XML-element.</span><span class="sxs-lookup"><span data-stu-id="045e1-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="045e1-123">Enhedsnavn = Bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="045e1-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="045e1-124">Upload datafilen = ny version af SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="045e1-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="045e1-125">Klik på **Ja** for at overskrive den eksisterende fil.</span><span class="sxs-lookup"><span data-stu-id="045e1-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="045e1-126">Klik på **Ja** for at oprette en ny tilknytning.</span><span class="sxs-lookup"><span data-stu-id="045e1-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="045e1-127">Kontrollér, at S**equenceNumber** er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="045e1-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="045e1-128">Klik på **Vis tilknytning** på bankkontoudtogets enhed.</span><span class="sxs-lookup"><span data-stu-id="045e1-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="045e1-129">Kontrollér, at **SequenceNumber** er knyttet fra Kilde til Midlertidig.</span><span class="sxs-lookup"><span data-stu-id="045e1-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="045e1-130">Importér det nye udtog.</span><span class="sxs-lookup"><span data-stu-id="045e1-130">Import the new statement.</span></span>





