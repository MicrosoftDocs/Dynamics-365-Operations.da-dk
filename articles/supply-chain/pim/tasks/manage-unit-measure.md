--- 
title: "Administrere måleenhed"
description: "Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8524e006bbebe9600deb231f05d6df8fb3f33092
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="d8fdd-103">Administrere måleenhed</span><span class="sxs-lookup"><span data-stu-id="d8fdd-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8fdd-104">Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="d8fdd-105">Du kan gennemgå denne procedure ved at bruge demodataene eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="d8fdd-106">Gå til Vedligeholdelse af frigivet produkt.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="d8fdd-107">Klik på enheder.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="d8fdd-108">Opret en måleenhed</span><span class="sxs-lookup"><span data-stu-id="d8fdd-108">Create a unit of measure</span></span>
1. <span data-ttu-id="d8fdd-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-109">Click New.</span></span>
2. <span data-ttu-id="d8fdd-110">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="d8fdd-111">Angiv det id eller symbol, der skal bruges i forbindelse med måleenheden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="d8fdd-112">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d8fdd-113">Indtast et beskrivende navn for måleenheden i systemsproget.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="d8fdd-114">Vælg en indstilling i feltet Enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="d8fdd-115">Enhedsklassen definerer, hvilken logisk gruppering, f.eks. område, masse eller mængde, måleenheden er del af.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="d8fdd-116">Angiv et tal i feltet Decimalpræcision.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="d8fdd-117">Angiv antallet af decimaler, som den omregnede måleenhed skal afrundes til, når der er fuldført en beregning for måleenheden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="d8fdd-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="d8fdd-119">Definer enhedsoversættelser</span><span class="sxs-lookup"><span data-stu-id="d8fdd-119">Define unit translations</span></span>
1. <span data-ttu-id="d8fdd-120">Klik på Enhedstekster.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-120">Click Unit texts.</span></span>
2. <span data-ttu-id="d8fdd-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-121">Click New.</span></span>
    * <span data-ttu-id="d8fdd-122">Brug enhedstekst til at oprette en oversættelse af id'et eller et symbol, der repræsenterer måleenheden, til brug på eksterne dokumenter på debitor- eller kreditorspecifikke sprog.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="d8fdd-123">Indtast eller vælg en værdi i feltet Sprog.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="d8fdd-124">Skriv en værdi i feltet Tekst.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="d8fdd-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-125">Click Save.</span></span>
6. <span data-ttu-id="d8fdd-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-126">Close the page.</span></span>
7. <span data-ttu-id="d8fdd-127">Klik på Oversatte beskrivelser af enheder.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="d8fdd-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-128">Click New.</span></span>
    * <span data-ttu-id="d8fdd-129">Definer sprogspecifikke beskrivelser af måleenheden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="d8fdd-130">Indtast eller vælg en værdi i feltet Sprog.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="d8fdd-131">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="d8fdd-132">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-132">Click Save.</span></span>
12. <span data-ttu-id="d8fdd-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="d8fdd-134">Definer omregningsregler for enhed</span><span class="sxs-lookup"><span data-stu-id="d8fdd-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="d8fdd-135">Klik på Vis enhedsomregninger.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="d8fdd-136">Definer regler for konvertering af måleenheden til og fra andre enheder i den valgte enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="d8fdd-137">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="d8fdd-138">Angiv et tal i feltet Faktor.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="d8fdd-139">Omregningsfaktor mellem Fra enhed og Til enhed.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="d8fdd-140">Omregningsfaktoren fra centimeter til meter er f.eks. 100, fordi der går 100 centimeter på 1 meter.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="d8fdd-141">Indtast eller vælg en værdi i feltet Til-enhed.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="d8fdd-142">Vælg en indstilling i feltet Afrunding.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="d8fdd-143">Definer, hvordan den omregnede værdi skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="d8fdd-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-144">Click OK.</span></span>
7. <span data-ttu-id="d8fdd-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-145">Close the page.</span></span>


