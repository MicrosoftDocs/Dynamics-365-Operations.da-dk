---
title: Nummerering af dokumenter og bilag kronologisk
description: Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104362"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="34fb1-103">Nummerering af dokumenter og bilag kronologisk</span><span class="sxs-lookup"><span data-stu-id="34fb1-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="34fb1-104">I nogle lande er der et juridisk krav om at nummerere dokumenter og relaterede bilag i kronologisk rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="34fb1-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="34fb1-105">Kronologien skal understøttes af perioder.</span><span class="sxs-lookup"><span data-stu-id="34fb1-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="34fb1-106">Alle de tal, der tilhører tidligere perioder, skal være mindre end de tal, der tilhører senere perioder.</span><span class="sxs-lookup"><span data-stu-id="34fb1-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="34fb1-107">For at opfylde dette krav er der implementeret kronologisk nummereringsfunktionalitet.</span><span class="sxs-lookup"><span data-stu-id="34fb1-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="34fb1-108">Dette emne indeholder en forklaring på, hvordan du kan konfigurere og bruge kronologiske numre til relevante dokumenter og relaterede bilag.</span><span class="sxs-lookup"><span data-stu-id="34fb1-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="34fb1-109">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="34fb1-109">Prerequisites</span></span>

<span data-ttu-id="34fb1-110">I arbejdsområdet Funktionsstyring skal du aktivere funktionen **kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="34fb1-111">Få flere oplysninger i [Oversigt over funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34fb1-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="34fb1-112">Konfigurere kronologisk nummerering</span><span class="sxs-lookup"><span data-stu-id="34fb1-112">Configure chronological numbering</span></span>

<span data-ttu-id="34fb1-113">Kronologisk nummerering påvirker følgende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="34fb1-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="34fb1-114">**Debitor**</span><span class="sxs-lookup"><span data-stu-id="34fb1-114">**Accounts receivable**</span></span>
- <span data-ttu-id="34fb1-115">Debitorfaktura</span><span class="sxs-lookup"><span data-stu-id="34fb1-115">Customer invoice</span></span>
- <span data-ttu-id="34fb1-116">Debitorfakturabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-116">Customer invoice voucher</span></span>
- <span data-ttu-id="34fb1-117">Salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="34fb1-117">Sales credit note</span></span>
- <span data-ttu-id="34fb1-118">Salgskreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-118">Sales credit note voucher</span></span>
- <span data-ttu-id="34fb1-119">Fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="34fb1-119">Free text invoice</span></span>
- <span data-ttu-id="34fb1-120">Fritekstfakturabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-120">Free text invoice voucher</span></span>
- <span data-ttu-id="34fb1-121">Fritekstkreditnota</span><span class="sxs-lookup"><span data-stu-id="34fb1-121">Free text credit note</span></span>
- <span data-ttu-id="34fb1-122">Fritekstkreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-122">Free text credit note voucher</span></span>
- <span data-ttu-id="34fb1-123">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="34fb1-123">Packing slip</span></span>
- <span data-ttu-id="34fb1-124">Følgeseddelsbilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-124">Packing slip voucher</span></span>
- <span data-ttu-id="34fb1-125">Rettelsesbilag for følgeseddel</span><span class="sxs-lookup"><span data-stu-id="34fb1-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="34fb1-126">Rentenotabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-126">Interest note voucher</span></span>
- <span data-ttu-id="34fb1-127">Rykkerbilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-127">Collection letter voucher</span></span>

<span data-ttu-id="34fb1-128">**Kreditor**</span><span class="sxs-lookup"><span data-stu-id="34fb1-128">**Accounts payable**</span></span>
- <span data-ttu-id="34fb1-129">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-129">Invoice voucher</span></span>
- <span data-ttu-id="34fb1-130">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-130">Credit note voucher</span></span>
- <span data-ttu-id="34fb1-131">Produktkvitteringsbilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-131">Product receipt voucher</span></span>

<span data-ttu-id="34fb1-132">**Projektstyring**</span><span class="sxs-lookup"><span data-stu-id="34fb1-132">**Project management**</span></span>
- <span data-ttu-id="34fb1-133">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="34fb1-133">Invoice</span></span>
- <span data-ttu-id="34fb1-134">Fakturabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-134">Invoice voucher</span></span>
- <span data-ttu-id="34fb1-135">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="34fb1-135">Credit note</span></span>
- <span data-ttu-id="34fb1-136">Kreditnotabilag</span><span class="sxs-lookup"><span data-stu-id="34fb1-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="34fb1-137">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="34fb1-137">Define number sequences</span></span>

<span data-ttu-id="34fb1-138">Du kan definere nummerserier ved at gå til **Organisationsadministration** > **Nummerserier** > **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="34fb1-139">Du kan definere lige så mange nummerserier, der kræves for at dække de påvirkede perioder for påkrævede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="34fb1-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="34fb1-140">Angiv et firma for hver nummerserie.</span><span class="sxs-lookup"><span data-stu-id="34fb1-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="34fb1-141">Segmenter i nummerserierne skal defineres, så de giver kronologisk rækkefølge for perioder.</span><span class="sxs-lookup"><span data-stu-id="34fb1-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="34fb1-142">Segmentnavnene kan f.eks. indeholde et særligt præfiks, der identificerer en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="34fb1-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Konfiguration af nummerserie](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="34fb1-144">Konfigurere nummerseriegrupper</span><span class="sxs-lookup"><span data-stu-id="34fb1-144">Configure number sequence groups</span></span>

<span data-ttu-id="34fb1-145">Hvis du vil konfigurere nummerseriegrupper, skal du gå til **Debitor** > **Konfiguration** > **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="34fb1-146">Under fanen **Nummerserier** skal du definere lige så mange nummerseriegrupper, der er behov for, for at dække de berørte perioder.</span><span class="sxs-lookup"><span data-stu-id="34fb1-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="34fb1-147">For hver gruppe skal du vælge en af de understøttede dokumentreferencer i afsnittet **Reference**, og i feltet **Nummerseriekode** skal du referere til en nummerserie, der tidligere er oprettet for den relaterede periode.</span><span class="sxs-lookup"><span data-stu-id="34fb1-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Konfiguration af nummerseriegruppe](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="34fb1-149">Konfigurer også nummerseriegrupper i modulerne **Kreditor** og **Projektstyring og regnskab**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="34fb1-150">Konfigurere nummerseriegrupper kronologisk</span><span class="sxs-lookup"><span data-stu-id="34fb1-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="34fb1-151">Hvis du vil konfigurere nummerseriegruppers kronologi, skal du gå til **Organisationsadministration** > **Nummerserier** > **Kronologisk nummerseriegrupper**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="34fb1-152">Definer anvendelighedsbetingelserne for nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="34fb1-152">Define the applicability conditions for number sequence groups.</span></span>

![Kronologisk nummeropsætning](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="34fb1-154">Felt</span><span class="sxs-lookup"><span data-stu-id="34fb1-154">Field</span></span>            | <span data-ttu-id="34fb1-155">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="34fb1-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fb1-156">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="34fb1-156">Effective</span></span>  | <span data-ttu-id="34fb1-157">Startdatoen for anvendelse af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="34fb1-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="34fb1-158">Udløb</span><span class="sxs-lookup"><span data-stu-id="34fb1-158">Expiration</span></span>      | <span data-ttu-id="34fb1-159">Slutdatoen for anvendelse af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="34fb1-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="34fb1-160">Hvis der ikke anvendes en slutdato, skal du vælge **Aldrig**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="34fb1-161">Nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="34fb1-161">Number sequence group</span></span> | <span data-ttu-id="34fb1-162">Nummerseriegruppe, der skal bruges til generering af dokumentnumre i perioden.</span><span class="sxs-lookup"><span data-stu-id="34fb1-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="34fb1-163">Oprindelig nummerseriegruppe</span><span class="sxs-lookup"><span data-stu-id="34fb1-163">Original number sequence group</span></span> | <span data-ttu-id="34fb1-164">Denne nummerseriegruppekode bruges til yderligere filtrering af sager, hvis dokumenter allerede har fået tildelt en bestemt *permanent* nummerseriegruppe.</span><span class="sxs-lookup"><span data-stu-id="34fb1-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="34fb1-165">En tom værdi betragtes som en bestemt værdi.</span><span class="sxs-lookup"><span data-stu-id="34fb1-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="34fb1-166">Hvis du vil ignorere en foreløbig tildelt gruppe, skal du bruge indstillingen **Standard** til denne opsætning.</span><span class="sxs-lookup"><span data-stu-id="34fb1-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="34fb1-167">Standard</span><span class="sxs-lookup"><span data-stu-id="34fb1-167">Default</span></span> | <span data-ttu-id="34fb1-168">Hvis den er aktiveret, ignorerer systemet den foreløbige tildelte dokumentnummerseriegruppe og bruger kun start- og slutdatoerne for perioderne til analyse af anvendelighed.</span><span class="sxs-lookup"><span data-stu-id="34fb1-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="34fb1-169">Hvis de er deaktiveret, bruges den fulde kombination af **Gyldig fra** + **Udløb** + **Oprindelig nummerseriegruppe** til valg.</span><span class="sxs-lookup"><span data-stu-id="34fb1-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="34fb1-170">Bogføringsdokument</span><span class="sxs-lookup"><span data-stu-id="34fb1-170">Document posting</span></span>
<span data-ttu-id="34fb1-171">Når du bogfører et dokument, tildeles dokumentet den relevante nummerseriegruppe på grundlag af dokumentets bogføringsdato og bruges derefter til at generere et dokumentnummer baseret på den registrerede nummerserie.</span><span class="sxs-lookup"><span data-stu-id="34fb1-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="34fb1-172">Systemet indeholder en meddelelse om tildeling af nummerseriegrupper.</span><span class="sxs-lookup"><span data-stu-id="34fb1-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumentnummer](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="34fb1-174">I nogle lande er der allerede implementeret en bestemt logik til dokumentnummerering.</span><span class="sxs-lookup"><span data-stu-id="34fb1-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="34fb1-175">I dette tilfælde tilsidesætter landespecifik logikfunktionen **Kronologisk nummerering**.</span><span class="sxs-lookup"><span data-stu-id="34fb1-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
