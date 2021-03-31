---
title: Fejlhåndtering
description: I dette emne beskrives fejlhåndtering i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f996921ccac0b3c85ecea2460cb9e4614f8c04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226803"
---
# <a name="fault-management"></a><span data-ttu-id="86b57-103">Fejlhåndtering</span><span class="sxs-lookup"><span data-stu-id="86b57-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="86b57-104">I Styring af aktiver kan du bruge fejldesigneren til at konfigurere fejlsymptomer, fejlområder og fejltyper for aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="86b57-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="86b57-105">På denne måde kan du styre fejl, der er registreret på aktiver.</span><span class="sxs-lookup"><span data-stu-id="86b57-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="86b57-106">Desuden kan fejlårsager og forslag til rettelse af fejl registreres på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="86b57-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="86b57-107">Processen for registrering og administration af fejl består af disse trin.</span><span class="sxs-lookup"><span data-stu-id="86b57-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="86b57-108">Opret en liste over fejlsymptomer, fejlområder og fejltyper, der kan opstå på dine aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="86b57-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="86b57-109">Konfigurer symptomer, fejlområder og fejltyper i fejldesigneren.</span><span class="sxs-lookup"><span data-stu-id="86b57-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="86b57-110">Her er nogle eksempler, der kan hjælpe dig med at forstå forskellen mellem fejlsymptomer, fejlområder og fejltyper.</span><span class="sxs-lookup"><span data-stu-id="86b57-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="86b57-111">**Fejlsymptomer:**</span><span class="sxs-lookup"><span data-stu-id="86b57-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="86b57-112">Ubalanceret spænding</span><span class="sxs-lookup"><span data-stu-id="86b57-112">Unbalanced voltages</span></span>
- <span data-ttu-id="86b57-113">Kortslutning</span><span class="sxs-lookup"><span data-stu-id="86b57-113">Short circuit</span></span>
- <span data-ttu-id="86b57-114">Støj</span><span class="sxs-lookup"><span data-stu-id="86b57-114">Noise</span></span>
- <span data-ttu-id="86b57-115">Lækage</span><span class="sxs-lookup"><span data-stu-id="86b57-115">Leak</span></span>
- <span data-ttu-id="86b57-116">Vibrationer</span><span class="sxs-lookup"><span data-stu-id="86b57-116">Vibrations</span></span>

<span data-ttu-id="86b57-117">**Fejlområder:**</span><span class="sxs-lookup"><span data-stu-id="86b57-117">**Fault areas:**</span></span>

- <span data-ttu-id="86b57-118">Elektrisk</span><span class="sxs-lookup"><span data-stu-id="86b57-118">Electrical</span></span>
- <span data-ttu-id="86b57-119">Mekanisk</span><span class="sxs-lookup"><span data-stu-id="86b57-119">Mechanical</span></span>
- <span data-ttu-id="86b57-120">Hydraulisk</span><span class="sxs-lookup"><span data-stu-id="86b57-120">Hydraulic</span></span>
- <span data-ttu-id="86b57-121">Pneumatisk</span><span class="sxs-lookup"><span data-stu-id="86b57-121">Pneumatic</span></span>

<span data-ttu-id="86b57-122">**Fejltyper:**</span><span class="sxs-lookup"><span data-stu-id="86b57-122">**Fault types:**</span></span>

- <span data-ttu-id="86b57-123">Defekt hovedstatorvikling</span><span class="sxs-lookup"><span data-stu-id="86b57-123">Faulty main stator winding</span></span>
- <span data-ttu-id="86b57-124">Defekt diode</span><span class="sxs-lookup"><span data-stu-id="86b57-124">Faulty diode</span></span>
- <span data-ttu-id="86b57-125">Snavsede viklinger</span><span class="sxs-lookup"><span data-stu-id="86b57-125">Dirty windings</span></span>
- <span data-ttu-id="86b57-126">Defekt generator</span><span class="sxs-lookup"><span data-stu-id="86b57-126">Defective generator</span></span>
- <span data-ttu-id="86b57-127">Defekt sensor</span><span class="sxs-lookup"><span data-stu-id="86b57-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="86b57-128">Oprette fejlsymptomer</span><span class="sxs-lookup"><span data-stu-id="86b57-128">Create fault symptoms</span></span>

<span data-ttu-id="86b57-129">Udfør følgende trin for at oprette en liste over symptomer, der kan bruges i fejldesigneren.</span><span class="sxs-lookup"><span data-stu-id="86b57-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="86b57-130">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlsymptomer**.</span><span class="sxs-lookup"><span data-stu-id="86b57-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="86b57-131">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="86b57-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86b57-132">Angiv et navn til fejlsymptomet i feltet **Fejlsymptom**.</span><span class="sxs-lookup"><span data-stu-id="86b57-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="86b57-133">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="86b57-134">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86b57-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="86b57-135">Oprette fejlområder</span><span class="sxs-lookup"><span data-stu-id="86b57-135">Create fault areas</span></span>

<span data-ttu-id="86b57-136">Udfør følgende trin for at oprette en liste over områder eller steder, der kan bruges i fejldesigneren.</span><span class="sxs-lookup"><span data-stu-id="86b57-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="86b57-137">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlområder**.</span><span class="sxs-lookup"><span data-stu-id="86b57-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="86b57-138">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="86b57-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86b57-139">Angiv et navn til fejlområdet i feltet **Fejlområde**.</span><span class="sxs-lookup"><span data-stu-id="86b57-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="86b57-140">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="86b57-141">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86b57-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="86b57-142">Oprette fejltyper</span><span class="sxs-lookup"><span data-stu-id="86b57-142">Create fault types</span></span>

<span data-ttu-id="86b57-143">Udfør følgende trin for at oprette en liste over fejltyper, der kan bruges i fejldesigneren.</span><span class="sxs-lookup"><span data-stu-id="86b57-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="86b57-144">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejltyper**.</span><span class="sxs-lookup"><span data-stu-id="86b57-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="86b57-145">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="86b57-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86b57-146">Angiv et navn for fejltypen i feltet **Fejltype**.</span><span class="sxs-lookup"><span data-stu-id="86b57-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="86b57-147">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="86b57-148">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86b57-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="86b57-149">Konfigurere fejldesigneren</span><span class="sxs-lookup"><span data-stu-id="86b57-149">Set up the fault designer</span></span>

<span data-ttu-id="86b57-150">I fejldesigneren konfigurerer du fejldata på aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="86b57-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="86b57-151">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejldesigner**.</span><span class="sxs-lookup"><span data-stu-id="86b57-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="86b57-152">Vælg den type aktiv, du vil oprette en fejlpost for, i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="86b57-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="86b57-153">Vælg **Tilføj linje** i oversigtspanelet **Fejlsymptom**, og vælg derefter et fejlsymptom i feltet **Fejlsymptom**.</span><span class="sxs-lookup"><span data-stu-id="86b57-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="86b57-154">Vælg **Tilføj linje** i oversigtspanelet **Fejlområde**, og vælg derefter et fejlområde i feltet **Fejlområde**.</span><span class="sxs-lookup"><span data-stu-id="86b57-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="86b57-155">Vælg **Tilføj linje** i oversigtspanelet **Fejltype**, og vælg derefter en fejltype i feltet **Fejltype**.</span><span class="sxs-lookup"><span data-stu-id="86b57-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="86b57-156">Hvis du hurtigt vil oprette kombinationer af alle eksisterende fejlsymptomer, -områder og -typer for den valgte aktivtype, skal du vælge **Opret fejlkombinationer**.</span><span class="sxs-lookup"><span data-stu-id="86b57-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="86b57-157">Denne funktion er nyttig, hvis du har tilføjet mange fejlsymptomer, -områder og -typer.</span><span class="sxs-lookup"><span data-stu-id="86b57-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="86b57-158">Det er nemmere at slette linjer for kombinationer, der ikke er relevante for aktivtypen, end at oprette nye linjer manuelt.</span><span class="sxs-lookup"><span data-stu-id="86b57-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86b57-159">Hvis du vil kopiere opsætningen af fejlsymptomer, -områder og -typer fra én aktivtype til den valgte aktivtype, skal du vælge **Kopiér fra aktivtype**.</span><span class="sxs-lookup"><span data-stu-id="86b57-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="86b57-160">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="86b57-160">Select **Save** to save your changes.</span></span>

![Siden Fejldesigner](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="86b57-162">Oprette fejlårsager</span><span class="sxs-lookup"><span data-stu-id="86b57-162">Create fault causes</span></span>

<span data-ttu-id="86b57-163">Udfør følgende trin for at oprette en liste over kendte fejlårsager, der kan føjes til en arbejdsordre eller en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="86b57-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="86b57-164">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlårsager**.</span><span class="sxs-lookup"><span data-stu-id="86b57-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="86b57-165">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="86b57-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86b57-166">Angiv et navn for fejlårsagen i feltet **Fejlårsag**.</span><span class="sxs-lookup"><span data-stu-id="86b57-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="86b57-167">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="86b57-168">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86b57-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="86b57-169">Oprette fejlrettelser</span><span class="sxs-lookup"><span data-stu-id="86b57-169">Create fault remedies</span></span>

<span data-ttu-id="86b57-170">Udfør følgende trin for at oprette en liste over forslag til rettelser og reparationer, der kan føjes til en arbejdsordre eller en vedligeholdelsesanmodning.</span><span class="sxs-lookup"><span data-stu-id="86b57-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="86b57-171">Vælg **Styring af aktiver** \> **Opsætning** \> **Fejl** \> **Fejlrettelser**.</span><span class="sxs-lookup"><span data-stu-id="86b57-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="86b57-172">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="86b57-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86b57-173">Angiv et navn til fejlrettelsen i feltet **Fejlrettelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="86b57-174">Indtast en beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="86b57-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="86b57-175">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="86b57-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="86b57-176">Du kan ændre navnene på dine fejlsymptomer, -områder, -typer, -årsager og -rettelser efter behov.</span><span class="sxs-lookup"><span data-stu-id="86b57-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="86b57-177">Navneændringerne afspejles automatisk i de relaterede fejlregistreringer.</span><span class="sxs-lookup"><span data-stu-id="86b57-177">The name changes are automatically reflected in the related fault registrations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]