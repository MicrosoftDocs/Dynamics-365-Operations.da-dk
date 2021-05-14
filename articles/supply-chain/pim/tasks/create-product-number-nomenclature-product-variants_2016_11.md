---
title: Oprette et produktnummernomenklatur for konfigurerede produktvarianter
description: Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921005"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="58a47-103">Oprette et produktnummernomenklatur for konfigurerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="58a47-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58a47-104">Denne procedure viser, hvordan du konfigurerer en nomenklatur for produktnumre for konfigurerede produktvarianter, og hvordan den kan knyttes til en produktmaster, der kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="58a47-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="58a47-105">Denne fremgangsmåde viser også, hvordan du kan opbygge en konfigurationsnomenklatur en produktkonfigurations modelkomponent.</span><span class="sxs-lookup"><span data-stu-id="58a47-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="58a47-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="58a47-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="58a47-107">Den nye nomenklatur for produktnumre er knyttet til produktmasteren D0004.</span><span class="sxs-lookup"><span data-stu-id="58a47-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="58a47-108">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="58a47-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="58a47-109">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="58a47-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="58a47-110">Gå til **Administration af produktoplysninger \> Opsætning \> Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="58a47-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="58a47-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="58a47-111">Select **New**.</span></span>
1. <span data-ttu-id="58a47-112">Skriv en værdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="58a47-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="58a47-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="58a47-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="58a47-114">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-114">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-115">Vælg **Produktmasternummer**.</span><span class="sxs-lookup"><span data-stu-id="58a47-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="58a47-116">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-116">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-117">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="58a47-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="58a47-118">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-119">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="58a47-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="58a47-120">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-120">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-121">Vælg **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="58a47-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="58a47-122">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="58a47-123">Tildel nomenklaturen for produktnummer til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="58a47-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="58a47-124">Gå til **Administration af produktoplysninger \> Produkter \> Produktmastere**.</span><span class="sxs-lookup"><span data-stu-id="58a47-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="58a47-125">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="58a47-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="58a47-126">Filtrer f.eks. efter feltet **Produktnummer** med værdien "D".</span><span class="sxs-lookup"><span data-stu-id="58a47-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="58a47-127">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="58a47-128">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="58a47-128">Select **Edit**.</span></span>
1. <span data-ttu-id="58a47-129">Vælg *Ja* i feltet **Brug nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="58a47-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="58a47-130">Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.</span><span class="sxs-lookup"><span data-stu-id="58a47-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-131">Close the page.</span></span>
1. <span data-ttu-id="58a47-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="58a47-133">Opret nomenklatur for en komponent i en produktkonfigurationsmodel</span><span class="sxs-lookup"><span data-stu-id="58a47-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="58a47-134">Gå til **Administration af produktoplysninger \> Produkter \> Produktkonfigurationsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="58a47-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="58a47-135">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="58a47-136">Vælg linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="58a47-137">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="58a47-137">Select **Edit**.</span></span>
1. <span data-ttu-id="58a47-138">Vælg *Ja* i feltet **Brug konfigurationsnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="58a47-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="58a47-139">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-139">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-140">Vælg **Attributværdi**.</span><span class="sxs-lookup"><span data-stu-id="58a47-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="58a47-141">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-142">Indtast eller vælg en værdi i feltet **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="58a47-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-143">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-143">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-144">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="58a47-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="58a47-145">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-146">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="58a47-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="58a47-147">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-147">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-148">Vælg **Attributværdi**.</span><span class="sxs-lookup"><span data-stu-id="58a47-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="58a47-149">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-150">Indtast eller vælg en værdi i feltet **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="58a47-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-151">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-151">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-152">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="58a47-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="58a47-153">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-154">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="58a47-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="58a47-155">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-155">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-156">Vælg **Attributværdi**.</span><span class="sxs-lookup"><span data-stu-id="58a47-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="58a47-157">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-158">Indtast eller vælg en værdi i feltet **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="58a47-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-159">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-159">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-160">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="58a47-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="58a47-161">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-162">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="58a47-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="58a47-163">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-163">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-164">Vælg **Attributværdi**.</span><span class="sxs-lookup"><span data-stu-id="58a47-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="58a47-165">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-166">Indtast eller vælg en værdi i feltet **Attribut**.</span><span class="sxs-lookup"><span data-stu-id="58a47-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-167">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-167">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-168">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="58a47-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="58a47-169">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-170">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="58a47-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="58a47-171">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="58a47-171">Select **Add**.</span></span>
1. <span data-ttu-id="58a47-172">Vælge **Nummerserieværdi**.</span><span class="sxs-lookup"><span data-stu-id="58a47-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="58a47-173">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58a47-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="58a47-174">Indtast eller vælg en værdi i feltet **Nummerserie**.</span><span class="sxs-lookup"><span data-stu-id="58a47-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="58a47-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-175">Close the page.</span></span>
1. <span data-ttu-id="58a47-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-176">Close the page.</span></span>
1. <span data-ttu-id="58a47-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="58a47-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]