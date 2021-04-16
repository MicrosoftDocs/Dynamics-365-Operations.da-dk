---
title: Framelde personlige anbefalinger
description: I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7d0f505ce49bc9be0d027cbb0d636c9de0600b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804447"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="5237d-103">Fravælge tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5237d-104">I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5237d-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5237d-105">Under oprettelsen af en konto konfigureres nye kunder automatisk til at modtage personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="5237d-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="5237d-106">Dynamics 365 Commerce tilbyder dog forskellige måder for detailhandlere at lade brugerne framelde sig modtagelsen af disse anbefalinger og begrænse behandlingen af deres personlige data.</span><span class="sxs-lookup"><span data-stu-id="5237d-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="5237d-107">Godkendte brugere, der fravælger personligt tilpassede anbefalinger, vil straks ophøre med at få vist personligt tilpassede lister.</span><span class="sxs-lookup"><span data-stu-id="5237d-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="5237d-108">Desuden fjernes alle personlige data, der er indsamlet til personlig tilpasning, fra modellerne for tilpassede anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="5237d-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="5237d-109">Der er flere oplysninger om personligt tilpassede produktanbefalinger, under [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5237d-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="5237d-110">Forskellige måder for detailhandlere at implementere framelding på</span><span class="sxs-lookup"><span data-stu-id="5237d-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="5237d-111">Detailhandlere kan implementere framelding på tre måder.</span><span class="sxs-lookup"><span data-stu-id="5237d-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="5237d-112">Framelding på vegne af brugere</span><span class="sxs-lookup"><span data-stu-id="5237d-112">Opting out on behalf of users</span></span>

<span data-ttu-id="5237d-113">I Kontostyring i Commerce-administrationen kan detailhandlere vælge framelding på brugernes vegne.</span><span class="sxs-lookup"><span data-stu-id="5237d-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="5237d-114">Søg efter **Alle kunder** fra startsiden i administrationen.</span><span class="sxs-lookup"><span data-stu-id="5237d-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="5237d-115">Søg efter og vælg en kunde, og vælg derefter oversigtspanelet **Detail**.</span><span class="sxs-lookup"><span data-stu-id="5237d-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Oversigtspanelet Detail](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="5237d-117">Under **Beskyttelse af personlige oplysninger** skal du angive indstillingen **Deaktiver tilpasning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5237d-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Indstillinger for beskyttelse af personlige oplysninger](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="5237d-119">Vælg **Gem**, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="5237d-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="5237d-120">Modulbaseret framelding</span><span class="sxs-lookup"><span data-stu-id="5237d-120">Module-based opt-out experience</span></span>

<span data-ttu-id="5237d-121">Detailhandlere kan give godkendte brugere mulighed for selv at fravælge de personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="5237d-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="5237d-122">Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.</span><span class="sxs-lookup"><span data-stu-id="5237d-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="5237d-123">Brugerdefinerede udvidelser</span><span class="sxs-lookup"><span data-stu-id="5237d-123">Custom extensions</span></span>

<span data-ttu-id="5237d-124">Detailhandlere kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding.</span><span class="sxs-lookup"><span data-stu-id="5237d-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="5237d-125">Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5237d-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="5237d-126">Få en digital kopi af personligt tilpassede anbefalingers data på vegne af en godkendt bruger</span><span class="sxs-lookup"><span data-stu-id="5237d-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="5237d-127">Kunder vil måske gerne have en digital kopi af deres personlige data, og de kan også se en eksporteret visning af deres anbefalingsresultater.</span><span class="sxs-lookup"><span data-stu-id="5237d-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="5237d-128">Hvis en kunde anmoder om disse oplysninger, skal forhandleren oprette en tilpasset udvidelse, der kalder Application Programming Interface (API) til Retail-Server programmet og forespørger på de fulde resultater ud fra **Udvalgt til dig**-listen på basis af kundens kunde-id.</span><span class="sxs-lookup"><span data-stu-id="5237d-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="5237d-129">Resultatet kan derefter eksporteres i formatet med kommaseparerede værdier (CSV) og deles med kunden.</span><span class="sxs-lookup"><span data-stu-id="5237d-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="5237d-130">Følgende eksempel viser, hvordan en forhandler kan udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="5237d-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="5237d-131">Detailhandleren opretter en brugerdefineret udvidelse for at trække personlige anbefalingsdata ud på brugerens vegne.</span><span class="sxs-lookup"><span data-stu-id="5237d-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="5237d-132">Oplysninger om, hvordan du opretter moduler, kloner eksisterende moduler, kalder Retail Server-API'er og kalder datahandlinger, finder du under [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5237d-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="5237d-133">Den brugerdefinerede udvidelse kalder **get-recommendations**-kernedatahandlingen og overfører de nødvendige oplysninger til den ud fra kravene på listen.</span><span class="sxs-lookup"><span data-stu-id="5237d-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="5237d-134">Hvis der er tale om **Udvalgt til dig**-listen, skal udvidelsen overføre det korrekte listenavn og kunde-id til datahandlingen.</span><span class="sxs-lookup"><span data-stu-id="5237d-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="5237d-135">En måde at oprette den brugerdefinerede udvidelse på er at klone det eksisterende produktsamlingsmodul, der bruges til at returnere anbefalede resultater.</span><span class="sxs-lookup"><span data-stu-id="5237d-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="5237d-136">Hvis du kloner dette eksisterende modul, kan en forhandler ændre den eksisterende kode og tilføje en ny knap, der eksporterer anbefalingsresultaterne til en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="5237d-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="5237d-137">Der er flere oplysninger under [Klone et modul i modulbiblioteket](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5237d-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="5237d-138">En komplet visning af Retail Server-API-biblioteket finder du under [Kunde- og forbruger-API'er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="5237d-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="5237d-139">Når den brugerdefinerede udvidelse er oprettet, kan forhandleren eksportere en CSV-fil med alle anbefalingsresultater på baggrund af det entydige kunde-id for den godkendte bruger.</span><span class="sxs-lookup"><span data-stu-id="5237d-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="5237d-140">Detailhandleren kan dele den eksporterede CSV-fil, der indeholder den fulde personlige liste over anbefalede produkter, med den godkendte bruger.</span><span class="sxs-lookup"><span data-stu-id="5237d-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5237d-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5237d-141">Additional resources</span></span>

[<span data-ttu-id="5237d-142">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5237d-143">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="5237d-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="5237d-144">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="5237d-145">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="5237d-146">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="5237d-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="5237d-147">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="5237d-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="5237d-148">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="5237d-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5237d-149">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5237d-150">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="5237d-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5237d-151">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="5237d-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="5237d-152">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="5237d-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
