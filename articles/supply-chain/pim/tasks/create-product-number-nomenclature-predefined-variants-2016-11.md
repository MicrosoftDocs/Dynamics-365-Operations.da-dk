---
title: Oprette et produktnummernomenklatur for foruddefinerede produktvarianter
description: Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550573"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="f545f-103">Oprette et produktnummernomenklatur for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="f545f-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f545f-104">Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f545f-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="f545f-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="f545f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f545f-106">Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="f545f-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="f545f-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="f545f-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="f545f-108">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="f545f-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="f545f-109">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="f545f-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="f545f-110">Klik på Produktnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="f545f-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="f545f-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="f545f-111">Click New.</span></span>
4. <span data-ttu-id="f545f-112">Angiv i feltet Navn et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel ColorSize.</span><span class="sxs-lookup"><span data-stu-id="f545f-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="f545f-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f545f-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f545f-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f545f-114">Click Add.</span></span>
7. <span data-ttu-id="f545f-115">Klik på Produktmasternummer.</span><span class="sxs-lookup"><span data-stu-id="f545f-115">Click Product master number.</span></span>
8. <span data-ttu-id="f545f-116">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f545f-116">Click Add.</span></span>
9. <span data-ttu-id="f545f-117">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="f545f-117">Click Text constant.</span></span>
10. <span data-ttu-id="f545f-118">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="f545f-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="f545f-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f545f-119">Click Add.</span></span>
12. <span data-ttu-id="f545f-120">Klik på Farve.</span><span class="sxs-lookup"><span data-stu-id="f545f-120">Click Color.</span></span>
13. <span data-ttu-id="f545f-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f545f-121">Click Add.</span></span>
14. <span data-ttu-id="f545f-122">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="f545f-122">Click Text constant.</span></span>
15. <span data-ttu-id="f545f-123">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="f545f-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="f545f-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f545f-124">Click Add.</span></span>
17. <span data-ttu-id="f545f-125">Klik på Størrelse.</span><span class="sxs-lookup"><span data-stu-id="f545f-125">Click Size.</span></span>
18. <span data-ttu-id="f545f-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f545f-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="f545f-127">Tildel nomenklaturen til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="f545f-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="f545f-128">Klik på Produktdimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f545f-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="f545f-129">Vælg produktdimensionsgruppen SizeCol.</span><span class="sxs-lookup"><span data-stu-id="f545f-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="f545f-130">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="f545f-130">Click Edit.</span></span>
4. <span data-ttu-id="f545f-131">Vælg Ja i feltet Brug nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="f545f-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="f545f-132">Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="f545f-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="f545f-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f545f-133">Close the page.</span></span>

