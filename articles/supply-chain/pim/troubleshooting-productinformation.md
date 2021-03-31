---
title: Foretage fejlfinding af produktoplysninger
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktoplysninger.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223356"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="8cbb7-103">Foretage fejlfinding af produktoplysninger</span><span class="sxs-lookup"><span data-stu-id="8cbb7-103">Troubleshoot product information</span></span>

<span data-ttu-id="8cbb7-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="8cbb7-105">Jeg kan ikke slette et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-106">Issue description</span></span>

<span data-ttu-id="8cbb7-107">Du kan kun slette et frigivet produkt og alle dets varianter, hvis der ikke er relaterede transaktioner for det frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-108">Issue resolution</span></span>

<span data-ttu-id="8cbb7-109">Udfør følgende trin for at slette en frigivet produkt eller produktmaster.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="8cbb7-110">Luk alle åbne transaktioner for varerne.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="8cbb7-111">Reducer lagerbeholdningen til 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="8cbb7-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="8cbb7-112">Udfør lagerlukning.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="8cbb7-113">Slet alle produktvarianter for den produktmaster, du vil slette.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="8cbb7-114">Kan jeg ændre varenummeret for et frigivet produkt?</span><span class="sxs-lookup"><span data-stu-id="8cbb7-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="8cbb7-115">I de fleste tilfælde kan du ikke redigere varenumre for frigivne produkter, fordi ændringen vil medføre, at dataene bliver beskadiget.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="8cbb7-116">Du kan kun redigere varenummeret, hvis du skal reparere databeskadigelse, som blev forårsaget af en tidligere omdøbning af den primære nøgle for det frigivne produkt, som angivet på listen over [fjernede eller udfasede funktioner til Finance and Operations 10.0.0 med Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="8cbb7-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="8cbb7-117">Hvis du vil have mulighed for at redigere varenumre for frigivne produkter, skal du [stemme for denne ide i portalen Ideer](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="8cbb7-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="8cbb7-118">Standardrydningsprincippet fra produktet angives ikke på styklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-119">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-119">Issue description</span></span>

<span data-ttu-id="8cbb7-120">Når du føjer en vare til en styklistelinje, bruger systemet ikke de standardoplysninger om rydningsprincippet, der er konfigureret for varen.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="8cbb7-121">Det vil sige, at rydningsprincippet fra varen ikke vises på siden **Styklistelinje**.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-122">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-122">Issue resolution</span></span>

<span data-ttu-id="8cbb7-123">Hvis du angiver et rydningsprincip på en styklistelinje, vil det gælde for den pågældende styklistelinje.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="8cbb7-124">Men hvis træk rydningsprincippet er tomt, eller hvis det ikke er angivet på en styklistelinje, gælder det rydningsprincip, der er angivet for varen, stadig for den pågældende styklistelinje, selvom den ikke vises på styklistelinjen.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="8cbb7-125">Standardlogikken for andre funktioner i Microsoft Dynamics 365 Supply Chain Management fungerer normalt ikke på denne måde.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="8cbb7-126">Men den aktuelle funktionalitet kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="8cbb7-127">Ellers vil nogle af de eksisterende tilpasninger, der er afhængige af den, være brudte.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="8cbb7-128">Du kan bruge systemet til at gemme dublerede stregkoder for forskellige varer eller for den samme vare, der har forskellige dimensioner.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="8cbb7-129">Systemet gennemtvinger ikke entydige stregkoder i øjeblikket, og tilføjelsen af denne begrænsning vil være en nyskabende ændring.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="8cbb7-130">Microsoft har faktisk bevis på, at nogle eksisterende kundeinstallationer vil blive beskadiget af denne ændring.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="8cbb7-131">Vi vil dog overveje en bredere designændring for at aktivere denne funktion i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="8cbb7-132">Jeg modtager følgende fejlmeddelelse, når jeg redigerer varepostskabeloner: "Lagerlokationen kan ikke oprettes, fordi varen ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="8cbb7-133">Til lagervarer skal indstillingen Lagerført produkt på den tilknyttede varemodelgruppe vælges".</span><span class="sxs-lookup"><span data-stu-id="8cbb7-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-134">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-134">Issue description</span></span>

<span data-ttu-id="8cbb7-135">Dette problem opstår, hvis du følger disse trin i et forsøg på at oprette en skabelon for en vare, der ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="8cbb7-136">Åbn et frigivet produkt, der ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="8cbb7-137">I handlingsruden skal du under fanen **Indstillinger** vælge **Postoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="8cbb7-138">Vælg **Regnskabsskabelon** i dialogboksen **Postoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="8cbb7-139">I dette tilfælde får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="8cbb7-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="8cbb7-140">Lagerlokationen kan ikke oprettes, da varen ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="8cbb7-141">Til lagervarer skal indstillingen Lagerført produkt på den tilknyttede varemodelgruppe vælges.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-142">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-142">Issue resolution</span></span>

<span data-ttu-id="8cbb7-143">Processen med at oprette produktskabeloner kræver en ekstra produktspecifik logik.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="8cbb7-144">Du kan derfor ikke bruge standardknappen **Regnskabsskabelon** til dette formål.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="8cbb7-145">Ellers skal du udføre disse trin.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="8cbb7-146">Åbn et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-146">Open a released product.</span></span>
1. <span data-ttu-id="8cbb7-147">I gruppen **Ny** under fanen **Produkt** i handlingsruden skal du vælge **Skabelon \> Opret delt skabelon**.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="8cbb7-148">Hjælp-standardtekst, der tilføjes i produktattributter, angives ikke i et frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="8cbb7-149">En beskrivelse og hjælp-tekst, der tilføjes i produktattributterne, kan ikke ses eller angives som standard i de frigivne produkter.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="8cbb7-150">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="8cbb7-151">Det standardantal, der angives, er forskelligt, når det registreres fra en stykliste, og når det registreres fra en styklisteversion.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-152">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-152">Issue description</span></span>

<span data-ttu-id="8cbb7-153">Når du føjer en vare til en stykliste, angives antallet som standard til 1 i stedet for det antal, der er defineret i feltet **Min. ordreantal** på siden **Standardindstillinger for ordre** for et valgt produkt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="8cbb7-154">Men når du tilføjer en vare fra en styklisteversion, og varen og varianten vælges, tager det antal, der angives som standard, det minimumantal, der er angivet i standardordreindstillingerne for de specifikke dimensioner, i betragtning.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-155">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-155">Issue resolution</span></span>

<span data-ttu-id="8cbb7-156">Denne funktionsmåde forventes.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-156">This behavior is expected.</span></span> <span data-ttu-id="8cbb7-157">Men det faktum, at logikken er forskellig i styklisten og styklisteversionen, er et kendt problem.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="8cbb7-158">Denne funktionsmåde ændres dog ikke, fordi en ændring kan påvirke mange forskellige kundescenarier.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="8cbb7-159">Jeg kan ikke ændre de vedhæftede billeder, der er overført fra dataobjektet for vedhæftede filer i produktdokumentet, i de frigivne produktoplysninger.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-160">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-160">Issue description</span></span>

<span data-ttu-id="8cbb7-161">Dette problem kan opstå, når du knytter et billede til en vare ved hjælp af dataobjektet *Vedhæftede filer i produktdokument*.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="8cbb7-162">I dette tilfælde vises varebilledet for varen.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="8cbb7-163">Men hvis du vælger **Skift billede**, vises intet på listen over overførte billeder.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="8cbb7-164">Der vises desuden ingen vedhæftede filer for varen.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-165">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-165">Issue resolution</span></span>

<span data-ttu-id="8cbb7-166">Enheden *EcoResProductDocumentAttachmentEntity* (*Vedhæftede filer i produktdokument*) importerer vedhæftede dokumenter for *produkter*, men ikke for *frigivne produkter*.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="8cbb7-167">(Frigivne produkter kaldes også *varer*). Hvis du vil have vist vedhæftede filer for en vare på siden **Frigivne produktdetaljer**, skal du bruge enheden *EcoResReleasedProductDocumentAttachmentEntity* (*Vedhæftede frigivne produktdokumenter*) i stedet.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="8cbb7-168">Microsoft Flow-connectoren viser følgende fejlmeddelelse: "Opdatering ikke tilladt for feltet 'ProductNumber'".</span><span class="sxs-lookup"><span data-stu-id="8cbb7-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-169">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-169">Issue description</span></span>

<span data-ttu-id="8cbb7-170">Dette problem opstår, hvis du forsøger at opdatere feltet **Produktnummer** ved hjælp af *Frigivne produkter*-enhed V2 og Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-171">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-171">Issue resolution</span></span>

<span data-ttu-id="8cbb7-172">Denne funktionsmåde forventes.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-172">This behavior is expected.</span></span> <span data-ttu-id="8cbb7-173">Muligheden for at redigere produktnummeret for et frigivet produkt er fjernet i Dynamics 365 Finance and Operations 10.0.0 med Platform Update 24 for at hjælpe med at forhindre databeskadigelse.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="8cbb7-174">I undtagelsestilfælde, hvor du har brug for at reparere databeskadigelse forårsaget af en tidligere omdøbning af primærnøglen for et frigivet produkt, kan du kontakte Microsoft Support for at anmode om midlertidig fjernelse af denne begrænsning.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="8cbb7-175">Jeg kan ikke oprette en frigivet produktvariant i en anden juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-176">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-176">Issue description</span></span>

<span data-ttu-id="8cbb7-177">Hvis du forsøger at frigive en produktmaster uden varianter og derefter opretter varianterne i de enkelte juridiske enheder (firma), efterhånden som de er påkrævede, kan du ikke frigive varianterne ved hjælp af variantforslag.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="8cbb7-178">Du kan heller ikke oprette varianterne manuelt.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-179">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-179">Issue resolution</span></span>

<span data-ttu-id="8cbb7-180">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-180">This behavior is by design.</span></span> <span data-ttu-id="8cbb7-181">Relationen mellem en produktmaster og de dimensioner, masteren kan tage, opbevares på et delt niveau.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="8cbb7-182">Derfor kan du ikke oprette de tilgængelige dimensioner for en delt produktmaster i den specifikke juridiske enhed, hvor disse dimensioner frigives, og derefter replikere processen i hver juridiske enhed, hvor dimensionerne er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="8cbb7-183">Du skal i stedet ændre din frigivelsesproces for at kunne tilpasse den designede proces.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="8cbb7-184">Her er processen for frigivelse af produkter.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="8cbb7-185">Opret den delte produktmaster og de dimensioner, der kan frigives til de juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="8cbb7-186">Frigiv produkterne til de juridiske enheder ved enten at bruge variantforslag eller ved manuelt at tilføje de kombinationer, der skal frigives.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="8cbb7-187">Du kan også oprette et frigivet produkt direkte.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="8cbb7-188">Når jeg frigiver en variant i et andet firma, får jeg vist følgende fejlmeddelelse: "Der er allerede oprettet en produktvariant med de angivne dimensioner".</span><span class="sxs-lookup"><span data-stu-id="8cbb7-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8cbb7-189">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8cbb7-189">Issue description</span></span>

<span data-ttu-id="8cbb7-190">Hvis en produktvariant allerede er frigivet i firma A, og du forsøger at frigive den i firma B ved hjælp af knappen **Ny** på siden **Frigivne produktvarianter**, får du vist følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="8cbb7-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="8cbb7-191">Produktvariant med angivne dimensioner er allerede oprettet.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8cbb7-192">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8cbb7-192">Issue resolution</span></span>

<span data-ttu-id="8cbb7-193">Knappen **Ny** på siden **Frigivne produktvarianter** opretter varianten og frigiver den i firmaets kontekst.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="8cbb7-194">Hvis varianten allerede er oprettet, kan du ikke bruge knappen **Ny** til at frigive den i et andet firma.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="8cbb7-195">Du kan løse problemet ved at åbne **Produktmaster**-siden og vælge **Frigiv produkt** for at frigive den eksisterende variant i det ønskede firma.</span><span class="sxs-lookup"><span data-stu-id="8cbb7-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]