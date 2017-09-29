--- 
title: Oprette et produktnummer for foruddefinerede produktvarianter
description: Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="8b818-103">Oprette et produktnummer for foruddefinerede produktvarianter</span><span class="sxs-lookup"><span data-stu-id="8b818-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b818-104">Denne vejledning viser, hvordan du konfigurerer en nomenklatur for produktnumre for foruddefinerede produktvarianter, og hvordan du tildeler den til den rette produktdimensionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8b818-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="8b818-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="8b818-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8b818-106">Den nye nomenklatur for produktnummer tildeles til produktdimensionsgruppen Farve og størrelse.</span><span class="sxs-lookup"><span data-stu-id="8b818-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="8b818-107">Denne opgave udføres normalt af en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="8b818-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="8b818-108">Opret en nomenklatur for produktnummer</span><span class="sxs-lookup"><span data-stu-id="8b818-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="8b818-109">Klik på Definition af produktvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="8b818-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8b818-110">Klik på Produktnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="8b818-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="8b818-111">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="8b818-111">Click New.</span></span>
4. <span data-ttu-id="8b818-112">Angiv i feltet Navn et navn til nomenklaturen, der hjælper med at identificere målproduktdimensionsgruppen, for eksempel ColorSize.</span><span class="sxs-lookup"><span data-stu-id="8b818-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="8b818-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8b818-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8b818-114">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b818-114">Click Add.</span></span>
7. <span data-ttu-id="8b818-115">Klik på Produktmasternummer.</span><span class="sxs-lookup"><span data-stu-id="8b818-115">Click Product master number.</span></span>
8. <span data-ttu-id="8b818-116">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b818-116">Click Add.</span></span>
9. <span data-ttu-id="8b818-117">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8b818-117">Click Text constant.</span></span>
10. <span data-ttu-id="8b818-118">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="8b818-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="8b818-119">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b818-119">Click Add.</span></span>
12. <span data-ttu-id="8b818-120">Klik på Farve.</span><span class="sxs-lookup"><span data-stu-id="8b818-120">Click Color.</span></span>
13. <span data-ttu-id="8b818-121">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b818-121">Click Add.</span></span>
14. <span data-ttu-id="8b818-122">Klik på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8b818-122">Click Text constant.</span></span>
15. <span data-ttu-id="8b818-123">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="8b818-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="8b818-124">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="8b818-124">Click Add.</span></span>
17. <span data-ttu-id="8b818-125">Klik på Størrelse.</span><span class="sxs-lookup"><span data-stu-id="8b818-125">Click Size.</span></span>
18. <span data-ttu-id="8b818-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8b818-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="8b818-127">Tildel nomenklaturen til en produktmaster</span><span class="sxs-lookup"><span data-stu-id="8b818-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="8b818-128">Klik på Produktdimensionsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8b818-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="8b818-129">Vælg produktdimensionsgruppen SizeCol.</span><span class="sxs-lookup"><span data-stu-id="8b818-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="8b818-130">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="8b818-130">Click Edit.</span></span>
4. <span data-ttu-id="8b818-131">Vælg Ja i feltet Brug nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="8b818-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="8b818-132">Indtast eller vælg en værdi i feltet Nomenklatur for produktvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="8b818-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="8b818-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="8b818-133">Close the page.</span></span>


