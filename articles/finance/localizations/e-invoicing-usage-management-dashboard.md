---
title: Dashboardet Brugsstyring
description: Dette emne forklarer, hvordan du bruger dashboardet Brugsstyring til at overvåge brugen af tjenesten Elektronisk fakturering og altid overholder angivne standarder.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130500"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="f5a7e-103">Dashboardet Brugsstyring</span><span class="sxs-lookup"><span data-stu-id="f5a7e-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5a7e-104">Dashboardet **Brugsstyring** hjælper dig med at overvåge brugen af den elektroniske faktureringsservice og hjælper derfor din organisation med at overholde månedlig brug.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="f5a7e-105">Overholdelse bestemmes ved at beregne afsendelsesvolumen og sammenligne den med den anskaffede volumen for afsendelser for at identificere eventuelle afvigelser mellem den anskaffede volumen og den anvendte volumen.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="f5a7e-106">Dashboardet indeholder følgende indikatorer:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="f5a7e-107">En omkostningsindikator, som du kan bruge til at overvåge forbruget med henblik på licensoverholdelse:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="f5a7e-108">Forbrug pr. måned (eksport)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-108">Usage per month (export)</span></span>

- <span data-ttu-id="f5a7e-109">Tre driftsmæssige indikatorer, som du kan bruge til at spore brugen af tjenesten til elektronisk fakturering til administrationsformål:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="f5a7e-110">Brug af funktion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-110">Usage by feature</span></span>
    - <span data-ttu-id="f5a7e-111">Brug efter miljø</span><span class="sxs-lookup"><span data-stu-id="f5a7e-111">Usage by environment</span></span>
    - <span data-ttu-id="f5a7e-112">Forbrug pr. måned (import)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="f5a7e-113">Omfang af mål</span><span class="sxs-lookup"><span data-stu-id="f5a7e-113">Measurement scope</span></span>

- <span data-ttu-id="f5a7e-114">Måleenhed:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-114">Unit of measure:</span></span> 

    <span data-ttu-id="f5a7e-115">Dashboardet **Brugsstyring** tæller afsendelsen af forretningsdokumenter og importerede elektroniske fakturaer.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="f5a7e-116">Organisation:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-116">Organization:</span></span> 

    <span data-ttu-id="f5a7e-117">Optælling opsummeres ud fra organisationens lejer-id, uanset antallet af forekomster af Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management eller antallet af juridiske enheder, hvor tjenesten til elektronisk fakturering er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="f5a7e-118">Indikator: Brug pr. måned (eksport)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="f5a7e-119">Denne indikator indeholder oplysninger om de elektroniske fakturaer, som din organisation udsteder i løbet af en defineret periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="f5a7e-120">Område</span><span class="sxs-lookup"><span data-stu-id="f5a7e-120">Scope</span></span>
- <span data-ttu-id="f5a7e-121">Antallet af forretningsdokumenter, der afsendes fra Finance og Supply Chain Management til tjenesten for elektronisk fakturering, uanset antallet af linjer i forretningsdokumenterne.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="f5a7e-122">Antallet af afsendte forretningsdokumenter, der er blevet korrekt behandlet af den elektroniske faktureringsservice.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="f5a7e-123">Et dokument anses for at være behandlet korrekt, når flowet af handlinger, der er defineret i funktionsopsætningen, er fuldført.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="f5a7e-124">Når en elektronisk faktura sendes til en ekstern webtjeneste, er optællingen uafhængig af resultaterne af behandling af webtjenesten (accepterede, afviste eller skemavalideringsfejl).</span><span class="sxs-lookup"><span data-stu-id="f5a7e-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="f5a7e-125">Hvis webtjenesten har modtaget og besvaret anmodningen fra den elektroniske faktureringstjeneste, betragtes afsendelsen som en gyldig optælling.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="f5a7e-126">**Undtagelse:** Forretningsdokumenter tælles ikke med, hvis de sendes fra Finance og Supply Chain Management til den elektroniske faktureringsservice, f.eks. i de scenarier, hvor samme forretningsdokument skal sendes igen for at ændre status for den elektroniske faktura.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="f5a7e-127">Udstedelsen af en brasiliansk elektronisk faktura (regnskabsdokumentet) er f.eks. gyldig, mens annulleringsanmodningen for den ikke er medregnet.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="f5a7e-128">Udregning</span><span class="sxs-lookup"><span data-stu-id="f5a7e-128">Calculation</span></span>

<span data-ttu-id="f5a7e-129">Saldoberegningen foretages på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="f5a7e-130">Saldo = Gratis + Købt – Brugt</span><span class="sxs-lookup"><span data-stu-id="f5a7e-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="f5a7e-131">Placering:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-131">Where:</span></span>

- <span data-ttu-id="f5a7e-132">Gratis:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-132">Free:</span></span>
  
    <span data-ttu-id="f5a7e-133">En gratis volumen af forretningsdokumenter, som kunden kan sende pr. måned.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="f5a7e-134">Den indeholder en pakke med 100 forretningsdokumenter, der kan sendes til den elektroniske faktureringsservice.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="f5a7e-135">Den gratis volumen er ikke akkumuleret, og eventuel resterende saldo overføres ikke til næste periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="f5a7e-136">Købt:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-136">Purchased:</span></span>
  
    <span data-ttu-id="f5a7e-137">En pakke med 1.000 forretningsdokumenter, der kan sendes til den elektroniske faktureringsservice.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="f5a7e-138">Denne pakke skal anskaffes af din organisation på månedsbasis.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="f5a7e-139">Den købte volumen er ikke akkumuleret, og eventuel resterende saldo overføres ikke til næste periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="f5a7e-140">Brugt:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-140">Used:</span></span> 

    <span data-ttu-id="f5a7e-141">Antallet af afsendte forretningsdokumenter til den elektroniske faktureringsservice i henhold til definerede kriterier.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="f5a7e-142">Hvis din organisation planlægger at overskride den månedlige mængde på 100 gratis afsendelser, skal du købe den maksimale mængde for at sikre, at du overholder Microsofts licenspolitik for tjenesten til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="f5a7e-143">I øjeblikket skal købt volumen angives manuelt i overensstemmelse med anskaffelsesdatoen som flere pakker på 1.000 afsendelser.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="f5a7e-144">Indikator: Anvendelse efter funktion</span><span class="sxs-lookup"><span data-stu-id="f5a7e-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="f5a7e-145">Denne indikator viser brugen af funktioner for elektronisk fakturering til udstedelse af elektroniske fakturaer i en defineret periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="f5a7e-146">Udregning:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-146">Calculation:</span></span>
  
    <span data-ttu-id="f5a7e-147">Brugt = Antal gange hver enkelt funktion til elektronisk fakturering er blevet brugt under afsendelse af forretningsdokumenter til den elektroniske faktureringsservice.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="f5a7e-148">Indikator: Anvendelse efter miljø</span><span class="sxs-lookup"><span data-stu-id="f5a7e-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="f5a7e-149">Denne indikator viser brugen af servicemiljøer for elektronisk fakturering i en defineret periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="f5a7e-150">Udregning:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-150">Calculation:</span></span>
    
    <span data-ttu-id="f5a7e-151">Brugt = Antal gange hvert enkelt tjenestemiljø til elektronisk fakturering er blevet brugt under afsendelse af forretningsdokumenter til den elektroniske faktureringsservice.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="f5a7e-152">Indikator: Brug pr. måned (import)</span><span class="sxs-lookup"><span data-stu-id="f5a7e-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="f5a7e-153">Denne indikator viser omfanget af import af elektroniske fakturaer fra tjenesten Elektronisk fakturering til Finance og Supply Chain Management i en defineret periode.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="f5a7e-154">Område:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-154">Scope:</span></span>

    <span data-ttu-id="f5a7e-155">Elektroniske fakturaer, der importeres til Finance og Supply Chain Management, uanset antallet af linjer, som disse elektroniske fakturaer indeholder.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="f5a7e-156">Udregning:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-156">Calculation:</span></span>

    <span data-ttu-id="f5a7e-157">Modtaget = Antal importerede elektroniske fakturaer til Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="f5a7e-158">Funktioner</span><span class="sxs-lookup"><span data-stu-id="f5a7e-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="f5a7e-159">Indkøb</span><span class="sxs-lookup"><span data-stu-id="f5a7e-159">Purchase</span></span>

<span data-ttu-id="f5a7e-160">Under fanen **Brug pr. måned (eksport)** skal du vælge **Indkøb** for manuelt at registrere beløbet af anskaffede afsendelser.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="f5a7e-161">Vælg **Ny** for en bestemt dato, og angiv det antal **Pakker**, der er anskaffet på den pågældende dato.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="f5a7e-162">**Antal** beregnes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="f5a7e-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="f5a7e-163">Antal = Pakker \* 1,000</span><span class="sxs-lookup"><span data-stu-id="f5a7e-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="f5a7e-164">Det beregnede **Antal** afspejles i det **Købte** fra indikatoren **Forbrug pr. måned (eksport)**.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="f5a7e-165">Vedligeholdelse</span><span class="sxs-lookup"><span data-stu-id="f5a7e-165">Update</span></span>

<span data-ttu-id="f5a7e-166">Vælg **Opdater** i handlingsruden for at opdatere beregningen og opdatere de data, der vises på siden og i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="f5a7e-167">Nulstil historikdata</span><span class="sxs-lookup"><span data-stu-id="f5a7e-167">Reset history data</span></span>

<span data-ttu-id="f5a7e-168">Vælg **Nulstil historikdata** i handlingsruden for at opdatere den database, som indikatorerne beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="f5a7e-169">Dashboardet **Brugsstyring** viser ikke pengebeløb.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="f5a7e-170">I stedet viser det kun volumen af optalte afsendelser og importerede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="f5a7e-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
