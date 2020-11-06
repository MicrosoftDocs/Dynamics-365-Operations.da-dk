---
title: Bølgetrinskoder
description: Dette emne indeholder en oversigt over bølgetrinskoder, og hvordan de bruges.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9332e45f7213ed815e4417969b617256778598db
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017799"
---
# <a name="wave-step-codes"></a><span data-ttu-id="af126-103">Bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="af126-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af126-104">Bølgetrinskoder er koder, som brugerne kan konfigurere og bruge til at knytte bestemte forekomster af bølgemetoder til en tilsvarende skabelon.</span><span class="sxs-lookup"><span data-stu-id="af126-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="af126-105">Skabelonerne indeholder skabeloner til genopfyldning, containerisering, etiketudskrivning, lastopbygning og sortering.</span><span class="sxs-lookup"><span data-stu-id="af126-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="af126-106">Når der ikke bruges bølgetrinskoder, skal brugerne angive en fri tekst for at referere til en bestemt skabelon fra forekomsten af bølgemetoden.</span><span class="sxs-lookup"><span data-stu-id="af126-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="af126-107">Der er risiko for fejl i fri tekst, fordi brugerne skal sørge for, at den bølgetrinstekst, som de føjer til en bestemt bølgetrinsmetode i i en bølgeskabelon, nøjagtigt svarer til bølgetrinsteksten i destinationsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="af126-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="af126-108">Bølgetrinskoder for en specifik bølgetrinstype oprettes på en separat side.</span><span class="sxs-lookup"><span data-stu-id="af126-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="af126-109">For hver forekomst af en bølgetrinsmetode i en bølgeskabelon, der kræver en bølgetrinskode, skal bølgetrinskoden være valgt på en rulleliste.</span><span class="sxs-lookup"><span data-stu-id="af126-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="af126-110">Valg på en rulleliste erstatter indtastning af fritekst og hjælper med at reducere risikoen og virkningerne af menneskelige fejl.</span><span class="sxs-lookup"><span data-stu-id="af126-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="af126-111">Opsætningskoder bruges til at sammenkæde en bølgetrinsmetode i en bølgeskabelon med en destinationsskabelon for metoden.</span><span class="sxs-lookup"><span data-stu-id="af126-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="af126-112">Brug af funktionen bølgetrinskoder er valgfri.</span><span class="sxs-lookup"><span data-stu-id="af126-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="af126-113">Den er aktiveret for alle juridiske enheder i hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="af126-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="af126-114">Installationsdemo</span><span class="sxs-lookup"><span data-stu-id="af126-114">Setup demo</span></span> 

<span data-ttu-id="af126-115">Til denne demo skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="af126-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="af126-116">Aktivér bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="af126-116">Enable wave step codes</span></span>

<span data-ttu-id="af126-117">Udfør følgende trin for at aktivere funktionen for bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="af126-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="af126-118">Gå til **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="af126-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="af126-119">Markeres, hvis du vil aktivere den funktion, der kaldes **Bølgetrinskode for hele organisationen**.</span><span class="sxs-lookup"><span data-stu-id="af126-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="af126-120">Alle eksisterende fritekster til bølgetrin i alle juridiske enheder opgraderes til den nye struktur.</span><span class="sxs-lookup"><span data-stu-id="af126-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="af126-121">Når opgraderingen er fuldført for alle juridiske enheder, er funktionen aktiveret.</span><span class="sxs-lookup"><span data-stu-id="af126-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="af126-122">Hvis funktionen ikke kan aktiveres for en eller flere juridiske enheder, er funktionen ikke aktiveret for nogen juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="af126-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="af126-123">Under aktiveringen foretages valideringer under dataopgraderingen.</span><span class="sxs-lookup"><span data-stu-id="af126-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="af126-124">Hvis opgraderingen mislykkes, vises en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="af126-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="af126-125">En opgradering kan mislykkes på grund af følgende konflikter:</span><span class="sxs-lookup"><span data-stu-id="af126-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="af126-126">Der findes identiske fritekster til bølgetrin.</span><span class="sxs-lookup"><span data-stu-id="af126-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="af126-127">Tilpasninger findes.</span><span class="sxs-lookup"><span data-stu-id="af126-127">Customizations exist.</span></span>
- <span data-ttu-id="af126-128">Et fritekst til bølgetrin, der er knyttet til en forekomst af bølgetrinsmetoden, stemmer ikke overens med den forventede skabelontype.</span><span class="sxs-lookup"><span data-stu-id="af126-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="af126-129">Når du har løst eventuelle konflikter, der er identificeret under valideringerne, kan forsøge af aktivere funktionen igen.</span><span class="sxs-lookup"><span data-stu-id="af126-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="af126-130">Når funktionen er aktiveret, bliver siden **Bølgetrinskoder** ( **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder** ) tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="af126-130">When the feature has been enabled, the **Wave step codes** page ( **Warehouse management \> Setup \> Waves \> Wave step codes** ) becomes available.</span></span> <span data-ttu-id="af126-131">Denne side viser de bølgetrinskoder, der blev opgraderet, da funktionen bølgetrinskoder for hele organisationen blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="af126-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="af126-132">Oprette nye bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="af126-132">Create new wave step codes</span></span>

<span data-ttu-id="af126-133">Du kan bruge siden **Bølgetrinskoder** til at oprette og slette bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="af126-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="af126-134">Alle nye bølgetrinskoder og deres tilknyttede id skal være entydige på tværs af alle bølgetrinstyper, og de skal defineres for en bestemt bølgetrinstype.</span><span class="sxs-lookup"><span data-stu-id="af126-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="af126-135">Anvende bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="af126-135">Apply wave step codes</span></span>

<span data-ttu-id="af126-136">Når du har defineret de relevante bølgetrinskoder, kan de anvendes på bølgeprocesmetoderne.</span><span class="sxs-lookup"><span data-stu-id="af126-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="af126-137">Du kan anvende bølgetrinskoder ved at gå til den relevante destinationsskabelon.</span><span class="sxs-lookup"><span data-stu-id="af126-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="af126-138">Her er de destinationsskabeloner, som bølgetrinskoderne peger på:</span><span class="sxs-lookup"><span data-stu-id="af126-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="af126-139">**Genopfyldningsskabeloner:** Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="af126-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="af126-140">**Lastopbygningsskabeloner** Lokationsstyring \> Konfiguration \> Last \> Lastopbygningsskabeloner</span><span class="sxs-lookup"><span data-stu-id="af126-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="af126-141">**Sorteringsskabeloner:** Lokationsstyring \> Konfiguration \> Emballage \> Udgående sorteringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="af126-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="af126-142">**Containeriseringsskabeloner:** Lokationsstyring \> Konfiguration \> Containere \> Skabeloner til containerbygning</span><span class="sxs-lookup"><span data-stu-id="af126-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="af126-143">**Labeludskrivningsskabeloner:** Lokationsstyring \> Konfiguration \> Dokumentrute \> Bølgelabelskabeloner</span><span class="sxs-lookup"><span data-stu-id="af126-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="af126-144">Skabelonerne på denne liste anvendes, når der refereres til dem fra en bølgeprocesmetode, der er valgt i en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="af126-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="af126-145">Når bølgetrinskoden på en bølgeprocessmetode i en bølgeskabelon svarer til bølgetrinskoden i en af skabelontyperne, anvendes skabelonen.</span><span class="sxs-lookup"><span data-stu-id="af126-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="af126-146">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="af126-146">Sample scenario</span></span>

<span data-ttu-id="af126-147">Følgende procedure hjælper med at sikre, at den genopfyldningsskabelon, du har oprettet, anvendes på bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="af126-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="af126-148">Gå ti **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder** , og opret en bølgetrinskode til typen **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="af126-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes** , and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="af126-149">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner** , og opret en genopfyldningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="af126-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates** , and create a replenishment template.</span></span>
3. <span data-ttu-id="af126-150">Vælg den bølgetrinskode, du har oprettet til **Genopfyldning** -typen, i genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="af126-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="af126-151">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner** , og vælg den bølgeskabelon, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="af126-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates** , and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="af126-152">Vælg **Genbestilling** -metoden i oversigtspanelet **Metoder** i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="af126-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="af126-153">Vælg den bølgetrinskode, du har oprettet i genopfyldningsskabelonen, i feltet **Kode for bølgetrin**.</span><span class="sxs-lookup"><span data-stu-id="af126-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="af126-154">Du udfører disse trin for hver juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="af126-154">You perform these steps for each legal entity.</span></span>
