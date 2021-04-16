---
title: Administrere måleenhed
description: Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.
author: sorenva
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 966e189e7395bec15d2c62735c6df3df2ab34b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817959"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="805d1-103">Administrere måleenhed</span><span class="sxs-lookup"><span data-stu-id="805d1-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="805d1-104">Denne fremgangsmåde viser, hvordan du definerer en måleenhed, angiver oversættelser for enheden og dens beskrivelse og definerer omregningsregler for relaterede enheder.</span><span class="sxs-lookup"><span data-stu-id="805d1-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="805d1-105">Du kan gennemgå denne procedure ved at bruge demodataene eller dine egne data.</span><span class="sxs-lookup"><span data-stu-id="805d1-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="805d1-106">Gå til **Navigationsrude > Moduler > Administration af produktoplysninger > Vedligeholdelse af frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="805d1-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="805d1-107">Klik på **Enheder**.</span><span class="sxs-lookup"><span data-stu-id="805d1-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="805d1-108">Opret en måleenhed</span><span class="sxs-lookup"><span data-stu-id="805d1-108">Create a unit of measure</span></span>
1. <span data-ttu-id="805d1-109">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="805d1-109">Click **New**.</span></span>
2. <span data-ttu-id="805d1-110">I feltet **Enhed** skal du angive en værdi.</span><span class="sxs-lookup"><span data-stu-id="805d1-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="805d1-111">Angiv det id eller symbol, der skal bruges i forbindelse med måleenheden.</span><span class="sxs-lookup"><span data-stu-id="805d1-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="805d1-112">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="805d1-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="805d1-113">Indtast et beskrivende navn for måleenheden i systemsproget.</span><span class="sxs-lookup"><span data-stu-id="805d1-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="805d1-114">I feltet **Enhedsklasse** skal du vælge en indstilling.</span><span class="sxs-lookup"><span data-stu-id="805d1-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="805d1-115">Enhedsklassen definerer, hvilken logisk gruppering, f.eks. område, masse eller mængde, måleenheden er del af.</span><span class="sxs-lookup"><span data-stu-id="805d1-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="805d1-116">I feltet **Decimalpræcision** skal du indtaste et tal.</span><span class="sxs-lookup"><span data-stu-id="805d1-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="805d1-117">Angiv antallet af decimaler, som den omregnede måleenhed skal afrundes til, når der er fuldført en beregning for måleenheden.</span><span class="sxs-lookup"><span data-stu-id="805d1-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="805d1-118">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="805d1-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="805d1-119">Definer enhedsoversættelser</span><span class="sxs-lookup"><span data-stu-id="805d1-119">Define unit translations</span></span>
1. <span data-ttu-id="805d1-120">Klik på **Enhedstekster** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="805d1-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="805d1-121">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="805d1-121">Click **New**.</span></span> <span data-ttu-id="805d1-122">Brug enhedstekst til at oprette en oversættelse af id'et eller et symbol, der repræsenterer måleenheden, til brug på eksterne dokumenter på debitor- eller kreditorspecifikke sprog.</span><span class="sxs-lookup"><span data-stu-id="805d1-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="805d1-123">I feltet **Sprog** skal du indtaste eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="805d1-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="805d1-124">I feltet **Tekst** skal du indtaste en værdi.</span><span class="sxs-lookup"><span data-stu-id="805d1-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="805d1-125">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="805d1-125">Click **Save**.</span></span>
6. <span data-ttu-id="805d1-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="805d1-126">Close the page.</span></span>
7. <span data-ttu-id="805d1-127">Klik på **Oversatte enhedsbeskrivelser** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="805d1-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="805d1-128">Klik på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="805d1-128">Click **New**.</span></span> <span data-ttu-id="805d1-129">Definer sprogspecifikke beskrivelser af måleenheden.</span><span class="sxs-lookup"><span data-stu-id="805d1-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="805d1-130">I feltet **Sprog** skal du indtaste eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="805d1-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="805d1-131">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="805d1-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="805d1-132">Klik på **Gem**.</span><span class="sxs-lookup"><span data-stu-id="805d1-132">Click **Save**.</span></span>
12. <span data-ttu-id="805d1-133">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="805d1-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="805d1-134">Definer omregningsregler for enhed</span><span class="sxs-lookup"><span data-stu-id="805d1-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="805d1-135">Klik på **Enhedsomregninger** i **Handlingsrude**.</span><span class="sxs-lookup"><span data-stu-id="805d1-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="805d1-136">Definer regler for konvertering af måleenheden til og fra andre enheder i den valgte enhedsklasse.</span><span class="sxs-lookup"><span data-stu-id="805d1-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="805d1-137">Klik på **Ny** for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="805d1-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="805d1-138">Angiv et tal i feltet **Faktor**.</span><span class="sxs-lookup"><span data-stu-id="805d1-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="805d1-139">Omregningsfaktor mellem Fra enhed og Til enhed.</span><span class="sxs-lookup"><span data-stu-id="805d1-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="805d1-140">Omregningsfaktoren fra centimeter til meter er f.eks. 100, fordi der går 100 centimeter på 1 meter.</span><span class="sxs-lookup"><span data-stu-id="805d1-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="805d1-141">Indtast eller vælg en værdi i feltet **Til enhed**.</span><span class="sxs-lookup"><span data-stu-id="805d1-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="805d1-142">Vælg en indstilling i feltet **Afrunding**.</span><span class="sxs-lookup"><span data-stu-id="805d1-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="805d1-143">Definer, hvordan den omregnede værdi skal afrundes.</span><span class="sxs-lookup"><span data-stu-id="805d1-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="805d1-144">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="805d1-144">Click **OK**.</span></span>
7. <span data-ttu-id="805d1-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="805d1-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]