---
title: Opret onlinekanal og definer kanalattributter
description: Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "312364"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="d2e88-103">Opret onlinekanal og definer kanalattributter</span><span class="sxs-lookup"><span data-stu-id="d2e88-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d2e88-104">Denne procedure gennemgår oprettelse af en ny onlinekanal og tilføjelse af den til organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="d2e88-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="d2e88-105">Du skal oprette organisationshierarkiet, før du kan oprette en ny onlinekanal.</span><span class="sxs-lookup"><span data-stu-id="d2e88-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="d2e88-106">Proceduren bruger USRT-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d2e88-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="d2e88-107">Opret en ny onlinekanal</span><span class="sxs-lookup"><span data-stu-id="d2e88-107">Create a new online channel</span></span>
1. <span data-ttu-id="d2e88-108">Gå til Detail og handel > Kanaler > Onlinebutikker.</span><span class="sxs-lookup"><span data-stu-id="d2e88-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="d2e88-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d2e88-109">Click New.</span></span>
3. <span data-ttu-id="d2e88-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="d2e88-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d2e88-111">Indtast eller vælg en værdi i feltet Lagersted.</span><span class="sxs-lookup"><span data-stu-id="d2e88-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="d2e88-112">Vælg en indstilling i feltet Lagertidszone.</span><span class="sxs-lookup"><span data-stu-id="d2e88-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="d2e88-113">Indtast eller vælg en værdi i feltet Standardkunde.</span><span class="sxs-lookup"><span data-stu-id="d2e88-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="d2e88-114">Indtast eller vælg en værdi i feltet Kundeadressekartotek.</span><span class="sxs-lookup"><span data-stu-id="d2e88-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="d2e88-115">Indtast eller vælg en værdi i feltet Betalingsbetingelse.</span><span class="sxs-lookup"><span data-stu-id="d2e88-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="d2e88-116">Indtast eller vælg en værdi i feltet Betalingsmåde.</span><span class="sxs-lookup"><span data-stu-id="d2e88-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="d2e88-117">Indtast eller vælg en værdi i feltet Profil til e-mailbesked.</span><span class="sxs-lookup"><span data-stu-id="d2e88-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="d2e88-118">Udvid sektionen Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="d2e88-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="d2e88-119">Indtast eller vælg en værdi i feltet BusinessUnit.</span><span class="sxs-lookup"><span data-stu-id="d2e88-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="d2e88-120">På samme måde kan du angive værdien for alle andre standarddimensioner.</span><span class="sxs-lookup"><span data-stu-id="d2e88-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="d2e88-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d2e88-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="d2e88-122">Føj onlinekanalen til organisationshierarkiet</span><span class="sxs-lookup"><span data-stu-id="d2e88-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="d2e88-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d2e88-123">Close the page.</span></span>
2. <span data-ttu-id="d2e88-124">Gå til Virksomhedsadministration > Organisationer > Organisationshierarkier.</span><span class="sxs-lookup"><span data-stu-id="d2e88-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="d2e88-125">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d2e88-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d2e88-126">Klik på Vis.</span><span class="sxs-lookup"><span data-stu-id="d2e88-126">Click View.</span></span>
5. <span data-ttu-id="d2e88-127">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="d2e88-127">Click Edit.</span></span>
    * <span data-ttu-id="d2e88-128">Du kan vælge en hvilket som helst hierarkinode, hvor du vil indsætte den nye kanal.</span><span class="sxs-lookup"><span data-stu-id="d2e88-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="d2e88-129">Klik på Indsæt.</span><span class="sxs-lookup"><span data-stu-id="d2e88-129">Click Insert.</span></span>
7. <span data-ttu-id="d2e88-130">Klik på Detailkanal.</span><span class="sxs-lookup"><span data-stu-id="d2e88-130">Click Retail channel.</span></span>
8. <span data-ttu-id="d2e88-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d2e88-131">Click OK.</span></span>
9. <span data-ttu-id="d2e88-132">Klik på Publicer for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d2e88-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="d2e88-133">Angiv en dato og et klokkeslæt i feltet Ikrafttrædelsesdato.</span><span class="sxs-lookup"><span data-stu-id="d2e88-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="d2e88-134">Klik på Publicer.</span><span class="sxs-lookup"><span data-stu-id="d2e88-134">Click Publish.</span></span>

