---
title: Integrere aktivstyring med anlægsaktiver
description: I dette emne forklares det, hvordan du kan integrere aktivstyrings- og anlægsaktivmoduler, så anlægsaktiver kan knyttes til vedligeholdelsesaktiver.
author: kamaybac
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a45bf1f62cdcc8abed2ec157a223e7f3fddec7ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809848"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="9b609-103">Integrere aktivstyring med anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="9b609-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b609-104">Hvis du integrerer **Aktivstyring**- og **Anlægsaktiv**-moduler, kan du knytte anlægsaktiver til vedligeholdelsesaktiver.</span><span class="sxs-lookup"><span data-stu-id="9b609-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="9b609-105">Brugere med anlægsaktiver kan derefter oprette et vedligeholdelsesaktiv ud fra et nyt eller eksisterende anlægsaktiv, og brugere af aktivstyring kan knytte et vedligeholdelsesaktiv til et eksisterende anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="9b609-106">Denne funktion gør det også nemt for brugere med anlægsaktiver at få vist de omkostninger, der blev bogført fra arbejdsordrer for relaterede vedligeholdelsesaktiver.</span><span class="sxs-lookup"><span data-stu-id="9b609-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="9b609-107">I dette emne refererer *vedligeholdelsesaktiver* til aktiver fra modulet **Aktivstyring**, og *anlægsaktiver* henviser til aktiver fra modulet **Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="9b609-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="9b609-108">Angive en standardplacering for nye vedligeholdelsesaktiver, der oprettes ud fra anlægsaktiver (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="9b609-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="9b609-109">Med denne valgfrie konfiguration kan du angive en standardarbejdssted for nye vedligeholdelsesaktiver, der oprettes ud fra anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="9b609-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="9b609-110">Du udfører typisk denne konfiguration kun én gang, hvis du overhovedet fuldfører den.</span><span class="sxs-lookup"><span data-stu-id="9b609-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="9b609-111">Benyt denne fremgangsmåde for at fuldføre konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="9b609-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="9b609-112">Gå til **Aktivstyring \> Opsætning \> Parametre til aktivstyring**.</span><span class="sxs-lookup"><span data-stu-id="9b609-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="9b609-113">Under fanen **Anlægsaktiver** i feltet **Arbejdssted** skal du vælge standardstedet.</span><span class="sxs-lookup"><span data-stu-id="9b609-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="9b609-114">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="9b609-115">Arbejde med integrerede vedligeholdelsesaktiver og anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="9b609-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="9b609-116">Dette afsnit indeholder en samling procedurer, der viser forskellige måder, du kan arbejde med funktionerne til integreret styring af aktiver og anlægsaktiver på.</span><span class="sxs-lookup"><span data-stu-id="9b609-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="9b609-117">Knytte et eksisterende vedligeholdelsesaktiv til et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="9b609-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="9b609-118">Knyt et eksisterende vedligeholdelsesaktiv til et anlægsaktiv ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-119">Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).</span><span class="sxs-lookup"><span data-stu-id="9b609-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="9b609-120">Vælg et aktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-120">Select an asset.</span></span>
1. <span data-ttu-id="9b609-121">I oversigtspanelet **Anlægsaktiv** skal du vælge et eksisterende anlægsaktiv i feltet **Nummer på anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="9b609-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="9b609-122">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="9b609-123">Se det anlægsaktiv, der er tilknyttet et valgt vedligeholdelsesaktiv</span><span class="sxs-lookup"><span data-stu-id="9b609-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="9b609-124">Du kan se det anlægsaktiv, der er tilknyttet et valgt vedligeholdelsesaktiv, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-125">Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).</span><span class="sxs-lookup"><span data-stu-id="9b609-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="9b609-126">Vælg et aktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-126">Select an asset.</span></span>
1. <span data-ttu-id="9b609-127">I oversigtspanelet **Anlægsaktiv** skal du vælge linket i feltet **Nummer på anlægsaktiv**.</span><span class="sxs-lookup"><span data-stu-id="9b609-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="9b609-128">Siden **Anlægsaktiver** for det valgte aktiv åbnes.</span><span class="sxs-lookup"><span data-stu-id="9b609-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="9b609-129">(Denne side findes typisk på **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**).</span><span class="sxs-lookup"><span data-stu-id="9b609-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="9b609-130">Se det vedligeholdelsesaktiv, der er tilknyttet et valgt anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="9b609-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="9b609-131">Du kan se det vedligeholdelsesaktiv, der er tilknyttet et valgt anlægsaktiv, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-132">Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="9b609-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="9b609-133">Vælg et aktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-133">Select an asset.</span></span>
1. <span data-ttu-id="9b609-134">Vælg **Vedligeholdelsesaktiv** i gruppen **Vis** under fanen **Styring af aktiver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="9b609-135">Siden **Vedligeholdelsesaktiv** for det aktiv, der er tilknyttet det valgte anlægsaktiv, åbnes.</span><span class="sxs-lookup"><span data-stu-id="9b609-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="9b609-136">(Denne side findes typisk på **Styring af aktiver \> Aktiver \> Alle aktiver**).</span><span class="sxs-lookup"><span data-stu-id="9b609-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="9b609-137">Se vedligeholdelsesomkostninger, der er tilknyttet et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="9b609-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="9b609-138">Arbejdsordrer for aktivstyring kan bogføres for vedligeholdelsesaktiver, og hver af disse arbejdsordrer har normalt en omkostning.</span><span class="sxs-lookup"><span data-stu-id="9b609-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="9b609-139">Når et anlægsaktiv er tilknyttet et vedligeholdelsesaktiv, kan du gå direkte fra anlægsaktivet for at få vist de relaterede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9b609-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="9b609-140">Du kan se de vedligeholdelsesomkostninger, der er tilknyttet et valgt anlægsaktiv, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-141">Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="9b609-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="9b609-142">Vælg et aktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-142">Select an asset.</span></span>
1. <span data-ttu-id="9b609-143">Vælg **Vedligeholdelsesomkostning** i gruppen **Vis** under fanen **Styring af aktiver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="9b609-144">Siden **Vedligeholdelsesomkostning** åbnes og viser de relaterede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="9b609-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="9b609-145">Oprette et nyt vedligeholdelsesaktiv til et eksisterende anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="9b609-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="9b609-146">Opret et nyt vedligeholdelsesaktiv til et eksisterende anlægsaktiv ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-147">Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="9b609-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="9b609-148">Vælg et aktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-148">Select an asset.</span></span>
1. <span data-ttu-id="9b609-149">Vælg **Opret vedligeholdelsesaktiv** i gruppen **Nyt** under fanen **Styring af aktiver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="9b609-150">(Hvis denne indstilling ikke er tilgængelig, er et vedligeholdelsesaktiv muligvis allerede knyttet til det valgte anlægsaktiv).</span><span class="sxs-lookup"><span data-stu-id="9b609-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="9b609-151">Afslut oprettelsen af aktivet som beskrevet under [Oprette et aktiv](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="9b609-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="9b609-152">Oprette et nyt anlægsaktiv og føje et eksisterende vedligeholdelsesaktiv til det</span><span class="sxs-lookup"><span data-stu-id="9b609-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="9b609-153">Opret et nyt anlægsaktiv, og føj et nyt vedligeholdelsesaktiv til det ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="9b609-154">Gå til **Anlægsaktiver \> Anlægsaktiver \> Anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="9b609-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="9b609-155">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9b609-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b609-156">Afslut oprettelsen af anlægsaktivet som beskrevet under [Oprette et anlægsaktiv](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="9b609-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="9b609-157">Vælg **Opret vedligeholdelsesaktiv** i gruppen **Nyt** under fanen **Styring af aktiver** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="9b609-158">Afslut oprettelsen af aktivet som beskrevet under [Oprette et aktiv](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="9b609-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="9b609-159">Fjerne tilknytningen mellem to aktiver</span><span class="sxs-lookup"><span data-stu-id="9b609-159">Remove the association between two assets</span></span>

<span data-ttu-id="9b609-160">I nogle tilfælde kan det være nødvendigt at fjerne tilknytningen mellem et vedligeholdelsesaktiv og dets anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="9b609-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="9b609-161">Hvis du f.eks. vil [oprette et nyt vedligeholdelsesaktiv](#new-maintenance-from-fixed) ud fra et anlægsaktiv, skal du først fjerne en eksisterende tilknytning.</span><span class="sxs-lookup"><span data-stu-id="9b609-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="9b609-162">Fjern en eksisterende tilknytning mellem et vedligeholdelsesaktiv og et anlægsaktiv ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="9b609-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="9b609-163">Gå til **Styring af aktiver \> Aktiver \> Alle aktiver** (eller **Aktive aktiver**).</span><span class="sxs-lookup"><span data-stu-id="9b609-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="9b609-164">Find og åbn anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="9b609-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="9b609-165">I oversigtspanelet **Anlægsaktiv** skal du fjerne værdien fra feltet **Arbejdssted**.</span><span class="sxs-lookup"><span data-stu-id="9b609-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="9b609-166">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="9b609-166">On the Action Pane, select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]