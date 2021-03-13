---
title: Aktivstyklister
description: I dette emne beskrives aktivstyklister i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetStandardSparePartsItemGroup, EntAssetObjectBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baaf516eb386c3cf63d72bf31800b8731121fe26
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019509"
---
# <a name="asset-boms"></a><span data-ttu-id="d763b-103">Aktivstyklister</span><span class="sxs-lookup"><span data-stu-id="d763b-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d763b-104">I dette emne beskrives aktivstyklister i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="d763b-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="d763b-105">På siden **Aktivstykliste** vises en oversigt over alle varer (reservedele og andre varer), der bruges på et aktiv i hele dets levetid.</span><span class="sxs-lookup"><span data-stu-id="d763b-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="d763b-106">Når du opretter et nyt aktiv, bør du overveje at oprette en aktivstykliste som en del af opsætningsproceduren.</span><span class="sxs-lookup"><span data-stu-id="d763b-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="d763b-107">På denne måde kan du spore varehistorikken for aktivet fra oprettelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="d763b-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="d763b-108">Når du har fuldført et vedligeholdelsesjob, og vareforbruget er registreret på en arbejdsordre, kan du spore forbruget af reservedele og andre varer, der bruges på aktivet.</span><span class="sxs-lookup"><span data-stu-id="d763b-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="d763b-109">Denne funktion giver dig mulighed for at beholde en komplet vareforbrugspost for alle dine aktiver.</span><span class="sxs-lookup"><span data-stu-id="d763b-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="d763b-110">Du kan for eksempel bruge posten til at overvåge, om en bestemt reservedel ofte udskiftes, eller til at holde styr på de reservedele eller andre elementer, der i øjeblikket bruges på et aktiv.</span><span class="sxs-lookup"><span data-stu-id="d763b-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="d763b-111">På en arbejdsordre kan vareforbruget omfatte både reservedele og andre ekstra varer, såsom smøremidler, bolte og pakninger.</span><span class="sxs-lookup"><span data-stu-id="d763b-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="d763b-112">En aktivstykliste kan opdateres automatisk på grundlag af opsætningen i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="d763b-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="d763b-113">Hvis der er oprettet en livscyklustilstand for arbejdsordren med henblik på at håndtere afsluttede eller fuldførte arbejdsordrer, og hvis indstillingen **Opdater aktivstykliste** for den pågældende arbejdsordres livscyklustilstand er angivet til **Ja** på siden **Arbejdsordrers livscyklustilstande**, vil alle varer, der anvendes til arbejdsordren, automatisk blive opdateret på siden **Aktivstykliste**, når arbejdsordren opdateres til den pågældende livscyklustilstand.</span><span class="sxs-lookup"><span data-stu-id="d763b-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="d763b-114">Du kan også opdatere en aktivstykliste manuelt ved at oprette nye varelinjer på siden **Aktivstykliste**.</span><span class="sxs-lookup"><span data-stu-id="d763b-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="d763b-115">På siden **Aktiv stykliste** kan du spore reservedelshistorikken for aktiver, når vareforbruget er blevet registreret på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="d763b-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="d763b-116">Hvis du vil bruge denne funktion, skal du vælge de varegrupper, der skal bruges til reservedelsregistreringen på siden **Reservedelsvaregrupper**.</span><span class="sxs-lookup"><span data-stu-id="d763b-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="d763b-117">Hvis du vil bruge funktionen aktivstykliste, skal du først oprette de påkrævede reservedelsvaregrupper.</span><span class="sxs-lookup"><span data-stu-id="d763b-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="d763b-118">Hvis du ønsker, at aktivstyklisten automatisk opdateres, når en arbejdsordre er fuldført, kan du dernæst oprette en livscyklustilstand for arbejdsordren for at håndtere den pågældende opdatering.</span><span class="sxs-lookup"><span data-stu-id="d763b-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="d763b-119">Konfigurer reservedelsvaregrupper</span><span class="sxs-lookup"><span data-stu-id="d763b-119">Set up spare parts item groups</span></span>

<span data-ttu-id="d763b-120">Opsætningen af reservedelshistorik er baseret på varegrupper, der er oprettet i modulet **Lager- og lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="d763b-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="d763b-121">I Styring af aktiver skal du oprette varegrupper, således at du kan spore reservedelshistorikken for varerne i de valgte varegrupper.</span><span class="sxs-lookup"><span data-stu-id="d763b-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="d763b-122">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Reservedelsvaregrupper**.</span><span class="sxs-lookup"><span data-stu-id="d763b-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="d763b-123">Vælg **Ny** for at oprette en varegruppe.</span><span class="sxs-lookup"><span data-stu-id="d763b-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="d763b-124">I feltet **Varegruppe** vælges gruppen.</span><span class="sxs-lookup"><span data-stu-id="d763b-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="d763b-125">Navnet på gruppen indtastes automatisk i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="d763b-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="d763b-126">Se og opdater aktivstyklister</span><span class="sxs-lookup"><span data-stu-id="d763b-126">View and update asset BOMs</span></span>

<span data-ttu-id="d763b-127">Når du bogfører vareforbruget på en arbejdsordre, kan du få vist det registrerede vareforbrug på siden **aktivstykliste**.</span><span class="sxs-lookup"><span data-stu-id="d763b-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="d763b-128">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="d763b-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="d763b-129">Vælg aktivet på listen, og vælg derefter **Aktivstykliste**.</span><span class="sxs-lookup"><span data-stu-id="d763b-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d763b-130">Hvis du vil se alle registreringer af vareforbrug, skal du vælge **Styring af aktiver** \> **Forespørgsler** \> **Aktiver** \> **Aktivstykliste**.</span><span class="sxs-lookup"><span data-stu-id="d763b-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="d763b-131">Vælg **Opdater aktivstykliste**.</span><span class="sxs-lookup"><span data-stu-id="d763b-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="d763b-132">Du kan føje aktiver, aktivtyper og ressourcer til opdateringen efter behov ved at vælge **Vælg.**</span><span class="sxs-lookup"><span data-stu-id="d763b-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="d763b-133">Vælg **OK** for at starte opdateringen.</span><span class="sxs-lookup"><span data-stu-id="d763b-133">Select **OK** to start the update.</span></span> <span data-ttu-id="d763b-134">Du kan også konfigurere funktionen Opdater som et batchjob.</span><span class="sxs-lookup"><span data-stu-id="d763b-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="d763b-135">Hvis du vil se flere oplysninger, der er relateret til varerne, kan du tilføje lagerdimensioner.</span><span class="sxs-lookup"><span data-stu-id="d763b-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="d763b-136">Vælg **Lager** \> **Vis dimensioner**, og markér derefter kasserne ud for de dimensioner, du ønsker at se.</span><span class="sxs-lookup"><span data-stu-id="d763b-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="d763b-137">Hvis du vil beholde denne opsætning for alle aktiver skal du på siden **Aktivstykliste** angive indstillingen **Gem opsætning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d763b-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="d763b-138">Hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges, skal du i relation til aktiver, jobtypestandarder, reservedele og arbejdsordrer vælge **Vare, hvor det er brugt**.</span><span class="sxs-lookup"><span data-stu-id="d763b-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="d763b-139">Hvis du kun vil se aktive varelinjer, skal du vælge **Se** \> **Nuværende**.</span><span class="sxs-lookup"><span data-stu-id="d763b-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="d763b-140">Hvis du vil se alle varelinjer, herunder linjer, hvor udløbsdatoen er tidligere end den aktuelle dato, skal du vælge **Se** \> **Alle**.</span><span class="sxs-lookup"><span data-stu-id="d763b-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="d763b-141">Når du har fuldført en arbejdsordre, anbefaler vi, at du opdaterer aktivstyklisten i overensstemmelse hermed, hvis nogle af de varer eller reservedele, der er relateret til det relaterede aktiv, er udløbet eller er blevet erstattet af andre varer eller reservedele.</span><span class="sxs-lookup"><span data-stu-id="d763b-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="d763b-142">Opret en ny varelinje i en aktivstykliste</span><span class="sxs-lookup"><span data-stu-id="d763b-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="d763b-143">Du kan oprette varelinjer for aktiver manuelt.</span><span class="sxs-lookup"><span data-stu-id="d763b-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="d763b-144">På siden **Aktivstykliste** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d763b-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="d763b-145">Vælg det **Aktiv**, du vil tilføje en varelinje for, i feltet aktiv.</span><span class="sxs-lookup"><span data-stu-id="d763b-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="d763b-146">Indtast et fortløbende linjenummer i feltet **Linjenummer**.</span><span class="sxs-lookup"><span data-stu-id="d763b-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="d763b-147">Indtast en ny startdato for varen i feltet **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="d763b-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="d763b-148">Hvis varen udløber, skal du angive en udløbsdato i feltet **Udløb**.</span><span class="sxs-lookup"><span data-stu-id="d763b-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="d763b-149">Vælg varen i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="d763b-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="d763b-150">Navnet indtastes automatisk i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="d763b-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="d763b-151">Angiv det forbrugte antal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="d763b-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="d763b-152">Feltet **Enhed** opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="d763b-152">The **Unit** field is automatically updated.</span></span>
