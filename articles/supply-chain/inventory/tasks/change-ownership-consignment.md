---
title: Ændre ejerskabet til konsignationslager ud fra produktionsbehov
description: Denne fremgangsmåde viser, hvordan du ændrer ejeren af konsignationslageret fra leverandøren til din juridiske enhed, når der er behov for lageret i produktionen.
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204234"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="aeddd-103">Ændre ejerskabet til konsignationslager ud fra produktionsbehov</span><span class="sxs-lookup"><span data-stu-id="aeddd-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aeddd-104">Denne fremgangsmåde viser, hvordan du ændrer ejeren af konsignationslageret fra leverandøren til din juridiske enhed, når der er behov for lageret i produktionen.</span><span class="sxs-lookup"><span data-stu-id="aeddd-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="aeddd-105">Denne ændring af ejerskabet sker ved at oprette og bogføre en ændringskladde for lagerejerskab.</span><span class="sxs-lookup"><span data-stu-id="aeddd-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="aeddd-106">Ændringskladdelinjer for ejerskab kan oprettes manuelt, eller som vist i denne registrering, baseret på eksisterende produktionsbehov.</span><span class="sxs-lookup"><span data-stu-id="aeddd-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="aeddd-107">Typisk udfører en tilsynsførende denne opgave.</span><span class="sxs-lookup"><span data-stu-id="aeddd-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="aeddd-108">Du kan bruge denne procedure på USMF-demodatafirmaet eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="aeddd-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="aeddd-109">Hvis du bruger dine egne data, skal du kontrollere, at du har følgende forudsætninger: navnet på en lagerbeholdning, der er blevet oprettet til ændring af lagerejerskab, fysisk registrerede kreditorejede disponible varer og en eller flere produktionsordrelinjer for materialet.</span><span class="sxs-lookup"><span data-stu-id="aeddd-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="aeddd-110">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="aeddd-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="aeddd-111">Udgående konsignationsprocesser understøttes ikke som standard, og automatisk behandling af ejerskabskladde understøttes ikke.</span><span class="sxs-lookup"><span data-stu-id="aeddd-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="aeddd-112">Opret en lagerejerskabskladde</span><span class="sxs-lookup"><span data-stu-id="aeddd-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="aeddd-113">Gå til Lagerstyring > Kladdeposteringer > Elementer > Ændring af lagerejerskab.</span><span class="sxs-lookup"><span data-stu-id="aeddd-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="aeddd-114">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="aeddd-114">Click New.</span></span>
    * <span data-ttu-id="aeddd-115">Kladden for ændring af beholdningsejerskab bruges til at ændre ejeren af konsignationslager fra leverandøren til den aktuelle juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="aeddd-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="aeddd-116">Denne ændring af ejerskabet sker ved at frigive den disponible lagerbeholdning, der ejes af leverandøren, og derefter modtage dette lager i den aktuelle juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="aeddd-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="aeddd-117">Indtast eller vælg en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="aeddd-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="aeddd-118">Du kan kun vælge lagerkladdenavne, der har kladdetypen Ændring af ejerskab.</span><span class="sxs-lookup"><span data-stu-id="aeddd-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="aeddd-119">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="aeddd-119">Click OK.</span></span>
5. <span data-ttu-id="aeddd-120">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="aeddd-120">Click Functions.</span></span>
6. <span data-ttu-id="aeddd-121">Klik på Opret kladdelinjer ud fra produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="aeddd-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="aeddd-122">Du kan starte processen til ændring af ejerskab ved at forespørge alle produktionslinjer, der er behov for forbrug af råvarer.</span><span class="sxs-lookup"><span data-stu-id="aeddd-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="aeddd-123">I Statusser, der skal medtages for lagerafgang skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="aeddd-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="aeddd-124">Brug denne indstilling til at filtrere efter afgangsstatus for lagerposteringer.</span><span class="sxs-lookup"><span data-stu-id="aeddd-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="aeddd-125">Du kan for eksempel oprette kladdelinjer for lager, der har statusserne Plukket og Reserveret fysisk.</span><span class="sxs-lookup"><span data-stu-id="aeddd-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="aeddd-126">Udvid posterne for at inkludere sektion.</span><span class="sxs-lookup"><span data-stu-id="aeddd-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="aeddd-127">I dette afsnit kan du anvende yderligere filtrering.</span><span class="sxs-lookup"><span data-stu-id="aeddd-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="aeddd-128">Du kan for eksempel vælge en dato for en bestemt råvare.</span><span class="sxs-lookup"><span data-stu-id="aeddd-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="aeddd-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="aeddd-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="aeddd-130">Bogfør ændringskladden for beholdningsejerskab</span><span class="sxs-lookup"><span data-stu-id="aeddd-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="aeddd-131">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="aeddd-131">Click Post.</span></span>
    * <span data-ttu-id="aeddd-132">Når kladden er bogført, frigives det lager, der ejes af leverandøren, ved hjælp af henvisningen "Ændring af ejerskab".</span><span class="sxs-lookup"><span data-stu-id="aeddd-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="aeddd-133">Lagerbeholdningen modtages derefter som disponibel ved hjælp af den lagertransaktion, der opdateres på produktkvitteringen for indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="aeddd-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="aeddd-134">Bemærk, at det kun er transaktioner, der vedrører den bogførte kladde, der oprettes.</span><span class="sxs-lookup"><span data-stu-id="aeddd-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="aeddd-135">Der oprettes ingen forventede lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="aeddd-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="aeddd-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="aeddd-136">Click OK.</span></span>
3. <span data-ttu-id="aeddd-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="aeddd-137">Close the page.</span></span>

