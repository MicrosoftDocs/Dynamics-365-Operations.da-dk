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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596214"
---
# <a name="country-of-origin"></a><span data-ttu-id="b9423-105">Oprindelsesland</span><span class="sxs-lookup"><span data-stu-id="b9423-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9423-106">Mange organisationer udsteder certifikater til deres leverandører for at sikre, at produkterne opfylder bestemte certificeringsstandarder.</span><span class="sxs-lookup"><span data-stu-id="b9423-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="b9423-107">Disse certifikater afhænger ofte af oprindelseslandet.</span><span class="sxs-lookup"><span data-stu-id="b9423-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="b9423-108">Oprindelseslandet giver dig mulighed for at sammenkæde et produkt med dets oprindelsesland og holde styr på dets produktcertificeringer.</span><span class="sxs-lookup"><span data-stu-id="b9423-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="b9423-109">Konfigurere kilde- og destinationslande</span><span class="sxs-lookup"><span data-stu-id="b9423-109">Configure source and destination countries</span></span>

<span data-ttu-id="b9423-110">Før du udsteder et certifikat for et produkt, skal du knytte produktet til destinationslandet og oprindelseslandet.</span><span class="sxs-lookup"><span data-stu-id="b9423-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="b9423-111">Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland**.</span><span class="sxs-lookup"><span data-stu-id="b9423-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="b9423-112">Vælg en eksisterende landeopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny landeopsætning.</span><span class="sxs-lookup"><span data-stu-id="b9423-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="b9423-113">Angiv følgende værdier for det valgte eller nye land.</span><span class="sxs-lookup"><span data-stu-id="b9423-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="b9423-114">Felt</span><span class="sxs-lookup"><span data-stu-id="b9423-114">Field</span></span> | <span data-ttu-id="b9423-115">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="b9423-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b9423-116">varenummer</span><span class="sxs-lookup"><span data-stu-id="b9423-116">Item number</span></span> | <span data-ttu-id="b9423-117">Vælg varenummeret for produktet.</span><span class="sxs-lookup"><span data-stu-id="b9423-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="b9423-118">Destinationsland</span><span class="sxs-lookup"><span data-stu-id="b9423-118">Destination country</span></span> | <span data-ttu-id="b9423-119">Vælg det land, du sender produktet til.</span><span class="sxs-lookup"><span data-stu-id="b9423-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="b9423-120">Oprindelsesland</span><span class="sxs-lookup"><span data-stu-id="b9423-120">Origin country</span></span> | <span data-ttu-id="b9423-121">Vælg det land, du sender produktet fra.</span><span class="sxs-lookup"><span data-stu-id="b9423-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="b9423-122">Formålet med denne konfiguration er at hjælpe dig med at generere en styklisterapport, hvor du kan medtage oprindelsesland for hver del, som kilde- og destinationslandene er angivet for.</span><span class="sxs-lookup"><span data-stu-id="b9423-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="b9423-123">Denne rapport kan hjælpe dig med at få et holistisk billede af, hvor dine dele kommer fra, og hvor de befinder sig.</span><span class="sxs-lookup"><span data-stu-id="b9423-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="b9423-124">Holde styr på kreditorcertifikater</span><span class="sxs-lookup"><span data-stu-id="b9423-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="b9423-125">Du kan bruge siden **Oprindelsesland for keditorcertifikater** til at holde styr på certifikater, som du udsteder til kreditorer.</span><span class="sxs-lookup"><span data-stu-id="b9423-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="b9423-126">Du skal beslutte, hvilke certifikatdokumenter du er ved at udstede, og hvordan du vil rapportere dem til kunderne.</span><span class="sxs-lookup"><span data-stu-id="b9423-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="b9423-127">Denne funktion hjælper dig med at holde styr på dine certifikater.</span><span class="sxs-lookup"><span data-stu-id="b9423-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="b9423-128">Du kan også vælge, om de relevante certifikatnumre skal vises på fakturaer, følgesedler og/eller ordrebekræftelser.</span><span class="sxs-lookup"><span data-stu-id="b9423-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="b9423-129">Benyt følgende fremgangsmåde for at konfigurere dine certifikatoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b9423-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="b9423-130">Gå til **Administration af produktoplysninger \> Konfiguration \> Produktoverholdelse \> Oprindelsesland \> Regler for oprindelsesland for kreditorcertifikater**.</span><span class="sxs-lookup"><span data-stu-id="b9423-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="b9423-131">Vælg en eksisterende certifikatopsætning, du vil redigere, eller vælg **Ny** i handlingsruden for at oprette en ny certifikatopsætning.</span><span class="sxs-lookup"><span data-stu-id="b9423-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="b9423-132">Angiv følgende indstillinger for det valgte eller nye certifikat.</span><span class="sxs-lookup"><span data-stu-id="b9423-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="b9423-133">Felt</span><span class="sxs-lookup"><span data-stu-id="b9423-133">Field</span></span> | <span data-ttu-id="b9423-134">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="b9423-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b9423-135">Kreditorkonto</span><span class="sxs-lookup"><span data-stu-id="b9423-135">Vendor account</span></span> | <span data-ttu-id="b9423-136">Vælg den kreditor, du har udstedt certifikatet til.</span><span class="sxs-lookup"><span data-stu-id="b9423-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="b9423-137">varenummer</span><span class="sxs-lookup"><span data-stu-id="b9423-137">Item number</span></span> | <span data-ttu-id="b9423-138">Vælg den vare, du har udstedt certifikatet for.</span><span class="sxs-lookup"><span data-stu-id="b9423-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="b9423-139">Land/område</span><span class="sxs-lookup"><span data-stu-id="b9423-139">Country/region</span></span> | <span data-ttu-id="b9423-140">Det destinationsland eller -område, hvor du skal bruge dette certifikat.</span><span class="sxs-lookup"><span data-stu-id="b9423-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="b9423-141">Certifikatnummer</span><span class="sxs-lookup"><span data-stu-id="b9423-141">Certificate number</span></span> | <span data-ttu-id="b9423-142">Angiv id-nummeret på det certifikat, du har udstedt.</span><span class="sxs-lookup"><span data-stu-id="b9423-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="b9423-143">Gyldig fra</span><span class="sxs-lookup"><span data-stu-id="b9423-143">Effective</span></span> | <span data-ttu-id="b9423-144">Vælg den første dato, hvor det aktuelle certifikat er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="b9423-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="b9423-145">Udløb</span><span class="sxs-lookup"><span data-stu-id="b9423-145">Expiration</span></span> | <span data-ttu-id="b9423-146">Vælg den sidste dato, hvor det aktuelle certifikat er gyldigt.</span><span class="sxs-lookup"><span data-stu-id="b9423-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="b9423-147">Udskriv på faktura</span><span class="sxs-lookup"><span data-stu-id="b9423-147">Print on invoice</span></span> | <span data-ttu-id="b9423-148">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de fakturaer, der er adresseret til det angivne land i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="b9423-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b9423-149">Udskriv på følgeseddel</span><span class="sxs-lookup"><span data-stu-id="b9423-149">Print on packing slip</span></span> | <span data-ttu-id="b9423-150">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på følgesedler, der er adresseret til det angivne land i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="b9423-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b9423-151">Udskriv på salgsordre</span><span class="sxs-lookup"><span data-stu-id="b9423-151">Print on sales order</span></span> | <span data-ttu-id="b9423-152">Markér dette afkrydsningsfelt for at udskrive certifikatnummeret på de salgsordrer, der er adresseret til det angivne land i det angivne datointerval.</span><span class="sxs-lookup"><span data-stu-id="b9423-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="b9423-153">Medtag oprindelseslandet på styklisterapporter</span><span class="sxs-lookup"><span data-stu-id="b9423-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="b9423-154">Når du genererer en styklisterapport, kan du medtage oprindelseslandet for hver del, som du har angivet kilde- og destinations lande for, på siden **Regler for oprindelsesland**.</span><span class="sxs-lookup"><span data-stu-id="b9423-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="b9423-155">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="b9423-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b9423-156">Vælg eller opret et produkt for at åbne dets side for **Frigivne produktdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="b9423-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="b9423-157">Gå til handlingsruden, og vælg **Designer** i gruppen **Stykliste** under fanen **Tekniker**.</span><span class="sxs-lookup"><span data-stu-id="b9423-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="b9423-158">På den side, der vises, skal du i handlingsruden vælge **Stykliste \> Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="b9423-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="b9423-159">I dialogboksen **Styklistelinjer** skal du angive feltet **Destinationsland** til det destinationsland, du vil have vist i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b9423-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="b9423-160">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9423-160">Select **OK**.</span></span>

<span data-ttu-id="b9423-161">En rapport, der viser oplysninger om de enkelte deles oprindelsesland, genereres og vises.</span><span class="sxs-lookup"><span data-stu-id="b9423-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="b9423-162">Her er et eksempel på rapporten.</span><span class="sxs-lookup"><span data-stu-id="b9423-162">Here is an example of the report.</span></span>

<span data-ttu-id="b9423-163">![Rapport om oprindelsesland](media/country-of-origin-report.png "Rapport om oprindelsesland")</span><span class="sxs-lookup"><span data-stu-id="b9423-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
