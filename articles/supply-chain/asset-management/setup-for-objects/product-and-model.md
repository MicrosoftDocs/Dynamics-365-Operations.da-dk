---
title: Aktivproducenter og -modeller
description: I dette emne beskrives, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80900301262a0a19ade7c699891a0918921b4104
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825680"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="79494-103">Aktivproducenter og -modeller</span><span class="sxs-lookup"><span data-stu-id="79494-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="79494-104">I dette emne beskrives, hvordan du konfigurerer aktivproducenter og relaterede modeller i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="79494-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="79494-105">Modeller kan relateres til aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="79494-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="79494-106">Konfigurer produktmodelrelationer</span><span class="sxs-lookup"><span data-stu-id="79494-106">Set up product-model relations</span></span>

1. <span data-ttu-id="79494-107">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Producent og model**.</span><span class="sxs-lookup"><span data-stu-id="79494-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="79494-108">Vælg **Ny** for at oprette et nyt produkt.</span><span class="sxs-lookup"><span data-stu-id="79494-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="79494-109">I feltet **Producent** skal du indtaste aktivproducentens navn.</span><span class="sxs-lookup"><span data-stu-id="79494-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="79494-110">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="79494-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="79494-111">I oversigts panelet **Modeller** skal du vælge **Tilføj** for at oprette en aktivmodel, der skal relateres til aktivproducenten.</span><span class="sxs-lookup"><span data-stu-id="79494-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="79494-112">I feltet **Model** skal du indtaste aktivmodellens navn.</span><span class="sxs-lookup"><span data-stu-id="79494-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="79494-113">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="79494-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="79494-114">I feltet **Aktivtype** skal du vælge den aktivtype, som producentmodellen skal relateres til.</span><span class="sxs-lookup"><span data-stu-id="79494-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79494-115">Du kan også oprette relationer for aktivtyper, producenter og modeller i opslaget **Aktivtyper**.</span><span class="sxs-lookup"><span data-stu-id="79494-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="79494-116">Du kan finde flere oplysninger under [Aktivtyper](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="79494-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="79494-117">I oversigtspanelet **Detaljer** viser feltet **Modeller** antallet af aktivmodeller, der er konfigureret for den valgte aktivproducent.</span><span class="sxs-lookup"><span data-stu-id="79494-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="79494-118">Feltet **Aktiver** viser antallet af aktiver, der bruger den valgte producent.</span><span class="sxs-lookup"><span data-stu-id="79494-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="79494-119">Feltet **Aktiver** viser antallet af objekter, der bruger den valgte producentmodel.</span><span class="sxs-lookup"><span data-stu-id="79494-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="79494-120">En aktivtype kan have ingen aktivproducentmodelrelationer, den kan relateres til én aktivproducentmodel eller den kan være relateret til flere aktivproducentmodeller.</span><span class="sxs-lookup"><span data-stu-id="79494-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="79494-121">Hvis en aktivtype er relateret til mindst én producentmodel, kan kun de kombinationer, der er konfigureret i opslaget **Producentmodel**, vælges på disse sider for Styring af aktiver, hvor en kombination af en aktivtype, producent og model kan konfigureres.</span><span class="sxs-lookup"><span data-stu-id="79494-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="79494-122">Disse sider omfatter **Alle aktiver**, **Aktivstjenesteniveauer**, **Jobtypestandarder** og **Vedligeholdelsesbudget linjer**.</span><span class="sxs-lookup"><span data-stu-id="79494-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="79494-123">Hvis nogle af aktivtyperne ikke er relateret til en producentmodel, vises kun de aktivtyper og producentmodeller, der heller ikke har nogen relation til aktivtyper, på siderne.</span><span class="sxs-lookup"><span data-stu-id="79494-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="79494-124">Vælge en producent og model på et objekt</span><span class="sxs-lookup"><span data-stu-id="79494-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="79494-125">Vælg **Styring af aktiver** \> **Almindelig** \> **Aktiver** \> **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="79494-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="79494-126">I kolonnen **Aktiv** skal du vælge linket til aktivet.</span><span class="sxs-lookup"><span data-stu-id="79494-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="79494-127">Siden med **Detaljer** vises.</span><span class="sxs-lookup"><span data-stu-id="79494-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="79494-128">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="79494-128">Select **Edit**.</span></span>
4. <span data-ttu-id="79494-129">I oversigtspanelet **Generelt** skal du vælge værdier i felterne **Producent** og **model**.</span><span class="sxs-lookup"><span data-stu-id="79494-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]