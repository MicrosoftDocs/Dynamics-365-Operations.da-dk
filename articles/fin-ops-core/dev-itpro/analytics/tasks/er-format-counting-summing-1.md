---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141919"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="09fa2-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 1: Oprettelsesformat)</span><span class="sxs-lookup"><span data-stu-id="09fa2-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09fa2-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="09fa2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="09fa2-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="09fa2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="09fa2-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="09fa2-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="09fa2-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="09fa2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="09fa2-108">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="09fa2-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="09fa2-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="09fa2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="09fa2-110">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="09fa2-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="09fa2-111">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="09fa2-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="09fa2-112">Vælg udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="09fa2-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="09fa2-113">.</span><span class="sxs-lookup"><span data-stu-id="09fa2-113">provider.</span></span>
3. <span data-ttu-id="09fa2-114">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="09fa2-114">Click Repositories.</span></span>
    * <span data-ttu-id="09fa2-115">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="09fa2-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="09fa2-116">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="09fa2-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="09fa2-117">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="09fa2-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="09fa2-118">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="09fa2-118">Click Create repository.</span></span>
7. <span data-ttu-id="09fa2-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="09fa2-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="09fa2-120">Få de Intrastat-konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="09fa2-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="09fa2-121">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="09fa2-121">Click Open.</span></span>
2. <span data-ttu-id="09fa2-122">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="09fa2-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="09fa2-123">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="09fa2-123">Click Import.</span></span>
    * <span data-ttu-id="09fa2-124">Klik på Importer for version 1.1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09fa2-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="09fa2-125">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="09fa2-125">Click Yes.</span></span>
5. <span data-ttu-id="09fa2-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09fa2-126">Close the page.</span></span>
6. <span data-ttu-id="09fa2-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="09fa2-127">Close the page.</span></span>
7. <span data-ttu-id="09fa2-128">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="09fa2-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="09fa2-129">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="09fa2-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="09fa2-130">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="09fa2-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

