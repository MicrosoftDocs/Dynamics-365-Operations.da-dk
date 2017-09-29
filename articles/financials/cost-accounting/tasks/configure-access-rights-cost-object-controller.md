--- 
title: Konfigurere adgangsrettigheder for en controller for omkostningsobjekt
description: Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b0647e1ec55d23607d07f38105e42af498ad1174
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="0dc81-103">Konfigurere adgangsrettigheder for en controller for omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="0dc81-103">Configure access rights for a cost object controller</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dc81-104">Brug denne procedure til at konfigurere adgangsrettigheder for en omkostningsobjektcontroller.</span><span class="sxs-lookup"><span data-stu-id="0dc81-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="0dc81-105">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="0dc81-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="0dc81-106">Tildele rollen Controller til omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="0dc81-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="0dc81-107">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="0dc81-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="0dc81-108">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="0dc81-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0dc81-109">For eksempel kan du filtrere på værdien 'alicia' i feltet Brugernavn.</span><span class="sxs-lookup"><span data-stu-id="0dc81-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="0dc81-110">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0dc81-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0dc81-111">Klik på Tildel roller.</span><span class="sxs-lookup"><span data-stu-id="0dc81-111">Click Assign roles.</span></span>
5. <span data-ttu-id="0dc81-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0dc81-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0dc81-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0dc81-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="0dc81-114">Aktivere sikkerhed for adgangsliste</span><span class="sxs-lookup"><span data-stu-id="0dc81-114">Enable access list security</span></span>
1. <span data-ttu-id="0dc81-115">Gå til Omkostningsregnskab > Dimensioner > Dimensionshierarkier.</span><span class="sxs-lookup"><span data-stu-id="0dc81-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="0dc81-116">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0dc81-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0dc81-117">Vælg organisation.</span><span class="sxs-lookup"><span data-stu-id="0dc81-117">Select Organization.</span></span>  
3. <span data-ttu-id="0dc81-118">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0dc81-118">Click Edit.</span></span>
4. <span data-ttu-id="0dc81-119">Vælg Ja i feltet Adgangslistehierarki.</span><span class="sxs-lookup"><span data-stu-id="0dc81-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="0dc81-120">Klik på Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="0dc81-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="0dc81-121">Tildele adgangsrettigheder til bruger</span><span class="sxs-lookup"><span data-stu-id="0dc81-121">Assign access rights to user</span></span>
1. <span data-ttu-id="0dc81-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0dc81-122">Click New.</span></span>
2. <span data-ttu-id="0dc81-123">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0dc81-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0dc81-124">Indtast eller vælg en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="0dc81-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="0dc81-125">Vælg administrator.</span><span class="sxs-lookup"><span data-stu-id="0dc81-125">Select Admin.</span></span>  
4. <span data-ttu-id="0dc81-126">Vælg 'Organisation\Administrerende direktør\Administrerende direktør\FIM'.</span><span class="sxs-lookup"><span data-stu-id="0dc81-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="0dc81-127">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0dc81-127">Click New.</span></span>
6. <span data-ttu-id="0dc81-128">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0dc81-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0dc81-129">Indtast eller vælg en værdi i feltet Bruger-id.</span><span class="sxs-lookup"><span data-stu-id="0dc81-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="0dc81-130">Vælg Alicia.</span><span class="sxs-lookup"><span data-stu-id="0dc81-130">Select Alicia.</span></span>  
8. <span data-ttu-id="0dc81-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0dc81-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="0dc81-132">Aktivere adgangsrettigheder i omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="0dc81-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="0dc81-133">Gå til Omkostningsregnskab > Opsætning > Parametre.</span><span class="sxs-lookup"><span data-stu-id="0dc81-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="0dc81-134">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0dc81-134">Click the General tab.</span></span>
3. <span data-ttu-id="0dc81-135">Vælg Ja i feltet Aktivér læseadgang for dimensionsmedlemmer for omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0dc81-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="0dc81-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0dc81-136">Click Save.</span></span>
5. <span data-ttu-id="0dc81-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0dc81-137">Close the page.</span></span>
6. <span data-ttu-id="0dc81-138">Gå til Omkostningsregnskab > Opsætning > Konfiguration af arbejdsområde for omkostningsstyring.</span><span class="sxs-lookup"><span data-stu-id="0dc81-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="0dc81-139">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0dc81-139">Click Edit.</span></span>
8. <span data-ttu-id="0dc81-140">Vælg Ja i feltet Publiceret.</span><span class="sxs-lookup"><span data-stu-id="0dc81-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="0dc81-141">Hvis du vælger Ja, kan en bruger, der er tildelt en af følgende fire roller, se rapporterne i arbejdsområdet Omkostningsstyring: regnskabschef, bogholder, bogholderimedarbejder og omkostningsobjektcontroller.</span><span class="sxs-lookup"><span data-stu-id="0dc81-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="0dc81-142">Hvis du vælger Nej, er det kun en bruger, der er tildelt en af følgende roller, der kan se rapporterne: regnskabschef, bogholder og bogholderimedarbejder.</span><span class="sxs-lookup"><span data-stu-id="0dc81-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="0dc81-143">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0dc81-143">Click Save.</span></span>


