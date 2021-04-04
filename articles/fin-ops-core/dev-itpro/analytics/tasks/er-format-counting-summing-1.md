---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)'
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565136"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="104de-104">ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)</span><span class="sxs-lookup"><span data-stu-id="104de-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="104de-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="104de-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="104de-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="104de-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="104de-107">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="104de-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="104de-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="104de-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="104de-109">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="104de-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="104de-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="104de-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="104de-111">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="104de-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="104de-112">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="104de-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="104de-113">Vælg udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="104de-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="104de-114">.</span><span class="sxs-lookup"><span data-stu-id="104de-114">provider.</span></span>
3. <span data-ttu-id="104de-115">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="104de-115">Click Repositories.</span></span>
    * <span data-ttu-id="104de-116">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="104de-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="104de-117">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="104de-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="104de-118">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="104de-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="104de-119">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="104de-119">Click Create repository.</span></span>
7. <span data-ttu-id="104de-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="104de-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="104de-121">Få de Intrastat-konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="104de-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="104de-122">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="104de-122">Click Open.</span></span>
2. <span data-ttu-id="104de-123">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="104de-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="104de-124">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="104de-124">Click Import.</span></span>
    * <span data-ttu-id="104de-125">Klik på Importer for version 1.1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="104de-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="104de-126">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="104de-126">Click Yes.</span></span>
5. <span data-ttu-id="104de-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="104de-127">Close the page.</span></span>
6. <span data-ttu-id="104de-128">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="104de-128">Close the page.</span></span>
7. <span data-ttu-id="104de-129">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="104de-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="104de-130">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="104de-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="104de-131">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="104de-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]