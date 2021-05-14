---
title: NMFC-koder (National Motor Freight Classification)
description: Dette emne beskriver, hvordan du kan arbejde med NMFC-koder (National Motor Freight Classification) i Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941876"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="16075-103">NMFC-koder (National Motor Freight Classification)</span><span class="sxs-lookup"><span data-stu-id="16075-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16075-104">Du kan bruge MNFC-koder (National Motor Freight Classification) til at klassificere varer, der kan fragtes.</span><span class="sxs-lookup"><span data-stu-id="16075-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="16075-105">NMFC-koden er en betegnelse, der bruges til at gruppere varer.</span><span class="sxs-lookup"><span data-stu-id="16075-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="16075-106">Transportfirmaerne kan evaluere varer til forsendelse ved at klassificere varerne ud fra overvejelser som f.eks. egnethed til lastbil, lastningsproblemer, håndtering af problemer og læsbarhed.</span><span class="sxs-lookup"><span data-stu-id="16075-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="16075-107">Varer grupperes i en af 18 fragtklasser ved hjælp af en række numre fra 50 til 500.</span><span class="sxs-lookup"><span data-stu-id="16075-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="16075-108">Den klasse, som en vare er grupperet i, er baseret på en evaluering af fire transportegenskaber: massefylde, muligheder for optimal lastning, håndtering og erstatningsansvar.</span><span class="sxs-lookup"><span data-stu-id="16075-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="16075-109">Tilsammen bestemmer disse egenskaber varens egnethed til transport.</span><span class="sxs-lookup"><span data-stu-id="16075-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="16075-110">En NMFC-kode er tilknyttet hver forsendelsesvare mindre end truckload (LTL).</span><span class="sxs-lookup"><span data-stu-id="16075-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="16075-111">En bærbar computer kan f.eks. tildeles en NMFC-kode med klasse 2,5, mens strømledninger kan tildeles en NMFC-kode med klasse 65.</span><span class="sxs-lookup"><span data-stu-id="16075-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="16075-112">Denne funktion kan hjælpe arbejdere med at bruge NMFC-koder til at klassificere LTL-forsendelsesvarer.</span><span class="sxs-lookup"><span data-stu-id="16075-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="16075-113">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="16075-113">Here are some examples:</span></span>

- <span data-ttu-id="16075-114">Hvis din virksomhed medtager en fragtbeskrivelse på fragtsedlen, har fragtmanden en ide om, hvad fragten går ud på.</span><span class="sxs-lookup"><span data-stu-id="16075-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="16075-115">Fragt er en vigtig klassifikation, da mange transportfirmaer baserer hele deres forretningsmodel på de typer fragt, de håndterer.</span><span class="sxs-lookup"><span data-stu-id="16075-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="16075-116">Denne klassifikation kan være vigtig for virksomheden, fordi den bruges til at bestemme omkostningerne for en given last.</span><span class="sxs-lookup"><span data-stu-id="16075-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="16075-117">Din virksomhed kan identificere rentabiliteten af et LTL-logistik- og transportfirma.</span><span class="sxs-lookup"><span data-stu-id="16075-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="16075-118">Dette emne beskriver, hvordan du kan arbejde med NMFC-koder i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="16075-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="16075-119">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="16075-119">Prerequisites</span></span>

<span data-ttu-id="16075-120">Før du kan oprette NMFC-koder, skal du konfigurere alle LTL-fragtklasser, der skal knyttes til dem.</span><span class="sxs-lookup"><span data-stu-id="16075-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="16075-121">LTL-fragtklasser repræsenterer varekategorier, hvorimod NMFC-koder er relateret til specifikke varer i hver af de 18 fragtklasser.</span><span class="sxs-lookup"><span data-stu-id="16075-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="16075-122">Du kan finde flere oplysninger om, hvordan du arbejder med LTL-klasser, i [Mindre end truckload-klasser (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="16075-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="16075-123">Oprette en NMFC-kode</span><span class="sxs-lookup"><span data-stu-id="16075-123">Create an NMFC code</span></span>

<span data-ttu-id="16075-124">Benyt følgende fremgangsmåde for at oprette en NMFC-kode.</span><span class="sxs-lookup"><span data-stu-id="16075-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="16075-125">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="16075-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="16075-126">Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="16075-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="16075-127">Gå til **Transportstyring \> Opsætning \> Transportstandarder \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="16075-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="16075-128">Vælg **Ny** for at oprette en NMFC-kode.</span><span class="sxs-lookup"><span data-stu-id="16075-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="16075-129">Angiv derefter følgende felter:</span><span class="sxs-lookup"><span data-stu-id="16075-129">Then set the following fields:</span></span>

    - <span data-ttu-id="16075-130">**NMFC-kode** – Indtast NMFC-koden for varetypen.</span><span class="sxs-lookup"><span data-stu-id="16075-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="16075-131">**Navn** – Angiv et navn til NMFC-koden.</span><span class="sxs-lookup"><span data-stu-id="16075-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="16075-132">**LTL-klasse** – Vælg den LTL-klasse, der er tilknyttet NMFC-koden.</span><span class="sxs-lookup"><span data-stu-id="16075-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="16075-133">**Håndteringsenhed for stykliste** – Definer standardhåndteringstypen for forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="16075-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="16075-134">Eksempel: Konfigurere NMFC-koder</span><span class="sxs-lookup"><span data-stu-id="16075-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="16075-135">I følgende eksempel vises det, hvordan du kan konfigurere to forskellige NMFC-koder, som kan bruges til forskellige produkter.</span><span class="sxs-lookup"><span data-stu-id="16075-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="16075-136">Gå til **Lagerstedsstyring \> Opsætning \> Lagerbeholdning \> NMFC-koder**.</span><span class="sxs-lookup"><span data-stu-id="16075-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="16075-137">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="16075-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="16075-138">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="16075-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="16075-139">**NMFC-kode:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="16075-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="16075-140">**Navn:** *Computere*</span><span class="sxs-lookup"><span data-stu-id="16075-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="16075-141">**LTL-klasse:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="16075-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="16075-142">**Håndteringsenhed for stykliste:** *Enhed*</span><span class="sxs-lookup"><span data-stu-id="16075-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="16075-143">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="16075-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="16075-144">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="16075-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="16075-145">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="16075-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="16075-146">**NMFC-kode:** *125*</span><span class="sxs-lookup"><span data-stu-id="16075-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="16075-147">**Navn:** *Telefoner*</span><span class="sxs-lookup"><span data-stu-id="16075-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="16075-148">**LTL-klasse:** *125*</span><span class="sxs-lookup"><span data-stu-id="16075-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="16075-149">**Håndteringsenhed for stykliste:** *Enhed*</span><span class="sxs-lookup"><span data-stu-id="16075-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="16075-150">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="16075-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16075-151">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="16075-151">Additional resources</span></span>

- [<span data-ttu-id="16075-152">Mindre end truckload-klasser (LTL)</span><span class="sxs-lookup"><span data-stu-id="16075-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="16075-153">Oprette en fragtseddel</span><span class="sxs-lookup"><span data-stu-id="16075-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
