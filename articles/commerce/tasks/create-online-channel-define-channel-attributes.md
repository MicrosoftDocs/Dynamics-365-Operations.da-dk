---
title: Opret onlinekanal og definer kanalattributter
description: Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bac365217c20bececa1b4ff2b9de12288326dcc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021998"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="d2d47-103">Opret onlinekanal og definer kanalattributter</span><span class="sxs-lookup"><span data-stu-id="d2d47-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d2d47-104">Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d2d47-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="d2d47-105">Du skal oprette organisationshierarkiet, før du kan oprette en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="d2d47-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="d2d47-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d2d47-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="d2d47-107">Opret en ny onlinekanal</span><span class="sxs-lookup"><span data-stu-id="d2d47-107">Create a new online channel</span></span>
1. <span data-ttu-id="d2d47-108">Gå til Retail og Commerce > Kanaler > Onlinebutikker.</span><span class="sxs-lookup"><span data-stu-id="d2d47-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="d2d47-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d2d47-109">Click New.</span></span>
3. <span data-ttu-id="d2d47-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2d47-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d2d47-111">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="d2d47-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="d2d47-112">Vælg en indstilling i feltet Lagertidszone.</span><span class="sxs-lookup"><span data-stu-id="d2d47-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="d2d47-113">Indtast eller vælg en værdi i feltet Standardkunde.</span><span class="sxs-lookup"><span data-stu-id="d2d47-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="d2d47-114">Indtast eller vælg en værdi i feltet Kundeadressekartotek.</span><span class="sxs-lookup"><span data-stu-id="d2d47-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="d2d47-115">Indtast eller vælg en værdi i feltet Betalingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="d2d47-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="d2d47-116">Indtast eller vælg en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="d2d47-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="d2d47-117">Indtast eller vælg en værdi i feltet Profil til e-mailbesked.</span><span class="sxs-lookup"><span data-stu-id="d2d47-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="d2d47-118">Udvid sektionen Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="d2d47-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="d2d47-119">Indtast eller vælg en værdi i feltet BusinessUnit.</span><span class="sxs-lookup"><span data-stu-id="d2d47-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="d2d47-120">På samme måde kan du angive værdien for alle andre standarddimensioner.</span><span class="sxs-lookup"><span data-stu-id="d2d47-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="d2d47-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d2d47-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="d2d47-122">Føj onlinekanalen til organisationshierarkiet</span><span class="sxs-lookup"><span data-stu-id="d2d47-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="d2d47-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d2d47-123">Close the page.</span></span>
2. <span data-ttu-id="d2d47-124">Gå til Virksomhedsadministration > Organisationer > Organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="d2d47-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="d2d47-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d2d47-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d2d47-126">Klik på Vis.</span><span class="sxs-lookup"><span data-stu-id="d2d47-126">Click View.</span></span>
5. <span data-ttu-id="d2d47-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d2d47-127">Click Edit.</span></span>
    * <span data-ttu-id="d2d47-128">Du kan vælge en hvilket som helst hierarkinode, hvor du vil indsætte den nye kanal.</span><span class="sxs-lookup"><span data-stu-id="d2d47-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="d2d47-129">Klik på Indsæt.</span><span class="sxs-lookup"><span data-stu-id="d2d47-129">Click Insert.</span></span>
7. <span data-ttu-id="d2d47-130">Klik på Commerce-kanal.</span><span class="sxs-lookup"><span data-stu-id="d2d47-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="d2d47-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2d47-131">Click OK.</span></span>
9. <span data-ttu-id="d2d47-132">Klik på Publicer for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d2d47-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="d2d47-133">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="d2d47-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="d2d47-134">Klik på Publicer.</span><span class="sxs-lookup"><span data-stu-id="d2d47-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="d2d47-135">Konfigurere ordrer for næsten i realtids-påmindelse</span><span class="sxs-lookup"><span data-stu-id="d2d47-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="d2d47-136">Gå til Retail og Commerce > Konfiguration af hovedkontor > Parametre > Commerce-parametre.</span><span class="sxs-lookup"><span data-stu-id="d2d47-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="d2d47-137">Vælg "Ja" i Brug realtidstjeneste til oprettelse af eCommerce-ordre.</span><span class="sxs-lookup"><span data-stu-id="d2d47-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="d2d47-138">Kør distributionsplanen 1070 for at synkronisere ændringerne til kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="d2d47-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


