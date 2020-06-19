---
title: Færdigmelde fra jobkortenheden
description: Dette emne beskriver, hvordan systemet konfigureres, så brugere af en jobkortenhed kan rapportere færdigvarer fra en produktionsordre til lageret.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403256"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="0e585-103">Færdigmelde fra jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="0e585-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e585-104">Arbejderne skal bruge siden **Rapportstatus** på jobkortenheden til at rapportere de mængder, der er færdiggjort for et produktionsjob.</span><span class="sxs-lookup"><span data-stu-id="0e585-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="0e585-105">Kontrollere, om færdigmeldte mængder føjes til lageret</span><span class="sxs-lookup"><span data-stu-id="0e585-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="0e585-106">Udfør følgende trin for at kontrollere, om og hvordan de mængder, der er færdigmeldt i den sidste operation, skal føjes til lageret.</span><span class="sxs-lookup"><span data-stu-id="0e585-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="0e585-107">Gå til **Produktkontrol \> Opsætning \> Produktionsudførelse \> Produktionsordrestandarder**.</span><span class="sxs-lookup"><span data-stu-id="0e585-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="0e585-108">På fanen **Færdigmelding** skal du angive feltet **Opdater færdigmelding online** til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="0e585-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="0e585-109">**Nej** – Der føjes intet antal til lageret, når der rapporteres mængder for den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="0e585-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="0e585-110">Status for produktionsordren ændres aldrig.</span><span class="sxs-lookup"><span data-stu-id="0e585-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="0e585-111">**Status + antal** – Statussen for produktionsordren ændres til *Færdigmeldt*, og antallet vil blive færdigmeldt til lageret.</span><span class="sxs-lookup"><span data-stu-id="0e585-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="0e585-112">**Antal** – Antallet færdigmeldes til lageret, men statussen for produktionsordren ændres aldrig.</span><span class="sxs-lookup"><span data-stu-id="0e585-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="0e585-113">**Status** – Kun statussen for produktionsordren ændres.</span><span class="sxs-lookup"><span data-stu-id="0e585-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="0e585-114">Der føjes ingen antal til lageret, når der rapporteres mængder for den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="0e585-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="0e585-115">Antal spores ikke på lageret, hvis de operationer, de er færdigmeldt på, ikke er defineret som den sidste operation.</span><span class="sxs-lookup"><span data-stu-id="0e585-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="0e585-116">Disse antal kan dog bruges til at få vist status.</span><span class="sxs-lookup"><span data-stu-id="0e585-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="0e585-117">De kan også inkluderes i regler, der styrer, om arbejderne kan starte den næste operation, før en defineret tærskel for rapporterede antal i den forrige operation nås.</span><span class="sxs-lookup"><span data-stu-id="0e585-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="0e585-118">Du kan definere disse regler på fanen **Validering af antal** på siden **Produktionsordrestandarder**.</span><span class="sxs-lookup"><span data-stu-id="0e585-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="0e585-119">Du kan finde flere oplysninger om, hvordan du arbejder med siden **Produktionsordrestandarder** i [Produktionsparametre i produktionsudførelse](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="0e585-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="0e585-120">Færdigmelde batchstyrede varer</span><span class="sxs-lookup"><span data-stu-id="0e585-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="0e585-121">Jobkortenheden understøtter tre scenarier til rapportering af batchvarer.</span><span class="sxs-lookup"><span data-stu-id="0e585-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="0e585-122">Disse scenarier gælder både for varer, der er aktiveret til avancerede lagerprocesser, og for varer, der ikke er aktiveret til avancerede lagerprocesser.</span><span class="sxs-lookup"><span data-stu-id="0e585-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="0e585-123">**Manuelt tildelte batchnumre:** Arbejderne angiver et brugerdefineret batchnummer.</span><span class="sxs-lookup"><span data-stu-id="0e585-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="0e585-124">Dette batchnummer kan komme fra en ekstern kilde, der ikke er kendt af systemet.</span><span class="sxs-lookup"><span data-stu-id="0e585-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="0e585-125">**Foruddefinerede batchnumre:** Arbejderne vælger et batchnummer på en liste over batchnumre, som systemet automatisk genererer, før produktionsordren frigives til jobkortenheden.</span><span class="sxs-lookup"><span data-stu-id="0e585-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="0e585-126">**Faste batchnumre:** Arbejderne angiver og vælger ikke et batchnummer.</span><span class="sxs-lookup"><span data-stu-id="0e585-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="0e585-127">I stedet tildeler systemet automatisk et batchnummer til produktionsordren, før den frigives.</span><span class="sxs-lookup"><span data-stu-id="0e585-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="0e585-128">Følg disse trin for at aktivere et scenarie.</span><span class="sxs-lookup"><span data-stu-id="0e585-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="0e585-129">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="0e585-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0e585-130">Vælg produktet, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="0e585-130">Select the product to configure.</span></span>
1. <span data-ttu-id="0e585-131">I oversigtspanelet **Styr lager** i feltet **Batchnummergruppe** skal du vælge den sporingsnummergruppe, der er konfigureret til at understøtte dit scenarie.</span><span class="sxs-lookup"><span data-stu-id="0e585-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="0e585-132">Hvis der ikke er knyttet en batchnummergruppe til et batchstyret produkt, er jobkortenheden som standard angivet til manuel indtastning for batchnummeret under færdigmelding.</span><span class="sxs-lookup"><span data-stu-id="0e585-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="0e585-133">I det følgende underafsnit beskrives, hvordan du kan konfigurere sporingsnummergrupper, så hvert af de tre scenarier for rapportering om batchvarer understøttes.</span><span class="sxs-lookup"><span data-stu-id="0e585-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="0e585-134">Aktivere batchnummerrapportering på jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="0e585-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="0e585-135">Hvis du vil sætte dine jobkortenheder i gang med at acceptere et batchnummer under færdigmeldingen, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere følgende funktioner (i denne rækkefølge):</span><span class="sxs-lookup"><span data-stu-id="0e585-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="0e585-136">Forbedret brugeroplevelse for dialogboksen Rapport i gang på jobkortenheden.</span><span class="sxs-lookup"><span data-stu-id="0e585-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="0e585-137">Aktivér denne funktion for at kunne angive batch- og serienumre, når der færdigmeldes fra jobkortenheden (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="0e585-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="0e585-138">Konfigurere en sporingsnummergruppe, så arbejderne kan tildele et batchnummer manuelt</span><span class="sxs-lookup"><span data-stu-id="0e585-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="0e585-139">Du skal følge disse trin for at konfigurere en sporingsnummergruppe og tillade manuelt tildelte batchnumre.</span><span class="sxs-lookup"><span data-stu-id="0e585-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="0e585-140">Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="0e585-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="0e585-141">Opret eller vælg den sporingsnummergruppe, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="0e585-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="0e585-142">I oversigtspanelet **Generelt** skal du angive indstillingen **Manuel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0e585-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="0e585-143">![Siden sporingsnummergrupper](media/tracking-number-group-manual.png "Siden sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="0e585-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="0e585-144">Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.</span><span class="sxs-lookup"><span data-stu-id="0e585-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="0e585-145">Når du bruger dette scenarie, er feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en tekstboks, hvor arbejderne kan angive en hvilken som helst værdi.</span><span class="sxs-lookup"><span data-stu-id="0e585-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="0e585-146">![Siden Rapportstatus med et felt til manuelle batchnumre](media/job-card-device-batch-manual.png "Siden Rapportstatus med et felt til manuelle batchnumre")</span><span class="sxs-lookup"><span data-stu-id="0e585-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="0e585-147">Konfigurere en sporingsnummergruppe, der viser en liste over foruddefinerede batchnumre</span><span class="sxs-lookup"><span data-stu-id="0e585-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="0e585-148">Du skal følge disse trin for at konfigurere en sporingsnummergruppe og lave en liste over foruddefinerede batchnumre.</span><span class="sxs-lookup"><span data-stu-id="0e585-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="0e585-149">Gå til **Lagerstyring \> Opsætning > Dimensioner \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="0e585-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="0e585-150">Opret eller vælg den sporingsnummergruppe, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="0e585-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="0e585-151">I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0e585-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="0e585-152">Brug feltet **Pr. antal** til at opdele batchnumre pr. antal ud fra den værdi, du angiver.</span><span class="sxs-lookup"><span data-stu-id="0e585-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="0e585-153">Du har f.eks. en produktionsordre på ti stykker, og feltet **Pr. antal** er angivet til *2*.</span><span class="sxs-lookup"><span data-stu-id="0e585-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="0e585-154">I dette tilfælde tildeles der fem batchnumre til produktionsordren, når den oprettes.</span><span class="sxs-lookup"><span data-stu-id="0e585-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="0e585-155">![Siden sporingsnummergrupper](media/tracking-number-group-predefined.png "Siden Sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="0e585-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="0e585-156">Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.</span><span class="sxs-lookup"><span data-stu-id="0e585-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="0e585-157">Når du bruger dette scenarie, er feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden indeholder, en rulleliste, hvor arbejderne skal vælge en foruddefineret værdi.</span><span class="sxs-lookup"><span data-stu-id="0e585-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="0e585-158">![Siden Rapportstatus med en liste over foruddefinerede batchnumre](media/job-card-device-batch-predefined.png "Siden Rapportstatus med en liste over foruddefinerede batchnumre")</span><span class="sxs-lookup"><span data-stu-id="0e585-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="0e585-159">Konfigurere en sporingsnummergruppe, som automatisk tildeler batchnumre</span><span class="sxs-lookup"><span data-stu-id="0e585-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="0e585-160">Hvis der automatisk skal tildeles batchnumre uden arbejderinput, skal du følge disse trin for at konfigurere en sporingsnummergruppe.</span><span class="sxs-lookup"><span data-stu-id="0e585-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="0e585-161">Gå til **Lagerstyring \> Opsætning \> Dimensionser \> Sporingsnummergrupper**.</span><span class="sxs-lookup"><span data-stu-id="0e585-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="0e585-162">Opret eller vælg den sporingsnummergruppe, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="0e585-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="0e585-163">I oversigtspanelet **Generelt** skal du angive indstillingen **Kun på lagertransaktioner** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0e585-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="0e585-164">Angiv indstillingen **Manuel** til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="0e585-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="0e585-165">![Siden sporingsnummergrupper](media/tracking-number-group-fixed.png "Siden sporingsnummergrupper")</span><span class="sxs-lookup"><span data-stu-id="0e585-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="0e585-166">Angiv andre værdier efter behov, og vælg derefter denne sporingsnummergruppe som batchnummergruppe for de frigivne produkter, du vil bruge dette scenarie for.</span><span class="sxs-lookup"><span data-stu-id="0e585-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="0e585-167">Når du bruger dette scenarie, viser feltet **Batchnummer**, som siden **Rapport i gang** på jobkortenheden leverer, en værdi, men arbejderne kan ikke redigere denne værdi.</span><span class="sxs-lookup"><span data-stu-id="0e585-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="0e585-168">![Siden Rapportstatus med et fast batchnummer](media/job-card-device-batch-fixed.png "Siden Rapportstatus med et fast batchnummer")</span><span class="sxs-lookup"><span data-stu-id="0e585-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="0e585-169">Rapportere som færdig til en nummerplade</span><span class="sxs-lookup"><span data-stu-id="0e585-169">Report as finished to a license plate</span></span>

<span data-ttu-id="0e585-170">Avancerede lagerprocesser kan bruge nummerpladedimensionen til at spore lager på lagersteder, der er konfigureret til dette formål.</span><span class="sxs-lookup"><span data-stu-id="0e585-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="0e585-171">I dette tilfælde er nummeret på nummerpladen nødvendigt, når en arbejder rapporterer antal som færdige.</span><span class="sxs-lookup"><span data-stu-id="0e585-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="0e585-172">Aktivere nummerpladerapportering og labeludskrivning</span><span class="sxs-lookup"><span data-stu-id="0e585-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="0e585-173">Hvis du vil bruge de funktioner, der er beskrevet i dette afsnit, skal du bruge [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere følgende funktioner (i denne rækkefølge):</span><span class="sxs-lookup"><span data-stu-id="0e585-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="0e585-174">Id for færdigmelding tilføjet i jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="0e585-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="0e585-175">Aktivér automatisk generering af id-nummer ved færdigmelding i jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="0e585-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="0e585-176">Udskriv etiket fra jobkortenhed</span><span class="sxs-lookup"><span data-stu-id="0e585-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="0e585-177">Konfigurere rapportering som færdig til en nummerplade</span><span class="sxs-lookup"><span data-stu-id="0e585-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="0e585-178">Hvis du vil styre, om arbejdere skal genbruge en eksisterende nummerplade eller generere en ny nummerplade, når de færdigmelder antal, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="0e585-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="0e585-179">Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurere jobkort for enheder**.</span><span class="sxs-lookup"><span data-stu-id="0e585-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="0e585-180">For hver enhed skal du angive følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="0e585-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="0e585-181">**Generér nummerplade** – Angiv denne indstilling til **Ja** for at generere en ny nummerplade for hver færdigmeldingsrapport.</span><span class="sxs-lookup"><span data-stu-id="0e585-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="0e585-182">Angiv den til **Nej**, hvis en eksisterende nummerplade skal anvendes til hver færdigmeldingsrapport.</span><span class="sxs-lookup"><span data-stu-id="0e585-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="0e585-183">**Udskriv label** – Angiv denne indstilling til **Ja**, hvis arbejderen skal udskrive en nummerpladelabel for hver færdigmeldingsrapport.</span><span class="sxs-lookup"><span data-stu-id="0e585-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="0e585-184">Angiv den til **Nej**, hvis der ikke kræves en label.</span><span class="sxs-lookup"><span data-stu-id="0e585-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="0e585-185">![Siden Konfigurere jobkort for enheder](media/config-job-card-raf.png "Siden Konfigurere jobkort for enheder")</span><span class="sxs-lookup"><span data-stu-id="0e585-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="0e585-186">Gå til **Lokationsstyring \> Opsætning \> Dokumentrute \> Dokumentrute** for at konfigurere labelen.</span><span class="sxs-lookup"><span data-stu-id="0e585-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="0e585-187">Yderligere oplysninger finder du i afsnittet [Aktivere udskrivning af id-etiket](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="0e585-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
