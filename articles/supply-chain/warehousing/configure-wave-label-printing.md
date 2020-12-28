---
title: Konfigurere og bruge bølgeetiketudskrivning
description: Dette emne beskriver udskrivning af bølgeetiketter og forklarer, hvordan du konfigurerer det.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/27/2020
ms.locfileid: "4425069"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="a4318-103">Konfigurere og bruge bølgeetiketudskrivning</span><span class="sxs-lookup"><span data-stu-id="a4318-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4318-104">Ved udskrivning af bølgeetiket kan du vælge en alternativ metode til udskrivning af etiketter ved at introducere en ny metode til bølgetrin, der giver dig mulighed for at oprette og udskrive etiketter direkte fra bølgeskabelonen under bølgeudførelse.</span><span class="sxs-lookup"><span data-stu-id="a4318-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="a4318-105">Etiketterne vil derfor allerede være tilgængelige, før arbejderne kører arbejdsordren på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="a4318-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="a4318-106">Arbejderne kan derefter tilknytte de nødvendige etiketter under plukning i stedet for efter plukning.</span><span class="sxs-lookup"><span data-stu-id="a4318-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="a4318-107">Ved udskrivning af bølgeetiketter bruges ZPL (Zebra Programming Language) til oprettelse af etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="a4318-108">Et etiketlayout er inddelt i tre sektioner (overskrift, brødtekst og sidefod) for at give mulighed for etiketter med gentagelsesstruktur.</span><span class="sxs-lookup"><span data-stu-id="a4318-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="a4318-109">Med bølgeetiketskabeloner kan du fortælle systemet, hvilket etiketlayout der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="a4318-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="a4318-110">Brugerne kan angive, hvilken printer der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="a4318-110">Users can specify which printer is used.</span></span> <span data-ttu-id="a4318-111">De kan også udskrive etiketter på flere printere på samme tid efter behov.</span><span class="sxs-lookup"><span data-stu-id="a4318-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="a4318-112">Siden **Historik over bølgeetiketter** viser en oversigt over alle de etiketter, der er oprettet med denne opsætning.</span><span class="sxs-lookup"><span data-stu-id="a4318-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="a4318-113">Du kan udskrive og sortere etiketter ud fra arbejdsoverskrifterne, du kan udskrive brudetiketter efter arbejdsoverskrift, og og du kan udskrive containerindholdsetiketter, kasseetiketter og andre lignende etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="a4318-114">Denne funktionalitet erstatter ikke eksisterende udskrivningsfunktioner for etiketter, der er baseret på dokumentdistribution.</span><span class="sxs-lookup"><span data-stu-id="a4318-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="a4318-115">Ved udskrivning af bølgeetiketter kan du vælge mellem følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="a4318-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="a4318-116">Udskriv etiketter i overensstemmelse med antallet af kartoner på en enkelt arbejdslinje uden brug af containerisering.</span><span class="sxs-lookup"><span data-stu-id="a4318-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="a4318-117">(En "karton" er en enhed, der er angivet i enhedsseriegruppelinjer.)</span><span class="sxs-lookup"><span data-stu-id="a4318-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="a4318-118">Udskriv flere forskellige etiketserier (f.eks. kartoner og palleetiketter).</span><span class="sxs-lookup"><span data-stu-id="a4318-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="a4318-119">Medtag etiketfasttekst (f.eks. 1/124, 2/124,... 124/124), og definer intervallet for fasttekst (f.eks. arbejdslinje, lastlinje eller forsendelse).</span><span class="sxs-lookup"><span data-stu-id="a4318-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="a4318-120">Opret og udskriv et fragtseddel-id på etiketter, før fragtsedlen genereres.</span><span class="sxs-lookup"><span data-stu-id="a4318-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="a4318-121">Opret en entydig SSCC (serial shipping container code) for hver enkelt karton, og medtag den på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="a4318-122">Opret GS1-kompatible nummerserier til fragtseddel-id'er og SSCC'er.</span><span class="sxs-lookup"><span data-stu-id="a4318-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="a4318-123">Genudskriv etiketter både fra mobilenheder og den detaljerede klient.</span><span class="sxs-lookup"><span data-stu-id="a4318-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="a4318-124">Annuller etiketter (f.eks. i korte pluk-scenarier), og udskriv dem igen.</span><span class="sxs-lookup"><span data-stu-id="a4318-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="a4318-125">Rydde op i historikken over bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="a4318-126">Forbedringer af layoutene til dokumentruteplanlægning deles mellem layoutene til dokumentruteplanlægning og bølgeetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="a4318-127">(Yderligere oplysninger finder du i [Dokumentruteplanlægning for layout til id-etiketter](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="a4318-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="a4318-128">Disse forbedringer gør det mere effektivt at mærke kartoner før palletisering.</span><span class="sxs-lookup"><span data-stu-id="a4318-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="a4318-129">De er særligt fordelagtige for firmaer, der leverer til store detailhandlere, der automatisk bekræfter ordretilgang ved at scanne hver enkelt karton separat.</span><span class="sxs-lookup"><span data-stu-id="a4318-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="a4318-130">Du kan implementere de konfigurationsscenarier, der er beskrevet i dette emne, enten enkeltvis eller i kombination, afhængigt af dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="a4318-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="a4318-131">Du kan designe flere bølgeetiketskabeloner, der fungerer i rækkefølge (som vist i scenarie 3).</span><span class="sxs-lookup"><span data-stu-id="a4318-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="a4318-132">Du kan f.eks. bruge scenarie 1 til at udskrive kartoner og scenarie 2 til at udskrive palleetiketter (hvis paller på lager er forskellig i størrelse og sammensætning).</span><span class="sxs-lookup"><span data-stu-id="a4318-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="a4318-133">Slå funktionen til udskrivning af bølgeetiketter til</span><span class="sxs-lookup"><span data-stu-id="a4318-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="a4318-134">Før du kan bruge funktionen *Udskrivning af bølgeetiketter*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="a4318-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a4318-135">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="a4318-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a4318-136">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="a4318-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a4318-137">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="a4318-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a4318-138">**Funktionsnavn:** *Udskrivning af bølgeetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="a4318-139">Scenarie 1: Udskrivning af bølgeetiketter, hvor der genereres en enkelt bølgeetiket</span><span class="sxs-lookup"><span data-stu-id="a4318-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="a4318-140">Dette scenarie viser, hvordan et firma kan udskrive forsendelsesetiketter for en stor forhandler, der automatisk bekræfter ordretilgange ved at scanne hver enkelt karton for sig.</span><span class="sxs-lookup"><span data-stu-id="a4318-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="a4318-141">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="a4318-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a4318-142">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="a4318-142">Make demo data available</span></span>

<span data-ttu-id="a4318-143">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a4318-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="a4318-144">Kontroller, at bølgeetiketmetoden er tilgængelig</span><span class="sxs-lookup"><span data-stu-id="a4318-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="a4318-145">Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a4318-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="a4318-146">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="a4318-147">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="a4318-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="a4318-148">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="a4318-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="a4318-149">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="a4318-149">Configure a wave template</span></span>

<span data-ttu-id="a4318-150">Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.</span><span class="sxs-lookup"><span data-stu-id="a4318-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="a4318-151">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a4318-152">Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.</span><span class="sxs-lookup"><span data-stu-id="a4318-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="a4318-153">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="a4318-154">I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*.</span><span class="sxs-lookup"><span data-stu-id="a4318-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="a4318-155">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="a4318-156">Oprette et bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="a4318-156">Create a wave label layout</span></span>

<span data-ttu-id="a4318-157">Etiketlayoutet bestemmer, hvilke oplysninger der udskrives på etiketten, og hvordan de er opstillet. Her skal du angive den ZPL-kode, der sendes til printeren.</span><span class="sxs-lookup"><span data-stu-id="a4318-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="a4318-158">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="a4318-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="a4318-159">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-160">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="a4318-161">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="a4318-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="a4318-162">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-163">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="a4318-164">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="a4318-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="a4318-165">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="a4318-166">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-167">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="a4318-168">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="a4318-169">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="a4318-170">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="a4318-171">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-171">**Row height:** *0*</span></span>

        <span data-ttu-id="a4318-172">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="a4318-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="a4318-173">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="a4318-174">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="a4318-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="a4318-175">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="a4318-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="a4318-176">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a4318-177">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="a4318-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-178">Close the page.</span></span>
1. <span data-ttu-id="a4318-179">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a4318-180">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-181">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-182">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-183">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="a4318-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="a4318-184">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="a4318-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="a4318-185">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="a4318-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="a4318-186">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="a4318-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="a4318-187">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-188">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="a4318-189">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="a4318-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="a4318-190">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="a4318-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="a4318-191">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="a4318-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="a4318-192">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="a4318-193">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="a4318-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="a4318-194">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="a4318-195">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="a4318-196">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="a4318-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="a4318-197">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="a4318-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="a4318-198">Din etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="a4318-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="a4318-199">Oprette et bølgeetikettype</span><span class="sxs-lookup"><span data-stu-id="a4318-199">Create a wave label type</span></span>

<span data-ttu-id="a4318-200">Bølgeetikettyper bruges til at knytte bølgeetiketskabeloner til en enhed på enhedsseriegruppelinjer.</span><span class="sxs-lookup"><span data-stu-id="a4318-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="a4318-201">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.</span><span class="sxs-lookup"><span data-stu-id="a4318-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="a4318-202">Tilføj en bølgetype, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="a4318-203">**Etikettype:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="a4318-204">**Beskrivelse:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="a4318-205">Konfigurer enhedsseriegrupper</span><span class="sxs-lookup"><span data-stu-id="a4318-205">Set up unit sequence groups</span></span>

<span data-ttu-id="a4318-206">Konfigurer derefter enhedsseriegruppen for bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="a4318-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="a4318-207">Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="a4318-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="a4318-208">Vælg gruppen **Hver boks PL**.</span><span class="sxs-lookup"><span data-stu-id="a4318-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="a4318-209">For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="a4318-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="a4318-210">Oprette et bølgeetiketskabelon</span><span class="sxs-lookup"><span data-stu-id="a4318-210">Create a wave label template</span></span>

<span data-ttu-id="a4318-211">Opret derefter en bølgeetiketskabelon til bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="a4318-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="a4318-212">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="a4318-213">Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:</span><span class="sxs-lookup"><span data-stu-id="a4318-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="a4318-214">**Navn på etiketskabelon:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="a4318-215">**Beskrivelse:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="a4318-216">**Kode for bølgetrin:** *UdskrivEtiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="a4318-217">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="a4318-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a4318-218">Gå til oversigtspanelet **Generelt**, og indstil feltet **Bølgeetikettype**  til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="a4318-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="a4318-219">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en ny række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-220">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="a4318-221">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="a4318-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="a4318-222">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="a4318-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="a4318-223">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-224">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="a4318-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="a4318-225">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="a4318-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="a4318-226">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-227">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-228">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-229">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="a4318-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="a4318-230">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="a4318-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="a4318-231">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="a4318-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="a4318-232">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="a4318-233">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-234">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-235">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-236">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="a4318-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="a4318-237">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="a4318-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a4318-238">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-239">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="a4318-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="a4318-240">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="a4318-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="a4318-241">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="a4318-242">I dialogboksen **Gruppe af bølgeetiketskabeloner** skal du vælge den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id* og derefter markere afkrydsningsfeltet **Etiket-build-id** for denne række.</span><span class="sxs-lookup"><span data-stu-id="a4318-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-243">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="a4318-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="a4318-244">Denne etiketserie kan udskrives på etiketlayoutet.</span><span class="sxs-lookup"><span data-stu-id="a4318-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="a4318-245">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="a4318-245">Configure number sequence extensions</span></span>

<span data-ttu-id="a4318-246">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="a4318-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="a4318-247">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="a4318-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="a4318-248">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="a4318-249">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="a4318-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="a4318-250">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="a4318-251">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a4318-252">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a4318-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a4318-253">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="a4318-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a4318-254">Tilføj to salgslinjer, der har følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="a4318-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="a4318-255">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="a4318-255">Sales order line 1:</span></span>

        - <span data-ttu-id="a4318-256">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a4318-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="a4318-257">**Antal:** *9024*</span><span class="sxs-lookup"><span data-stu-id="a4318-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="a4318-258">**Enhed:** *hver* (9024 hver = 376 boks = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="a4318-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="a4318-259">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="a4318-259">Sales order line 2:</span></span>

        - <span data-ttu-id="a4318-260">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a4318-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="a4318-261">**Antal:** *9016*</span><span class="sxs-lookup"><span data-stu-id="a4318-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="a4318-262">**Enhed:** *hver* (9016 hver = 322 boks = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="a4318-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-263">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="a4318-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="a4318-264">De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="a4318-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="a4318-265">Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="a4318-266">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="a4318-266">Select sales order line 1.</span></span> <span data-ttu-id="a4318-267">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="a4318-268">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="a4318-269">Gentag trin 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="a4318-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="a4318-270">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a4318-271">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="a4318-271">The following events occur:</span></span>

    - <span data-ttu-id="a4318-272">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="a4318-273">Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="a4318-274">Der genereres og udskrives bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="a4318-275">Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1 og 322 boks-etiketter til linje 2).</span><span class="sxs-lookup"><span data-stu-id="a4318-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="a4318-276">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="a4318-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="a4318-277">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="a4318-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="a4318-278">Du kan få vist og udskrive bølgeetiketter fra følgende sider.</span><span class="sxs-lookup"><span data-stu-id="a4318-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="a4318-279">Gå til handlingsruden på enhver side, og vælg **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="a4318-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="a4318-280">Alle forsendelser \> Forsendelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="a4318-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="a4318-281">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="a4318-281">All loads \> Load details</span></span>
- <span data-ttu-id="a4318-282">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="a4318-282">All waves</span></span>
- <span data-ttu-id="a4318-283">Bølgelabels</span><span class="sxs-lookup"><span data-stu-id="a4318-283">Wave labels</span></span>
- <span data-ttu-id="a4318-284">Historik for bølgelabel</span><span class="sxs-lookup"><span data-stu-id="a4318-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="a4318-285">Scenarie 2: Udskrivning af bølgeetiketter til containerisering (uden bølgeetiketposter)</span><span class="sxs-lookup"><span data-stu-id="a4318-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="a4318-286">I dette scenarie kan du udskrive bølgeetiketter, når du bruger containerisering, til automatisk opdeling af varer i kartoner, og du har derfor ikke brug for en bølgeetiketpost.</span><span class="sxs-lookup"><span data-stu-id="a4318-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="a4318-287">I dette tilfælde fungerer container-id'et som pladsholder for SSCC.</span><span class="sxs-lookup"><span data-stu-id="a4318-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="a4318-288">Her er de væsentligste forskelle mellem dette scenarie og scenario 1:</span><span class="sxs-lookup"><span data-stu-id="a4318-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="a4318-289">**Bølgeetiketskabeloner:** Du kan ikke vælge en bølgeetikettype, og du behøver ikke en gruppering af etiketbuilds.</span><span class="sxs-lookup"><span data-stu-id="a4318-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="a4318-290">Ellers skal du konfigurere bølgeetiketskabelonen og oprette en kæde til bølgeskabelonen på samme måde som beskrevet i scenarie 1.</span><span class="sxs-lookup"><span data-stu-id="a4318-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="a4318-291">Du skal lade bølgeetikettypen være tom, hvis der ikke skal genereres bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="a4318-292">**Bølgeetiketlayout:** Du kan konfigurere række indstillingerne for bølgeetiketlayoutet for arbejdslinjer i stedet for bølgeetiketposter.</span><span class="sxs-lookup"><span data-stu-id="a4318-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="a4318-293">Du skal konfigurere rækkeindstillingen for etiketlayoutet ved hjælp af tabellen **WHSArbejdslinje** i stedet for tabellen **WHS-Bølgeetiket**.</span><span class="sxs-lookup"><span data-stu-id="a4318-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="a4318-294">Indstillingen **Rækker pr. side** bestemmer det antal rækker, som brødtekstsektionen skal indeholde.</span><span class="sxs-lookup"><span data-stu-id="a4318-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="a4318-295">Denne konfiguration er også velegnet til forretningssituationer, hvor flere forskellige varer pakkes ind i én mærket boks eller på en palle, og denne pakkeproces kan defineres ved oprettelse af arbejde (f.eks. arbejde, der er grupperet efter forsendelse).</span><span class="sxs-lookup"><span data-stu-id="a4318-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="a4318-296">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="a4318-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a4318-297">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="a4318-297">Make demo data available</span></span>

<span data-ttu-id="a4318-298">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a4318-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="a4318-299">Kontroller, at bølgeetiketmetoden er tilgængelig</span><span class="sxs-lookup"><span data-stu-id="a4318-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="a4318-300">Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="a4318-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="a4318-301">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="a4318-302">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="a4318-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="a4318-303">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="a4318-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="a4318-304">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="a4318-304">Set up a wave template</span></span>

<span data-ttu-id="a4318-305">Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.</span><span class="sxs-lookup"><span data-stu-id="a4318-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="a4318-306">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="a4318-307">Vælg en skabelon som f.eks. **63 Containerisering**.</span><span class="sxs-lookup"><span data-stu-id="a4318-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="a4318-308">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="a4318-309">I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*.</span><span class="sxs-lookup"><span data-stu-id="a4318-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="a4318-310">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="a4318-311">Oprette et bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="a4318-311">Create a wave label layout</span></span>

1. <span data-ttu-id="a4318-312">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="a4318-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="a4318-313">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-314">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="a4318-315">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="a4318-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="a4318-316">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-317">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="a4318-318">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="a4318-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="a4318-319">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="a4318-320">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-321">**Række-id:** *Arbejdslinje*</span><span class="sxs-lookup"><span data-stu-id="a4318-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="a4318-322">**Rækketabelnavn:** *WHS-arbejdslinje*</span><span class="sxs-lookup"><span data-stu-id="a4318-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="a4318-323">**Startposition for række:** *500*</span><span class="sxs-lookup"><span data-stu-id="a4318-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="a4318-324">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="a4318-325">**Rækkehøjde:** *-50*</span><span class="sxs-lookup"><span data-stu-id="a4318-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="a4318-326">I dette felt defineres højden af hver række.</span><span class="sxs-lookup"><span data-stu-id="a4318-326">This field defines the height of each row.</span></span> <span data-ttu-id="a4318-327">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="a4318-328">**Rækker pr. side:** *5*</span><span class="sxs-lookup"><span data-stu-id="a4318-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="a4318-329">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a4318-330">Denne opsætning vil udskrive flere ZPL-etiketter pr. arbejde, hvor hver side kan indeholde op til fem arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="a4318-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="a4318-331">Hvis der f.eks. udskrives en etiket for en container med 12 linjer, udskrives der tre etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="a4318-332">Hvis du vil udskrive en separat label for hver pluklinje, skal du angive denne værdi til *1*.</span><span class="sxs-lookup"><span data-stu-id="a4318-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="a4318-333">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-333">Close the page.</span></span>
1. <span data-ttu-id="a4318-334">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a4318-335">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-336">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-337">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-338">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="a4318-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="a4318-339">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="a4318-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="a4318-340">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="a4318-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="a4318-341">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-342">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="a4318-343">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="a4318-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="a4318-344">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="a4318-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="a4318-345">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="a4318-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="a4318-346">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="a4318-347">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="a4318-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="a4318-348">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="a4318-349">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="a4318-350">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="a4318-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="a4318-351">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="a4318-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="a4318-352">Din etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="a4318-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="a4318-353">Oprette et bølgeetiketskabelon</span><span class="sxs-lookup"><span data-stu-id="a4318-353">Create a wave label template</span></span>

1. <span data-ttu-id="a4318-354">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="a4318-355">Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:</span><span class="sxs-lookup"><span data-stu-id="a4318-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="a4318-356">**Navn på etiketskabelon:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="a4318-357">**Beskrivelse:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="a4318-358">**Kode for bølgetrin:** *UdskrivEtiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="a4318-359">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="a4318-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="a4318-360">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-361">**Etiketlayout-id:** *Container*</span><span class="sxs-lookup"><span data-stu-id="a4318-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="a4318-362">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="a4318-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="a4318-363">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="a4318-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="a4318-364">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-365">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="a4318-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="a4318-366">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="a4318-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="a4318-367">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-368">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-369">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-370">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="a4318-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="a4318-371">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="a4318-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="a4318-372">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="a4318-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="a4318-373">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="a4318-373">Configure number sequence extensions</span></span>

<span data-ttu-id="a4318-374">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="a4318-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="a4318-375">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="a4318-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="a4318-376">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="a4318-377">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="a4318-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="a4318-378">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="a4318-379">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a4318-380">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a4318-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a4318-381">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="a4318-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="a4318-382">Tilføj fem salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="a4318-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="a4318-383">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="a4318-383">Sales order line 1:</span></span>

        - <span data-ttu-id="a4318-384">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a4318-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="a4318-385">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="a4318-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="a4318-386">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="a4318-386">Sales order line 2:</span></span>

        - <span data-ttu-id="a4318-387">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a4318-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="a4318-388">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="a4318-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="a4318-389">Salgsordrelinje 3:</span><span class="sxs-lookup"><span data-stu-id="a4318-389">Sales order line 3:</span></span>

        - <span data-ttu-id="a4318-390">**Varenummer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="a4318-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="a4318-391">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="a4318-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="a4318-392">Salgsordrelinje 4:</span><span class="sxs-lookup"><span data-stu-id="a4318-392">Sales order line 4:</span></span>

        - <span data-ttu-id="a4318-393">**Varenummer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="a4318-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="a4318-394">**Antal:** *40*</span><span class="sxs-lookup"><span data-stu-id="a4318-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="a4318-395">Salgsordrelinje 5:</span><span class="sxs-lookup"><span data-stu-id="a4318-395">Sales order line 5:</span></span>

        - <span data-ttu-id="a4318-396">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="a4318-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="a4318-397">**Antal:** *50*</span><span class="sxs-lookup"><span data-stu-id="a4318-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-398">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="a4318-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="a4318-399">De skal være lager på det angivne lagersted.</span><span class="sxs-lookup"><span data-stu-id="a4318-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="a4318-400">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="a4318-400">Select sales order line 1.</span></span> <span data-ttu-id="a4318-401">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="a4318-402">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="a4318-403">Gentag trin 4 og 5 for hver ekstra salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="a4318-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="a4318-404">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a4318-405">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="a4318-405">The following events occur:</span></span>

    - <span data-ttu-id="a4318-406">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="a4318-407">Etiketlayoutet bruges til at definere etikettens format, og slutresultatet vil være en etiket, der har fem linjer, og som udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="a4318-408">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="a4318-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="a4318-409">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="a4318-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="a4318-410">Du kan udskrive disse bølgeetiketter igen ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Historik over bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="a4318-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="a4318-411">Scenarie 3: Udskrivning af bølgeetiketter til etiketter med flere niveauer</span><span class="sxs-lookup"><span data-stu-id="a4318-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="a4318-412">Dette scenarie viser, hvordan du kan bruge funktionen til udskrivning af bølgeetiketter, når lagerprocesserne kræver flere niveauer af forsendelsesetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="a4318-413">Der kan f eks. være adskilte etiketter for kartoner og paller, og det kan være nødvendigt at udskrive en brudetiket for hele forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="a4318-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="a4318-414">Brudetiketter er en separat type etiket, der kan bruges som delelinje mellem ruller og containere, f eks. etiketter til forsendelses-id'et og en stregkode, så etiketterne nemt kan sorteres, når de er udskrevet.</span><span class="sxs-lookup"><span data-stu-id="a4318-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="a4318-415">Den væsentligste forskel mellem konfigurationen af dette scenarie og konfigurationen af scenarie 1, ud over det faktum, at etiketter er aktiveret, er, at der skal knyttes flere bølgeetikettyper til linjerne i enhedsseriegrupperne.</span><span class="sxs-lookup"><span data-stu-id="a4318-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="a4318-416">Hvis du vil udføre denne konfiguration, skal du konfigurere følgende elementer for dette scenarie:</span><span class="sxs-lookup"><span data-stu-id="a4318-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="a4318-417">**Bølgebehandlingsmetoder:** Du kan markere bølgeetiketmetoden som "kan gentages", føje den to (eller flere) gange til bølgeskabelonen og angive forskellige bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="a4318-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="a4318-418">**Bølgeetiketskabeloner:** Du kan konfigurere bølgeetiketskabelonerne og knytte dem til bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="a4318-419">Hver enkelt bølgeetiketskabelon har sin egen bølgeetikettype.</span><span class="sxs-lookup"><span data-stu-id="a4318-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="a4318-420">**Bølgeetiketlayout:** Du kan oprette flere bølgeetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="a4318-421">Der vil være et separat etiketlayout for hvert "lag" af etiketter, og der vil også være et brudetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="a4318-422">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="a4318-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="a4318-423">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="a4318-423">Make demo data available</span></span>

<span data-ttu-id="a4318-424">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="a4318-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="a4318-425">Konfigurere en bølgebehandlingsmetode</span><span class="sxs-lookup"><span data-stu-id="a4318-425">Set up a wave process method</span></span>

1. <span data-ttu-id="a4318-426">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="a4318-427">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="a4318-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="a4318-428">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="a4318-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="a4318-429">Når det gælder metoden **bølgeEtiketUdskrivning** skal du markere afkrydsningsfeltet **Gør metode reperterbar**.</span><span class="sxs-lookup"><span data-stu-id="a4318-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="a4318-430">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="a4318-430">Set up a wave template</span></span>

1. <span data-ttu-id="a4318-431">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="a4318-432">Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.</span><span class="sxs-lookup"><span data-stu-id="a4318-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="a4318-433">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="a4318-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="a4318-434">I kolonnen **Valgte metoder** skal du tildele en værdi for **Bølgetrinkode** som f.eks. *Karton* til metoden **Udskrivning af bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="a4318-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="a4318-435">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="a4318-436">Flyt metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder** en gang mere.</span><span class="sxs-lookup"><span data-stu-id="a4318-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="a4318-437">I kolonnen **Valgte metoder** skal du tildele en anden værdi for **Bølgetrinkode** som f.eks. *Palle* til den anden metode til **Udskrivning af bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="a4318-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="a4318-438">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="a4318-439">Oprette tre bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="a4318-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="a4318-440">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="a4318-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="a4318-441">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-442">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="a4318-443">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="a4318-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="a4318-444">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-445">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="a4318-446">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="a4318-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="a4318-447">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="a4318-448">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-449">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="a4318-450">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="a4318-451">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="a4318-452">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="a4318-453">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-453">**Row height:** *0*</span></span>

        <span data-ttu-id="a4318-454">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="a4318-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="a4318-455">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="a4318-456">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="a4318-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="a4318-457">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="a4318-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="a4318-458">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a4318-459">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="a4318-460">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-460">Close the page.</span></span>
1. <span data-ttu-id="a4318-461">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a4318-462">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-463">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-464">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-465">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="a4318-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="a4318-466">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="a4318-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="a4318-467">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="a4318-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="a4318-468">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="a4318-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="a4318-469">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-470">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="a4318-471">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="a4318-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="a4318-472">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="a4318-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="a4318-473">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="a4318-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="a4318-474">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="a4318-475">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="a4318-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="a4318-476">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="a4318-477">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="a4318-478">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="a4318-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="a4318-479">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="a4318-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="a4318-480">Den første etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="a4318-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="a4318-481">Opret en anden layoutpost, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-482">**Etiketlayout-id:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="a4318-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="a4318-483">**Beskrivelse:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="a4318-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="a4318-484">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-485">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="a4318-486">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="a4318-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="a4318-487">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="a4318-488">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-489">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="a4318-490">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="a4318-491">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="a4318-492">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="a4318-493">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="a4318-493">**Row height:** *0*</span></span>

        <span data-ttu-id="a4318-494">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="a4318-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="a4318-495">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="a4318-496">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="a4318-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="a4318-497">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="a4318-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="a4318-498">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a4318-499">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="a4318-500">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-500">Close the page.</span></span>
1. <span data-ttu-id="a4318-501">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a4318-502">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-503">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-504">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-505">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="a4318-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="a4318-506">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="a4318-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="a4318-507">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="a4318-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="a4318-508">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="a4318-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="a4318-509">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-510">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="a4318-511">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="a4318-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="a4318-512">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="a4318-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="a4318-513">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="a4318-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="a4318-514">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="a4318-515">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="a4318-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="a4318-516">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="a4318-517">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="a4318-518">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="a4318-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="a4318-519">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="a4318-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="a4318-520">Den anden etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="a4318-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="a4318-521">Opret en tredje layoutpost, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-522">**Etiketlayout-id:** *Brud*</span><span class="sxs-lookup"><span data-stu-id="a4318-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="a4318-523">**Beskrivelse:** *Brudetiket*</span><span class="sxs-lookup"><span data-stu-id="a4318-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="a4318-524">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-525">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="a4318-526">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en ZPL-kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="a4318-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="a4318-527">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="a4318-528">Denne gang er brødtekst ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="a4318-528">This time, no body is required.</span></span> <span data-ttu-id="a4318-529">Du skal derfor blot angive den nødvendige tekst i sektionen **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="a4318-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="a4318-530">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="a4318-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="a4318-531">Den tredje etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="a4318-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-532">Denne tredje etiket er en brudetiket, der vil blive brugt som delelinje mellem etiketruller.</span><span class="sxs-lookup"><span data-stu-id="a4318-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="a4318-533">Oprette to bølgeetikettyper</span><span class="sxs-lookup"><span data-stu-id="a4318-533">Create two wave label types</span></span>

1. <span data-ttu-id="a4318-534">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.</span><span class="sxs-lookup"><span data-stu-id="a4318-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="a4318-535">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-536">**Etikettype:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="a4318-537">**Beskrivelse:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="a4318-538">Opret en anden post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="a4318-539">**Etikettype:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="a4318-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="a4318-540">**Beskrivelse:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="a4318-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="a4318-541">Konfigurer enhedsseriegrupper</span><span class="sxs-lookup"><span data-stu-id="a4318-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="a4318-542">Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="a4318-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="a4318-543">Vælg eller opret en **Hver boks PL**-gruppe.</span><span class="sxs-lookup"><span data-stu-id="a4318-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="a4318-544">For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="a4318-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="a4318-545">For linjen **PL** skal du indstille feltet **Bølgeniveautype** til *Palle*.</span><span class="sxs-lookup"><span data-stu-id="a4318-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="a4318-546">Oprette bølgeetiketskabeloner</span><span class="sxs-lookup"><span data-stu-id="a4318-546">Create wave label templates</span></span>

1. <span data-ttu-id="a4318-547">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="a4318-548">Opret en etiketskabelon, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="a4318-549">**Navn på etiketskabelon:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="a4318-550">**Beskrivelse:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="a4318-551">**Kode for bølgetrin:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="a4318-552">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="a4318-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a4318-553">I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Karton*.</span><span class="sxs-lookup"><span data-stu-id="a4318-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="a4318-554">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-555">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="a4318-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="a4318-556">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="a4318-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="a4318-557">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="a4318-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="a4318-558">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-559">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="a4318-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="a4318-560">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="a4318-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="a4318-561">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-562">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-563">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-564">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="a4318-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="a4318-565">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="a4318-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="a4318-566">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="a4318-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="a4318-567">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="a4318-568">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-569">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-570">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-571">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="a4318-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="a4318-572">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="a4318-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a4318-573">Tilføj en anden række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-574">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-575">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-576">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="a4318-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="a4318-577">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="a4318-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a4318-578">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-579">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="a4318-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="a4318-580">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="a4318-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="a4318-581">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="a4318-582">Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:</span><span class="sxs-lookup"><span data-stu-id="a4318-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="a4318-583">**Udskriv brudetiket:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="a4318-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="a4318-584">**Etiketlayout-id:** Vælg en brudetiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="a4318-585">(Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)</span><span class="sxs-lookup"><span data-stu-id="a4318-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="a4318-586">**Printernavn:** Vælg printeren til brudetiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="a4318-587">(Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="a4318-588">Andre scenarier er dog mulige.)</span><span class="sxs-lookup"><span data-stu-id="a4318-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="a4318-589">Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.</span><span class="sxs-lookup"><span data-stu-id="a4318-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-590">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="a4318-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="a4318-591">Denne etiketserie kan udskrives på et etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="a4318-592">Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="a4318-593">Vælg **OK** for at lukke dialogboksen **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="a4318-594">Opret en anden etiketskabelon, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="a4318-595">**Navn på etiketskabelon:** *Palleetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="a4318-596">**Beskrivelse:** *Palleetiketter*</span><span class="sxs-lookup"><span data-stu-id="a4318-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="a4318-597">**Kode for bølgetrin:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="a4318-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="a4318-598">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="a4318-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a4318-599">I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Palle*.</span><span class="sxs-lookup"><span data-stu-id="a4318-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="a4318-600">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-601">**Etiketlayout-id:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="a4318-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="a4318-602">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="a4318-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="a4318-603">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="a4318-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="a4318-604">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4318-605">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="a4318-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="a4318-606">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="a4318-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="a4318-607">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-608">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-609">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="a4318-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="a4318-610">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="a4318-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="a4318-611">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="a4318-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="a4318-612">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="a4318-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="a4318-613">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="a4318-614">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-615">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-616">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-617">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="a4318-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="a4318-618">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="a4318-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a4318-619">Tilføj en anden række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="a4318-620">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-621">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="a4318-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="a4318-622">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="a4318-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="a4318-623">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="a4318-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="a4318-624">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="a4318-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="a4318-625">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="a4318-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="a4318-626">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="a4318-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="a4318-627">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="a4318-628">Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:</span><span class="sxs-lookup"><span data-stu-id="a4318-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="a4318-629">**Udskriv brudetiket:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="a4318-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="a4318-630">**Etiketlayout-id:** Vælg en brudetiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="a4318-631">(Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)</span><span class="sxs-lookup"><span data-stu-id="a4318-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="a4318-632">**Printernavn:** Vælg printeren til brudetiketten.</span><span class="sxs-lookup"><span data-stu-id="a4318-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="a4318-633">(Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a4318-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="a4318-634">Andre scenarier er dog mulige.)</span><span class="sxs-lookup"><span data-stu-id="a4318-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="a4318-635">Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.</span><span class="sxs-lookup"><span data-stu-id="a4318-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-636">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="a4318-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="a4318-637">Denne etiketserie kan udskrives på et etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="a4318-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="a4318-638">Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.</span><span class="sxs-lookup"><span data-stu-id="a4318-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="a4318-639">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="a4318-639">Configure number sequence extensions</span></span>

<span data-ttu-id="a4318-640">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="a4318-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="a4318-641">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="a4318-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="a4318-642">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="a4318-643">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="a4318-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="a4318-644">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="a4318-645">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="a4318-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a4318-646">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a4318-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a4318-647">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="a4318-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="a4318-648">Tilføj to salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="a4318-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="a4318-649">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="a4318-649">Sales order line 1:</span></span>

        - <span data-ttu-id="a4318-650">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a4318-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="a4318-651">**Antal:** *9024*</span><span class="sxs-lookup"><span data-stu-id="a4318-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="a4318-652">**Enhed:** *hver* (9024 hver = 376 boks = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="a4318-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="a4318-653">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="a4318-653">Sales order line 2:</span></span>

        - <span data-ttu-id="a4318-654">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="a4318-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="a4318-655">**Antal:** *9016*</span><span class="sxs-lookup"><span data-stu-id="a4318-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="a4318-656">**Enhed:** *hver* (9016 hver = 322 boks = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="a4318-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4318-657">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="a4318-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="a4318-658">De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="a4318-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="a4318-659">Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="a4318-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="a4318-660">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="a4318-660">Select sales order line 1.</span></span> <span data-ttu-id="a4318-661">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="a4318-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="a4318-662">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="a4318-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="a4318-663">Gentag trin 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="a4318-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="a4318-664">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a4318-665">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="a4318-665">The following events occur:</span></span> 

    - <span data-ttu-id="a4318-666">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="a4318-667">Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a4318-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="a4318-668">Der genereres og udskrives bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="a4318-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="a4318-669">Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1, 322 boks-etiketter til linje 2, 47 palle-etiketter til linje 1, 47 palle-etiketter til linje 2 og to brudetiketter, der har forsendelses-id'et).</span><span class="sxs-lookup"><span data-stu-id="a4318-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="a4318-670">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="a4318-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="a4318-671">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="a4318-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="a4318-672">Du kan få vist og udskrive bølgeetiketter fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="a4318-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="a4318-673">Alle forsendelser \> Forsendelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="a4318-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="a4318-674">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="a4318-674">All loads \> Load details</span></span>
- <span data-ttu-id="a4318-675">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="a4318-675">All waves</span></span>
- <span data-ttu-id="a4318-676">Bølgelabels</span><span class="sxs-lookup"><span data-stu-id="a4318-676">Wave labels</span></span>
- <span data-ttu-id="a4318-677">Historik for bølgelabel</span><span class="sxs-lookup"><span data-stu-id="a4318-677">Wave label history</span></span>

<span data-ttu-id="a4318-678">På de fleste af disse sider kan du finde den relevante funktion ved at vælge **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a4318-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
