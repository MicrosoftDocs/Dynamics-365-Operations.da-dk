---
title: Konfigurere adgangsrettigheder for en controller for omkostningsobjekt
description: Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4b50782c7a1b69b6953c65d6df155f003028333
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976301"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="b2f48-103">Konfigurere adgangsrettigheder for en controller for omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b2f48-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2f48-104">Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.</span><span class="sxs-lookup"><span data-stu-id="b2f48-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="b2f48-105">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b2f48-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="b2f48-106">Tildele rollen Controller til omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="b2f48-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="b2f48-107">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="b2f48-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="b2f48-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="b2f48-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b2f48-109">For eksempel kan du filtrere på værdien 'alicia' i feltet Brugernavn.</span><span class="sxs-lookup"><span data-stu-id="b2f48-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="b2f48-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b2f48-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b2f48-111">Klik på Tildel roller.</span><span class="sxs-lookup"><span data-stu-id="b2f48-111">Click Assign roles.</span></span>
5. <span data-ttu-id="b2f48-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b2f48-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b2f48-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b2f48-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="b2f48-114">Aktivere sikkerhed for adgangsliste</span><span class="sxs-lookup"><span data-stu-id="b2f48-114">Enable access list security</span></span>
1. <span data-ttu-id="b2f48-115">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="b2f48-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="b2f48-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b2f48-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b2f48-117">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="b2f48-117">Select Organization.</span></span>  
3. <span data-ttu-id="b2f48-118">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b2f48-118">Click Edit.</span></span>
4. <span data-ttu-id="b2f48-119">Vælg Ja i feltet Adgangslistehierarki.</span><span class="sxs-lookup"><span data-stu-id="b2f48-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="b2f48-120">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="b2f48-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="b2f48-121">Tildele adgangsrettigheder til bruger</span><span class="sxs-lookup"><span data-stu-id="b2f48-121">Assign access rights to user</span></span>
1. <span data-ttu-id="b2f48-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b2f48-122">Click New.</span></span>
2. <span data-ttu-id="b2f48-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b2f48-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b2f48-124">Indtast eller vælg en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="b2f48-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="b2f48-125">Vælg administrator.</span><span class="sxs-lookup"><span data-stu-id="b2f48-125">Select Admin.</span></span>  
4. <span data-ttu-id="b2f48-126">Vælg 'Organisation\Administrerende direktør\Administrerende direktør\FIM'.</span><span class="sxs-lookup"><span data-stu-id="b2f48-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="b2f48-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="b2f48-127">Click New.</span></span>
6. <span data-ttu-id="b2f48-128">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b2f48-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b2f48-129">Indtast eller vælg en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="b2f48-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="b2f48-130">Vælg Alicia.</span><span class="sxs-lookup"><span data-stu-id="b2f48-130">Select Alicia.</span></span>  
8. <span data-ttu-id="b2f48-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b2f48-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="b2f48-132">Aktivere adgangsrettigheder i omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="b2f48-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="b2f48-133">Gå til Omkostningsregnskab > Opsætning > Parametre.</span><span class="sxs-lookup"><span data-stu-id="b2f48-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="b2f48-134">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="b2f48-134">Click the General tab.</span></span>
3. <span data-ttu-id="b2f48-135">Vælg Ja i feltet Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b2f48-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="b2f48-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b2f48-136">Click Save.</span></span>
5. <span data-ttu-id="b2f48-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="b2f48-137">Close the page.</span></span>
6. <span data-ttu-id="b2f48-138">Gå til Omkostningsregnskab > Opsætning > Konfiguration af arbejdsområde for omkostningsstyring.</span><span class="sxs-lookup"><span data-stu-id="b2f48-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="b2f48-139">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="b2f48-139">Click Edit.</span></span>
8. <span data-ttu-id="b2f48-140">Vælg Ja i feltet Publiceret.</span><span class="sxs-lookup"><span data-stu-id="b2f48-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="b2f48-141">Hvis du vælger Ja, kan en bruger, der er tildelt en af følgende fire roller, se rapporterne i arbejdsområdet Omkostningsstyring: regnskabschef, bogholder, bogholderimedarbejder og omkostningsobjektcontroller.</span><span class="sxs-lookup"><span data-stu-id="b2f48-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="b2f48-142">Hvis du vælger Nej, er det kun en bruger, der er tildelt en af følgende roller, der kan se rapporterne: regnskabschef, bogholder og bogholderimedarbejder.</span><span class="sxs-lookup"><span data-stu-id="b2f48-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="b2f48-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="b2f48-143">Click Save.</span></span>

