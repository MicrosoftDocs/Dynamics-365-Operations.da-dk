--- 
title: "Oprette format for optælling og sammenlægning"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 7613b78d4a9ab63f5be9773a8699fe3ed94636eb
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="85f2f-103">Oprette format for optælling og sammenlægning</span><span class="sxs-lookup"><span data-stu-id="85f2f-103">Create format for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85f2f-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="85f2f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="85f2f-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="85f2f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="85f2f-106">Du skal fuldføre trinnene i proceduren "Opret en konfigurationsudbyder, og markér den som aktiv" for at fuldføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="85f2f-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="85f2f-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="85f2f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="85f2f-108">Få adgang til listen over de konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="85f2f-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="85f2f-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="85f2f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="85f2f-110">Sørg for, at udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="85f2f-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="85f2f-111">er tilgængelig og markeret som aktiv.</span><span class="sxs-lookup"><span data-stu-id="85f2f-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="85f2f-112">Vælg udbyderen "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="85f2f-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="85f2f-113">.</span><span class="sxs-lookup"><span data-stu-id="85f2f-113">provider.</span></span>
3. <span data-ttu-id="85f2f-114">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="85f2f-114">Click Repositories.</span></span>
    * <span data-ttu-id="85f2f-115">Hvis der allerede findes et lager af typen "Operationsressourcer", kan du springe over de resterende trin i den aktuelle underopgave.</span><span class="sxs-lookup"><span data-stu-id="85f2f-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="85f2f-116">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="85f2f-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="85f2f-117">Angiv 'Operationsressourcer' i feltet Konfigurationslagertype.</span><span class="sxs-lookup"><span data-stu-id="85f2f-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="85f2f-118">Klik på Opretlager.</span><span class="sxs-lookup"><span data-stu-id="85f2f-118">Click Create repository.</span></span>
7. <span data-ttu-id="85f2f-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="85f2f-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="85f2f-120">Få de Intrastat-konfigurationer, der leveres af Microsoft</span><span class="sxs-lookup"><span data-stu-id="85f2f-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="85f2f-121">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="85f2f-121">Click Open.</span></span>
2. <span data-ttu-id="85f2f-122">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="85f2f-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="85f2f-123">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="85f2f-123">Click Import.</span></span>
    * <span data-ttu-id="85f2f-124">Klik på Importer for version 1.1 af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="85f2f-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="85f2f-125">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="85f2f-125">Click Yes.</span></span>
5. <span data-ttu-id="85f2f-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="85f2f-126">Close the page.</span></span>
6. <span data-ttu-id="85f2f-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="85f2f-127">Close the page.</span></span>
7. <span data-ttu-id="85f2f-128">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="85f2f-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="85f2f-129">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="85f2f-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="85f2f-130">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="85f2f-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


