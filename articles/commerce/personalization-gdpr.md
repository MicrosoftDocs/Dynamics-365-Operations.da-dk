---
title: Framelde personlige anbefalinger
description: I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: e822d0097443d7da347c29ebfa63ad6a2d7cbf8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000631"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="dbcf2-103">Framelde personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbcf2-104">I dette emne forklares det, hvordan du kan lade kunderne framelde sig personlige anbefalinger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbcf2-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="dbcf2-105">Overview</span></span>

<span data-ttu-id="dbcf2-106">Under oprettelsen af en konto konfigureres nye kunder automatisk til at modtage personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="dbcf2-107">Dynamics 365 Commerce tilbyder dog forskellige måder for detailhandlere at lade brugerne framelde sig modtagelsen af disse anbefalinger og begrænse behandlingen af deres personlige data.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="dbcf2-108">Godkendte brugere, der fravælger personligt tilpassede anbefalinger, vil straks ophøre med at få vist personligt tilpassede lister.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="dbcf2-109">Desuden fjernes alle personlige data, der er indsamlet til personlig tilpasning, fra modellerne for tilpassede anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="dbcf2-110">Der er flere oplysninger om personligt tilpassede produktanbefalinger, under [Aktivere personlige anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="dbcf2-111">Forskellige måder for detailhandlere at implementere framelding på</span><span class="sxs-lookup"><span data-stu-id="dbcf2-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="dbcf2-112">Detailhandlere kan implementere framelding på tre måder.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="dbcf2-113">Framelding på vegne af brugere</span><span class="sxs-lookup"><span data-stu-id="dbcf2-113">Opting out on behalf of users</span></span>

<span data-ttu-id="dbcf2-114">I Kontostyring i Commerce-administrationen kan detailhandlere vælge framelding på brugernes vegne.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="dbcf2-115">Søg efter **Alle kunder** fra startsiden i administrationen.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="dbcf2-116">Søg efter og vælg en kunde, og vælg derefter oversigtspanelet **Detail**.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Oversigtspanelet Detail](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="dbcf2-118">Under **Beskyttelse af personlige oplysninger** skal du angive indstillingen **Deaktiver tilpasning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Indstillinger for beskyttelse af personlige oplysninger](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="dbcf2-120">Vælg **Gem**, og luk siden.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="dbcf2-121">Modulbaseret framelding</span><span class="sxs-lookup"><span data-stu-id="dbcf2-121">Module-based opt-out experience</span></span>

<span data-ttu-id="dbcf2-122">Detailhandlere kan give godkendte brugere mulighed for selv at fravælge de personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="dbcf2-123">Hvis du vil levere denne framelding, skal du tilføje brugerframeldingsmodulet på debitorkontoprofilsider.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="dbcf2-124">Brugerdefinerede udvidelser</span><span class="sxs-lookup"><span data-stu-id="dbcf2-124">Custom extensions</span></span>

<span data-ttu-id="dbcf2-125">Detailhandlere kan oprette deres egne udvidelser for at administrere brugernes mulighed for framelding.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="dbcf2-126">Yderligere oplysninger finder du under [Kalde Retail Server-API'er](e-commerce-extensibility/call-retail-server-apis.md) og [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="dbcf2-127">Få en digital kopi af personligt tilpassede anbefalingers data på vegne af en godkendt bruger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="dbcf2-128">Kunder vil måske gerne have en digital kopi af deres personlige data, og de kan også se en eksporteret visning af deres anbefalingsresultater.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="dbcf2-129">Hvis en kunde anmoder om disse oplysninger, skal forhandleren oprette en tilpasset udvidelse, der kalder Application Programming Interface (API) til Retail-Server programmet og forespørger på de fulde resultater ud fra **Udvalgt til dig**-listen på basis af kundens kunde-id.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="dbcf2-130">Resultatet kan derefter eksporteres i formatet med kommaseparerede værdier (CSV) og deles med kunden.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="dbcf2-131">Følgende eksempel viser, hvordan en forhandler kan udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="dbcf2-132">Detailhandleren opretter en brugerdefineret udvidelse for at trække personlige anbefalingsdata ud på brugerens vegne.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="dbcf2-133">Oplysninger om, hvordan du opretter moduler, kloner eksisterende moduler, kalder Retail Server-API'er og kalder datahandlinger, finder du under [Udvidelsesmuligheder for onlinekanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="dbcf2-134">Den brugerdefinerede udvidelse kalder **get-recommendations**-kernedatahandlingen og overfører de nødvendige oplysninger til den ud fra kravene på listen.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="dbcf2-135">Hvis der er tale om **Udvalgt til dig**-listen, skal udvidelsen overføre det korrekte listenavn og kunde-id til datahandlingen.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="dbcf2-136">En måde at oprette den brugerdefinerede udvidelse på er at klone det eksisterende produktsamlingsmodul, der bruges til at returnere anbefalede resultater.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="dbcf2-137">Hvis du kloner dette eksisterende modul, kan en forhandler ændre den eksisterende kode og tilføje en ny knap, der eksporterer anbefalingsresultaterne til en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="dbcf2-138">Der er flere oplysninger under [Klone et modul i modulbiblioteket](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-138">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="dbcf2-139">En komplet visning af Retail Server-API-biblioteket finder du under [Kunde- og forbruger-API'er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="dbcf2-140">Når den brugerdefinerede udvidelse er oprettet, kan forhandleren eksportere en CSV-fil med alle anbefalingsresultater på baggrund af det entydige kunde-id for den godkendte bruger.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="dbcf2-141">Detailhandleren kan dele den eksporterede CSV-fil, der indeholder den fulde personlige liste over anbefalede produkter, med den godkendte bruger.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbcf2-142">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dbcf2-142">Additional resources</span></span>

[<span data-ttu-id="dbcf2-143">Oversigt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="dbcf2-144">Aktivér Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="dbcf2-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="dbcf2-145">Aktivér produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="dbcf2-146">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="dbcf2-147">Aktivere anbefalinger af "Køb tilsvarende"</span><span class="sxs-lookup"><span data-stu-id="dbcf2-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="dbcf2-148">Tilføje produktanbefalinger på POS</span><span class="sxs-lookup"><span data-stu-id="dbcf2-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="dbcf2-149">Føje anbefalinger til transaktionsskærmen</span><span class="sxs-lookup"><span data-stu-id="dbcf2-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="dbcf2-150">Justere resultater for AI-ML-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="dbcf2-151">Oprette overvågede anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="dbcf2-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="dbcf2-152">Oprette anbefalinger med demonstrationsdata</span><span class="sxs-lookup"><span data-stu-id="dbcf2-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="dbcf2-153">Ofte stillede spørgsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="dbcf2-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
