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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 862987b8ccdc4272bdd404e78391ad447bc290b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996345"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="21874-103">Konfigurere og bruge bølgeetiketudskrivning</span><span class="sxs-lookup"><span data-stu-id="21874-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21874-104">Ved udskrivning af bølgeetiket kan du vælge en alternativ metode til udskrivning af etiketter ved at introducere en ny metode til bølgetrin, der giver dig mulighed for at oprette og udskrive etiketter direkte fra bølgeskabelonen under bølgeudførelse.</span><span class="sxs-lookup"><span data-stu-id="21874-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="21874-105">Etiketterne vil derfor allerede være tilgængelige, før arbejderne kører arbejdsordren på en mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="21874-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="21874-106">Arbejderne kan derefter tilknytte de nødvendige etiketter under plukning i stedet for efter plukning.</span><span class="sxs-lookup"><span data-stu-id="21874-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="21874-107">Ved udskrivning af bølgeetiketter bruges ZPL (Zebra Programming Language) til oprettelse af etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="21874-108">Et etiketlayout er inddelt i tre sektioner (overskrift, brødtekst og sidefod) for at give mulighed for etiketter med gentagelsesstruktur.</span><span class="sxs-lookup"><span data-stu-id="21874-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="21874-109">Med bølgeetiketskabeloner kan du fortælle systemet, hvilket etiketlayout der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="21874-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="21874-110">Brugerne kan angive, hvilken printer der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="21874-110">Users can specify which printer is used.</span></span> <span data-ttu-id="21874-111">De kan også udskrive etiketter på flere printere på samme tid efter behov.</span><span class="sxs-lookup"><span data-stu-id="21874-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="21874-112">Siden **Historik over bølgeetiketter** viser en oversigt over alle de etiketter, der er oprettet med denne opsætning.</span><span class="sxs-lookup"><span data-stu-id="21874-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="21874-113">Du kan udskrive og sortere etiketter ud fra arbejdsoverskrifterne, du kan udskrive brudetiketter efter arbejdsoverskrift, og og du kan udskrive containerindholdsetiketter, kasseetiketter og andre lignende etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="21874-114">Denne funktionalitet erstatter ikke eksisterende udskrivningsfunktioner for etiketter, der er baseret på dokumentdistribution.</span><span class="sxs-lookup"><span data-stu-id="21874-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="21874-115">Ved udskrivning af bølgeetiketter kan du vælge mellem følgende forbedringer:</span><span class="sxs-lookup"><span data-stu-id="21874-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="21874-116">Udskriv etiketter i overensstemmelse med antallet af kartoner på en enkelt arbejdslinje uden brug af containerisering.</span><span class="sxs-lookup"><span data-stu-id="21874-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="21874-117">(En "karton" er en enhed, der er angivet i enhedsseriegruppelinjer.)</span><span class="sxs-lookup"><span data-stu-id="21874-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="21874-118">Udskriv flere forskellige etiketserier (f.eks. kartoner og palleetiketter).</span><span class="sxs-lookup"><span data-stu-id="21874-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="21874-119">Medtag etiketfasttekst (f.eks. 1/124, 2/124,... 124/124), og definer intervallet for fasttekst (f.eks. arbejdslinje, lastlinje eller forsendelse).</span><span class="sxs-lookup"><span data-stu-id="21874-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="21874-120">Opret og udskriv et fragtseddel-id på etiketter, før fragtsedlen genereres.</span><span class="sxs-lookup"><span data-stu-id="21874-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="21874-121">Opret en entydig SSCC (serial shipping container code) for hver enkelt karton, og medtag den på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="21874-122">Opret GS1-kompatible nummerserier til fragtseddel-id'er og SSCC'er.</span><span class="sxs-lookup"><span data-stu-id="21874-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="21874-123">Genudskriv etiketter både fra mobilenheder og den detaljerede klient.</span><span class="sxs-lookup"><span data-stu-id="21874-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="21874-124">Annuller etiketter (f.eks. i korte pluk-scenarier), og udskriv dem igen.</span><span class="sxs-lookup"><span data-stu-id="21874-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="21874-125">Rydde op i historikken over bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="21874-126">Forbedringer af layoutene til dokumentruteplanlægning deles mellem layoutene til dokumentruteplanlægning og bølgeetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="21874-127">(Yderligere oplysninger finder du i [Dokumentruteplanlægning for layout til id-etiketter](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="21874-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="21874-128">Disse forbedringer gør det mere effektivt at mærke kartoner før palletisering.</span><span class="sxs-lookup"><span data-stu-id="21874-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="21874-129">De er særligt fordelagtige for firmaer, der leverer til store detailhandlere, der automatisk bekræfter ordretilgang ved at scanne hver enkelt karton separat.</span><span class="sxs-lookup"><span data-stu-id="21874-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="21874-130">Du kan implementere de konfigurationsscenarier, der er beskrevet i dette emne, enten enkeltvis eller i kombination, afhængigt af dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="21874-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="21874-131">Du kan designe flere bølgeetiketskabeloner, der fungerer i rækkefølge (som vist i scenarie 3).</span><span class="sxs-lookup"><span data-stu-id="21874-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="21874-132">Du kan f.eks. bruge scenarie 1 til at udskrive kartoner og scenarie 2 til at udskrive palleetiketter (hvis paller på lager er forskellig i størrelse og sammensætning).</span><span class="sxs-lookup"><span data-stu-id="21874-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="21874-133">Slå funktionen til udskrivning af bølgeetiketter til</span><span class="sxs-lookup"><span data-stu-id="21874-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="21874-134">Før du kan bruge funktionen *Udskrivning af bølgeetiketter*, skal den være aktiveret i dit system.</span><span class="sxs-lookup"><span data-stu-id="21874-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="21874-135">Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="21874-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="21874-136">Dér vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="21874-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="21874-137">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="21874-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="21874-138">**Funktionsnavn:** *Udskrivning af bølgeetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="21874-139">Scenarie 1: Udskrivning af bølgeetiketter, hvor der genereres en enkelt bølgeetiket</span><span class="sxs-lookup"><span data-stu-id="21874-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="21874-140">Dette scenarie viser, hvordan et firma kan udskrive forsendelsesetiketter for en stor forhandler, der automatisk bekræfter ordretilgange ved at scanne hver enkelt karton for sig.</span><span class="sxs-lookup"><span data-stu-id="21874-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="21874-141">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="21874-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="21874-142">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="21874-142">Make demo data available</span></span>

<span data-ttu-id="21874-143">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="21874-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="21874-144">Kontroller, at bølgeetiketmetoden er tilgængelig</span><span class="sxs-lookup"><span data-stu-id="21874-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="21874-145">Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="21874-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="21874-146">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="21874-147">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="21874-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="21874-148">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="21874-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="21874-149">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="21874-149">Configure a wave template</span></span>

<span data-ttu-id="21874-150">Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.</span><span class="sxs-lookup"><span data-stu-id="21874-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="21874-151">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="21874-152">Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.</span><span class="sxs-lookup"><span data-stu-id="21874-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="21874-153">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="21874-154">I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*.</span><span class="sxs-lookup"><span data-stu-id="21874-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="21874-155">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21874-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="21874-156">Oprette et bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="21874-156">Create a wave label layout</span></span>

<span data-ttu-id="21874-157">Etiketlayoutet bestemmer, hvilke oplysninger der udskrives på etiketten, og hvordan de er opstillet. Her skal du angive den ZPL-kode, der sendes til printeren.</span><span class="sxs-lookup"><span data-stu-id="21874-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="21874-158">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="21874-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="21874-159">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="21874-160">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="21874-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="21874-161">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="21874-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="21874-162">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-163">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="21874-164">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="21874-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="21874-165">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="21874-166">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-167">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="21874-168">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="21874-169">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="21874-170">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="21874-171">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-171">**Row height:** *0*</span></span>

        <span data-ttu-id="21874-172">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="21874-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="21874-173">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="21874-174">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="21874-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="21874-175">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="21874-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="21874-176">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="21874-177">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="21874-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21874-178">Close the page.</span></span>
1. <span data-ttu-id="21874-179">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="21874-180">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-181">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-182">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-183">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="21874-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="21874-184">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="21874-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="21874-185">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="21874-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="21874-186">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="21874-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="21874-187">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-188">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="21874-189">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="21874-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="21874-190">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="21874-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

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

1. <span data-ttu-id="21874-191">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="21874-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="21874-192">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-192">Here is an example.</span></span>

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

1. <span data-ttu-id="21874-193">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="21874-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="21874-194">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="21874-195">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="21874-196">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="21874-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="21874-197">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="21874-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="21874-198">Din etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="21874-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="21874-199">Oprette et bølgeetikettype</span><span class="sxs-lookup"><span data-stu-id="21874-199">Create a wave label type</span></span>

<span data-ttu-id="21874-200">Bølgeetikettyper bruges til at knytte bølgeetiketskabeloner til en enhed på enhedsseriegruppelinjer.</span><span class="sxs-lookup"><span data-stu-id="21874-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="21874-201">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.</span><span class="sxs-lookup"><span data-stu-id="21874-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="21874-202">Tilføj en bølgetype, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="21874-203">**Etikettype:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="21874-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="21874-204">**Beskrivelse:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="21874-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="21874-205">Konfigurer enhedsseriegrupper</span><span class="sxs-lookup"><span data-stu-id="21874-205">Set up unit sequence groups</span></span>

<span data-ttu-id="21874-206">Konfigurer derefter enhedsseriegruppen for bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="21874-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="21874-207">Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="21874-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="21874-208">Vælg gruppen **Hver boks PL**.</span><span class="sxs-lookup"><span data-stu-id="21874-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="21874-209">For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="21874-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="21874-210">Oprette et bølgeetiketskabelon</span><span class="sxs-lookup"><span data-stu-id="21874-210">Create a wave label template</span></span>

<span data-ttu-id="21874-211">Opret derefter en bølgeetiketskabelon til bølgeetikettypen.</span><span class="sxs-lookup"><span data-stu-id="21874-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="21874-212">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="21874-213">Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:</span><span class="sxs-lookup"><span data-stu-id="21874-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="21874-214">**Navn på etiketskabelon:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="21874-215">**Beskrivelse:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="21874-216">**Kode for bølgetrin:** *UdskrivEtiket*</span><span class="sxs-lookup"><span data-stu-id="21874-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="21874-217">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="21874-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="21874-218">Gå til oversigtspanelet **Generelt**, og indstil feltet **Bølgeetikettype**  til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="21874-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="21874-219">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en ny række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="21874-220">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="21874-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="21874-221">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="21874-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="21874-222">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="21874-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="21874-223">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-224">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="21874-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="21874-225">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="21874-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="21874-226">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-227">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-228">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-229">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="21874-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="21874-230">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="21874-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="21874-231">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="21874-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="21874-232">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="21874-233">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-234">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-235">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-236">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="21874-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="21874-237">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="21874-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="21874-238">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-239">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="21874-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="21874-240">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="21874-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="21874-241">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="21874-242">I dialogboksen **Gruppe af bølgeetiketskabeloner** skal du vælge den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id* og derefter markere afkrydsningsfeltet **Etiket-build-id** for denne række.</span><span class="sxs-lookup"><span data-stu-id="21874-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-243">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="21874-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="21874-244">Denne etiketserie kan udskrives på etiketlayoutet.</span><span class="sxs-lookup"><span data-stu-id="21874-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="21874-245">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="21874-245">Configure number sequence extensions</span></span>

<span data-ttu-id="21874-246">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="21874-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="21874-247">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="21874-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="21874-248">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="21874-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="21874-249">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="21874-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="21874-250">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="21874-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="21874-251">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21874-252">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21874-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21874-253">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="21874-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="21874-254">Tilføj to salgslinjer, der har følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="21874-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="21874-255">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="21874-255">Sales order line 1:</span></span>

        - <span data-ttu-id="21874-256">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="21874-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="21874-257">**Antal:** *9024*</span><span class="sxs-lookup"><span data-stu-id="21874-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="21874-258">**Enhed:** *hver* (9024 hver = 376 boks = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="21874-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="21874-259">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="21874-259">Sales order line 2:</span></span>

        - <span data-ttu-id="21874-260">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="21874-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="21874-261">**Antal:** *9016*</span><span class="sxs-lookup"><span data-stu-id="21874-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="21874-262">**Enhed:** *hver* (9016 hver = 322 boks = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="21874-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-263">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="21874-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="21874-264">De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="21874-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="21874-265">Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="21874-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="21874-266">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="21874-266">Select sales order line 1.</span></span> <span data-ttu-id="21874-267">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="21874-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="21874-268">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="21874-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="21874-269">Gentag trin 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="21874-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="21874-270">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="21874-271">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="21874-271">The following events occur:</span></span>

    - <span data-ttu-id="21874-272">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="21874-273">Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="21874-274">Der genereres og udskrives bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="21874-275">Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1 og 322 boks-etiketter til linje 2).</span><span class="sxs-lookup"><span data-stu-id="21874-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="21874-276">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="21874-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="21874-277">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="21874-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="21874-278">Du kan få vist og udskrive bølgeetiketter fra følgende sider.</span><span class="sxs-lookup"><span data-stu-id="21874-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="21874-279">Gå til handlingsruden på enhver side, og vælg **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="21874-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="21874-280">Alle forsendelser \> Forsendelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="21874-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="21874-281">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="21874-281">All loads \> Load details</span></span>
- <span data-ttu-id="21874-282">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="21874-282">All waves</span></span>
- <span data-ttu-id="21874-283">Bølgelabels</span><span class="sxs-lookup"><span data-stu-id="21874-283">Wave labels</span></span>
- <span data-ttu-id="21874-284">Historik for bølgelabel</span><span class="sxs-lookup"><span data-stu-id="21874-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="21874-285">Scenarie 2: Udskrivning af bølgeetiketter til containerisering (uden bølgeetiketposter)</span><span class="sxs-lookup"><span data-stu-id="21874-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="21874-286">I dette scenarie kan du udskrive bølgeetiketter, når du bruger containerisering, til automatisk opdeling af varer i kartoner, og du har derfor ikke brug for en bølgeetiketpost.</span><span class="sxs-lookup"><span data-stu-id="21874-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="21874-287">I dette tilfælde fungerer container-id'et som pladsholder for SSCC.</span><span class="sxs-lookup"><span data-stu-id="21874-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="21874-288">Her er de væsentligste forskelle mellem dette scenarie og scenario 1:</span><span class="sxs-lookup"><span data-stu-id="21874-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="21874-289">**Bølgeetiketskabeloner:** Du kan ikke vælge en bølgeetikettype, og du behøver ikke en gruppering af etiketbuilds.</span><span class="sxs-lookup"><span data-stu-id="21874-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="21874-290">Ellers skal du konfigurere bølgeetiketskabelonen og oprette en kæde til bølgeskabelonen på samme måde som beskrevet i scenarie 1.</span><span class="sxs-lookup"><span data-stu-id="21874-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="21874-291">Du skal lade bølgeetikettypen være tom, hvis der ikke skal genereres bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="21874-292">**Bølgeetiketlayout:** Du kan konfigurere række indstillingerne for bølgeetiketlayoutet for arbejdslinjer i stedet for bølgeetiketposter.</span><span class="sxs-lookup"><span data-stu-id="21874-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="21874-293">Du skal konfigurere rækkeindstillingen for etiketlayoutet ved hjælp af tabellen **WHSArbejdslinje** i stedet for tabellen **WHS-Bølgeetiket**.</span><span class="sxs-lookup"><span data-stu-id="21874-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="21874-294">Indstillingen **Rækker pr. side** bestemmer det antal rækker, som brødtekstsektionen skal indeholde.</span><span class="sxs-lookup"><span data-stu-id="21874-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="21874-295">Denne konfiguration er også velegnet til forretningssituationer, hvor flere forskellige varer pakkes ind i én mærket boks eller på en palle, og denne pakkeproces kan defineres ved oprettelse af arbejde (f.eks. arbejde, der er grupperet efter forsendelse).</span><span class="sxs-lookup"><span data-stu-id="21874-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="21874-296">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="21874-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="21874-297">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="21874-297">Make demo data available</span></span>

<span data-ttu-id="21874-298">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="21874-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="21874-299">Kontroller, at bølgeetiketmetoden er tilgængelig</span><span class="sxs-lookup"><span data-stu-id="21874-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="21874-300">Du skal muligvis oprette bølgeprocesmetoderne igen for at gøre metoden til bølgeetiketudskrivning tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="21874-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="21874-301">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="21874-302">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="21874-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="21874-303">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="21874-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="21874-304">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="21874-304">Set up a wave template</span></span>

<span data-ttu-id="21874-305">Med bølgeskabeloner kan du knytte bestemte forekomster af bølgemetoder til en tilsvarende bølgeetiketskabelon.</span><span class="sxs-lookup"><span data-stu-id="21874-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="21874-306">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="21874-307">Vælg en skabelon som f.eks. **63 Containerisering**.</span><span class="sxs-lookup"><span data-stu-id="21874-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="21874-308">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="21874-309">I kolonnen **Valgte metoder** skal du vælge metoden **Udskrivning af bølgeetiketter** og angive feltet **Bølgetrinskode** til *UdskrivEtiket*.</span><span class="sxs-lookup"><span data-stu-id="21874-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="21874-310">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21874-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="21874-311">Oprette et bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="21874-311">Create a wave label layout</span></span>

1. <span data-ttu-id="21874-312">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="21874-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="21874-313">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="21874-314">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="21874-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="21874-315">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="21874-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="21874-316">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-317">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="21874-318">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="21874-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="21874-319">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="21874-320">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-321">**Række-id:** *Arbejdslinje*</span><span class="sxs-lookup"><span data-stu-id="21874-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="21874-322">**Rækketabelnavn:** *WHS-arbejdslinje*</span><span class="sxs-lookup"><span data-stu-id="21874-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="21874-323">**Startposition for række:** *500*</span><span class="sxs-lookup"><span data-stu-id="21874-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="21874-324">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="21874-325">**Rækkehøjde:** *-50*</span><span class="sxs-lookup"><span data-stu-id="21874-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="21874-326">I dette felt defineres højden af hver række.</span><span class="sxs-lookup"><span data-stu-id="21874-326">This field defines the height of each row.</span></span> <span data-ttu-id="21874-327">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="21874-328">**Rækker pr. side:** *5*</span><span class="sxs-lookup"><span data-stu-id="21874-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="21874-329">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="21874-330">Denne opsætning vil udskrive flere ZPL-etiketter pr. arbejde, hvor hver side kan indeholde op til fem arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="21874-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="21874-331">Hvis der f.eks. udskrives en etiket for en container med 12 linjer, udskrives der tre etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="21874-332">Hvis du vil udskrive en separat label for hver pluklinje, skal du angive denne værdi til *1*.</span><span class="sxs-lookup"><span data-stu-id="21874-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="21874-333">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21874-333">Close the page.</span></span>
1. <span data-ttu-id="21874-334">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="21874-335">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-336">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-337">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-338">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="21874-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="21874-339">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="21874-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="21874-340">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="21874-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="21874-341">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-342">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="21874-343">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="21874-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="21874-344">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="21874-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="21874-345">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="21874-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="21874-346">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-346">Here is an example.</span></span>

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

1. <span data-ttu-id="21874-347">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="21874-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="21874-348">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="21874-349">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="21874-350">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="21874-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="21874-351">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="21874-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="21874-352">Din etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="21874-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="21874-353">Oprette et bølgeetiketskabelon</span><span class="sxs-lookup"><span data-stu-id="21874-353">Create a wave label template</span></span>

1. <span data-ttu-id="21874-354">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="21874-355">Føj en bølgeniveauskabelon, og angiv følgende værdier i sidehovedet:</span><span class="sxs-lookup"><span data-stu-id="21874-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="21874-356">**Navn på etiketskabelon:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="21874-357">**Beskrivelse:** *Containeretiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="21874-358">**Kode for bølgetrin:** *UdskrivEtiket*</span><span class="sxs-lookup"><span data-stu-id="21874-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="21874-359">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="21874-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="21874-360">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-361">**Etiketlayout-id:** *Container*</span><span class="sxs-lookup"><span data-stu-id="21874-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="21874-362">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="21874-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="21874-363">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="21874-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="21874-364">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-365">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="21874-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="21874-366">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="21874-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="21874-367">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-368">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-369">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-370">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="21874-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="21874-371">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="21874-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="21874-372">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="21874-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="21874-373">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="21874-373">Configure number sequence extensions</span></span>

<span data-ttu-id="21874-374">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="21874-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="21874-375">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="21874-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="21874-376">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="21874-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="21874-377">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="21874-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="21874-378">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="21874-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="21874-379">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21874-380">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21874-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21874-381">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="21874-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="21874-382">Tilføj fem salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="21874-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="21874-383">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="21874-383">Sales order line 1:</span></span>

        - <span data-ttu-id="21874-384">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="21874-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="21874-385">**Antal:** *10*</span><span class="sxs-lookup"><span data-stu-id="21874-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="21874-386">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="21874-386">Sales order line 2:</span></span>

        - <span data-ttu-id="21874-387">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="21874-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="21874-388">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="21874-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="21874-389">Salgsordrelinje 3:</span><span class="sxs-lookup"><span data-stu-id="21874-389">Sales order line 3:</span></span>

        - <span data-ttu-id="21874-390">**Varenummer:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="21874-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="21874-391">**Antal:** *20*</span><span class="sxs-lookup"><span data-stu-id="21874-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="21874-392">Salgsordrelinje 4:</span><span class="sxs-lookup"><span data-stu-id="21874-392">Sales order line 4:</span></span>

        - <span data-ttu-id="21874-393">**Varenummer:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="21874-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="21874-394">**Antal:** *40*</span><span class="sxs-lookup"><span data-stu-id="21874-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="21874-395">Salgsordrelinje 5:</span><span class="sxs-lookup"><span data-stu-id="21874-395">Sales order line 5:</span></span>

        - <span data-ttu-id="21874-396">**Varenummer:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="21874-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="21874-397">**Antal:** *50*</span><span class="sxs-lookup"><span data-stu-id="21874-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-398">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="21874-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="21874-399">De skal være lager på det angivne lagersted.</span><span class="sxs-lookup"><span data-stu-id="21874-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="21874-400">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="21874-400">Select sales order line 1.</span></span> <span data-ttu-id="21874-401">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="21874-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="21874-402">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="21874-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="21874-403">Gentag trin 4 og 5 for hver ekstra salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="21874-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="21874-404">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="21874-405">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="21874-405">The following events occur:</span></span>

    - <span data-ttu-id="21874-406">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="21874-407">Etiketlayoutet bruges til at definere etikettens format, og slutresultatet vil være en etiket, der har fem linjer, og som udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="21874-408">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="21874-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="21874-409">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="21874-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="21874-410">Du kan udskrive disse bølgeetiketter igen ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Historik over bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="21874-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="21874-411">Scenarie 3: Udskrivning af bølgeetiketter til etiketter med flere niveauer</span><span class="sxs-lookup"><span data-stu-id="21874-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="21874-412">Dette scenarie viser, hvordan du kan bruge funktionen til udskrivning af bølgeetiketter, når lagerprocesserne kræver flere niveauer af forsendelsesetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="21874-413">Der kan f eks. være adskilte etiketter for kartoner og paller, og det kan være nødvendigt at udskrive en brudetiket for hele forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="21874-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="21874-414">Brudetiketter er en separat type etiket, der kan bruges som delelinje mellem ruller og containere, f eks. etiketter til forsendelses-id'et og en stregkode, så etiketterne nemt kan sorteres, når de er udskrevet.</span><span class="sxs-lookup"><span data-stu-id="21874-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="21874-415">Den væsentligste forskel mellem konfigurationen af dette scenarie og konfigurationen af scenarie 1, ud over det faktum, at etiketter er aktiveret, er, at der skal knyttes flere bølgeetikettyper til linjerne i enhedsseriegrupperne.</span><span class="sxs-lookup"><span data-stu-id="21874-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="21874-416">Hvis du vil udføre denne konfiguration, skal du konfigurere følgende elementer for dette scenarie:</span><span class="sxs-lookup"><span data-stu-id="21874-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="21874-417">**Bølgebehandlingsmetoder:** Du kan markere bølgeetiketmetoden som "kan gentages", føje den to (eller flere) gange til bølgeskabelonen og angive forskellige bølgetrinskoder.</span><span class="sxs-lookup"><span data-stu-id="21874-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="21874-418">**Bølgeetiketskabeloner:** Du kan konfigurere bølgeetiketskabelonerne og knytte dem til bølgeskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="21874-419">Hver enkelt bølgeetiketskabelon har sin egen bølgeetikettype.</span><span class="sxs-lookup"><span data-stu-id="21874-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="21874-420">**Bølgeetiketlayout:** Du kan oprette flere bølgeetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="21874-421">Der vil være et separat etiketlayout for hvert "lag" af etiketter, og der vil også være et brudetiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="21874-422">Dette scenarie viser forløbet fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="21874-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="21874-423">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="21874-423">Make demo data available</span></span>

<span data-ttu-id="21874-424">Hvis du vil følge dette scenarie skal du have installeret demodata, og du skal bruge den juridiske enhed **USMF**.</span><span class="sxs-lookup"><span data-stu-id="21874-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="21874-425">Konfigurere en bølgebehandlingsmetode</span><span class="sxs-lookup"><span data-stu-id="21874-425">Set up a wave process method</span></span>

1. <span data-ttu-id="21874-426">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="21874-427">Kontroller, at **bølgeEtiketUdskrivning** findes på listen.</span><span class="sxs-lookup"><span data-stu-id="21874-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="21874-428">Hvis den ikke gør det, skal du vælge **Genopret metoder** i handlingsruden for at tilføje den.</span><span class="sxs-lookup"><span data-stu-id="21874-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="21874-429">Når det gælder metoden **bølgeEtiketUdskrivning** skal du markere afkrydsningsfeltet **Gør metode reperterbar**.</span><span class="sxs-lookup"><span data-stu-id="21874-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="21874-430">Konfigurere en bølgeskabelon</span><span class="sxs-lookup"><span data-stu-id="21874-430">Set up a wave template</span></span>

1. <span data-ttu-id="21874-431">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="21874-432">Vælg en skabelon som f.eks. **62 Forsendelsesstandard**.</span><span class="sxs-lookup"><span data-stu-id="21874-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="21874-433">I oversigtspanelet **Metoder** skal du flytte metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder**.</span><span class="sxs-lookup"><span data-stu-id="21874-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="21874-434">I kolonnen **Valgte metoder** skal du tildele en værdi for **Bølgetrinkode** som f.eks. *Karton* til metoden **Udskrivning af bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="21874-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="21874-435">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21874-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="21874-436">Flyt metoden **Udskrivning af bølgeetiketter** til kolonnen **Valgte metoder** en gang mere.</span><span class="sxs-lookup"><span data-stu-id="21874-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="21874-437">I kolonnen **Valgte metoder** skal du tildele en anden værdi for **Bølgetrinkode** som f.eks. *Palle* til den anden metode til **Udskrivning af bølgeetiketter**.</span><span class="sxs-lookup"><span data-stu-id="21874-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="21874-438">Du kan få flere oplysninger om bølgetrinkoder under [Bølgetrinkoder](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21874-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="21874-439">Oprette tre bølgeetiketlayout</span><span class="sxs-lookup"><span data-stu-id="21874-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="21874-440">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketlayout**.</span><span class="sxs-lookup"><span data-stu-id="21874-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="21874-441">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="21874-442">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="21874-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="21874-443">**Beskrivelse:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="21874-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="21874-444">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-445">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="21874-446">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="21874-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="21874-447">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="21874-448">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-449">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="21874-450">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="21874-451">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="21874-452">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="21874-453">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-453">**Row height:** *0*</span></span>

        <span data-ttu-id="21874-454">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="21874-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="21874-455">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="21874-456">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="21874-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="21874-457">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="21874-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="21874-458">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="21874-459">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="21874-460">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21874-460">Close the page.</span></span>
1. <span data-ttu-id="21874-461">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="21874-462">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-463">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-464">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-465">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="21874-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="21874-466">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="21874-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="21874-467">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="21874-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="21874-468">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="21874-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="21874-469">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-470">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="21874-471">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="21874-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="21874-472">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="21874-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


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

1. <span data-ttu-id="21874-473">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="21874-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="21874-474">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-474">Here is an example.</span></span>

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

1. <span data-ttu-id="21874-475">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="21874-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="21874-476">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="21874-477">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="21874-478">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="21874-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="21874-479">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="21874-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="21874-480">Den første etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="21874-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="21874-481">Opret en anden layoutpost, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="21874-482">**Etiketlayout-id:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="21874-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="21874-483">**Beskrivelse:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="21874-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="21874-484">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-485">Vælg **Indstillinger for bølgeetiketrækker** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="21874-486">Siden **Indstillinger for bølgeetiketrækker** vises.</span><span class="sxs-lookup"><span data-stu-id="21874-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="21874-487">Her kan du konfigurere den dynamiske del af etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="21874-488">Tilføj en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-489">**Række-id:** *Bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="21874-490">**Rækketabelnavn:** *WHS-bølgeetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="21874-491">**Startposition for række:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="21874-492">I dette felt defineres den lodrette position, hvor rækken skal begynde på etiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="21874-493">**Rækkehøjde:** *0*</span><span class="sxs-lookup"><span data-stu-id="21874-493">**Row height:** *0*</span></span>

        <span data-ttu-id="21874-494">I dette felt defineres højden af hver række (i punkter) i henhold til ZPL-standarden.</span><span class="sxs-lookup"><span data-stu-id="21874-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="21874-495">Rækkehøjden er positiv for vandrette etiketter og negative for lodrette etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="21874-496">Da der kun er én række i dette eksempel, kan du angive værdien til *0* (nul).</span><span class="sxs-lookup"><span data-stu-id="21874-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="21874-497">**Rækker pr. side:** *1*</span><span class="sxs-lookup"><span data-stu-id="21874-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="21874-498">Dette felt definerer det antal rækker, der kan udskrives på hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="21874-499">Denne opsætning medfører, at der udskrives en separat ZPL-etiket for hver post i tabellen Bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="21874-500">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="21874-500">Close the page.</span></span>
1. <span data-ttu-id="21874-501">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="21874-502">I dialogboksen for forespørgselseditor skal du under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-503">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-504">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-505">**Felt:** *Arbejdstype*</span><span class="sxs-lookup"><span data-stu-id="21874-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="21874-506">**Kriterier:** *Pluk*</span><span class="sxs-lookup"><span data-stu-id="21874-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="21874-507">Denne forespørgsel sikrer, at der kun udskrives arbejdslinjer af pluktypen på etiketten og ikke arbejdslinjer af læg på lager-typen.</span><span class="sxs-lookup"><span data-stu-id="21874-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="21874-508">Hvis du vil have mulighed for at udskrive fragtseddel-id'et, skal du under fanen **Join-forbindelser** vælge tabellen **Arbejdslinje** og knytte tabellen **Forsendelser** til den.</span><span class="sxs-lookup"><span data-stu-id="21874-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="21874-509">Luk dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-510">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="21874-511">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="21874-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="21874-512">Hvis du f. eks. bruger Zebra-printere, kan du bruge følgende kode.</span><span class="sxs-lookup"><span data-stu-id="21874-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="21874-513">I sektionen **Brødtekst** skal du i feltet **Etiketbrødtekst** angiv en ZPL-kode for den påkrævede brødtekst.</span><span class="sxs-lookup"><span data-stu-id="21874-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="21874-514">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="21874-515">I sektionen **Brødtekst** skal du i feltet **Etiketsidefod** angiv en ZPL-kode for den påkrævede sidefod.</span><span class="sxs-lookup"><span data-stu-id="21874-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="21874-516">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="21874-517">Denne opsætning vil udskrive én kopi af hver etiket.</span><span class="sxs-lookup"><span data-stu-id="21874-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="21874-518">Hvis du har brug for flere kopier (f.eks. én kopi for hver side af pallen), skal du angive værdien **n-** for **\^PQn** i sidefoden til det påkrævede antal kopier.</span><span class="sxs-lookup"><span data-stu-id="21874-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="21874-519">Hvis du f.eks. vil udskrive fire kopier af hver etiket, skal du angive **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="21874-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="21874-520">Den anden etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="21874-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="21874-521">Opret en tredje layoutpost, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="21874-522">**Etiketlayout-id:** *Brud*</span><span class="sxs-lookup"><span data-stu-id="21874-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="21874-523">**Beskrivelse:** *Brudetiket*</span><span class="sxs-lookup"><span data-stu-id="21874-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="21874-524">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-525">Oversigtspanelet **Layout af printertekst** indeholder tre sektioner, hvor du kan skrive printerkode: **Sidehoved**, **Brødtekst** og **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="21874-526">I sektionen **Sidehoved** skal du i feltet **Etiketsidehoved** angiv en ZPL-kode for det påkrævede sidehoved.</span><span class="sxs-lookup"><span data-stu-id="21874-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="21874-527">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="21874-528">Denne gang er brødtekst ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="21874-528">This time, no body is required.</span></span> <span data-ttu-id="21874-529">Du skal derfor blot angive den nødvendige tekst i sektionen **Sidefod**.</span><span class="sxs-lookup"><span data-stu-id="21874-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="21874-530">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="21874-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="21874-531">Den tredje etiket er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="21874-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-532">Denne tredje etiket er en brudetiket, der vil blive brugt som delelinje mellem etiketruller.</span><span class="sxs-lookup"><span data-stu-id="21874-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="21874-533">Oprette to bølgeetikettyper</span><span class="sxs-lookup"><span data-stu-id="21874-533">Create two wave label types</span></span>

1. <span data-ttu-id="21874-534">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetikettyper**.</span><span class="sxs-lookup"><span data-stu-id="21874-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="21874-535">Opret en post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="21874-536">**Etikettype:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="21874-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="21874-537">**Beskrivelse:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="21874-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="21874-538">Opret en anden post, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="21874-539">**Etikettype:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="21874-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="21874-540">**Beskrivelse:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="21874-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="21874-541">Konfigurer enhedsseriegrupper</span><span class="sxs-lookup"><span data-stu-id="21874-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="21874-542">Gå til **Lokationsstyring \> Opsætning \> Lagersted \> Enhedsseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="21874-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="21874-543">Vælg eller opret en **Hver boks PL**-gruppe.</span><span class="sxs-lookup"><span data-stu-id="21874-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="21874-544">For linjen **Boks** skal du indstille feltet **Bølgeniveautype** til *Karton*.</span><span class="sxs-lookup"><span data-stu-id="21874-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="21874-545">For linjen **PL** skal du indstille feltet **Bølgeniveautype** til *Palle*.</span><span class="sxs-lookup"><span data-stu-id="21874-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="21874-546">Oprette bølgeetiketskabeloner</span><span class="sxs-lookup"><span data-stu-id="21874-546">Create wave label templates</span></span>

1. <span data-ttu-id="21874-547">Gå til **Lokationsstyring \> Opsætning \> Dokumentruteplanlægning \> Bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="21874-548">Opret en etiketskabelon, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="21874-549">**Navn på etiketskabelon:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="21874-550">**Beskrivelse:** *Kartonetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="21874-551">**Kode for bølgetrin:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="21874-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="21874-552">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="21874-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="21874-553">I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Karton*.</span><span class="sxs-lookup"><span data-stu-id="21874-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="21874-554">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-555">**Etiketlayout-id:** *karton*</span><span class="sxs-lookup"><span data-stu-id="21874-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="21874-556">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="21874-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="21874-557">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="21874-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="21874-558">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-559">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="21874-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="21874-560">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="21874-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="21874-561">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-562">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-563">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-564">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="21874-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="21874-565">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="21874-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="21874-566">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="21874-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="21874-567">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="21874-568">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-569">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-570">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-571">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="21874-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="21874-572">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="21874-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="21874-573">Tilføj en anden række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="21874-574">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-575">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-576">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="21874-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="21874-577">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="21874-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="21874-578">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-579">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="21874-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="21874-580">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="21874-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="21874-581">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="21874-582">Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:</span><span class="sxs-lookup"><span data-stu-id="21874-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="21874-583">**Udskriv brudetiket:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="21874-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="21874-584">**Etiketlayout-id:** Vælg en brudetiket.</span><span class="sxs-lookup"><span data-stu-id="21874-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="21874-585">(Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)</span><span class="sxs-lookup"><span data-stu-id="21874-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="21874-586">**Printernavn:** Vælg printeren til brudetiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="21874-587">(Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="21874-588">Andre scenarier er dog mulige.)</span><span class="sxs-lookup"><span data-stu-id="21874-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="21874-589">Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.</span><span class="sxs-lookup"><span data-stu-id="21874-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-590">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="21874-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="21874-591">Denne etiketserie kan udskrives på et etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="21874-592">Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.</span><span class="sxs-lookup"><span data-stu-id="21874-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="21874-593">Vælg **OK** for at lukke dialogboksen **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="21874-594">Opret en anden etiketskabelon, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="21874-595">**Navn på etiketskabelon:** *Palleetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="21874-596">**Beskrivelse:** *Palleetiketter*</span><span class="sxs-lookup"><span data-stu-id="21874-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="21874-597">**Kode for bølgetrin:** *Palle*</span><span class="sxs-lookup"><span data-stu-id="21874-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="21874-598">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="21874-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="21874-599">I oversigtspanelet **Generelt** skal du i feltet **Bølgeetikettype** vælge en værdi som f.eks. *Palle*.</span><span class="sxs-lookup"><span data-stu-id="21874-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="21874-600">I oversigtspanelet **Detaljer om bølgeetiketskabeloner** skal du tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-601">**Etiketlayout-id:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="21874-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="21874-602">**Printernavn:** Vælg en relevant ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="21874-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="21874-603">**Kør forespørgsel:** *Ja* (denne indstilling er valgfri, men den anbefales for at opnå den optimale ydeevne).</span><span class="sxs-lookup"><span data-stu-id="21874-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="21874-604">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="21874-605">Valgfrit: Hvis du konfigurerer et kundespecifikt etiketdesign, skal du oprette en forespørgsel for at finde kundens konto.</span><span class="sxs-lookup"><span data-stu-id="21874-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="21874-606">Gå til oversigtspanelet **Detaljer om bølgeetiketskabeloner**, og vælg **Rediger forespørgsel**.</span><span class="sxs-lookup"><span data-stu-id="21874-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="21874-607">I dialogboksen for forespørgselseditor skal du derefter under fanen **Område** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-608">**Tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-609">**Afledt tabel:** *Forsendelser*</span><span class="sxs-lookup"><span data-stu-id="21874-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="21874-610">**Felt:** *Kontonummer*</span><span class="sxs-lookup"><span data-stu-id="21874-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="21874-611">**Kriterier:** Angiv det relevante debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="21874-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="21874-612">Når du er færdig, skal du vælge **OK** for at lukke dialogboksen for forespørgselseditor.</span><span class="sxs-lookup"><span data-stu-id="21874-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="21874-613">I handlingsruden skal du vælge **Rediger forespørgsel** for at at åbne dialogboksen for forespørgselseditoren for hele etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="21874-614">I dialogboksen for forespørgselseditor skal du under fanen **Sortering** tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="21874-615">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-616">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-617">**Felt:** *Referencelastlinje-id (post-id)*</span><span class="sxs-lookup"><span data-stu-id="21874-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="21874-618">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="21874-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="21874-619">Tilføj en anden række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="21874-620">**Tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-621">**Afledt tabel:** *Arbejdslinjer*</span><span class="sxs-lookup"><span data-stu-id="21874-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="21874-622">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="21874-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="21874-623">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="21874-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="21874-624">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="21874-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="21874-625">I en meddelelsesboks beder dig om at bekræfte nulstillingen af grupperingsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="21874-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="21874-626">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="21874-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="21874-627">Gå til handlingsruden, og vælg **Gruppe af bølgeetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="21874-628">Gå til dialogboksen **Gruppe af bølgeetiketskabeloner**, og angiv følgende værdier for hver række i feltet **Referencefeltnavn**, der er angivet til *Forsendelses-id*:</span><span class="sxs-lookup"><span data-stu-id="21874-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="21874-629">**Udskriv brudetiket:** Markér dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="21874-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="21874-630">**Etiketlayout-id:** Vælg en brudetiket.</span><span class="sxs-lookup"><span data-stu-id="21874-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="21874-631">(Du kan f.eks. vælge det etiketlayout for *Brud*, som du har oprettet tidligere i dette scenarie.)</span><span class="sxs-lookup"><span data-stu-id="21874-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="21874-632">**Printernavn:** Vælg printeren til brudetiketten.</span><span class="sxs-lookup"><span data-stu-id="21874-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="21874-633">(Hvis du vil opdele etiketten, skal du son regel vælge den samme printer, som er valgt i oversigtspanelet **Detaljer om bølgetiketskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="21874-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="21874-634">Andre scenarier er dog mulige.)</span><span class="sxs-lookup"><span data-stu-id="21874-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="21874-635">Når det gælder den række, hvor feltet **Referencefeltnavn** er indstillet til *Referencelastlinje-id*, skal du markere afkrydsningsfeltet **Etiket-build-id**.</span><span class="sxs-lookup"><span data-stu-id="21874-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-636">Denne opsætning opretter en etiketserie ("karton 1 af X") pr. lastlinje i hele bølgen, uanset opsætningen af arbejdsgrupperingen.</span><span class="sxs-lookup"><span data-stu-id="21874-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="21874-637">Denne etiketserie kan udskrives på et etiketlayout.</span><span class="sxs-lookup"><span data-stu-id="21874-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="21874-638">Derudover vil etiketter til forskellige forsendelser blive adskilt af den valgte brudetiket.</span><span class="sxs-lookup"><span data-stu-id="21874-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="21874-639">Konfigurere nummerserieudvidelser</span><span class="sxs-lookup"><span data-stu-id="21874-639">Configure number sequence extensions</span></span>

<span data-ttu-id="21874-640">Nummerserieudvidelser styrer GS1-overholdelse af specifikke nummerserier.</span><span class="sxs-lookup"><span data-stu-id="21874-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="21874-641">Denne konfiguration er valgfri for det aktuelle scenarie.</span><span class="sxs-lookup"><span data-stu-id="21874-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="21874-642">Du kan finde flere oplysninger og konfigurationsinstruktioner under [Konfigurere nummerserieudvidelser](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="21874-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="21874-643">Oprette en salgsordre og frigive den til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="21874-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="21874-644">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="21874-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="21874-645">Opret salgsordre, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="21874-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21874-646">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21874-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21874-647">**Lagersted:** *62*</span><span class="sxs-lookup"><span data-stu-id="21874-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="21874-648">Tilføj to salgsordrelinjer:</span><span class="sxs-lookup"><span data-stu-id="21874-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="21874-649">Salgsordrelinje 1:</span><span class="sxs-lookup"><span data-stu-id="21874-649">Sales order line 1:</span></span>

        - <span data-ttu-id="21874-650">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="21874-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="21874-651">**Antal:** *9024*</span><span class="sxs-lookup"><span data-stu-id="21874-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="21874-652">**Enhed:** *hver* (9024 hver = 376 boks = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="21874-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="21874-653">Salgsordrelinje 2:</span><span class="sxs-lookup"><span data-stu-id="21874-653">Sales order line 2:</span></span>

        - <span data-ttu-id="21874-654">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="21874-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="21874-655">**Antal:** *9016*</span><span class="sxs-lookup"><span data-stu-id="21874-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="21874-656">**Enhed:** *hver* (9016 hver = 322 boks = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="21874-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="21874-657">De varer og antal, der angives her, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="21874-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="21874-658">De skal bruge den enhedsseriegruppe, du har defineret tidligere, relevante enhedskonverteringer fra *hver* til *boks* til *PL* skal defineres for dem, og de skal have lager på lagerstedet *62*.</span><span class="sxs-lookup"><span data-stu-id="21874-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="21874-659">Du kan finde flere oplysninger i [Måleenhed og lagerføringspolitikker](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="21874-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="21874-660">Vælg salgsordrelinje 1.</span><span class="sxs-lookup"><span data-stu-id="21874-660">Select sales order line 1.</span></span> <span data-ttu-id="21874-661">I sektionen **Salgsordrelinje** skal du i menuen **Lager** vælge **Reservationer**.</span><span class="sxs-lookup"><span data-stu-id="21874-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="21874-662">På siden **Reservation** skal du i handlingsruden vælge **Reserver parti** og derefter lukke siden.</span><span class="sxs-lookup"><span data-stu-id="21874-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="21874-663">Gentag trin 4 og 5 for salgsordrelinje 2.</span><span class="sxs-lookup"><span data-stu-id="21874-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="21874-664">Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="21874-665">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="21874-665">The following events occur:</span></span> 

    - <span data-ttu-id="21874-666">Systemet behandler den oprettede forsendelse ved hjælp af den skabelon, der indeholder trinnet til udskrivning af etiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="21874-667">Etiketlayoutet bruges til at definere etikettens format, og resultatet vil være en etiket, der udskrives på den printer, der er valgt i etiketskabelonen.</span><span class="sxs-lookup"><span data-stu-id="21874-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="21874-668">Der genereres og udskrives bølgeetiketter.</span><span class="sxs-lookup"><span data-stu-id="21874-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="21874-669">Antallet af etiketter vil være lig med antallet af kartoner (i dette eksempel 376 boks-etiketter til linje 1, 322 boks-etiketter til linje 2, 47 palle-etiketter til linje 1, 47 palle-etiketter til linje 2 og to brudetiketter, der har forsendelses-id'et).</span><span class="sxs-lookup"><span data-stu-id="21874-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="21874-670">Der genereres et nyt fragtseddel-id for forsendelserne.</span><span class="sxs-lookup"><span data-stu-id="21874-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="21874-671">Hvis du har konfigureret nummerserieudvidelserne, følger bølgeetiket-id'erne **SSCC-18**-nummerformatet.</span><span class="sxs-lookup"><span data-stu-id="21874-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="21874-672">Du kan få vist og udskrive bølgeetiketter fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="21874-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="21874-673">Alle forsendelser \> Forsendelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="21874-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="21874-674">Alle laster \> Lastdetaljer</span><span class="sxs-lookup"><span data-stu-id="21874-674">All loads \> Load details</span></span>
- <span data-ttu-id="21874-675">Alle bølger</span><span class="sxs-lookup"><span data-stu-id="21874-675">All waves</span></span>
- <span data-ttu-id="21874-676">Bølgelabels</span><span class="sxs-lookup"><span data-stu-id="21874-676">Wave labels</span></span>
- <span data-ttu-id="21874-677">Historik for bølgelabel</span><span class="sxs-lookup"><span data-stu-id="21874-677">Wave label history</span></span>

<span data-ttu-id="21874-678">På de fleste af disse sider kan du finde den relevante funktion ved at vælge **Bølgeetiketter** i gruppen **Relaterede oplysninger** under fanen **Forsendelser** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="21874-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
