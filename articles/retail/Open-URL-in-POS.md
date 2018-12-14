---
title: "Åbne URL-adresse i POS"
description: "Dette emne indeholder en oversigt over de forbedringer, der er foretaget i produkt- og kundesøgefunktionen i Microsoft Dynamics 365 for Retail."
author: AamirAllaq
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: f7df0a91948a494465fbd55af99757e3890357ce
ms.openlocfilehash: 4b8a0291855460b79f3a241eccb4b55b009804bf
ms.contentlocale: da-dk
ms.lasthandoff: 12/04/2018

---

# <a name="open-url-in-pos"></a><span data-ttu-id="68df9-103">Åbne URL-adresse i POS</span><span class="sxs-lookup"><span data-stu-id="68df9-103">Open URL in POS</span></span>

<span data-ttu-id="68df9-104">I dette emne beskrives, hvordan du kan konfigurere en knap i Retail POS til at åbne en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="68df9-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="68df9-105">Denne funktion kræver ikke tilpasning af kode og kan konfigureres af en person, der ikke har rollen som udvikler.</span><span class="sxs-lookup"><span data-stu-id="68df9-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span>

<span data-ttu-id="68df9-106">Denne funktion gør det muligt ved hjælp af knapmatrixdesigneren at konfigurere en knap i POS til at åbne en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="68df9-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="68df9-107">Dette understøttes i øjeblikket i følgende konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="68df9-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="68df9-108">Åbne i et nyt vindue</span><span class="sxs-lookup"><span data-stu-id="68df9-108">Open in new window.</span></span>
- <span data-ttu-id="68df9-109">Åbne i POS</span><span class="sxs-lookup"><span data-stu-id="68df9-109">Open within POS.</span></span>
- <span data-ttu-id="68df9-110">Åbne en oprindelig app</span><span class="sxs-lookup"><span data-stu-id="68df9-110">Open a native app.</span></span> 

## <a name="open-in-new-window"></a><span data-ttu-id="68df9-111">Åbn i et nyt vindue</span><span class="sxs-lookup"><span data-stu-id="68df9-111">Open in new window</span></span>

<span data-ttu-id="68df9-112">Denne konfiguration definerer, om URL-adressen skal åbnes i et nyt vindue eller i appen.</span><span class="sxs-lookup"><span data-stu-id="68df9-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="68df9-113">Når konfigurationen er indstillet til at åbne en URL-adresse i appen, er sidenavigationspanelet og øverste søjle i POS synlige og tilgængelige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="68df9-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="68df9-114">Når konfigurationen er indstillet til at åbne i et nyt vindue, åbnes URL-adressen i et nyt appvindue i Modern POS til Windows og i en ny fane i browseren i alle andre POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="68df9-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="68df9-115">Du kan aktivere denne ved at konfigurere URL-adressen med indstillingen **Åbn i nyt vindue** valgt.</span><span class="sxs-lookup"><span data-stu-id="68df9-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="68df9-116">Åbne i POS</span><span class="sxs-lookup"><span data-stu-id="68df9-116">Open within POS</span></span>
<span data-ttu-id="68df9-117">Åbning af en URL-adresse i POS understøttes i øjeblikket kun for Modern POS i Windows.</span><span class="sxs-lookup"><span data-stu-id="68df9-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="68df9-118">På andre klienter er denne funktion under udvikling og planlagt til frigivelse i fremtidige opdateringer.</span><span class="sxs-lookup"><span data-stu-id="68df9-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="68df9-119">Du kan aktivere denne ved at konfigurere URL-adressen uden at vælge indstillingen **Åbn i nyt vindue**.</span><span class="sxs-lookup"><span data-stu-id="68df9-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="68df9-120">Åbne en oprindelig app</span><span class="sxs-lookup"><span data-stu-id="68df9-120">Open a native app</span></span>
<span data-ttu-id="68df9-121">Med denne funktion kan du også indstille ikke-web-URL-adresser til at åbne en oprindelig app.</span><span class="sxs-lookup"><span data-stu-id="68df9-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="68df9-122">Du kan for eksempel angive URL-protokoller som MailTo, SIP, IM eller MSTEAMS, som derefter kan håndteres af de respektive oprindelige apps på værtsenheden.</span><span class="sxs-lookup"><span data-stu-id="68df9-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="68df9-123">Du kan aktivere denne ved at konfigurere URL-adressen med indstillingen **Åbn i nyt vindue** valgt.</span><span class="sxs-lookup"><span data-stu-id="68df9-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span> 

- <span data-ttu-id="68df9-124">For Windows-computere kan du i [Eksportere eller importere standardprogramtilknytninger](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) finde oplysninger om, hvordan du indstiller standardprotokoltilknytninger, hvis du konfigurerer computeren ved hjælp af DISM (Deployment Image Servicing and Management).</span><span class="sxs-lookup"><span data-stu-id="68df9-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span> 
- <span data-ttu-id="68df9-125">Hvis du bruger MDM, f.eks. Intune, til at administrere Windows-computere, skal du se [Politik CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="68df9-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span> 
- <span data-ttu-id="68df9-126">Hvis du er udvikler og bygger et brugerdefineret websted, skal du se [Start standardappen for en URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="68df9-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span> 

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="68df9-127">Åbne en oprindelig app problemfrit</span><span class="sxs-lookup"><span data-stu-id="68df9-127">Open a native app seamlessly</span></span>
<span data-ttu-id="68df9-128">I Windows, iOS og Android er det også muligt at åbne apps mere problemfrit ved hjælp af app-protokoltilknytning.</span><span class="sxs-lookup"><span data-stu-id="68df9-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="68df9-129">Hvis din app ikke allerede er konfigureret til at håndtere åbning fra en webbrowser, skal du muligvis bede en udvikler om at konfigurere dette.</span><span class="sxs-lookup"><span data-stu-id="68df9-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="68df9-130">For Windows, se [Aktivere apps til websteder ved hjælp af app-URI-handlere](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="68df9-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="68df9-131">For IOS, se [Universal Links til udviklere](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="68df9-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="68df9-132">For Android, se [Håndtering af Android App Links](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="68df9-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>  


|   <span data-ttu-id="68df9-133">Klient</span><span class="sxs-lookup"><span data-stu-id="68df9-133">Client</span></span>                |<span data-ttu-id="68df9-134">Åbn i et nyt vindue</span><span class="sxs-lookup"><span data-stu-id="68df9-134">Open in new window</span></span> |<span data-ttu-id="68df9-135">Åbne en oprindelig app</span><span class="sxs-lookup"><span data-stu-id="68df9-135">Open native app</span></span> | <span data-ttu-id="68df9-136">Åbne i POS</span><span class="sxs-lookup"><span data-stu-id="68df9-136">Open within POS</span></span>            | <span data-ttu-id="68df9-137">Oplysninger</span><span class="sxs-lookup"><span data-stu-id="68df9-137">Details</span></span>                           |
|-------------------------|-------------------|----------------|--------------------------|-----------------------------------|
| <span data-ttu-id="68df9-138">Modern POS i Windows</span><span class="sxs-lookup"><span data-stu-id="68df9-138">Modern POS on Windows</span></span>   | <span data-ttu-id="68df9-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="68df9-139">✓\*</span></span>                |    <span data-ttu-id="68df9-140">✓</span><span class="sxs-lookup"><span data-stu-id="68df9-140">✓</span></span>          |       <span data-ttu-id="68df9-141">✓</span><span class="sxs-lookup"><span data-stu-id="68df9-141">✓</span></span>                  | <span data-ttu-id="68df9-142">\*Åbner i et nyt Modern POS-vindue</span><span class="sxs-lookup"><span data-stu-id="68df9-142">\*Opens in new Modern POS window</span></span>   |
| <span data-ttu-id="68df9-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="68df9-143">Cloud POS</span></span>               | <span data-ttu-id="68df9-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="68df9-144">✓\*</span></span>                |    <span data-ttu-id="68df9-145">✓</span><span class="sxs-lookup"><span data-stu-id="68df9-145">✓</span></span>          |       <span data-ttu-id="68df9-146">X</span><span class="sxs-lookup"><span data-stu-id="68df9-146">X</span></span>                   |  <span data-ttu-id="68df9-147">\*Åbner under en ny fane i browseren</span><span class="sxs-lookup"><span data-stu-id="68df9-147">\*Opens in new browser tab</span></span>       |
| <span data-ttu-id="68df9-148">Moderne POS i iOS</span><span class="sxs-lookup"><span data-stu-id="68df9-148">Modern POS on iOS</span></span>       | <span data-ttu-id="68df9-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="68df9-149">✓\*</span></span>                |    <span data-ttu-id="68df9-150">✓</span><span class="sxs-lookup"><span data-stu-id="68df9-150">✓</span></span>          |       <span data-ttu-id="68df9-151">X</span><span class="sxs-lookup"><span data-stu-id="68df9-151">X</span></span>                  |  <span data-ttu-id="68df9-152">\*Åbner under en ny fane i browseren</span><span class="sxs-lookup"><span data-stu-id="68df9-152">\*Opens in new browser tab</span></span>        |
| <span data-ttu-id="68df9-153">Modern POS i Android</span><span class="sxs-lookup"><span data-stu-id="68df9-153">Modern POS on Android</span></span>   | <span data-ttu-id="68df9-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="68df9-154">✓\*</span></span>                |    <span data-ttu-id="68df9-155">✓</span><span class="sxs-lookup"><span data-stu-id="68df9-155">✓</span></span>          |       <span data-ttu-id="68df9-156">X</span><span class="sxs-lookup"><span data-stu-id="68df9-156">X</span></span>                  |  <span data-ttu-id="68df9-157">\*Åbner under en ny fane i browseren</span><span class="sxs-lookup"><span data-stu-id="68df9-157">\*Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="68df9-158">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="68df9-158">Before you begin</span></span>
<span data-ttu-id="68df9-159">Før du begynder, skal du gennemgå, hvordan du konfigurerer [Skærmlayout til POS](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="68df9-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="68df9-160">Åbne URL-adresse i POS</span><span class="sxs-lookup"><span data-stu-id="68df9-160">Open URL in POS</span></span>
<span data-ttu-id="68df9-161">Hvis du vil konfigurere en URL-adresse, så den kan åbnes i POS, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="68df9-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1.  <span data-ttu-id="68df9-162">I hovedkontoret skal du gå til **Detail > Konfiguration af kanal > POS-opsætning > POS > Skærmlayout**.</span><span class="sxs-lookup"><span data-stu-id="68df9-162">In head office, go to **Retail > Channel Setup > POS Setup > POS > Screen Layouts**.</span></span>
2.  <span data-ttu-id="68df9-163">Vælg **Knapmatricer > Designer**.</span><span class="sxs-lookup"><span data-stu-id="68df9-163">Select **Button Grids > Designer**.</span></span>
3.  <span data-ttu-id="68df9-164">Opret en ny knap.</span><span class="sxs-lookup"><span data-stu-id="68df9-164">Create a new button.</span></span>
4.  <span data-ttu-id="68df9-165">Vælg **Knap**-egenskaber.</span><span class="sxs-lookup"><span data-stu-id="68df9-165">Select **Button** properties.</span></span>
5.  <span data-ttu-id="68df9-166">Vælg **Åbn URL** som handling.</span><span class="sxs-lookup"><span data-stu-id="68df9-166">Select **Open URL** as the action.</span></span>
6.  <span data-ttu-id="68df9-167">Angiv den URL-adresse, du vil bruge.</span><span class="sxs-lookup"><span data-stu-id="68df9-167">Enter the URL that you want to use.</span></span>
7.  <span data-ttu-id="68df9-168">Angiv, om URL-adressen skal åbnes i et nyt vindue.</span><span class="sxs-lookup"><span data-stu-id="68df9-168">Configure whether to open the URL in a new window.</span></span>

