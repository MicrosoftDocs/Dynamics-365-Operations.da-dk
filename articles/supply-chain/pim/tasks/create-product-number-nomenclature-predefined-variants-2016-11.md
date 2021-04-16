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
ms.openlocfilehash: 8c69dc3f8e70c3b0a760f54d2251757ac997a432
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841617"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="84bd6-103">Oprette et produktnummernomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="84bd6-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84bd6-104">Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="84bd6-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="84bd6-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="84bd6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="84bd6-106">Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="84bd6-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="84bd6-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="84bd6-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="84bd6-108">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="84bd6-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="84bd6-109">Vælg **Definition af produktvariantmodel**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="84bd6-110">Vælg **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="84bd6-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-111">Select **New**.</span></span>
4. <span data-ttu-id="84bd6-112">Angiv i feltet **Navn** et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="84bd6-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="84bd6-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="84bd6-114">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-114">Select **Add**.</span></span>
7. <span data-ttu-id="84bd6-115">Vælg **Produktmasternummer**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="84bd6-116">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-116">Select **Add**.</span></span>
9. <span data-ttu-id="84bd6-117">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="84bd6-118">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="84bd6-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="84bd6-119">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-119">Select **Add**.</span></span>
12. <span data-ttu-id="84bd6-120">Vælg **Farve**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-120">Select **Color**.</span></span>
13. <span data-ttu-id="84bd6-121">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-121">Select **Add**.</span></span>
14. <span data-ttu-id="84bd6-122">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="84bd6-123">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="84bd6-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="84bd6-124">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-124">Select **Add**.</span></span>
17. <span data-ttu-id="84bd6-125">Vælg **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-125">Select **Size**.</span></span>
18. <span data-ttu-id="84bd6-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84bd6-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="84bd6-127">Tildel nomenklaturen til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="84bd6-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="84bd6-128">Vælg **Produktdimensionsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="84bd6-129">Vælg **SizeCol-produktdimensionsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="84bd6-130">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-130">Select **Edit**.</span></span>
4. <span data-ttu-id="84bd6-131">Vælg **Ja** i feltet **Brug nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="84bd6-132">Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.</span><span class="sxs-lookup"><span data-stu-id="84bd6-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="84bd6-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="84bd6-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]