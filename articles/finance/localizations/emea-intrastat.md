---
title: Intrastat-oversigt
description: Dette emne indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU. Den indeholder en oversigt over rapporteringsprocessen og beskriver de nødvendige indstillinger og forudsætninger.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: db97d05d79a100ebdcfb5b4931b37243b77bd352
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814989"
---
# <a name="intrastat-overview"></a><span data-ttu-id="e5c63-104">Intrastat-oversigt</span><span class="sxs-lookup"><span data-stu-id="e5c63-104">Intrastat overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5c63-105">Dette emne indeholder oplysninger om Intrastat-rapportering for handel med varer og i nogle tilfælde tjenester mellem lande/områder i EU.</span><span class="sxs-lookup"><span data-stu-id="e5c63-105">This topic provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="e5c63-106">Den indeholder en oversigt over rapporteringsprocessen og beskriver de nødvendige indstillinger og forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="e5c63-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="e5c63-107">Intrastat er det system, der bruges til indsamling af oplysninger og generering af statistik over varehandel blandt lande/områder i EU.</span><span class="sxs-lookup"><span data-stu-id="e5c63-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="e5c63-108">Intrastat-rapportering er påkrævet, når et produkt krydser grænsen til et andet EU-land/område.</span><span class="sxs-lookup"><span data-stu-id="e5c63-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="e5c63-109">I nogle lande/områder gælder Intrastat-rapportering også for tjenester.</span><span class="sxs-lookup"><span data-stu-id="e5c63-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="e5c63-110">Obligatoriske og fakultative elementer kan indsamles i Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e5c63-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="e5c63-111">Følgende elementer er obligatoriske: momsnr. på den part, der er ansvarlig for at levere oplysninger, referenceperioden, strømmen (modtagelse eller forsendelse), den ottecifrede varekode, partnerens medlemsstat (afsendelsesmedlemsstaten på modtagelser) og bestemmelsesmedlemsstaten for forsendelser, varernes værdi, mængden af varer (nettomasse og supplerende enheder) og transaktionens art.</span><span class="sxs-lookup"><span data-stu-id="e5c63-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="e5c63-112">Lande/regioner kan også indsamle valgfrie elementer i forskellige situationer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="e5c63-113">Nogle valgfrie elementer er land/region, leveringsbetingelserne, transportmåden, en mere detaljeret varekode end CN8, oprindelsesområdet for forsendelser og destinationsområdet for modtagelser, den statistiske procedure, den statistiske værdi, en beskrivelse af varerne og havn/lufthavn for lastning/losning.</span><span class="sxs-lookup"><span data-stu-id="e5c63-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="e5c63-114">Oversigt over Intrastat-rapporteringsprocessen</span><span class="sxs-lookup"><span data-stu-id="e5c63-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="e5c63-115">I følgende afsnit beskrives den samlede strøm af oplysninger, der bruges til Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e5c63-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="e5c63-116">1. Angiv en transaktion, der krydser grænsen til et andet EU-land/område</span><span class="sxs-lookup"><span data-stu-id="e5c63-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="e5c63-117">En debitorfaktura, fritekstfaktura, indkøbsordrefaktura, projektfaktura, følgeseddel for kunden og leverandørens produktkvittering eller overflytningsordre overføres til Intrastat-kladden, hvis landetypen for destination (på udførsel) eller forsendelse (på indførsel) er **EU**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="e5c63-118">Denne funktion blev udvidet til Microsoft Dynamics 365 for Operations (1611) og gør det muligt at angive fragtadresser for en transaktion inden for Fællesskabet.</span><span class="sxs-lookup"><span data-stu-id="e5c63-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="e5c63-119">Hvis en fragtadresse afviger fra en leverandørs virksomhedsadresse (eller kundes virksomhedsadresse for returordre), bruges Intrastat-rapporteringen med disse oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e5c63-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="e5c63-120">Når du opretter en salgsordre, fritekstfaktura, indkøbsordre, kreditorfaktura, projektfaktura eller overflytningsordre, har nogle felter, der er relateret til udenrigshandel, standardværdier i dokumentets sidehoved eller på linjen.</span><span class="sxs-lookup"><span data-stu-id="e5c63-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="e5c63-121">Standardkoden for transaktionen er taget fra det tilsvarende felt på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-122">Standarden for varekode, oprindelsesland/-område og oprindelsesstat tages fra varen.</span><span class="sxs-lookup"><span data-stu-id="e5c63-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="e5c63-123">Du kan ændre standardværdierne, og du kan også udfylde andre udenlandske handelsrelaterede oplysninger: den statistiske procedure, transportmåde og havn.</span><span class="sxs-lookup"><span data-stu-id="e5c63-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="e5c63-124">2. Brug denne Intrastat-kladde til at generere oplysninger om handel mellem lande/områder i EU.</span><span class="sxs-lookup"><span data-stu-id="e5c63-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="e5c63-125">Til statistiske formål kan du generere oplysninger om handel mellem EU-lande/områder hver måned.</span><span class="sxs-lookup"><span data-stu-id="e5c63-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="e5c63-126">Du kan overføre posteringer fra en fritekstfaktura, debitorfaktura, debitors følgeseddel, kreditorfaktura, kreditor følgeseddel, projektfaktura eller overflytningsordre, på grundlag af kriterier for overførsel, der er angivet på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-127">Du kan også angive transaktioner manuelt.</span><span class="sxs-lookup"><span data-stu-id="e5c63-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="e5c63-128">Du kan manuelt opdatere overførte transaktioner i Intrastat-kladden, hvis opdateringer er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="e5c63-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="e5c63-129">Under bestemte betingelser, der er angivet på siden **Komprimering af Intrastat**, kan du komprimere transaktionerne i Intrastat-kladden.</span><span class="sxs-lookup"><span data-stu-id="e5c63-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="e5c63-130">For nogle lande/områder kan du anvende en tærskel på små transaktioner.</span><span class="sxs-lookup"><span data-stu-id="e5c63-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="e5c63-131">Du kan rapportere transaktioner, der ligger under tærsklen, under den angivne varekode.</span><span class="sxs-lookup"><span data-stu-id="e5c63-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="e5c63-132">Du kan opdatere varekoden på de tilsvarende Intrastat-kladdelinjer, baseret på indstillingen **Minimumsgrænse** på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-133">Du kan også komprimere de transaktioner, der er baseret på indstillingen **Komprimering af Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="e5c63-134">Du kan validere fuldstændigheden af transaktioner i Intrastat-kladden, baseret på indstillingen **Kontroller opsætning** på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-135">Dataene i de tilsvarende felter kan valideres for nøjagtighed: land/område, stat eller region, vægt, varekode, transaktionskode, supplerende enhed, havn, oprindelse, vilkår for levering, transportmåde og momsundtagelsesnummer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="e5c63-136">Transaktioner, der ikke er fuldført, markeres som ikke gyldig.</span><span class="sxs-lookup"><span data-stu-id="e5c63-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="e5c63-137">3. Brug denne Intrastat-kladde til at rapportere oplysninger om handel mellem lande/områder i EU.</span><span class="sxs-lookup"><span data-stu-id="e5c63-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="e5c63-138">Til statistiske formål kan du rapportere oplysninger om handel mellem EU-lande/områder hver måned.</span><span class="sxs-lookup"><span data-stu-id="e5c63-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="e5c63-139">Du kan udskrive Intrastat-rapporten, baseret på indstillingen **Rapportformattilknytning** på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-140">Du kan generere en elektronisk fil, baseret på indstillingen **Filformattilknytning** på siden **Udenrigshandelsparametre**.</span><span class="sxs-lookup"><span data-stu-id="e5c63-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="e5c63-141">Se Opgaveregistrering for Intrastat-rapportering for at få yderligere oplysninger om Intrastat-rapportering, herunder de nødvendige forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="e5c63-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="e5c63-142">Generere en EU Intrastat-opgørelse</span><span class="sxs-lookup"><span data-stu-id="e5c63-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="e5c63-143">Overføre transaktioner til Intrastat</span><span class="sxs-lookup"><span data-stu-id="e5c63-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="e5c63-144">Angiv fragtadresse for en transaktion inden for EU.</span><span class="sxs-lookup"><span data-stu-id="e5c63-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e5c63-145">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e5c63-145">Prerequisites</span></span>
<span data-ttu-id="e5c63-146">Tabellen nedenfor viser kravene til Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e5c63-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5c63-147">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="e5c63-147">Prerequisite</span></span></th>
<th><span data-ttu-id="e5c63-148">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e5c63-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5c63-149">Adresseopsætning</span><span class="sxs-lookup"><span data-stu-id="e5c63-149">Address setup</span></span></td>
<td><span data-ttu-id="e5c63-150">Angiv ISO-koderne for lande/områder.</span><span class="sxs-lookup"><span data-stu-id="e5c63-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-151">Juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="e5c63-151">Legal entity</span></span></td>
<td><span data-ttu-id="e5c63-152">Angiv momsfritagelsesnumre til import og eksport, afdelingens lokalnummer til import/eksport og den Intrastat-kode, der er tilknyttet den juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="e5c63-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-153">Produktkategorihierarki (salgshierarki, indkøbshierarki)</span><span class="sxs-lookup"><span data-stu-id="e5c63-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="e5c63-154">Tildel Intrastat-varekoder til kategorinoder på fanen <strong>Varekoder</strong> på siden <strong>Kategorihierarki</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5c63-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="e5c63-155">Når du tildeler en varekode til en overordnet kategorinode, er den pågældende kode gældende for alle underordnede kategorinoder.</span><span class="sxs-lookup"><span data-stu-id="e5c63-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="e5c63-156">De valgte varekoder bliver tilgængelig i visningen <strong>Valgte</strong>, når du vælger en varekode i de frigivne produktdetaljer og på linjer for salgsordre, indkøbsordre og overførselsordre.</span><span class="sxs-lookup"><span data-stu-id="e5c63-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-157">Frigivne produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="e5c63-157">Released product details</span></span></td>
<td><span data-ttu-id="e5c63-158">Opret følgende udenrigshandelsdata for frigivne produkter:</span><span class="sxs-lookup"><span data-stu-id="e5c63-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="e5c63-159"><strong>Varekode</strong> – Vælg enten en liste over valgte varer, der er hentet fra tildelte produktkategorier, eller den komplette liste over Intrastat-varekoder.</span><span class="sxs-lookup"><span data-stu-id="e5c63-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="e5c63-160"><strong>Statistiske gebyrer i procent</strong></span><span class="sxs-lookup"><span data-stu-id="e5c63-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="e5c63-161"><strong>Oprindelsesland/-område</strong> – Vælg det standardland/-område, hvor varerne blev helt fremstillet eller produceret.</span><span class="sxs-lookup"><span data-stu-id="e5c63-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="e5c63-162"><strong>Område for oprindelse/destination</strong> – Vælg standardområdet for destinationen for modtagelser og stat/provins for afsendelser.</span><span class="sxs-lookup"><span data-stu-id="e5c63-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="e5c63-163"><strong>Nettovægt i kg</strong></span><span class="sxs-lookup"><span data-stu-id="e5c63-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-164">Debitorer</span><span class="sxs-lookup"><span data-stu-id="e5c63-164">Customers</span></span></td>
<td><span data-ttu-id="e5c63-165">Angiv kundens leveringsadresse i EU-landet.</span><span class="sxs-lookup"><span data-stu-id="e5c63-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-166">Kreditorer</span><span class="sxs-lookup"><span data-stu-id="e5c63-166">Vendors</span></span></td>
<td><span data-ttu-id="e5c63-167">Angiv leverandørens adresse i EU-landet.</span><span class="sxs-lookup"><span data-stu-id="e5c63-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-168">Tillæg</span><span class="sxs-lookup"><span data-stu-id="e5c63-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="e5c63-169">Angiv den tillægskode, der skal medtages i fakturabeløbet, statistiske beløb eller begge.</span><span class="sxs-lookup"><span data-stu-id="e5c63-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="e5c63-170">På siden <strong>Gebyrkoder</strong> på fanen <strong>Udenrigshandel</strong> skal du aktivere <strong>Intrastat-fakturaværdi</strong> for at inkludere tillægsbeløbet i fakturaværdien og aktivere <strong>Værdi af Intrastat-statistik</strong> for at inkludere tillægsbeløbet i den statistiske værdi.</span><span class="sxs-lookup"><span data-stu-id="e5c63-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-171">Elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="e5c63-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="e5c63-172">Angiv elektronisk rapportering af konfigurationer for at eksportere Intrastat-data i en elektronisk fil, der har det format, der er anmodet om af de relevante myndigheder, og se Intrastat-data i et brugervenligt, læsbart format (for eksempel i Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="e5c63-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-173">Lagersted</span><span class="sxs-lookup"><span data-stu-id="e5c63-173">Warehousing</span></span></td>
<td><span data-ttu-id="e5c63-174">Tilknyt kreditorkonti til lagerstedskoder til udfyldning af SE-nummer ved overførsel af flytteordre.</span><span class="sxs-lookup"><span data-stu-id="e5c63-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="e5c63-175">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5c63-175">Setup</span></span>
<span data-ttu-id="e5c63-176">I følgende afsnit beskrives de indstillinger, der skal bruges til Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="e5c63-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="e5c63-177">Konfigurer alle nødvendige Intrastat-relaterede lister</span><span class="sxs-lookup"><span data-stu-id="e5c63-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5c63-178">Liste</span><span class="sxs-lookup"><span data-stu-id="e5c63-178">List</span></span></th>
<th><span data-ttu-id="e5c63-179">Flere oplysninger</span><span class="sxs-lookup"><span data-stu-id="e5c63-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5c63-180">Varekoder</span><span class="sxs-lookup"><span data-stu-id="e5c63-180">Commodity codes</span></span></td>
<td><span data-ttu-id="e5c63-181">Opret et kategorihierarki af typen <strong>Varekode</strong>, og angiv alle varekoder i henhold til den kombinerede nomenklatur-liste.</span><span class="sxs-lookup"><span data-stu-id="e5c63-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="e5c63-182">For hver enkelt vare kan du angive følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="e5c63-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="e5c63-183">Navnet på varen og varekoden.</span><span class="sxs-lookup"><span data-stu-id="e5c63-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="e5c63-184">Det brugervenlige navn og/eller det oversatte navn</span><span class="sxs-lookup"><span data-stu-id="e5c63-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="e5c63-185">Indstillinger for rapportering af yderligere (supplerende) enheder under fanen <strong>Udenrigshandel</strong>. Du kan vælge den ekstra enhed på enhedslisten.</span><span class="sxs-lookup"><span data-stu-id="e5c63-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="e5c63-186">Du kan også angive, om vægten af varer skal rapporteres sammen med den valgte ekstra enhed.</span><span class="sxs-lookup"><span data-stu-id="e5c63-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-187">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="e5c63-187">Transaction codes</span></span></td>
<td><span data-ttu-id="e5c63-188">Angiv arten af transaktionen i henhold til dit lands/områdes krav.</span><span class="sxs-lookup"><span data-stu-id="e5c63-188">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="e5c63-189">For hver transaktionskode, du har angivet, skal du angive regler for beregning af fakturabeløb og statistiske beløb for overførselsordrer og salgs-/købsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="e5c63-190">For overførselsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:</span><span class="sxs-lookup"><span data-stu-id="e5c63-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="e5c63-191"><strong>Tom</strong> – beløbet vil være 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="e5c63-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="e5c63-192"><strong>Økonomisk kostbeløb</strong> – beløbet er lig med omkostningerne.</span><span class="sxs-lookup"><span data-stu-id="e5c63-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="e5c63-193"><strong>Samlede omkostninger</strong> – beløbet er lig med den samlede kostpris for transaktionen.</span><span class="sxs-lookup"><span data-stu-id="e5c63-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="e5c63-194"><strong>Manuel</strong> – beløbet er lig med det beløb, der angives manuelt på overførselsforslagslinjen.</span><span class="sxs-lookup"><span data-stu-id="e5c63-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="e5c63-195">For salgsordrer og indkøbsordrer skal du angive en af følgende regler for beregning af fakturabeløb og statistiske beløb:</span><span class="sxs-lookup"><span data-stu-id="e5c63-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="e5c63-196"><strong>Tom</strong> – beløbet vil være 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="e5c63-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="e5c63-197"><strong>Fakturabeløb</strong> – beløbet er lig med det beløb, der er faktureret for varen.</span><span class="sxs-lookup"><span data-stu-id="e5c63-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="e5c63-198"><strong>Grundbeløb</strong> – beløbet, der er lig med det beløb, der skal faktureres, før nogen rabat.</span><span class="sxs-lookup"><span data-stu-id="e5c63-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-199">Transportmåder</span><span class="sxs-lookup"><span data-stu-id="e5c63-199">Transport methods</span></span></td>
<td><span data-ttu-id="e5c63-200">Angiv transportmåden i henhold til dit lands/områdes krav.</span><span class="sxs-lookup"><span data-stu-id="e5c63-200">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="e5c63-201">For hver leveringsmåde kan du konfigurere en standardtransportmåde på fanen <strong>Udenrigshandel</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5c63-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-202">Havne</span><span class="sxs-lookup"><span data-stu-id="e5c63-202">Ports</span></span></td>
<td><span data-ttu-id="e5c63-203">Angiv havn/lufthavn for lastning/losning, hvis disse oplysninger er indsamlet af dit land/område.</span><span class="sxs-lookup"><span data-stu-id="e5c63-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-204">Statistiske procedurer</span><span class="sxs-lookup"><span data-stu-id="e5c63-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="e5c63-205">Angiv den statistiske procedure, hvis disse oplysninger er indsamlet af dit land/område.</span><span class="sxs-lookup"><span data-stu-id="e5c63-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="e5c63-206">Angiv regler for komprimering af Intrastat-transaktioner</span><span class="sxs-lookup"><span data-stu-id="e5c63-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="e5c63-207">På siden **Komprimering af Intrastat** kan du vælge felterne, der skal bruges til komprimering.</span><span class="sxs-lookup"><span data-stu-id="e5c63-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="e5c63-208">Alle transaktioner, der har den samme kombination af værdier for de valgte felter i Intrastat-kladden, komprimeres til en enkelt transaktion, når du kører funktionen Komprimer i Intrastat-kladden.</span><span class="sxs-lookup"><span data-stu-id="e5c63-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="e5c63-209">Konfigurer udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="e5c63-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="e5c63-210">Brug siden **Udenrigshandelsparametre** til at konfigurere parametre i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e5c63-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5c63-211">Fane</span><span class="sxs-lookup"><span data-stu-id="e5c63-211">Tab</span></span></th>
<th><span data-ttu-id="e5c63-212">Parametre</span><span class="sxs-lookup"><span data-stu-id="e5c63-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5c63-213">Generel</span><span class="sxs-lookup"><span data-stu-id="e5c63-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="e5c63-214"><strong>Generelt</strong> – Angiv følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="e5c63-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="e5c63-215">Standardværdien transaktionskoder for salgsordrer, indkøbsordrer, kreditnotaer og overførselsordrer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="e5c63-216">Den transaktionskode, der er oprettet for kreditnotaer, bruges også som kode for fysisk returnerede varer og bruges til afvigende fysiske returneringer kontra korrektionskreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span> <span data-ttu-id="e5c63-217">Returneringer af fysiske varer rapporteres i Intrastat-overførsel med en anden retning.</span><span class="sxs-lookup"><span data-stu-id="e5c63-217">Returns of physical goods are reported in Intrastat transfer with a different direction.</span></span> <span data-ttu-id="e5c63-218">Modtagelsesreturen rapporteres som ekspedition, og afsendelsen rapporteres som modtagelse.</span><span class="sxs-lookup"><span data-stu-id="e5c63-218">The return of arrival is reported as dispatch and the return of dispatch is reported as arrival.</span></span></li>
<li><span data-ttu-id="e5c63-219">Den medarbejder, der er ansvarlig for udarbejdelse, af Intrastat-rapporter.</span><span class="sxs-lookup"><span data-stu-id="e5c63-219">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="e5c63-220"><strong>Minimumsgrænse</strong> – Angiv indstillinger for opdatering af transaktioner, der ligger under tærsklen:</span><span class="sxs-lookup"><span data-stu-id="e5c63-220"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="e5c63-221">Tærskelbeløb og vægt</span><span class="sxs-lookup"><span data-stu-id="e5c63-221">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="e5c63-222">Varekode, der skal gælde for transaktioner, der er under tærsklen</span><span class="sxs-lookup"><span data-stu-id="e5c63-222">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="e5c63-223"><strong>Overfør</strong> – Angiv kriterierne for at overføre transaktioner til Intrastat-kladden.</span><span class="sxs-lookup"><span data-stu-id="e5c63-223"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="e5c63-224">Du kan angive, at transaktioner kun overføres, når varerne opfylder en eller flere af følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="e5c63-224">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="e5c63-225">Varerne er ikke serviceartikler.</span><span class="sxs-lookup"><span data-stu-id="e5c63-225">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="e5c63-226">Varerne har en varekode.</span><span class="sxs-lookup"><span data-stu-id="e5c63-226">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="e5c63-227">Varerne har en vægt.</span><span class="sxs-lookup"><span data-stu-id="e5c63-227">The items have a weight.</span></span></li>
<li><span data-ttu-id="e5c63-228">Varerne har supplerende enheder.</span><span class="sxs-lookup"><span data-stu-id="e5c63-228">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="e5c63-229"><strong>Kontrollér opsætning</strong> – Angiv regler for validering af fuldstændigheden af Intrastat-data.</span><span class="sxs-lookup"><span data-stu-id="e5c63-229"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="e5c63-230">Du kan vælge, hvilke data der skal valideres.</span><span class="sxs-lookup"><span data-stu-id="e5c63-230">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="e5c63-231"><strong>Regler for afrunding</strong> – Angiv følgende indstillinger for afrunding af beløb og vægt i Intrastat-rapportering:</span><span class="sxs-lookup"><span data-stu-id="e5c63-231"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="e5c63-232">Afrundingsreglen (præcision)</span><span class="sxs-lookup"><span data-stu-id="e5c63-232">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="e5c63-233">Afrundingsmetoden: op, ned eller normal</span><span class="sxs-lookup"><span data-stu-id="e5c63-233">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="e5c63-234">Antallet af decimaler for beløb og vægt</span><span class="sxs-lookup"><span data-stu-id="e5c63-234">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="e5c63-235">Instruktioner for afrunding af vægt, der er mindre end 1 kilogram (kg): op til 1 kg, normal eller ingen afrunding</span><span class="sxs-lookup"><span data-stu-id="e5c63-235">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="e5c63-236"><strong>Elektronisk rapportering</strong> – Angiv referencer til elektronisk rapportering af konfigurationer, så du kan generere en elektronisk fil og rapport.</span><span class="sxs-lookup"><span data-stu-id="e5c63-236"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="e5c63-237"><strong>Varekodehierarki</strong> – Angiv kategorihierarkiet af typen <strong>Varekode</strong>, der repræsenterer Intrastat-varekoder CN8.</span><span class="sxs-lookup"><span data-stu-id="e5c63-237"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
  <li> <span data-ttu-id="e5c63-238"><strong>Valutakurstype</strong> – Du kan også angive en valutakurs, der skal bruges til at rapportere Intrastat-salgs- og købstransaktioner i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="e5c63-238"><strong>Exchange rate type</strong> – Optionally, specify an exchange rate to be used to report Intrastat sales and purchase transactions in foreign currencies.</span></span> <span data-ttu-id="e5c63-239">Dette bruges, hvis valutakursen er anderledes end den, der blev anvendt, da posten blev bogført.</span><span class="sxs-lookup"><span data-stu-id="e5c63-239">This is used if the rate is different than the one applied when posting the transaction.</span></span></li>  
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-240">Kontaktoplysninger for agent</span><span class="sxs-lookup"><span data-stu-id="e5c63-240">Agent contact information</span></span></td>
<td><span data-ttu-id="e5c63-241">Angiv agentens navn, adresse, momsundtagelsesnummer, telefonnummer og faxnummer.</span><span class="sxs-lookup"><span data-stu-id="e5c63-241">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e5c63-242">Egenskaber for land/område</span><span class="sxs-lookup"><span data-stu-id="e5c63-242">Country/region properties</span></span></td>
<td><span data-ttu-id="e5c63-243">Angiv landet/området for den aktuelle juridiske enhed til <strong>Indland</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5c63-243">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="e5c63-244">Angiv land/område i EU-lande/områder, der deltager i EU-handel med den aktuelle juridiske enhed til <strong>EU</strong>.</span><span class="sxs-lookup"><span data-stu-id="e5c63-244">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="e5c63-245">For hvert land/område kan du også identificere lande-/områdekoden for formål med udenrigshandel.</span><span class="sxs-lookup"><span data-stu-id="e5c63-245">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5c63-246">Nummerserie</span><span class="sxs-lookup"><span data-stu-id="e5c63-246">Number sequence</span></span></td>
<td><span data-ttu-id="e5c63-247">Angiv nummerserien for Intrastat-kladden.</span><span class="sxs-lookup"><span data-stu-id="e5c63-247">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]