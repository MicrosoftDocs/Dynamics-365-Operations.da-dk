---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920651"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="9eb49-103">Oprette et produktnummernomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="9eb49-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9eb49-104">Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9eb49-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="9eb49-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="9eb49-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9eb49-106">Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="9eb49-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="9eb49-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="9eb49-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="9eb49-108">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="9eb49-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="9eb49-109">Gå til **Administration af produktoplysninger \> Opsætning \> Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="9eb49-110">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-110">Select **New**.</span></span>
1. <span data-ttu-id="9eb49-111">Angiv i feltet **Navn** et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="9eb49-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="9eb49-112">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="9eb49-113">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-113">Select **Add**.</span></span>
1. <span data-ttu-id="9eb49-114">Vælg **Produktmasternummer**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="9eb49-115">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-115">Select **Add**.</span></span>
1. <span data-ttu-id="9eb49-116">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="9eb49-117">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="9eb49-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9eb49-118">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-118">Select **Add**.</span></span>
1. <span data-ttu-id="9eb49-119">Vælg **Farve**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-119">Select **Color**.</span></span>
1. <span data-ttu-id="9eb49-120">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-120">Select **Add**.</span></span>
1. <span data-ttu-id="9eb49-121">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="9eb49-122">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="9eb49-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="9eb49-123">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-123">Select **Add**.</span></span>
1. <span data-ttu-id="9eb49-124">Vælg **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-124">Select **Size**.</span></span>
1. <span data-ttu-id="9eb49-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9eb49-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="9eb49-126">Tildel nomenklaturen til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="9eb49-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="9eb49-127">Vælg **Produktdimensionsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="9eb49-128">Vælg **SizeCol-produktdimensionsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="9eb49-129">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-129">Select **Edit**.</span></span>
4. <span data-ttu-id="9eb49-130">Vælg **Ja** i feltet **Brug nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="9eb49-131">Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.</span><span class="sxs-lookup"><span data-stu-id="9eb49-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="9eb49-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="9eb49-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]