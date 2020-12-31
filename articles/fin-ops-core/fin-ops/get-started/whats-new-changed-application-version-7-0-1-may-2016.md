---
title: Nyheder eller ændringer i Dynamics AX-programversion 7.0.1 (maj 2016)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics AX-programversion 7.0.1. Denne version blev udgivet i maj 2016 og har build-nummer 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1dd76150dd1519adf2c453db8e874d6db32b5906
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693136"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="14180-104">Nyheder eller ændringer i Dynamics AX-programversion 7.0.1 (maj 2016)</span><span class="sxs-lookup"><span data-stu-id="14180-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14180-105">I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics AX-programversion 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="14180-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="14180-106">Denne version blev udgivet i maj 2016 og har build-nummer 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="14180-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="14180-107">Elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="14180-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="14180-108">Hvad kan du gøre?</span><span class="sxs-lookup"><span data-stu-id="14180-108">What can you do?</span></span> | <span data-ttu-id="14180-109">Hvorfor er det vigtigt?</span><span class="sxs-lookup"><span data-stu-id="14180-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14180-110">Konfigurere kørselsdialogboks til design af elektronisk rapporteringsrapporter, så brugerne kan vælge de økonomiske dimensioner, som de ønsker.</span><span class="sxs-lookup"><span data-stu-id="14180-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="14180-111">På kørselstidspunktet kan brugerne vælge flere økonomiske dimensioner i dialogboksen til kørsel af en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="14180-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="14180-112">Detaljerne for de valgte økonomiske dimensioner vises i det elektroniske dokument, der genereres.</span><span class="sxs-lookup"><span data-stu-id="14180-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="14180-113">Konfigurere adgang til flere økonomiske dimensioner under udarbejdelsen af en ER-rapport via en enkelt tilknytning til den ønskede datakilde.</span><span class="sxs-lookup"><span data-stu-id="14180-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="14180-114">Det samme ER-rapportkonfiguration kan bruges til at generere elektroniske dokumenter, der præsenterer transaktionsdata samt oplysninger om økonomiske dimensioner, uanset antallet af økonomiske dimensioner, der er enten valgt af brugeren eller er konfigureret for den aktuelle juridiske enhed eller forekomst.</span><span class="sxs-lookup"><span data-stu-id="14180-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="14180-115">Konfigurere en ER-rapport for at indtaste data i dynamisk genererede kolonner i et elektronisk dokument, som oprettet i OPENXML-regnearksformat.</span><span class="sxs-lookup"><span data-stu-id="14180-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="14180-116">En ER-rapport kan indtaste data i et OPENXML-regneark, der er genereret, ved at replikere kolonner vandret.</span><span class="sxs-lookup"><span data-stu-id="14180-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="14180-117">Derfor kan den samme ER-konfiguration genbruges til at generere elektroniske dokumenter, der har et forskelligt antal dynamisk genererede kolonner.</span><span class="sxs-lookup"><span data-stu-id="14180-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="14180-118">Konfigurere ER-destinationer, så outputresultatet af et format dirigeres til en bestemt destination: fil, e-mail eller arkiv (Microsoft SharePoint-mappe eller Microsoft Azure Storage).</span><span class="sxs-lookup"><span data-stu-id="14180-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="14180-119">Tidligere, når du kørte en ER-konfiguration, vistes en meddelelsesboks, der krævede brugerhandling for at gemme eller åbne en fil.</span><span class="sxs-lookup"><span data-stu-id="14180-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="14180-120">Nu kan du forudkonfigurere en destination til hver formatkonfiguration og til hver outputkomponent (en mappe eller en fil) separat.</span><span class="sxs-lookup"><span data-stu-id="14180-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="14180-121">Brugere, der har de nødvendige adgangsrettigheder, kan også ændre indstillingerne for destinationen på kørselstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="14180-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="14180-122">POS – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="14180-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="14180-123">Hvad kan du gøre?</span><span class="sxs-lookup"><span data-stu-id="14180-123">What can you do?</span></span> | <span data-ttu-id="14180-124">Hvorfor er det vigtigt?</span><span class="sxs-lookup"><span data-stu-id="14180-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14180-125">Bruge Google Chrome-browseren.</span><span class="sxs-lookup"><span data-stu-id="14180-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="14180-126">Detailhandlere kan nu starte Cloud POS fra Chrome-browseren og kan opleve alle de funktioner, der er tilgængelige i Microsoft Edge og Internet Explorer-versionen af Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="14180-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="14180-127">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="14180-127">Financial reporting</span></span>

| <span data-ttu-id="14180-128">Hvad kan du gøre?</span><span class="sxs-lookup"><span data-stu-id="14180-128">What can you do?</span></span> | <span data-ttu-id="14180-129">Hvorfor er det vigtigt?</span><span class="sxs-lookup"><span data-stu-id="14180-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14180-130">Genopbygge Økonomirapporterings-datacenteret.</span><span class="sxs-lookup"><span data-stu-id="14180-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="14180-131">Når du flytter Dynamics AX-databaser mellem miljøer eller foretager andre indgribende ændringer i miljøet, skal Økonomirapporteringsdatabasen evt. genopbygges.</span><span class="sxs-lookup"><span data-stu-id="14180-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="14180-132">Der leveres nu et Windows PowerShell-script til at genopbygge databasen for dig.</span><span class="sxs-lookup"><span data-stu-id="14180-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="14180-133">Du kan ikke længere vælge rapportdesignerindstillinger, der ikke er gyldige.</span><span class="sxs-lookup"><span data-stu-id="14180-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="14180-134">Flere rapportdesignerindstillinger, der blev brugt i versioner af Management Reporter på markedet, gælder ikke for denne version af Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="14180-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="14180-135">Disse indstillinger er relateret til økonomisk rapport-design, output og sammenkædning.</span><span class="sxs-lookup"><span data-stu-id="14180-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="14180-136">Disse indstillinger er blevet fjernet fra designeren til økonomirapporter for at forhindre brugerfejl.</span><span class="sxs-lookup"><span data-stu-id="14180-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="14180-137">Økonomistyring</span><span class="sxs-lookup"><span data-stu-id="14180-137">Financial management</span></span>

| <span data-ttu-id="14180-138">Hvad kan du gøre?</span><span class="sxs-lookup"><span data-stu-id="14180-138">What can you do?</span></span> | <span data-ttu-id="14180-139">Hvorfor er det vigtigt?</span><span class="sxs-lookup"><span data-stu-id="14180-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="14180-140">Generere positive betalingsfiler til kreditorbetalinger.</span><span class="sxs-lookup"><span data-stu-id="14180-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="14180-141">Der kan genereres positive betalingsfiler for at hjælpe med at forebygge checkbedrageri.</span><span class="sxs-lookup"><span data-stu-id="14180-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="14180-142">Lager og produktion</span><span class="sxs-lookup"><span data-stu-id="14180-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="14180-143">Hvad kan du gøre?</span><span class="sxs-lookup"><span data-stu-id="14180-143">What can you do?</span></span></th>
<th><span data-ttu-id="14180-144">Hvorfor er det vigtigt?</span><span class="sxs-lookup"><span data-stu-id="14180-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="14180-145">Definere en arbejdspolitik for lagerstedet, der styrer oprettelsen af arbejde for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="14180-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="14180-146">Lagerstedsprocesser omfatter ikke altid arbejde.</span><span class="sxs-lookup"><span data-stu-id="14180-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="14180-147">Ved hjælp af den nye politik for lagerstedsarbejde kan du forhindre, at der oprettes arbejde med pluk af råmaterialer og læg-på-lager af færdigvarer for en række produkter på bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="14180-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14180-148">Angive, at en udlagringslokationen for produktion ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="14180-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="14180-149">Du kan nu angive, at en produktudlagringslokation ikke er id-kontrolleret.</span><span class="sxs-lookup"><span data-stu-id="14180-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="14180-150">Denne funktion er for eksempel nyttig, når en upstream-produktionsordre rapporterer varer som færdigmeldte direkte til et sted, der fungerer som produktionsindlagringslokation for en downstream-produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="14180-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14180-151">Understøtte styklister, der omfatter varer med forskellige produktdimensioner af samme vare.</span><span class="sxs-lookup"><span data-stu-id="14180-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="14180-152">Når du bruger en eller flere af produktdimensionerne i produktionen, kan der opstå situationer, hvor du vil producere en vare, der er baseret på en anden variant af den samme vare.</span><span class="sxs-lookup"><span data-stu-id="14180-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="14180-153">Du kan finde flere oplysninger på <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">denne blog</a>.</span><span class="sxs-lookup"><span data-stu-id="14180-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14180-154">Produktionsordrer med cirkulære strukturer på første niveau af deres styklister er udelukket fra kalkulation på styklisteniveau for materialeressourceplanlægning.</span><span class="sxs-lookup"><span data-stu-id="14180-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="14180-155">Det er ikke muligt at tildele korrekte styklisteniveauer til produktvarianter for produktionsordrer, der forårsager cirkularitet i styklistehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="14180-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="14180-156">Beregne separate styklisteniveauer for materialeressourceplanlægning og omkostningsberegning:</span><span class="sxs-lookup"><span data-stu-id="14180-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="14180-157">For planlægning af materialeressource beregnes styklisteniveauer i den nye <strong>ReqItemLevel</strong>-tabel.</span><span class="sxs-lookup"><span data-stu-id="14180-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="14180-158">Afsluttede produktionsordrer ignoreres i beregningen.</span><span class="sxs-lookup"><span data-stu-id="14180-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="14180-159">Til beregning af produktionsomkostninger beregnes styklisteniveauer i <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="14180-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="14180-160">Afsluttede produktionsordrer medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="14180-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="14180-161">Når du kører materialeressourceplanlægning, eksempelvis planlægning og udfoldning af varedisponeringsplan, skal kun styklisteniveauer, der bruges til planlægning af materialeressourcer, genberegnes.</span><span class="sxs-lookup"><span data-stu-id="14180-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="14180-162">Med andre ord er der ingen grund til at beregne styklisteniveauer, der anvendes til beregning af efterkalkulation af produktion.</span><span class="sxs-lookup"><span data-stu-id="14180-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="14180-163">Når du kører efterkalkulationsoperationer, for eksempel lagerlukning, skal kun styklisteniveauer, der anvendes til efterkalkulations-produktionsberegning, genberegnes.</span><span class="sxs-lookup"><span data-stu-id="14180-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="14180-164">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="14180-164">Additional resources</span></span>

[<span data-ttu-id="14180-165">Nyheder eller ændringer på Finance and Operations-startsiden</span><span class="sxs-lookup"><span data-stu-id="14180-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="14180-166">Nye eller opdaterede opgaveguider (maj 2016)</span><span class="sxs-lookup"><span data-stu-id="14180-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
