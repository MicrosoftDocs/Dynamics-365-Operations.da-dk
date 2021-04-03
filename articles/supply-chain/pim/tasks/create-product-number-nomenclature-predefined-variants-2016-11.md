---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257406"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="958da-103">Oprette et produktnummernomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="958da-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="958da-104">Dette emne viser, hvordan du konfigurerer en nomenklatur for produktnumre til foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="958da-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="958da-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="958da-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="958da-106">Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="958da-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="958da-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="958da-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="958da-108">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="958da-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="958da-109">Vælg **Definition af produktvariantmodel**.</span><span class="sxs-lookup"><span data-stu-id="958da-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="958da-110">Vælg **Produktnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="958da-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="958da-111">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="958da-111">Select **New**.</span></span>
4. <span data-ttu-id="958da-112">Angiv i feltet **Navn** et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="958da-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="958da-113">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="958da-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="958da-114">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="958da-114">Select **Add**.</span></span>
7. <span data-ttu-id="958da-115">Vælg **Produktmasternummer**.</span><span class="sxs-lookup"><span data-stu-id="958da-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="958da-116">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="958da-116">Select **Add**.</span></span>
9. <span data-ttu-id="958da-117">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="958da-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="958da-118">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="958da-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="958da-119">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="958da-119">Select **Add**.</span></span>
12. <span data-ttu-id="958da-120">Vælg **Farve**.</span><span class="sxs-lookup"><span data-stu-id="958da-120">Select **Color**.</span></span>
13. <span data-ttu-id="958da-121">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="958da-121">Select **Add**.</span></span>
14. <span data-ttu-id="958da-122">Vælg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="958da-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="958da-123">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="958da-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="958da-124">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="958da-124">Select **Add**.</span></span>
17. <span data-ttu-id="958da-125">Vælg **Størrelse**.</span><span class="sxs-lookup"><span data-stu-id="958da-125">Select **Size**.</span></span>
18. <span data-ttu-id="958da-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="958da-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="958da-127">Tildel nomenklaturen til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="958da-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="958da-128">Vælg **Produktdimensionsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="958da-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="958da-129">Vælg **SizeCol-produktdimensionsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="958da-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="958da-130">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="958da-130">Select **Edit**.</span></span>
4. <span data-ttu-id="958da-131">Vælg **Ja** i feltet **Brug nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="958da-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="958da-132">Indtast eller vælg en værdi i feltet **Nomenklatur for produktvariantnummer**.</span><span class="sxs-lookup"><span data-stu-id="958da-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="958da-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="958da-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]