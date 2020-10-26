---
title: Fakturaautomatisering for scannede dokumenter
description: Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d19d0e10f477e498e8f0fff1f431bc4bfdd9a1
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3904949"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="60168-103">Fakturaautomatisering for scannede dokumenter</span><span class="sxs-lookup"><span data-stu-id="60168-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60168-104">Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="60168-105">Organisationer, der ønsker at strømline deres kreditorprocesser, identificerer ofte fakturabehandling som en af de vigtigste procesområder, der skal være mere effektive.</span><span class="sxs-lookup"><span data-stu-id="60168-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="60168-106">I mange tilfælde overfører disse organisationer behandlingen af papirfakturaer til en tredjepartserviceudbyder af optisk tegngenkendelse (OCR).</span><span class="sxs-lookup"><span data-stu-id="60168-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="60168-107">Derefter modtager de maskinlæsbare fakturametadata sammen med et scannet billede af hver faktura.</span><span class="sxs-lookup"><span data-stu-id="60168-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="60168-108">Som hjælp til automatisering oprettes en sidste løsning derefter for at kunne forbruge disse artefakter i faktureringssystemet.</span><span class="sxs-lookup"><span data-stu-id="60168-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="60168-109">Nu er denne sidste automatisering som standard aktiveret via en løsning til fakturaautomatisering.</span><span class="sxs-lookup"><span data-stu-id="60168-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="60168-110">Løsningskontekst</span><span class="sxs-lookup"><span data-stu-id="60168-110">Solution context</span></span>

<span data-ttu-id="60168-111">Løsningen til fakturaautomatisering er en standardgrænseflade, der kan acceptere fakturametadata til fakturahovedet og fakturalinjer samt vedhæftede filer, der vedrører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="60168-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="60168-112">Alle eksterne systemer, der kan generere artefakter, som er i overensstemmelse med denne grænseflade, vil kunne sende feedet til automatisk behandling af fakturaer og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="60168-113">I følgende illustration vises et eksempel på integrationsscenarie, hvor Contoso er gået sammen med en OCR-tjenesteudbyder til behandling af kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="60168-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="60168-114">Contosos kreditorer sender fakturaer til tjenesteudbyderen via mail.</span><span class="sxs-lookup"><span data-stu-id="60168-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="60168-115">Udbyderen genererer via OCR-behandling fakturametadata (hoved og/eller linjer) og et scannet billede af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="60168-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="60168-116">Et integrationslag transformerer derefter disse artefakter, så de kan forbruges.</span><span class="sxs-lookup"><span data-stu-id="60168-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Eksempel på integrationsscenarie](media/vendor_invoice_automation_01.png)

<span data-ttu-id="60168-118">Flere variationer af det foregående scenarie er mulige, hvis fakturaintegration er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="60168-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="60168-119">Overførsel af data er en anden metode, hvor denne grænseflade kan bruges til at oprette fakturaer og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="60168-120">Løsningskomponenter</span><span class="sxs-lookup"><span data-stu-id="60168-120">Solution components</span></span>

<span data-ttu-id="60168-121">Løsningens fodaftryk består af følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="60168-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="60168-122">Dataenheder for fakturahoved, fakturalinjer og fakturaens vedhæftede filer</span><span class="sxs-lookup"><span data-stu-id="60168-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="60168-123">Undtagelsesbehandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="60168-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="60168-124">En side om side-fremviser af vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="60168-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="60168-125">Resten af dette emne indeholder detaljerede beskrivelser af disse løsningskomponenter.</span><span class="sxs-lookup"><span data-stu-id="60168-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="60168-126">Dataenheder</span><span class="sxs-lookup"><span data-stu-id="60168-126">Data entities</span></span>

<span data-ttu-id="60168-127">En datapakke er arbejdsenheden, der skal sendes til, så fakturahoveder, fakturalinjer og fakturaens vedhæftede filer kan oprettes.</span><span class="sxs-lookup"><span data-stu-id="60168-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="60168-128">Følgende dataenheder anvendes for de artefakter, der udgør datapakken:</span><span class="sxs-lookup"><span data-stu-id="60168-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="60168-129">Kreditorfakturahoved</span><span class="sxs-lookup"><span data-stu-id="60168-129">Vendor invoice header</span></span>
+ <span data-ttu-id="60168-130">Kreditorfakturalinje</span><span class="sxs-lookup"><span data-stu-id="60168-130">Vendor invoice line</span></span>
+ <span data-ttu-id="60168-131">Vedhæftet dokument til kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="60168-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="60168-132">Kreditorfakturaens vedhæftede dokument er en ny dataenhed, der indføres i forbindelse med denne funktion.</span><span class="sxs-lookup"><span data-stu-id="60168-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="60168-133">Kreditorfakturahovedets enhed er blevet ændret, så det understøtter vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="60168-134">Kreditorfakturaens linjeenhed er ikke blevet ændret for denne funktion.</span><span class="sxs-lookup"><span data-stu-id="60168-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="60168-135">Få detaljerede oplysninger om datapakker i [Oversigt over datastyring](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="60168-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="60168-136">Du kan finde oplysninger om, hvordan du opretter datapakker ved hjælp af arbejdsområdet Datastyring, i [Behandle og forbruge datapakker i Dynamics 365 Finance and Operations-app-løsning](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="60168-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="60168-137">Du kan hurtigt generere testdata, der indeholder fakturaer og vedhæftede filer, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="60168-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="60168-138">Log på din forekomst.</span><span class="sxs-lookup"><span data-stu-id="60168-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="60168-139">Gå til **Kreditor** > **Fakturaer** > **Ventende kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="60168-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="60168-140">Opret fakturaer, der har linjer og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="60168-141">De vedhæftede filer skal være i hovedet.</span><span class="sxs-lookup"><span data-stu-id="60168-141">The attachments must be header attachments.</span></span> <span data-ttu-id="60168-142">Enheden Vedhæftet dokument til kreditorfaktura understøtter i øjeblikket ikke vedhæftede filer i en linje.</span><span class="sxs-lookup"><span data-stu-id="60168-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="60168-143">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="60168-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="60168-144">Opret et eksportjob, der omfatter enhederne Kreditorfakturahovedet, Kreditorfakturalinje og Vedhæftet dokument til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="60168-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="60168-145">Eksportér dataene.</span><span class="sxs-lookup"><span data-stu-id="60168-145">Export the data.</span></span>
1. <span data-ttu-id="60168-146">Hent de eksporterede data som en pakke.</span><span class="sxs-lookup"><span data-stu-id="60168-146">Download the exported data as a package.</span></span> <span data-ttu-id="60168-147">Du kan nu bruge pakken til at importere data til målforekomster til testformål.</span><span class="sxs-lookup"><span data-stu-id="60168-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="60168-148">Bestemmelse af den juridiske enhed for en faktura</span><span class="sxs-lookup"><span data-stu-id="60168-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="60168-149">Fakturaer, der importeres via datapakker, kan knyttes til den juridiske enhed, de tilhører, på to måder:</span><span class="sxs-lookup"><span data-stu-id="60168-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="60168-150">Importjobbet, der behandler fakturaen, importerer den til det samme regnskab, hvor jobbet er planlagt i **Datastyring**-arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="60168-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="60168-151">Med andre ord fastsætter jobbets regnskab det regnskab, som fakturaen tilhører.</span><span class="sxs-lookup"><span data-stu-id="60168-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="60168-152">Når der sendes en datapakke, der indeholder fakturaer, til Finance, kan kalderen (dvs. det integrationsprogram, der kører uden for Finance) udtrykkeligt nævne regnskabs-id i HTTP-anmodningen.</span><span class="sxs-lookup"><span data-stu-id="60168-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="60168-153">I dette tilfælde tilsidesættes den regnskabskontekst, hvor behandlingsjobbet kører i Finance, og fakturaerne importeres til det regnskab, der blev sendt via HTTP-anmodningen.</span><span class="sxs-lookup"><span data-stu-id="60168-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="60168-154">Denne funktionsmåde er standardfunktionsmåde for datastyring.</span><span class="sxs-lookup"><span data-stu-id="60168-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="60168-155">Den er forklaret her i forbindelse med fakturaer for at give en komplet beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="60168-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="60168-156">Behandling af undtagelser</span><span class="sxs-lookup"><span data-stu-id="60168-156">Exception processing</span></span>

<span data-ttu-id="60168-157">I scenarier, hvor kommer kreditorfakturaer kommer ind i Finance and Operations via integration, skal det være nemt for et kreditorteammedlem at behandle undtagelser eller mislykkede fakturaer og at oprette ventende fakturaer ud fra mislykkedes fakturaer.</span><span class="sxs-lookup"><span data-stu-id="60168-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="60168-158">Denne undtagelsesbehandling for kreditorfakturaer er nu en del af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60168-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="60168-159">Listesiden Undtagelser</span><span class="sxs-lookup"><span data-stu-id="60168-159">Exceptions list page</span></span>

<span data-ttu-id="60168-160">Den nye listeside for fakturaundtagelser findes under **Kreditor** > **Fakturaer** > **Importfejl** > **Kreditorfakturaer, der blev ikke importeret**.</span><span class="sxs-lookup"><span data-stu-id="60168-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="60168-161">Denne side viser alle kreditorfakturahoveders poster fra den midlertidige tabel i dataenheden Kreditorfakturahoved.</span><span class="sxs-lookup"><span data-stu-id="60168-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="60168-162">Bemærk, at du kan få vist de samme poster fra **Datastyring**-arbejdsområdet, hvor du også kan udføre de samme handlinger, der findes i funktionen for undtagelseshåndtering.</span><span class="sxs-lookup"><span data-stu-id="60168-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="60168-163">Dog er funktionen for undtagelseshåndtering i brugergrænsefladen optimeret til en funktionel bruger.</span><span class="sxs-lookup"><span data-stu-id="60168-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Listesiden Undtagelser](media/vendor_invoice_automation_02.png)

<span data-ttu-id="60168-165">Denne listeside indeholder følgende felter, der leveres via feedet:</span><span class="sxs-lookup"><span data-stu-id="60168-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="60168-166">**Regnskab** – Det regnskab, som fakturaen tilhører</span><span class="sxs-lookup"><span data-stu-id="60168-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="60168-167">**Fejlmeddelelse** – Den fejlmeddelelse, der vises i datastyringen for at forklare, hvorfor fakturaen kunne ikke oprettes</span><span class="sxs-lookup"><span data-stu-id="60168-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="60168-168">**Nummer** – Fakturanummeret</span><span class="sxs-lookup"><span data-stu-id="60168-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="60168-169">**Fakturakonto**</span><span class="sxs-lookup"><span data-stu-id="60168-169">**Invoice account**</span></span>
+ <span data-ttu-id="60168-170">**Navn** – Leverandørens navn</span><span class="sxs-lookup"><span data-stu-id="60168-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="60168-171">**Kreditorkonto**</span><span class="sxs-lookup"><span data-stu-id="60168-171">**Vendor account**</span></span>
+ <span data-ttu-id="60168-172">**Indkøbsordre** – Indkøbsordrenummeret for fakturaen</span><span class="sxs-lookup"><span data-stu-id="60168-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="60168-173">**Bogføringsdato**</span><span class="sxs-lookup"><span data-stu-id="60168-173">**Posting date**</span></span>
+ <span data-ttu-id="60168-174">**Fakturadato**</span><span class="sxs-lookup"><span data-stu-id="60168-174">**Invoice date**</span></span>
+ <span data-ttu-id="60168-175">**Fakturabeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="60168-175">**Invoice description**</span></span>
+ <span data-ttu-id="60168-176">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="60168-176">**Currency**</span></span>
+ <span data-ttu-id="60168-177">**Logfil**</span><span class="sxs-lookup"><span data-stu-id="60168-177">**Log**</span></span>
+ <span data-ttu-id="60168-178">**Linjereference** – Den identifikator, der kommer fra det eksterne system</span><span class="sxs-lookup"><span data-stu-id="60168-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="60168-179">Linjereferencen er ikke faktura-id.</span><span class="sxs-lookup"><span data-stu-id="60168-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="60168-180">Denne listeside har også en indholdsrude, som du kan bruge på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="60168-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="60168-181">Få vist hele fejlmeddelelsen, så du ikke behøver at udvide kolonnen **Fejlmeddelelse** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="60168-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="60168-182">Få vist hele listen over vedhæftede filer for fakturaen, hvis vedhæftede filer blev leveret med fakturaen.</span><span class="sxs-lookup"><span data-stu-id="60168-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="60168-183">Listesiden understøtter følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="60168-184">**Rediger** – Åbn undtagelsesposten i redigeringstilstand, så du kan løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="60168-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="60168-185">**Indstillinger** – Få adgang til de standardindstillinger, der er tilgængelige på listesider.</span><span class="sxs-lookup"><span data-stu-id="60168-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="60168-186">Du kan bruge **Føj til arbejdsområde**-indstillingen til at fastgøre listesiden med undtagelser til arbejdsområdet som en liste eller et felt.</span><span class="sxs-lookup"><span data-stu-id="60168-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="60168-187">Siden Undtagelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="60168-187">Exception details page</span></span>

<span data-ttu-id="60168-188">Når du starter redigeringstilstand, vises siden Undtagelsesoplysninger for den faktura, der er problemer med.</span><span class="sxs-lookup"><span data-stu-id="60168-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="60168-189">Hvis der er vedhæftede filer, vises fakturaen og den vedhæftede fil som standard ved siden af hinanden på siden Undtagelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="60168-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Siden Undtagelsesoplysninger](media/vendor_invoice_automation_03.png)

<span data-ttu-id="60168-191">I foregående illustration er der ikke nogen linjer for kreditorfakturahoved, der fulgte med.</span><span class="sxs-lookup"><span data-stu-id="60168-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="60168-192">Linjeafsnittet er derfor tomt.</span><span class="sxs-lookup"><span data-stu-id="60168-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="60168-193">Siden Undtagelsesoplysninger understøtter følgende handling:</span><span class="sxs-lookup"><span data-stu-id="60168-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="60168-194">**Opret ventende faktura** – Når du har løst problemerne på fakturaen som en del af undtagelsesbehandlingen, kan du klikke på denne knap for at oprette den ventende faktura.</span><span class="sxs-lookup"><span data-stu-id="60168-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="60168-195">Oprettelse af ventende fakturaer foregår i baggrunden (som en asynkron handling).</span><span class="sxs-lookup"><span data-stu-id="60168-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="60168-196">Behandling af delt tjeneste vs. organisationsbaseret undtagelse</span><span class="sxs-lookup"><span data-stu-id="60168-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="60168-197">Listesiden med undtagelser understøtter standardsikkerhedskonstruktioner, som **Datastyring**-arbejdsområdet understøtter til behandling af midlertidige poster.</span><span class="sxs-lookup"><span data-stu-id="60168-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="60168-198">Importjobbet for fakturaer kan sikres på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="60168-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="60168-199">Af brugerrolle</span><span class="sxs-lookup"><span data-stu-id="60168-199">By user role</span></span>
+ <span data-ttu-id="60168-200">Pr. bruger</span><span class="sxs-lookup"><span data-stu-id="60168-200">By user</span></span>
+ <span data-ttu-id="60168-201">af juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="60168-201">By legal entity</span></span>

![Importjob, der er sikret af brugerrolle og juridisk enhed](media/vendor_invoice_automation_04.png)

<span data-ttu-id="60168-203">Hvis sikkerhed er konfigureret for importjobbet til fakturaer, bruger listesiden med undtagelser disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="60168-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="60168-204">Brugere vil kun kunne se fakturaundtagelsesposter, som denne konfiguration giver mulighed for at se.</span><span class="sxs-lookup"><span data-stu-id="60168-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="60168-205">For eksempel har Contoso besluttet at behandle fakturaundtagelser efter juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="60168-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="60168-206">Derfor er sikkerheden konfigureret på importjobbet for fakturaer på en sådan måde, at en bruger i juridisk enhed A kun kan se fakturaundtagelser i juridisk enhed A, mens en bruger i juridisk enhed B kun kan se fakturaundtagelser i juridisk enhed B. Denne konfiguration giver mulighed for opdeling af opgaver til administration af fakturaundtagelser.</span><span class="sxs-lookup"><span data-stu-id="60168-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="60168-207">Contoso kan også beslutte ikke at indføre en sikkerhed, så de samme brugere kan behandle fakturaundtagelser for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="60168-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="60168-208">Denne konfiguration giver mulighed for et delt tjenestescenarie til styring af fakturaundtagelser.</span><span class="sxs-lookup"><span data-stu-id="60168-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="60168-209">Side om side-fremviser af vedhæftede filer</span><span class="sxs-lookup"><span data-stu-id="60168-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="60168-210">Så du nemt kan få vist vedhæftede filer for kreditorfakturaer, indeholder følgende sider, der bruges i faktureringsprocessen, nu en vedhæftet fil-fremviser:</span><span class="sxs-lookup"><span data-stu-id="60168-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="60168-211">**Undtagelseshåndtering**</span><span class="sxs-lookup"><span data-stu-id="60168-211">**Exception handling**</span></span>
+ <span data-ttu-id="60168-212">**Ventende kreditorfakturaer**-siden (findes også i evalueringsprocessen for fakturaer)</span><span class="sxs-lookup"><span data-stu-id="60168-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="60168-213">**Fakturajournal**-forespørgselsside (for bogførte fakturaer)</span><span class="sxs-lookup"><span data-stu-id="60168-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="60168-214">Her er den vigtigste funktion i fremviseren af vedhæftede filer:</span><span class="sxs-lookup"><span data-stu-id="60168-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="60168-215">Få vist alle vedhæftede filtyper, som dokumentstyring understøtter (filer, billeder, URL-adresser og noter).</span><span class="sxs-lookup"><span data-stu-id="60168-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="60168-216">Få vist flere sider i TIFF-filer.</span><span class="sxs-lookup"><span data-stu-id="60168-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="60168-217">Du kan udføre følgende handlinger på billedfiler:</span><span class="sxs-lookup"><span data-stu-id="60168-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="60168-218">Fremhæve dele af billedet.</span><span class="sxs-lookup"><span data-stu-id="60168-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="60168-219">Blokere dele af billedet.</span><span class="sxs-lookup"><span data-stu-id="60168-219">Block parts of the image.</span></span>
  + <span data-ttu-id="60168-220">Tilføje anmærkninger på billedet.</span><span class="sxs-lookup"><span data-stu-id="60168-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="60168-221">Zoome ind og ud på billedet.</span><span class="sxs-lookup"><span data-stu-id="60168-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="60168-222">Panorere billedet.</span><span class="sxs-lookup"><span data-stu-id="60168-222">Pan the image.</span></span>
  + <span data-ttu-id="60168-223">Fortryde og annullere Fortryd af handlinger.</span><span class="sxs-lookup"><span data-stu-id="60168-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="60168-224">Tilpasse billedets størrelse.</span><span class="sxs-lookup"><span data-stu-id="60168-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="60168-225">Disse handlinger er kun tilgængelige for billedfiler (JPEG, TIFF, PNG osv.).</span><span class="sxs-lookup"><span data-stu-id="60168-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="60168-226">Eventuelle ændringer, du foretager af et billede ved hjælp af disse handlinger, gemmes i billedfilen.</span><span class="sxs-lookup"><span data-stu-id="60168-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="60168-227">Fremviseren omfatter ikke i øjeblikket versionsstyring og overvågning.</span><span class="sxs-lookup"><span data-stu-id="60168-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="60168-228">Standardvedhæftning</span><span class="sxs-lookup"><span data-stu-id="60168-228">Default attachment</span></span>

<span data-ttu-id="60168-229">Hvis en kreditorfaktura har mere end én vedhæftet fil, kan du angive et af dokumenterne som den standardvedhæftede fil på siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="60168-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="60168-230">**Er standardvedhæftning**-indstillingen er en ny indstilling, der er tilføjet som en del af denne funktion.</span><span class="sxs-lookup"><span data-stu-id="60168-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="60168-231">Denne indstilling vises også i dataenheden Vedhæftet dokument til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="60168-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="60168-232">Derfor kan standardvedhæftningen angives via integrationer.</span><span class="sxs-lookup"><span data-stu-id="60168-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="60168-233">Kun ét dokument kan angives som standardvedhæftning.</span><span class="sxs-lookup"><span data-stu-id="60168-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="60168-234">Når du har oprettet et dokument som standardvedhæftning, vises det automatisk i fremviseren, når fakturaen åbnes.</span><span class="sxs-lookup"><span data-stu-id="60168-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="60168-235">Hvis du ikke angiver noget dokument som standardvedhæftning, viser fremviseren ikke automatisk nogen vedhæftet fil, når fakturaen åbnes.</span><span class="sxs-lookup"><span data-stu-id="60168-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="60168-236">Vise/skjule fakturavedhæftninger</span><span class="sxs-lookup"><span data-stu-id="60168-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="60168-237">Med en ny knap, der findes på forespørgselssiderne **Behandling af undtagelsen**, **Ventende faktura** og **Fakturajournal**, kan du vise eller skjule fremviseren af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="60168-238">Sikkerhed</span><span class="sxs-lookup"><span data-stu-id="60168-238">Security</span></span>

<span data-ttu-id="60168-239">Følgende handlinger i fremviseren styres via rollebaseret sikkerhed:</span><span class="sxs-lookup"><span data-stu-id="60168-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="60168-240">Fremhævning</span><span class="sxs-lookup"><span data-stu-id="60168-240">Highlighting</span></span>
+ <span data-ttu-id="60168-241">Blokering</span><span class="sxs-lookup"><span data-stu-id="60168-241">Block</span></span>
+ <span data-ttu-id="60168-242">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="60168-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="60168-243">Siden Ventende kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="60168-243">Pending vendor invoices page</span></span>

<span data-ttu-id="60168-244">Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for at fremhævnings-, blokerings- og anmærkningshandlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="60168-245">**Vedligehold billede af kreditorfaktura** – Denne rettighed giver læse-/skriveadgang.</span><span class="sxs-lookup"><span data-stu-id="60168-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="60168-246">**Vis billede af kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang.</span><span class="sxs-lookup"><span data-stu-id="60168-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="60168-247">Følgende opgaver giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="60168-248">**Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="60168-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="60168-249">**Forespørg status for kreditorfaktura** – Rettigheden Vis billede af kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="60168-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="60168-250">Følgende roller giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="60168-251">**Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.</span><span class="sxs-lookup"><span data-stu-id="60168-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="60168-252">**Kreditorassistent**, **Kreditorchef**, **Medarbejder for centraliserede kreditorbetalinger** og **Ansvarlig for kreditorbetalinger** – Opgaven Forespørg status for kreditorfaktura er tildelt til disse roller.</span><span class="sxs-lookup"><span data-stu-id="60168-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="60168-253">Siden med undtagelsesoplysninger om fakturaer</span><span class="sxs-lookup"><span data-stu-id="60168-253">Invoice exception details page</span></span>

<span data-ttu-id="60168-254">Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for fremhævnings-, blokerings- og anmærkningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="60168-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="60168-255">De roller, der er nævnt i dette afsnit, giver fra starten skrivebeskyttet adgang til fakturabillederne i fremviseren af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="60168-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="60168-256">Hvis en rolle også skal have skriveadgang til billederne, kan du tildele denne rolle skriveadgang ved hjælp af den rettighed eller opgave, der er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="60168-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="60168-257">**Vedligehold billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver læse-/skriveadgang til fakturabillederne i fremviseren.</span><span class="sxs-lookup"><span data-stu-id="60168-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="60168-258">**Vis billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang til fakturabilledet i fremviseren.</span><span class="sxs-lookup"><span data-stu-id="60168-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="60168-259">Følgende opgaver giver skrivebeskyttet adgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="60168-260">**Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af enhed for overskrift til kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="60168-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="60168-261">Følgende roller giver skrivebeskyttet adgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="60168-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="60168-262">**Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.</span><span class="sxs-lookup"><span data-stu-id="60168-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="60168-263">Som standard, hvis brugerrollen giver redigeringsrettigheder på enhver side, skal brugeren også have redigeringsrettigheder til fremviseren af vedhæftede filer for fremhævnings-, blokerings- og anmærkningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="60168-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="60168-264">Hvis der er situationer, hvor en bestemt rolle skal have redigeringsrettigheder på siden, men ikke i fremviseren, kan der dog bruges de nødvendige rettigheder fra den foregående liste for at opfylde behovet.</span><span class="sxs-lookup"><span data-stu-id="60168-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
