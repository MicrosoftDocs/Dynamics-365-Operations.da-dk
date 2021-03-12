---
title: Konfigurer konsignation
description: Dette emne forklarer, hvordan du konfigurerer indgående konsignationslageroperationer.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bcc5ce7d9b9031fe8e9589798e07162106277767
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987273"
---
# <a name="set-up-consignment"></a><span data-ttu-id="e3d8b-103">Konfigurer konsignation</span><span class="sxs-lookup"><span data-stu-id="e3d8b-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3d8b-104">Dette emne forklarer, hvordan du konfigurerer indgående konsignationslageroperationer.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="e3d8b-105">Konsignationslager er lager, der ejes af en leverandør, men lagret på dit sted.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="e3d8b-106">Når du er klar til at forbruge eller bruge af lageret, overtager du ejerskabet af lageret.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="e3d8b-107">I dette emne beskrives den opsætning, der er nødvendig for at aktivere konsignationsprocesser.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="e3d8b-108">Yderligere oplysninger om konsignationsprocesser findes under [Opsætning af konsignation](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="e3d8b-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="e3d8b-109">Lagerejere</span><span class="sxs-lookup"><span data-stu-id="e3d8b-109">Inventory owners</span></span>
<span data-ttu-id="e3d8b-110">For at registrere fysisk indgående konsignationslager skal du definere en leverandørejer.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="e3d8b-111">Dette gøres på siden **Lagerejer**.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="e3d8b-112">Når du vælger en **kreditorkonto**, oprettes standardværdier for felterne **Navn** og **Ejer**.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="e3d8b-113">Værdien i feltet **Ejer** vil være synlig for leverandøren, så kan du ændre den, hvis dine kontonavne for kreditorer ikke er let for eksterne personer at genkende.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="e3d8b-114">Det er muligt at redigere feltet **Ejer**, men kun indtil tidspunktet, når du gemmer posten **Lagerejer**.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="e3d8b-115">Feltet **Navn** udfyldes med navnet på den part, der er tilknyttet kreditorkontoen, og dette kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="e3d8b-116">[![lagerejere](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="e3d8b-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="e3d8b-117">Sporingsdimensionsgruppe</span><span class="sxs-lookup"><span data-stu-id="e3d8b-117">Tracking dimension group</span></span>
<span data-ttu-id="e3d8b-118">Varer, der skal bruges i konsignationsprocesser, skal være tilknyttet en **sporingsdimensionsgruppe**, hvor dimensionen **Ejer** er sat til **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="e3d8b-119">Ejerdimensionen har altid **Fysisk lager** og **Økonomisk lager** som valgte indstillinger.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="e3d8b-120">**Disponer pr. dimension** er aldrig markeret.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="e3d8b-121">[![sporingsdimensionsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="e3d8b-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="e3d8b-122">Ændringskladde for beholdningsejerskab</span><span class="sxs-lookup"><span data-stu-id="e3d8b-122">Inventory ownership change journal</span></span>
<span data-ttu-id="e3d8b-123">Kladden **Ændring af beholdningsejerskab** bruges til at registrere overdragelse af ejendomsretten til konsignationslager fra leverandøren til den juridiske enhed, der bruger den.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="e3d8b-124">Det skal være identificeret med et lagerkladdenavn som enhver lagerkladde.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="e3d8b-125">Disse navne oprettes på siden **Lagerkladdenavne**, og **Kladdetype** skal være indstillet til **Ændring af ejerskab**.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="e3d8b-126">[![ændringskladde for beholdningsejerskab](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="e3d8b-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="e3d8b-127">Leverandørsamarbejde i konsignationsprocesser</span><span class="sxs-lookup"><span data-stu-id="e3d8b-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="e3d8b-128">Hvis dine kreditorer bruger leverandørsamarbejde som interface, kan de bruge dette til at overvåge forbruget af lageret på dit sted.</span><span class="sxs-lookup"><span data-stu-id="e3d8b-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="e3d8b-129">Yderligere oplysninger om opsætning af leverandører til at anvende leverandørsamarbejde findes i [Sikkerhed for bruger af leverandørportal](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="e3d8b-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>
