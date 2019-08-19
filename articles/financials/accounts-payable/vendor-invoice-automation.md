---
title: Automatisering af kreditorfaktura
description: Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
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
ms.openlocfilehash: 408922cde595649f3d2415172483cc22dac1e756
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836935"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="f0058-103">Automatisering af kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="f0058-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0058-104">Dette emne forklarer de funktioner, der er tilgængelige for start-til-slut-automatisering af kreditorfakturaer, tilmed fakturaer, der indeholder vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="f0058-105">Organisationer, der ønsker at strømline deres kreditorprocesser, identificerer ofte fakturabehandling som en af de vigtigste procesområder, der skal være mere effektive.</span><span class="sxs-lookup"><span data-stu-id="f0058-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="f0058-106">I mange tilfælde overfører disse organisationer behandlingen af papirfakturaer til en tredjepartserviceudbyder af optisk tegngenkendelse (OCR).</span><span class="sxs-lookup"><span data-stu-id="f0058-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="f0058-107">Derefter modtager de maskinlæsbare fakturametadata sammen med et scannet billede af hver faktura.</span><span class="sxs-lookup"><span data-stu-id="f0058-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="f0058-108">Som hjælp til automatisering oprettes en sidste løsning derefter for at kunne forbruge disse artefakter i faktureringssystemet.</span><span class="sxs-lookup"><span data-stu-id="f0058-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="f0058-109">Microsoft Dynamics 365 for Finance and Operations giver nu mulighed for denne sidste automatisering som standard via en løsning til fakturaautomatisering.</span><span class="sxs-lookup"><span data-stu-id="f0058-109">Microsoft Dynamics 365 for Finance and Operations now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="f0058-110">Løsningskontekst</span><span class="sxs-lookup"><span data-stu-id="f0058-110">Solution context</span></span>

<span data-ttu-id="f0058-111">Løsningen til fakturaautomatisering er en standardgrænseflade, der kan acceptere fakturametadata til fakturahovedet og fakturalinjer samt vedhæftede filer, der vedrører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f0058-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="f0058-112">Alle eksterne systemer, der kan generere artefakter, som er i overensstemmelse med denne grænseflade, vil kunne sende feedet til automatisk behandling af fakturaer og vedhæftede filer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0058-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="f0058-113">I følgende illustration vises et eksempel på integrationsscenarie, hvor Contoso er gået sammen med en OCR-tjenesteudbyder til behandling af kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="f0058-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="f0058-114">Contosos kreditorer sender fakturaer til tjenesteudbyderen via mail.</span><span class="sxs-lookup"><span data-stu-id="f0058-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="f0058-115">Udbyderen genererer via OCR-behandling fakturametadata (hoved og/eller linjer) og et scannet billede af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f0058-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="f0058-116">Et lag med integration transformerer derefter disse artefakter, så Finance and Operations kan forbruge dem.</span><span class="sxs-lookup"><span data-stu-id="f0058-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Eksempel på integrationsscenarie](media/vendor_invoice_automation_01.png)

<span data-ttu-id="f0058-118">Flere variationer af det foregående scenarie er mulige, hvis fakturaintegration er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="f0058-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="f0058-119">Overførsel af data er en anden metode, hvor denne grænseflade kan bruges til at oprette fakturaer og vedhæftede filer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0058-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="f0058-120">Løsningskomponenter</span><span class="sxs-lookup"><span data-stu-id="f0058-120">Solution components</span></span>

<span data-ttu-id="f0058-121">Løsningens fodaftryk består af følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="f0058-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="f0058-122">Dataenheder for fakturahoved, fakturalinjer og fakturaens vedhæftede filer</span><span class="sxs-lookup"><span data-stu-id="f0058-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="f0058-123">Undtagelsesbehandling af fakturaer</span><span class="sxs-lookup"><span data-stu-id="f0058-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="f0058-124">En side om side-fremviser af vedhæftede filer i fakturaer</span><span class="sxs-lookup"><span data-stu-id="f0058-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="f0058-125">Resten af dette emne indeholder detaljerede beskrivelser af disse løsningskomponenter.</span><span class="sxs-lookup"><span data-stu-id="f0058-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="f0058-126">Dataenheder</span><span class="sxs-lookup"><span data-stu-id="f0058-126">Data entities</span></span>

<span data-ttu-id="f0058-127">En datapakke er arbejdsenheden, der skal sendes til Finance and Operations , så fakturahoveder, fakturalinjer og fakturaens vedhæftede filer kan oprettes.</span><span class="sxs-lookup"><span data-stu-id="f0058-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="f0058-128">Følgende dataenheder anvendes for de artefakter, der udgør datapakken:</span><span class="sxs-lookup"><span data-stu-id="f0058-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="f0058-129">Kreditorfakturahoved</span><span class="sxs-lookup"><span data-stu-id="f0058-129">Vendor invoice header</span></span>
+ <span data-ttu-id="f0058-130">Kreditorfakturalinje</span><span class="sxs-lookup"><span data-stu-id="f0058-130">Vendor invoice line</span></span>
+ <span data-ttu-id="f0058-131">Vedhæftet dokument til kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="f0058-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="f0058-132">Kreditorfakturaens vedhæftede dokument er en ny dataenhed, der indføres i forbindelse med denne funktion.</span><span class="sxs-lookup"><span data-stu-id="f0058-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="f0058-133">Kreditorfakturahovedets enhed er blevet ændret, så det understøtter vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="f0058-134">Kreditorfakturaens linjeenhed er ikke blevet ændret for denne funktion.</span><span class="sxs-lookup"><span data-stu-id="f0058-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="f0058-135">Dette emne give ikke en detaljeret definition af en datapakke.</span><span class="sxs-lookup"><span data-stu-id="f0058-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="f0058-136">Det forklarer heller ikke, hvordan datapakker oprettes.</span><span class="sxs-lookup"><span data-stu-id="f0058-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="f0058-137">Du kan finde disse oplysninger i [Struktur for dataenheder og pakker](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="f0058-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="f0058-138">Du kan hurtigt generere testdata, der indeholder fakturaer og vedhæftede filer, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="f0058-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="f0058-139">Log på din forekomst af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0058-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="f0058-140">Gå til **Kreditor** > **Fakturaer** > **Ventende kreditorfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="f0058-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="f0058-141">Opret fakturaer, der har linjer og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0058-142">De vedhæftede filer skal være i hovedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-142">The attachments must be header attachments.</span></span> <span data-ttu-id="f0058-143">Enheden Vedhæftet dokument til kreditorfaktura understøtter i øjeblikket ikke vedhæftede filer i en linje.</span><span class="sxs-lookup"><span data-stu-id="f0058-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="f0058-144">Åbn arbejdsområdet **Datastyring**.</span><span class="sxs-lookup"><span data-stu-id="f0058-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="f0058-145">Opret et eksportjob, der omfatter enhederne Kreditorfakturahovedet, Kreditorfakturalinje og Vedhæftet dokument til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="f0058-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="f0058-146">Eksportér dataene.</span><span class="sxs-lookup"><span data-stu-id="f0058-146">Export the data.</span></span>
1. <span data-ttu-id="f0058-147">Hent de eksporterede data som en pakke.</span><span class="sxs-lookup"><span data-stu-id="f0058-147">Download the exported data as a package.</span></span> <span data-ttu-id="f0058-148">Du kan nu bruge pakken til at importere data til målforekomster til testformål.</span><span class="sxs-lookup"><span data-stu-id="f0058-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="f0058-149">Bestemmelse af den juridiske enhed for en faktura</span><span class="sxs-lookup"><span data-stu-id="f0058-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="f0058-150">Fakturaer, der importeres via datapakker, kan knyttes til den juridiske enhed, de tilhører, på to måder:</span><span class="sxs-lookup"><span data-stu-id="f0058-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="f0058-151">Importjobbet, der behandler fakturaen, importerer den til det samme regnskab, hvor jobbet er planlagt i **Datastyring**-arbejdsområdet.</span><span class="sxs-lookup"><span data-stu-id="f0058-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="f0058-152">Med andre ord fastsætter jobbets regnskab det regnskab, som fakturaen tilhører.</span><span class="sxs-lookup"><span data-stu-id="f0058-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="f0058-153">Når der sendes en datapakke, der indeholder fakturaer, til Finance and Operations, kan kalderen (dvs. det integrationsprogram, der kører uden for Finance and Operations) udtrykkeligt nævne regnskabs-id i HTTP-anmodningen.</span><span class="sxs-lookup"><span data-stu-id="f0058-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="f0058-154">I dette tilfælde tilsidesættes den regnskabskontekst, hvor behandlingsjobbet kører Finance and Operations, og fakturaerne importeres til det regnskab, der blev sendt via HTTP-anmodningen.</span><span class="sxs-lookup"><span data-stu-id="f0058-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="f0058-155">Denne funktionsmåde er standardfunktionsmåde for datastyring.</span><span class="sxs-lookup"><span data-stu-id="f0058-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="f0058-156">Den er forklaret her i forbindelse med fakturaer for at give en komplet beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f0058-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="f0058-157">Behandling af undtagelser</span><span class="sxs-lookup"><span data-stu-id="f0058-157">Exception processing</span></span>

<span data-ttu-id="f0058-158">I scenarier, hvor kommer kreditorfakturaer kommer ind i Finance and Operations via integration, skal det være nemt for et kreditorteammedlem at behandle undtagelser eller mislykkede fakturaer og at oprette ventende fakturaer ud fra mislykkedes fakturaer.</span><span class="sxs-lookup"><span data-stu-id="f0058-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="f0058-159">Denne undtagelsesbehandling for kreditorfakturaer er nu en del af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0058-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="f0058-160">Listesiden Undtagelser</span><span class="sxs-lookup"><span data-stu-id="f0058-160">Exceptions list page</span></span>

<span data-ttu-id="f0058-161">Den nye listeside for fakturaundtagelser findes under **Kreditor** > **Fakturaer** > **Importfejl** > **Kreditorfakturaer, der blev ikke importeret**.</span><span class="sxs-lookup"><span data-stu-id="f0058-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="f0058-162">Denne side viser alle kreditorfakturahoveders poster fra den midlertidige tabel i dataenheden Kreditorfakturahoved.</span><span class="sxs-lookup"><span data-stu-id="f0058-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="f0058-163">Bemærk, at du kan få vist de samme poster fra **Datastyring**-arbejdsområdet, hvor du også kan udføre de samme handlinger, der findes i funktionen for undtagelseshåndtering.</span><span class="sxs-lookup"><span data-stu-id="f0058-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="f0058-164">Dog er funktionen for undtagelseshåndtering i brugergrænsefladen optimeret til en funktionel bruger.</span><span class="sxs-lookup"><span data-stu-id="f0058-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Listesiden Undtagelser](media/vendor_invoice_automation_02.png)

<span data-ttu-id="f0058-166">Denne listeside indeholder følgende felter, der leveres via feedet:</span><span class="sxs-lookup"><span data-stu-id="f0058-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="f0058-167">**Regnskab** – Det regnskab, som fakturaen tilhører</span><span class="sxs-lookup"><span data-stu-id="f0058-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="f0058-168">**Fejlmeddelelse** – Den fejlmeddelelse, der vises i datastyringen for at forklare, hvorfor fakturaen kunne ikke oprettes</span><span class="sxs-lookup"><span data-stu-id="f0058-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="f0058-169">**Nummer** – Fakturanummeret</span><span class="sxs-lookup"><span data-stu-id="f0058-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="f0058-170">**Fakturakonto**</span><span class="sxs-lookup"><span data-stu-id="f0058-170">**Invoice account**</span></span>
+ <span data-ttu-id="f0058-171">**Navn** – Leverandørens navn</span><span class="sxs-lookup"><span data-stu-id="f0058-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="f0058-172">**Kreditorkonto**</span><span class="sxs-lookup"><span data-stu-id="f0058-172">**Vendor account**</span></span>
+ <span data-ttu-id="f0058-173">**Indkøbsordre** – Indkøbsordrenummeret for fakturaen</span><span class="sxs-lookup"><span data-stu-id="f0058-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="f0058-174">**Bogføringsdato**</span><span class="sxs-lookup"><span data-stu-id="f0058-174">**Posting date**</span></span>
+ <span data-ttu-id="f0058-175">**Fakturadato**</span><span class="sxs-lookup"><span data-stu-id="f0058-175">**Invoice date**</span></span>
+ <span data-ttu-id="f0058-176">**Fakturabeskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f0058-176">**Invoice description**</span></span>
+ <span data-ttu-id="f0058-177">**Valuta**</span><span class="sxs-lookup"><span data-stu-id="f0058-177">**Currency**</span></span>
+ <span data-ttu-id="f0058-178">**Logfil**</span><span class="sxs-lookup"><span data-stu-id="f0058-178">**Log**</span></span>
+ <span data-ttu-id="f0058-179">**Linjereference** – Den identifikator, der kommer fra det eksterne system</span><span class="sxs-lookup"><span data-stu-id="f0058-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0058-180">Linjereferencen er ikke faktura-id.</span><span class="sxs-lookup"><span data-stu-id="f0058-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="f0058-181">Denne listeside har også en indholdsrude, som du kan bruge på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="f0058-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="f0058-182">Få vist hele fejlmeddelelsen, så du ikke behøver at udvide kolonnen **Fejlmeddelelse** i gitteret.</span><span class="sxs-lookup"><span data-stu-id="f0058-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="f0058-183">Få vist hele listen over vedhæftede filer for fakturaen, hvis vedhæftede filer blev leveret med fakturaen.</span><span class="sxs-lookup"><span data-stu-id="f0058-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="f0058-184">Listesiden understøtter følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="f0058-185">**Rediger** – Åbn undtagelsesposten i redigeringstilstand, så du kan løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="f0058-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="f0058-186">**Indstillinger** – Få adgang til de standardindstillinger, der er tilgængelige på listesider.</span><span class="sxs-lookup"><span data-stu-id="f0058-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="f0058-187">Du kan bruge **Føj til arbejdsområde**-indstillingen til at fastgøre listesiden med undtagelser til arbejdsområdet som en liste eller et felt.</span><span class="sxs-lookup"><span data-stu-id="f0058-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="f0058-188">Siden Undtagelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="f0058-188">Exception details page</span></span>

<span data-ttu-id="f0058-189">Når du starter redigeringstilstand, vises siden Undtagelsesoplysninger for den faktura, der er problemer med.</span><span class="sxs-lookup"><span data-stu-id="f0058-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="f0058-190">Hvis der er vedhæftede filer, vises fakturaen og den vedhæftede fil som standard ved siden af hinanden på siden Undtagelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="f0058-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Siden Undtagelsesoplysninger](media/vendor_invoice_automation_03.png)

<span data-ttu-id="f0058-192">I foregående illustration er der ikke nogen linjer for kreditorfakturahoved, der fulgte med.</span><span class="sxs-lookup"><span data-stu-id="f0058-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="f0058-193">Linjeafsnittet er derfor tomt.</span><span class="sxs-lookup"><span data-stu-id="f0058-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="f0058-194">Siden Undtagelsesoplysninger understøtter følgende handling:</span><span class="sxs-lookup"><span data-stu-id="f0058-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="f0058-195">**Opret ventende faktura** – Når du har løst problemerne på fakturaen som en del af undtagelsesbehandlingen, kan du klikke på denne knap for at oprette den ventende faktura.</span><span class="sxs-lookup"><span data-stu-id="f0058-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="f0058-196">Oprettelse af ventende fakturaer foregår i baggrunden (som en asynkron handling).</span><span class="sxs-lookup"><span data-stu-id="f0058-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="f0058-197">Behandling af delt tjeneste vs. organisationsbaseret undtagelse</span><span class="sxs-lookup"><span data-stu-id="f0058-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="f0058-198">Listesiden med undtagelser understøtter standardsikkerhedskonstruktioner, som **Datastyring**-arbejdsområdet understøtter til behandling af midlertidige poster.</span><span class="sxs-lookup"><span data-stu-id="f0058-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="f0058-199">Importjobbet for fakturaer kan sikres på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="f0058-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="f0058-200">Af brugerrolle</span><span class="sxs-lookup"><span data-stu-id="f0058-200">By user role</span></span>
+ <span data-ttu-id="f0058-201">Pr. bruger</span><span class="sxs-lookup"><span data-stu-id="f0058-201">By user</span></span>
+ <span data-ttu-id="f0058-202">af juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="f0058-202">By legal entity</span></span>

![Importjob, der er sikret af brugerrolle og juridisk enhed](media/vendor_invoice_automation_04.png)

<span data-ttu-id="f0058-204">Hvis sikkerhed er konfigureret for importjobbet til fakturaer, bruger listesiden med undtagelser disse indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f0058-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="f0058-205">Brugere vil kun kunne se fakturaundtagelsesposter, som denne konfiguration giver mulighed for at se.</span><span class="sxs-lookup"><span data-stu-id="f0058-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="f0058-206">For eksempel har Contoso besluttet at behandle fakturaundtagelser efter juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="f0058-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="f0058-207">Derfor er sikkerheden konfigureret på importjobbet for fakturaer på en sådan måde, at en bruger i juridisk enhed A kun kan se fakturaundtagelser i juridisk enhed A, mens en bruger i juridisk enhed B kun kan se fakturaundtagelser i juridisk enhed B. Denne konfiguration giver mulighed for opdeling af opgaver til administration af fakturaundtagelser.</span><span class="sxs-lookup"><span data-stu-id="f0058-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="f0058-208">Contoso kan også beslutte ikke at indføre en sikkerhed, så de samme brugere kan behandle fakturaundtagelser for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="f0058-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="f0058-209">Denne konfiguration giver mulighed for et delt tjenestescenarie til styring af fakturaundtagelser.</span><span class="sxs-lookup"><span data-stu-id="f0058-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="f0058-210">Side om side-fremviser af vedhæftede filer</span><span class="sxs-lookup"><span data-stu-id="f0058-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="f0058-211">Så du nemt kan få vist vedhæftede filer for kreditorfakturaer, indeholder følgende sider, der bruges i faktureringsprocessen, nu en vedhæftet fil-fremviser:</span><span class="sxs-lookup"><span data-stu-id="f0058-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="f0058-212">**Undtagelseshåndtering**</span><span class="sxs-lookup"><span data-stu-id="f0058-212">**Exception handling**</span></span>
+ <span data-ttu-id="f0058-213">**Ventende kreditorfakturaer**-siden (findes også i evalueringsprocessen for fakturaer)</span><span class="sxs-lookup"><span data-stu-id="f0058-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="f0058-214">**Fakturajournal**-forespørgselsside (for bogførte fakturaer)</span><span class="sxs-lookup"><span data-stu-id="f0058-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="f0058-215">Her er den vigtigste funktion i fremviseren af vedhæftede filer:</span><span class="sxs-lookup"><span data-stu-id="f0058-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="f0058-216">Få vist alle vedhæftede filtyper, som dokumentstyring understøtter (filer, billeder, URL-adresser og noter).</span><span class="sxs-lookup"><span data-stu-id="f0058-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="f0058-217">Få vist flere sider i TIFF-filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="f0058-218">Du kan udføre følgende handlinger på billedfiler:</span><span class="sxs-lookup"><span data-stu-id="f0058-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="f0058-219">Fremhæve dele af billedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="f0058-220">Blokere dele af billedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-220">Block parts of the image.</span></span>
  + <span data-ttu-id="f0058-221">Tilføje anmærkninger på billedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="f0058-222">Zoome ind og ud på billedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="f0058-223">Panorere billedet.</span><span class="sxs-lookup"><span data-stu-id="f0058-223">Pan the image.</span></span>
  + <span data-ttu-id="f0058-224">Fortryde og annullere Fortryd af handlinger.</span><span class="sxs-lookup"><span data-stu-id="f0058-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="f0058-225">Tilpasse billedets størrelse.</span><span class="sxs-lookup"><span data-stu-id="f0058-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="f0058-226">Disse handlinger er kun tilgængelige for billedfiler (JPEG, TIFF, PNG osv.).</span><span class="sxs-lookup"><span data-stu-id="f0058-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="f0058-227">Eventuelle ændringer, du foretager af et billede ved hjælp af disse handlinger, gemmes i billedfilen.</span><span class="sxs-lookup"><span data-stu-id="f0058-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="f0058-228">Fremviseren omfatter ikke i øjeblikket versionsstyring og overvågning.</span><span class="sxs-lookup"><span data-stu-id="f0058-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="f0058-229">Standardvedhæftning</span><span class="sxs-lookup"><span data-stu-id="f0058-229">Default attachment</span></span>

<span data-ttu-id="f0058-230">Hvis en kreditorfaktura har mere end én vedhæftet fil, kan du angive et af dokumenterne som den standardvedhæftede fil på siden **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="f0058-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="f0058-231">**Er standardvedhæftning**-indstillingen er en ny indstilling, der er tilføjet som en del af denne funktion.</span><span class="sxs-lookup"><span data-stu-id="f0058-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="f0058-232">Denne indstilling vises også i dataenheden Vedhæftet dokument til kreditorfaktura.</span><span class="sxs-lookup"><span data-stu-id="f0058-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="f0058-233">Derfor kan standardvedhæftningen angives via integrationer.</span><span class="sxs-lookup"><span data-stu-id="f0058-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="f0058-234">Kun ét dokument kan angives som standardvedhæftning.</span><span class="sxs-lookup"><span data-stu-id="f0058-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="f0058-235">Når du har oprettet et dokument som standardvedhæftning, vises det automatisk i fremviseren, når fakturaen åbnes.</span><span class="sxs-lookup"><span data-stu-id="f0058-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="f0058-236">Hvis du ikke angiver noget dokument som standardvedhæftning, viser fremviseren ikke automatisk nogen vedhæftet fil, når fakturaen åbnes.</span><span class="sxs-lookup"><span data-stu-id="f0058-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="f0058-237">Vise/skjule fakturavedhæftninger</span><span class="sxs-lookup"><span data-stu-id="f0058-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="f0058-238">Med en ny knap, der findes på forespørgselssiderne **Behandling af undtagelsen**, **Ventende faktura** og **Fakturajournal**, kan du vise eller skjule fremviseren af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="f0058-239">Sikkerhed</span><span class="sxs-lookup"><span data-stu-id="f0058-239">Security</span></span>

<span data-ttu-id="f0058-240">Følgende handlinger i fremviseren styres via rollebaseret sikkerhed:</span><span class="sxs-lookup"><span data-stu-id="f0058-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="f0058-241">Fremhævning</span><span class="sxs-lookup"><span data-stu-id="f0058-241">Highlighting</span></span>
+ <span data-ttu-id="f0058-242">Blokering</span><span class="sxs-lookup"><span data-stu-id="f0058-242">Block</span></span>
+ <span data-ttu-id="f0058-243">Anmærkning</span><span class="sxs-lookup"><span data-stu-id="f0058-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="f0058-244">Siden Ventende kreditorfakturaer</span><span class="sxs-lookup"><span data-stu-id="f0058-244">Pending vendor invoices page</span></span>

<span data-ttu-id="f0058-245">Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for at fremhævnings-, blokerings- og anmærkningshandlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="f0058-246">**Vedligehold billede af kreditorfaktura** – Denne rettighed giver læse-/skriveadgang.</span><span class="sxs-lookup"><span data-stu-id="f0058-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="f0058-247">**Vis billede af kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang.</span><span class="sxs-lookup"><span data-stu-id="f0058-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="f0058-248">Følgende opgaver giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="f0058-249">**Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="f0058-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="f0058-250">**Forespørg status for kreditorfaktura** – Rettigheden Vis billede af kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="f0058-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="f0058-251">Følgende roller giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="f0058-252">**Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.</span><span class="sxs-lookup"><span data-stu-id="f0058-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="f0058-253">**Kreditorassistent**, **Kreditorchef**, **Medarbejder for centraliserede kreditorbetalinger** og **Ansvarlig for kreditorbetalinger** – Opgaven Forespørg status for kreditorfaktura er tildelt til disse roller.</span><span class="sxs-lookup"><span data-stu-id="f0058-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="f0058-254">Siden med undtagelsesoplysninger om fakturaer</span><span class="sxs-lookup"><span data-stu-id="f0058-254">Invoice exception details page</span></span>

<span data-ttu-id="f0058-255">Følgende rettigheder giver skrivebeskyttet adgang eller læse- og skriveadgang til fremviseren for fremhævnings-, blokerings- og anmærkningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="f0058-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="f0058-256">De roller, der er nævnt i dette afsnit, giver fra starten skrivebeskyttet adgang til fakturabillederne i fremviseren af vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="f0058-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="f0058-257">Hvis en rolle også skal have skriveadgang til billederne, kan du tildele denne rolle skriveadgang ved hjælp af den rettighed eller opgave, der er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="f0058-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="f0058-258">**Vedligehold billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver læse-/skriveadgang til fakturabillederne i fremviseren.</span><span class="sxs-lookup"><span data-stu-id="f0058-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="f0058-259">**Vis billede af enhed for overskrift til kreditorfaktura** – Denne rettighed giver skrivebeskyttet adgang til fakturabilledet i fremviseren.</span><span class="sxs-lookup"><span data-stu-id="f0058-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="f0058-260">Følgende opgaver giver skrivebeskyttet adgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="f0058-261">**Vedligehold kreditorfakturaer** – Rettigheden Vedligehold billede af enhed for overskrift til kreditorfaktura er tildelt denne opgave.</span><span class="sxs-lookup"><span data-stu-id="f0058-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="f0058-262">Følgende roller giver skrivebeskyttet adgang til fremviseren for disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="f0058-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="f0058-263">**Kreditorassistent** og **Kreditorchef** – Opgaven Vedligehold kreditorfakturaer er tildelt disse roller.</span><span class="sxs-lookup"><span data-stu-id="f0058-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="f0058-264">Som standard, hvis brugerrollen giver redigeringsrettigheder på enhver side, skal brugeren også have redigeringsrettigheder til fremviseren af vedhæftede filer for fremhævnings-, blokerings- og anmærkningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="f0058-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="f0058-265">Hvis der er situationer, hvor en bestemt rolle skal have redigeringsrettigheder på siden, men ikke i fremviseren, kan der dog bruges de nødvendige rettigheder fra den foregående liste for at opfylde behovet.</span><span class="sxs-lookup"><span data-stu-id="f0058-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
