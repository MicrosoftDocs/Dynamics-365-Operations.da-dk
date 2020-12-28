---
title: Oprindelsesland
description: Mange organisationer udsteder certifikater til deres leverandører for at sikre, at produkterne opfylder bestemte certificeringsstandarder. Disse certifikater afhænger ofte af oprindelseslandet. Dette emne indeholder oplysninger om oprindelseslandsfunktionen, som giver dig mulighed for at sammenkæde et produkt med oprindelseslandet og holde styr på dets produktcertificeringer.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424292"
---
# <a name="country-of-origin"></a><span data-ttu-id="e838a-105">Oprindelsesland</span><span class="sxs-lookup"><span data-stu-id="e838a-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e838a-106">Mange organisationer udsteder certifikater til deres leverandører for at sikre, at produkterne opfylder bestemte certificeringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="e838a-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="e838a-107">Disse certifikater afhænger ofte af oprindelseslandet.</span><span class="sxs-lookup"><span data-stu-id="e838a-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="e838a-108">Oprindelseslandet giver dig mulighed for at sammenkæde et produkt med dets oprindelsesland og holde styr på dets produktcertificeringer.</span><span class="sxs-lookup"><span data-stu-id="e838a-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="e838a-109">Aktivere funktionen for oprindelsesland</span><span class="sxs-lookup"><span data-stu-id="e838a-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="e838a-110">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="e838a-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e838a-111">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="e838a-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e838a-112">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="e838a-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e838a-113">**Modul:** *Administration af produktoplysninger*</span><span class="sxs-lookup"><span data-stu-id="e838a-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="e838a-114">**Funktionsnavn:** *Administrationsfunktion for oprindelsesland*</span><span class="sxs-lookup"><span data-stu-id="e838a-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="e838a-115">Konfigurere kilde- og destinationslande</span><span class="sxs-lookup"><span data-stu-id="e838a-115">Configure source and destination countries</span></span>

<span data-ttu-id="e838a-116">Før du udsteder et certifikat for et produkt, skal du knytte produktet til destinationslandet og oprindelseslandet.</span><span class="sxs-lookup"><span data-stu-id="e838a-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="e838a-117">Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland**.</span><span class="sxs-lookup"><span data-stu-id="e838a-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="e838a-118">Vælg en eksisterende landeopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny landeopsætning.</span><span class="sxs-lookup"><span data-stu-id="e838a-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="e838a-119">Angiv følgende værdier for det valgte eller nye land/område.</span><span class="sxs-lookup"><span data-stu-id="e838a-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="e838a-120">Felt</span><span class="sxs-lookup"><span data-stu-id="e838a-120">Field</span></span> | <span data-ttu-id="e838a-121">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="e838a-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e838a-122">varenummer</span><span class="sxs-lookup"><span data-stu-id="e838a-122">Item number</span></span> | <span data-ttu-id="e838a-123">Vælg varenummeret for produktet.</span><span class="sxs-lookup"><span data-stu-id="e838a-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="e838a-124">Destinationsland</span><span class="sxs-lookup"><span data-stu-id="e838a-124">Destination country</span></span> | <span data-ttu-id="e838a-125">Vælg det land/område, du sender produktet til.</span><span class="sxs-lookup"><span data-stu-id="e838a-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="e838a-126">Oprindelsesland</span><span class="sxs-lookup"><span data-stu-id="e838a-126">Origin country</span></span> | <span data-ttu-id="e838a-127">Vælg det land/område, du sender produktet fra.</span><span class="sxs-lookup"><span data-stu-id="e838a-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="e838a-128">Formålet med denne konfiguration er at hjælpe dig med at generere en styklisterapport, hvor du kan medtage oprindelsesland for hver del, som kilde- og destinationslandene er angivet for.</span><span class="sxs-lookup"><span data-stu-id="e838a-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="e838a-129">Denne rapport kan hjælpe dig med at få et holistisk billede af, hvor dine dele kommer fra, og hvor de befinder sig.</span><span class="sxs-lookup"><span data-stu-id="e838a-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="e838a-130">Holde styr på kreditorcertifikater</span><span class="sxs-lookup"><span data-stu-id="e838a-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="e838a-131">Du kan bruge siden **Oprindelsesland for keditorcertifikater** til at holde styr på certifikater, som du udsteder til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="e838a-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="e838a-132">Du skal beslutte, hvilke certifikatdokumenter du er ved at udstede, og hvordan du vil rapportere dem til kunderne.</span><span class="sxs-lookup"><span data-stu-id="e838a-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="e838a-133">Denne funktion hjælper dig med at holde styr på dine certifikater.</span><span class="sxs-lookup"><span data-stu-id="e838a-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="e838a-134">Du kan også vælge, om de relevante certifikatnumre skal vises på fakturaer, følgesedler og/eller ordrebekræftelser.</span><span class="sxs-lookup"><span data-stu-id="e838a-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="e838a-135">Benyt følgende fremgangsmåde for at konfigurere dine certifikatoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e838a-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="e838a-136">Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland for kreditorcertifikater**.</span><span class="sxs-lookup"><span data-stu-id="e838a-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="e838a-137">Vælg en eksisterende certifikatopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny certifikatopsætning.</span><span class="sxs-lookup"><span data-stu-id="e838a-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="e838a-138">Angiv følgende indstillinger for det valgte eller nye certifikat.</span><span class="sxs-lookup"><span data-stu-id="e838a-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="e838a-139">Felt</span><span class="sxs-lookup"><span data-stu-id="e838a-139">Field</span></span> | <span data-ttu-id="e838a-140">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="e838a-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e838a-141">Kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="e838a-141">Vendor account</span></span> | <span data-ttu-id="e838a-142">Vælg den kreditor, du har udstedt certifikatet til.</span><span class="sxs-lookup"><span data-stu-id="e838a-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="e838a-143">varenummer</span><span class="sxs-lookup"><span data-stu-id="e838a-143">Item number</span></span> | <span data-ttu-id="e838a-144">Vælg den vare, du har udstedt certifikatet for.</span><span class="sxs-lookup"><span data-stu-id="e838a-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="e838a-145">Land/område</span><span class="sxs-lookup"><span data-stu-id="e838a-145">Country/region</span></span> | <span data-ttu-id="e838a-146">Det destinationsland eller -område, hvor du skal bruge dette certifikat.</span><span class="sxs-lookup"><span data-stu-id="e838a-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="e838a-147">Certifikatnummer</span><span class="sxs-lookup"><span data-stu-id="e838a-147">Certificate number</span></span> | <span data-ttu-id="e838a-148">Angiv id-nummeret på det certifikat, du har udstedt.</span><span class="sxs-lookup"><span data-stu-id="e838a-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="e838a-149">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="e838a-149">Effective</span></span> | <span data-ttu-id="e838a-150">Vælg den første dato, hvor det aktuelle certifikat er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="e838a-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="e838a-151">Udløb</span><span class="sxs-lookup"><span data-stu-id="e838a-151">Expiration</span></span> | <span data-ttu-id="e838a-152">Vælg den sidste dato, hvor det aktuelle certifikat er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="e838a-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="e838a-153">Udskriv på faktura</span><span class="sxs-lookup"><span data-stu-id="e838a-153">Print on invoice</span></span> | <span data-ttu-id="e838a-154">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de fakturaer, der er adresseret til det angivne land/område i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="e838a-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e838a-155">Udskriv på følgeseddel</span><span class="sxs-lookup"><span data-stu-id="e838a-155">Print on packing slip</span></span> | <span data-ttu-id="e838a-156">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på følgesedler, der er adresseret til det angivne land/område i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="e838a-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e838a-157">Udskriv på salgsordre</span><span class="sxs-lookup"><span data-stu-id="e838a-157">Print on sales order</span></span> | <span data-ttu-id="e838a-158">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de salgsordrer, der er adresseret til det angivne land/område i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="e838a-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="e838a-159">Medtag oprindelseslandet på styklisterapporter</span><span class="sxs-lookup"><span data-stu-id="e838a-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="e838a-160">Når du genererer en styklisterapport, kan du medtage oprindelseslandet for hver del, som du har angivet kilde- og destinationslande for, på siden **Regler for oprindelsesland**.</span><span class="sxs-lookup"><span data-stu-id="e838a-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="e838a-161">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="e838a-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e838a-162">Vælg eller opret et produkt for at åbne dets side for **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="e838a-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="e838a-163">Gå til handlingsruden, og vælg **Designer** i gruppen **Stykliste** under fanen **Tekniker**.</span><span class="sxs-lookup"><span data-stu-id="e838a-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="e838a-164">På den side, der vises, skal du i handlingsruden vælge **Stykliste \> Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="e838a-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="e838a-165">I dialogboksen **Styklistelinjer** skal du angive feltet **Destinationsland** til det destinationsland, du vil have vist i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e838a-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="e838a-166">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e838a-166">Select **OK**.</span></span>

<span data-ttu-id="e838a-167">En rapport, der viser oplysninger om de enkelte deles oprindelsesland, genereres og vises.</span><span class="sxs-lookup"><span data-stu-id="e838a-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="e838a-168">Her er et eksempel på rapporten.</span><span class="sxs-lookup"><span data-stu-id="e838a-168">Here is an example of the report.</span></span>

<span data-ttu-id="e838a-169">![Rapport om oprindelsesland](media/country-of-origin-report.png "Rapport om oprindelsesland")</span><span class="sxs-lookup"><span data-stu-id="e838a-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
