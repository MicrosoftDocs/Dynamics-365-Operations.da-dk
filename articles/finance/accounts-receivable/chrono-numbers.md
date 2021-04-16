---
title: Nummerering af dokumenter og bilag kronologisk
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838855"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="eefe7-103">Nummerering af dokumenter og bilag kronologisk</span><span class="sxs-lookup"><span data-stu-id="eefe7-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eefe7-104">I nogle lande er der et juridisk krav om at nummerere dokumenter og relaterede bilag i kronologisk rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="eefe7-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="eefe7-105">Kronologien skal understøttes af perioder.</span><span class="sxs-lookup"><span data-stu-id="eefe7-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="eefe7-106">Alle de tal, der tilhører tidligere perioder, skal være mindre end de tal, der tilhører senere perioder.</span><span class="sxs-lookup"><span data-stu-id="eefe7-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="eefe7-107">For at opfylde dette krav er der implementeret kronologisk nummereringsfunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="eefe7-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="eefe7-108">Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.</span><span class="sxs-lookup"><span data-stu-id="eefe7-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eefe7-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="eefe7-109">Prerequisites</span></span>

<span data-ttu-id="eefe7-110">I arbejdsområdet Funktionsstyring skal du aktivere funktionen **kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="eefe7-111">Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eefe7-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="eefe7-112">Konfigurere kronologisk nummerering</span><span class="sxs-lookup"><span data-stu-id="eefe7-112">Configure chronological numbering</span></span>

<span data-ttu-id="eefe7-113">Kronologisk nummerering påvirker følgende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="eefe7-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="eefe7-114">**Debitor**</span><span class="sxs-lookup"><span data-stu-id="eefe7-114">**Accounts receivable**</span></span>
- <span data-ttu-id="eefe7-115">Debitorfaktura</span><span class="sxs-lookup"><span data-stu-id="eefe7-115">Customer invoice</span></span>
- <span data-ttu-id="eefe7-116">Debitorfakturabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-116">Customer invoice voucher</span></span>
- <span data-ttu-id="eefe7-117">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="eefe7-117">Sales credit note</span></span>
- <span data-ttu-id="eefe7-118">Salgskreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-118">Sales credit note voucher</span></span>
- <span data-ttu-id="eefe7-119">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="eefe7-119">Free text invoice</span></span>
- <span data-ttu-id="eefe7-120">Fritekstfakturabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-120">Free text invoice voucher</span></span>
- <span data-ttu-id="eefe7-121">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="eefe7-121">Free text credit note</span></span>
- <span data-ttu-id="eefe7-122">Fritekstkreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-122">Free text credit note voucher</span></span>
- <span data-ttu-id="eefe7-123">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="eefe7-123">Packing slip</span></span>
- <span data-ttu-id="eefe7-124">Følgeseddelsbilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-124">Packing slip voucher</span></span>
- <span data-ttu-id="eefe7-125">Rettelsesbilag for følgeseddel</span><span class="sxs-lookup"><span data-stu-id="eefe7-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="eefe7-126">Rentenotabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-126">Interest note voucher</span></span>
- <span data-ttu-id="eefe7-127">Rykkerbilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-127">Collection letter voucher</span></span>

<span data-ttu-id="eefe7-128">**Kreditor**</span><span class="sxs-lookup"><span data-stu-id="eefe7-128">**Accounts payable**</span></span>
- <span data-ttu-id="eefe7-129">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-129">Invoice voucher</span></span>
- <span data-ttu-id="eefe7-130">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-130">Credit note voucher</span></span>
- <span data-ttu-id="eefe7-131">Produktkvitteringsbilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-131">Product receipt voucher</span></span>

<span data-ttu-id="eefe7-132">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="eefe7-132">**Project management**</span></span>
- <span data-ttu-id="eefe7-133">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="eefe7-133">Invoice</span></span>
- <span data-ttu-id="eefe7-134">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-134">Invoice voucher</span></span>
- <span data-ttu-id="eefe7-135">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="eefe7-135">Credit note</span></span>
- <span data-ttu-id="eefe7-136">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="eefe7-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="eefe7-137">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="eefe7-137">Define number sequences</span></span>

<span data-ttu-id="eefe7-138">Du kan definere nummerserier ved at gå til **Organisationsadministration** > **Nummerserier** > **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="eefe7-139">Du kan definere lige så mange nummerserier, der kræves for at dække de påvirkede perioder for påkrævede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="eefe7-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="eefe7-140">Angiv et firma for hver nummerserie.</span><span class="sxs-lookup"><span data-stu-id="eefe7-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="eefe7-141">Segmenter i nummerserierne skal defineres, så de giver kronologisk rækkefølge for perioder.</span><span class="sxs-lookup"><span data-stu-id="eefe7-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="eefe7-142">Segmentnavnene kan f.eks. indeholde et særligt præfiks, der identificerer en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="eefe7-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Konfiguration af nummerserie](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="eefe7-144">Konfigurere nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="eefe7-144">Configure number sequence groups</span></span>

<span data-ttu-id="eefe7-145">Hvis du vil konfigurere nummerseriegrupper, skal du gå til **Debitor** > **Konfiguration** > **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="eefe7-146">Under fanen **Nummerserier** skal du definere lige så mange nummerseriegrupper, der er behov for, for at dække de berørte perioder.</span><span class="sxs-lookup"><span data-stu-id="eefe7-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="eefe7-147">For hver gruppe skal du vælge en af de understøttede dokumentreferencer i afsnittet **Reference**, og i feltet **Nummerseriekode** skal du referere til en nummerserie, der tidligere er oprettet for den relaterede periode.</span><span class="sxs-lookup"><span data-stu-id="eefe7-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Konfiguration af nummerseriegruppe](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="eefe7-149">Konfigurer også nummerseriegrupper i modulerne **Kreditor** og **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="eefe7-150">Konfigurere nummerseriegrupper kronologisk</span><span class="sxs-lookup"><span data-stu-id="eefe7-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="eefe7-151">Hvis du vil konfigurere nummerseriegruppers kronologi, skal du gå til **Organisationsadministration** > **Nummerserier** > **Kronologisk nummerseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="eefe7-152">Definer anvendelighedsbetingelserne for nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="eefe7-152">Define the applicability conditions for number sequence groups.</span></span>

![Kronologisk nummeropsætning](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="eefe7-154">Felt</span><span class="sxs-lookup"><span data-stu-id="eefe7-154">Field</span></span>            | <span data-ttu-id="eefe7-155">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="eefe7-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefe7-156">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="eefe7-156">Effective</span></span>  | <span data-ttu-id="eefe7-157">Startdatoen for anvendelse af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="eefe7-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="eefe7-158">Udløb</span><span class="sxs-lookup"><span data-stu-id="eefe7-158">Expiration</span></span>      | <span data-ttu-id="eefe7-159">Slutdatoen for anvendelse af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="eefe7-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="eefe7-160">Hvis der ikke anvendes en slutdato, skal du vælge **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="eefe7-161">Nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="eefe7-161">Number sequence group</span></span> | <span data-ttu-id="eefe7-162">Nummerseriegruppe, der skal bruges til generering af dokumentnumre i perioden.</span><span class="sxs-lookup"><span data-stu-id="eefe7-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="eefe7-163">Oprindelig nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="eefe7-163">Original number sequence group</span></span> | <span data-ttu-id="eefe7-164">Denne nummerseriegruppekode bruges til yderligere filtrering af sager, hvis dokumenter allerede har fået tildelt en bestemt *permanent* nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="eefe7-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="eefe7-165">En tom værdi betragtes som en bestemt værdi.</span><span class="sxs-lookup"><span data-stu-id="eefe7-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="eefe7-166">Hvis du vil ignorere en foreløbig tildelt gruppe, skal du bruge indstillingen **Standard** til denne opsætning.</span><span class="sxs-lookup"><span data-stu-id="eefe7-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="eefe7-167">Standard</span><span class="sxs-lookup"><span data-stu-id="eefe7-167">Default</span></span> | <span data-ttu-id="eefe7-168">Hvis den er aktiveret, ignorerer systemet den foreløbige tildelte dokumentnummerseriegruppe og bruger kun start- og slutdatoerne for perioderne til analyse af anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="eefe7-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="eefe7-169">Hvis de er deaktiveret, bruges den fulde kombination af **Gyldig fra** + **Udløb** + **Oprindelig nummerseriegruppe** til valg.</span><span class="sxs-lookup"><span data-stu-id="eefe7-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="eefe7-170">Bogføringsdokument</span><span class="sxs-lookup"><span data-stu-id="eefe7-170">Document posting</span></span>
<span data-ttu-id="eefe7-171">Når du bogfører et dokument, tildeles dokumentet den relevante nummerseriegruppe på grundlag af dokumentets bogføringsdato og bruges derefter til at generere et dokumentnummer baseret på den registrerede nummerserie.</span><span class="sxs-lookup"><span data-stu-id="eefe7-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="eefe7-172">Systemet indeholder en meddelelse om tildeling af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="eefe7-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="eefe7-174">I nogle lande er der allerede implementeret en bestemt logik til dokumentnummerering.</span><span class="sxs-lookup"><span data-stu-id="eefe7-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="eefe7-175">I dette tilfælde tilsidesætter landespecifik logikfunktionen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="eefe7-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
