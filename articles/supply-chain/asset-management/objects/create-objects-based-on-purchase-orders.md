---
title: Oprette aktiver baseret på indkøbsordrer
description: Dette emne forklarer, hvordan du kan oprette en liste over aktivelementer, der kan bruges som grundlag for oprettelse af aktiver til vedligeholdelsesjob i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889019"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="743ae-103">Oprette aktiver baseret på indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="743ae-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="743ae-104">Dette emne forklarer, hvordan du kan oprette en liste over aktivelementer, der kan bruges som grundlag for oprettelse af aktiver til vedligeholdelsesjob i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="743ae-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="743ae-105">På basis af aktivelementerne kan du få vist en oversigt over de indkøbsordrelinjer, der er oprettet på disse elementer.</span><span class="sxs-lookup"><span data-stu-id="743ae-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="743ae-106">Formålet med denne funktion er nemt at kunne oprette et aktiv i Styring af aktiver baseret på en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="743ae-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="743ae-107">Først skal du oprette de varer, der skal bruges til at oprette aktiver ud fra en indkøbsordre, i **Aktivelementer**.</span><span class="sxs-lookup"><span data-stu-id="743ae-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="743ae-108">Når du har oprettet en indkøbsordrelinje, skal du oprette aktiverne i **Ventende aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="743ae-109">Det er muligt at beslutte, på hvilket stadie af indkøbsordren aktivet skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="743ae-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="743ae-110">Vælge aktivelementer</span><span class="sxs-lookup"><span data-stu-id="743ae-110">Select asset items</span></span>

1. <span data-ttu-id="743ae-111">Klik på **Styring af aktiver** > **Opsætning** > **Aktiver** > **Elementer**.</span><span class="sxs-lookup"><span data-stu-id="743ae-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="743ae-112">Klik på **Nyt** for at oprette et nyt aktivelement.</span><span class="sxs-lookup"><span data-stu-id="743ae-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="743ae-113">Vælg elementet i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="743ae-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="743ae-114">Når du forlader dette felt, indsættes varenavnet automatisk i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="743ae-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="743ae-115">Vælg en aktivtype for varen i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="743ae-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="743ae-116">Vælg aktivproducent og -model for varen.</span><span class="sxs-lookup"><span data-stu-id="743ae-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="743ae-117">Gem varen.</span><span class="sxs-lookup"><span data-stu-id="743ae-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="743ae-118">Oprette aktiver ud fra ventende aktiver</span><span class="sxs-lookup"><span data-stu-id="743ae-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="743ae-119">Klik på **Styring af aktiver** > **Almindeligt** > **Aktiver** > **Ventende aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="743ae-120">Du kan se en opdateret liste over indkøbsordrer baseret på de varer, som er valgt i **Aktivelementer**.</span><span class="sxs-lookup"><span data-stu-id="743ae-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="743ae-121">Du kan filtrere statussen for indkøbsordrer for at vælge, i hvilken livscyklusstilstand aktivet skal oprettes.</span><span class="sxs-lookup"><span data-stu-id="743ae-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="743ae-122">Du vil måske kun oprette aktiver, når der er bogført en produktkvittering på en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="743ae-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="743ae-123">Vælg **Referencenummer**-linket på en indkøbsordrelinje for at få vist detaljerede oplysninger om varen.</span><span class="sxs-lookup"><span data-stu-id="743ae-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="743ae-124">Hvis du vil redigere, hvilke dimensioner der vises i oversigtspanelet **Lagerdimensioner**, skal du klikke på knappen **Vis dimensioner** og foretage dine valg.</span><span class="sxs-lookup"><span data-stu-id="743ae-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="743ae-125">Hvis du vil oprette et aktiv, der er baseret på en indkøbsordrelinje, skal du markere afkrydsningsfeltet i kolonnen **Markér** for den pågældende linje på listesiden og klikke på **Opret aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="743ae-126">Der vises en meddelelse med oplysning om aktiv-id'et.</span><span class="sxs-lookup"><span data-stu-id="743ae-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="743ae-127">Vælg aktivet på listen **Alle aktiver**, og klik på knappen **Rediger** for at føje yderligere oplysninger til aktivet.</span><span class="sxs-lookup"><span data-stu-id="743ae-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="743ae-128">Hvis du vil slette en linje i **Ventende aktiver**, fordi du ikke vil oprette et aktiv, skal du markere afkrydsningsfeltet i kolonnen **Markér** for den pågældende linje og klikke på **Kassér ventende aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="743ae-129">Der vises en meddelelse med oplysning om aktiv-id'et.</span><span class="sxs-lookup"><span data-stu-id="743ae-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="743ae-130">Du sletter ikke indkøbsordren eller salgsordren, men kun den post, som du kunne have oprettet et aktiv for i **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="743ae-131">Alle produktdimensioner (størrelse, farve, konfiguration osv.) overføres automatisk til aktivattributterne.</span><span class="sxs-lookup"><span data-stu-id="743ae-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="743ae-132">Sporingsdimensioner (serienummer) gemmes direkte på aktivet, når aktivet oprettes.</span><span class="sxs-lookup"><span data-stu-id="743ae-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="743ae-133">Finde ventende aktiver</span><span class="sxs-lookup"><span data-stu-id="743ae-133">Find pending assets</span></span>

<span data-ttu-id="743ae-134">Du kan beregne **antal ventende aktiver** for at kontrollere, om der er ventende aktiver.</span><span class="sxs-lookup"><span data-stu-id="743ae-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="743ae-135">For eksempel kan denne funktion bruges til at modtage en besked, hver gang et ventende aktiv er klar til at blive oprettet som et aktiv.</span><span class="sxs-lookup"><span data-stu-id="743ae-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="743ae-136">Klik på **Styring af aktiver** > **Periodisk** > **Aktiver** > **Antal ventende aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="743ae-137">Klik på **OK** for at køre jobbet og opdatere listen i **Ventende aktiver**.</span><span class="sxs-lookup"><span data-stu-id="743ae-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="743ae-138">Du kan konfigurere dette job til at køre som et batchjob, f.eks. en gang om dagen.</span><span class="sxs-lookup"><span data-stu-id="743ae-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="743ae-139">**Advarsel!** Hvis data ændres på en indkøbsordre, *efter* at du har oprettet et aktiv baseret på det pågældende element, afspejles disse ændringer ikke på aktivet.</span><span class="sxs-lookup"><span data-stu-id="743ae-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
