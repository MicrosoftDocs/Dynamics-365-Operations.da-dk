---
title: Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed
description: Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188458"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="33f53-103">Avanceret bankafstemning MT940-import – opgraderingstrin for sammensat dataenhed</span><span class="sxs-lookup"><span data-stu-id="33f53-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33f53-104">Et løbenummer skal føjes til bankkontoudtogets importenhed for at understøtte formatet MT940.</span><span class="sxs-lookup"><span data-stu-id="33f53-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="33f53-105">Brug følgende trin til at tilføje importenhed for bankkontoudtog, der understøtter formatet MT940.</span><span class="sxs-lookup"><span data-stu-id="33f53-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="33f53-106">Kompilerer og synkroniserer følgende:</span><span class="sxs-lookup"><span data-stu-id="33f53-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="33f53-107">Sammensat Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="33f53-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="33f53-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="33f53-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="33f53-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="33f53-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="33f53-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="33f53-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="33f53-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="33f53-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="33f53-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="33f53-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="33f53-113">Datastyring\\dataprojekter.</span><span class="sxs-lookup"><span data-stu-id="33f53-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="33f53-114">Indlæse MT940-importprojekter</span><span class="sxs-lookup"><span data-stu-id="33f53-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="33f53-115">Ændre XSLT.</span><span class="sxs-lookup"><span data-stu-id="33f53-115">Change XSLT.</span></span>
            -   <span data-ttu-id="33f53-116">Klik på **Vis tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="33f53-116">Click **View map**.</span></span>
            -   <span data-ttu-id="33f53-117">Klik på **Vis tilknytning** på bankkontoudtogets dokumentet.</span><span class="sxs-lookup"><span data-stu-id="33f53-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="33f53-118">Klik på **Transformationer**</span><span class="sxs-lookup"><span data-stu-id="33f53-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="33f53-119">Slet filen BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="33f53-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="33f53-120">Tilføj den nye version af BankReconiliation-to-Composite.xsl.</span><span class="sxs-lookup"><span data-stu-id="33f53-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="33f53-121">Vis **løbenummeret** på **kildedata**-layout.</span><span class="sxs-lookup"><span data-stu-id="33f53-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="33f53-122">Kildedataformat = XML-element.</span><span class="sxs-lookup"><span data-stu-id="33f53-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="33f53-123">Enhedsnavn = Bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="33f53-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="33f53-124">Upload datafilen = ny version af SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="33f53-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="33f53-125">Klik på **Ja** for at overskrive den eksisterende fil.</span><span class="sxs-lookup"><span data-stu-id="33f53-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="33f53-126">Klik på **Ja** for at oprette en ny tilknytning.</span><span class="sxs-lookup"><span data-stu-id="33f53-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="33f53-127">Kontrollér, at S**equenceNumber** er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="33f53-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="33f53-128">Klik på **Vis tilknytning** på bankkontoudtogets enhed.</span><span class="sxs-lookup"><span data-stu-id="33f53-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="33f53-129">Kontrollér, at **SequenceNumber** er knyttet fra Kilde til Midlertidig.</span><span class="sxs-lookup"><span data-stu-id="33f53-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="33f53-130">Importér det nye udtog.</span><span class="sxs-lookup"><span data-stu-id="33f53-130">Import the new statement.</span></span>




