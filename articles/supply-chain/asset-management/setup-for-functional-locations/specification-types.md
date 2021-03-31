---
title: Vedligeholdelsesattributtyper
description: Dette emne beskriver, hvordan du opretter attributtyper i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b93c2ab284d5746f4ecd48cd8b8ffe59aea9f90
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217239"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="b62a6-103">Vedligeholdelsesattributtyper</span><span class="sxs-lookup"><span data-stu-id="b62a6-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b62a6-104">Dette emne beskriver, hvordan du opretter attributtyper i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="b62a6-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="b62a6-105">Attributter bruges til at beskrive egenskaberne for forskellige elementer.</span><span class="sxs-lookup"><span data-stu-id="b62a6-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="b62a6-106">Du kan konfigurere attributter for følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="b62a6-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="b62a6-107">Arbejdsstedstyper</span><span class="sxs-lookup"><span data-stu-id="b62a6-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="b62a6-108">Oprette arbejdssteder</span><span class="sxs-lookup"><span data-stu-id="b62a6-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="b62a6-109">Aktivtyper</span><span class="sxs-lookup"><span data-stu-id="b62a6-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="b62a6-110">Aktiver</span><span class="sxs-lookup"><span data-stu-id="b62a6-110">Assets</span></span>

<span data-ttu-id="b62a6-111">De attributter, du kan angive, varierer afhængigt af elementet.</span><span class="sxs-lookup"><span data-stu-id="b62a6-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="b62a6-112">For et arbejdssted kan du eksempelvis oprette attributter til konfigurationen og den fysiske størrelse af stedet.</span><span class="sxs-lookup"><span data-stu-id="b62a6-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="b62a6-113">For en aktivtype eller et aktiv kan du konfigurere attributter for motorvolumen, strømforbrug og maksimal belastningskapacitet under forskellige forhold.</span><span class="sxs-lookup"><span data-stu-id="b62a6-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="b62a6-114">Oprette attributtyper</span><span class="sxs-lookup"><span data-stu-id="b62a6-114">Create attribute types</span></span>

<span data-ttu-id="b62a6-115">Du kan oprette dine egne attributtyper.</span><span class="sxs-lookup"><span data-stu-id="b62a6-115">You can create your own attribute types.</span></span> <span data-ttu-id="b62a6-116">Derudover kan du overføre produktdimensioner til siden **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="b62a6-117">Vælg **Styring af aktiver** \> **Opsætning** \> **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="b62a6-118">Første gang du konfigurerer attributtyper, skal du vælge **Opret produktdimensioner** for automatisk at overføre standarderne for produktdimensioner.</span><span class="sxs-lookup"><span data-stu-id="b62a6-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="b62a6-119">Vælg **Ny** for at oprette en ny attributtype.</span><span class="sxs-lookup"><span data-stu-id="b62a6-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="b62a6-120">Angiv et navn for attributtypen i feltet **Attributtype**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="b62a6-121">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="b62a6-122">Vælg den relevante attributenhed efter behov i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="b62a6-123">Vælg en datatype for enheden i feltet **Datatype**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="b62a6-124">Hvis du har valgt **Streng** som datatype, skal du følge disse trin for at oprette værdier for attributtypen:</span><span class="sxs-lookup"><span data-stu-id="b62a6-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="b62a6-125">Vælg attributtypen, og vælg dernæst **Værdier**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="b62a6-126">Vælg **Ny** i feltet **Attributværdier**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="b62a6-127">Vælg en attributtype (dimension) i feltet **Attributtype**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="b62a6-128">Indtast en relateret værdi i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="b62a6-129">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="b62a6-130">Gem posten.</span><span class="sxs-lookup"><span data-stu-id="b62a6-130">Save the record.</span></span>
    7. <span data-ttu-id="b62a6-131">Vend tilbage til siden **Attributtyper**.</span><span class="sxs-lookup"><span data-stu-id="b62a6-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="b62a6-132">Gem posten.</span><span class="sxs-lookup"><span data-stu-id="b62a6-132">Save the record.</span></span>

    <span data-ttu-id="b62a6-133">Feltet **Arbejdsstedstyper** viser antallet af arbejdssteder, der bruger attributtypen.</span><span class="sxs-lookup"><span data-stu-id="b62a6-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="b62a6-134">Feltet **Aktivtyper** viser antallet af aktivtyper, der bruger det.</span><span class="sxs-lookup"><span data-stu-id="b62a6-134">The **Asset types** field shows the number of asset types that are using it.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]