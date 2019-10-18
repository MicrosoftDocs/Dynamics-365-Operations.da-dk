---
title: Bølgetrinskoder
description: Dette emne indeholder en oversigt over bølgetrinskoder, og hvordan de bruges.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992351"
---
# <a name="wave-step-codes"></a><span data-ttu-id="a834b-103">Bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="a834b-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="a834b-104">Om bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="a834b-104">About wave step codes</span></span>

<span data-ttu-id="a834b-105">Bølgetrinskoder er koder, som brugerne kan konfigurere og bruge til at knytte bestemte forekomster af bølgemetoder til en tilsvarende skabelon.</span><span class="sxs-lookup"><span data-stu-id="a834b-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="a834b-106">Skabelonerne indeholder skabeloner til genopfyldning, containerisering, etiketudskrivning, lastopbygning og sortering.</span><span class="sxs-lookup"><span data-stu-id="a834b-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="a834b-107">Når der ikke bruges bølgetrinskoder, skal brugerne angive en fri tekst for at referere til en bestemt skabelon fra forekomsten af bølgemetoden.</span><span class="sxs-lookup"><span data-stu-id="a834b-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="a834b-108">Der er fejlrisiko for fri tekst, fordi brugerne skal sørge for, at den bølgetrinstekst, som de føjer til en bestemt bølgetrinsmetode i i en bølgeskabelon, nøjagtigt svarer til bølgetrinsteksten i destinationsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a834b-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="a834b-109">Bølgetrinskoder for en specifik bølgetrinstype oprettes på en separat side.</span><span class="sxs-lookup"><span data-stu-id="a834b-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="a834b-110">For hver forekomst af en bølgetrinsmetode i en bølgeskabelon, der kræver en bølgetrinskode, skal bølgetrinskoden være valgt på en rulleliste.</span><span class="sxs-lookup"><span data-stu-id="a834b-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="a834b-111">Valg på en rulleliste erstatter indtastning af fritekst og hjælper med at reducere risikoen og virkningerne af menneskelige fejl.</span><span class="sxs-lookup"><span data-stu-id="a834b-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="a834b-112">Opsætningskoder bruges til at sammenkæde en bølgetrinsmetode i en bølgeskabelon med en destinationsskabelon for metoden.</span><span class="sxs-lookup"><span data-stu-id="a834b-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="a834b-113">Det er valgfrit at bruge funktionen for bølgetrinskoder, og inddragelse sker pr. juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="a834b-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="a834b-114">Hvis en bestemt juridisk enhed bruger funktionen, bliver alle eksisterende bølgetrinskoder i den juridiske enhed derfor opgraderet til den nye struktur.</span><span class="sxs-lookup"><span data-stu-id="a834b-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="a834b-115">Installationsdemo</span><span class="sxs-lookup"><span data-stu-id="a834b-115">Setup demo</span></span> 

<span data-ttu-id="a834b-116">Til denne demo skal du have installeret demodata, og du skal bruge demodatafirmaet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a834b-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="a834b-117">Aktivér bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="a834b-117">Enable wave step codes</span></span>

<span data-ttu-id="a834b-118">Udfør følgende trin for at aktivere funktionen for bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="a834b-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="a834b-119">Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.</span><span class="sxs-lookup"><span data-stu-id="a834b-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="a834b-120">Under fanen **Generelt** på oversigtspanelet **Bølgebehandling** skal du vælge **Ja** i indstillingen **Aktivér bølgetrinskoder**.</span><span class="sxs-lookup"><span data-stu-id="a834b-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="a834b-121">Alle eksisterende fritekster til bølgetrin opgraderes til den nye struktur.</span><span class="sxs-lookup"><span data-stu-id="a834b-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="a834b-122">Når denne opgradering er fuldført for en juridisk enhed, er indstillingen **Aktiver bølgetrinskoder** ikke længere tilgængelig på siden **Parametre til lokationsstyring**.</span><span class="sxs-lookup"><span data-stu-id="a834b-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="a834b-123">Valideringer udføres under opgraderingen, og hvis opgraderingen mislykkes, får du vist en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="a834b-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="a834b-124">En opgradering kan mislykkes på grund af følgende konflikter:</span><span class="sxs-lookup"><span data-stu-id="a834b-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="a834b-125">Der findes identiske fritekster til bølgetrin.</span><span class="sxs-lookup"><span data-stu-id="a834b-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="a834b-126">Tilpasninger findes.</span><span class="sxs-lookup"><span data-stu-id="a834b-126">Customizations exist.</span></span>
- <span data-ttu-id="a834b-127">Et fritekst til bølgetrin, der er knyttet til en forekomst af bølgetrinsmetoden, stemmer ikke overens med den forventede skabelontype.</span><span class="sxs-lookup"><span data-stu-id="a834b-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="a834b-128">Når du har løst eventuelle konflikter, der er identificeret under valideringerne, kan du køre opgraderingsprocessen igen.</span><span class="sxs-lookup"><span data-stu-id="a834b-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="a834b-129">Når opgraderingen lykkes, bliver siden **Bølgetrinskoder** (**Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder**) tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a834b-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="a834b-130">Denne side viser de bølgetrinskoder, der blev opgraderet, da funktionen bølgetrinskoder blev slået til.</span><span class="sxs-lookup"><span data-stu-id="a834b-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="a834b-131">Oprette nye bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="a834b-131">Create new wave step codes</span></span>

<span data-ttu-id="a834b-132">Du kan bruge siden **Bølgetrinskoder** til at oprette og slette bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="a834b-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="a834b-133">Alle nye bølgetrinskoder og deres tilknyttede id skal være entydige på tværs af alle bølgetrinstyper, og de skal defineres for en bestemt bølgetrinstype.</span><span class="sxs-lookup"><span data-stu-id="a834b-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="a834b-134">Anvende bølgetrinskoder</span><span class="sxs-lookup"><span data-stu-id="a834b-134">Apply wave step codes</span></span>

<span data-ttu-id="a834b-135">Når du har defineret de relevante bølgetrinskoder, kan de anvendes på bølgeprocesmetoderne.</span><span class="sxs-lookup"><span data-stu-id="a834b-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="a834b-136">Du kan anvende bølgetrinskoder ved at gå til den relevante destinationsskabelon.</span><span class="sxs-lookup"><span data-stu-id="a834b-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="a834b-137">Her er de destinationsskabeloner, som bølgetrinskoderne peger på:</span><span class="sxs-lookup"><span data-stu-id="a834b-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="a834b-138">**Genopfyldningsskabeloner:** Lagerstedsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="a834b-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="a834b-139">**Lastopbygningsskabeloner** Lokationsstyring \> Konfiguration \> Last \> Lastopbygningsskabeloner</span><span class="sxs-lookup"><span data-stu-id="a834b-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="a834b-140">**Sorteringsskabeloner:** Lokationsstyring \> Konfiguration \> Emballage \> Udgående sorteringsskabeloner</span><span class="sxs-lookup"><span data-stu-id="a834b-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="a834b-141">**Containeriseringsskabeloner:** Lokationsstyring \> Konfiguration \> Containere \> Skabeloner til containerbygning</span><span class="sxs-lookup"><span data-stu-id="a834b-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="a834b-142">**Labeludskrivningsskabeloner:** Lokationsstyring \> Konfiguration \> Dokumentrute \> Bølgelabelskabeloner</span><span class="sxs-lookup"><span data-stu-id="a834b-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="a834b-143">Skabelonerne på denne liste anvendes, når der refereres til dem fra en bølgeprocesmetode, der er valgt i en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="a834b-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="a834b-144">Når bølgetrinskoden på en bølgeprocessmetode i en bølgeskabelon svarer til bølgetrinskoden i en af skabelontyperne, anvendes skabelonen.</span><span class="sxs-lookup"><span data-stu-id="a834b-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="a834b-145">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="a834b-145">Sample scenario</span></span>

<span data-ttu-id="a834b-146">Følgende procedure hjælper med at sikre, at den genopfyldningsskabelon, du har oprettet, anvendes på bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a834b-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="a834b-147">Gå ti **Lokationsstyring \> Konfiguration \> Bølger \> Bølgetrinskoder**, og opret en bølgetrinskode til typen **Genopfyldning**.</span><span class="sxs-lookup"><span data-stu-id="a834b-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="a834b-148">Gå til **Lokationsstyring \> Konfiguration \> Genopfyldning \> Genopfyldningsskabeloner** , og opret en genopfyldningsskabelon.</span><span class="sxs-lookup"><span data-stu-id="a834b-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="a834b-149">Vælg den bølgetrinskode, du har oprettet til **Genopfyldning**-typen, i genopfyldningsskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a834b-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="a834b-150">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**, og vælg den bølgeskabelon, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="a834b-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="a834b-151">Vælg **Genbestilling**-metoden i oversigtspanelet **Metoder** i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="a834b-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="a834b-152">Vælg den bølgetrinskode, du har oprettet i genopfyldningsskabelonen, i feltet **Kode for bølgetrin**.</span><span class="sxs-lookup"><span data-stu-id="a834b-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
