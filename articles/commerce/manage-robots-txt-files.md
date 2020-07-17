---
title: Administrer robots.txt-filer
description: Dette emne beskriver, hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b3856a7a0b4b198e71ce9af6691b1d90362f3e7
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533407"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="5f108-103">Administrer robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="5f108-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5f108-104">Dette emne beskriver, hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f108-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5f108-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="5f108-105">Overview</span></span>

<span data-ttu-id="5f108-106">Standarden for "robots exclusion standard" eller robots.txt er en standard, som websteder bruger til at kommunikere med webrobotter.</span><span class="sxs-lookup"><span data-stu-id="5f108-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="5f108-107">Den oplyser webrobotter om alle de områder på et websted, der ikke bør besøges.</span><span class="sxs-lookup"><span data-stu-id="5f108-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="5f108-108">Robotter bruges ofte af søgemaskiner til at indeksere websteder.</span><span class="sxs-lookup"><span data-stu-id="5f108-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="5f108-109">Hvis du vil udelukke robotter fra en server, skal du oprette en fil på serveren.</span><span class="sxs-lookup"><span data-stu-id="5f108-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="5f108-110">I denne fil skal du angive en adgangspolitik for robotter.</span><span class="sxs-lookup"><span data-stu-id="5f108-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="5f108-111">Filen skal være tilgængelig via HTTP på den lokale URL-adresse **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5f108-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="5f108-112">Robots.txt-filen hjælper søgemaskiner med at indeksere indholdet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="5f108-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="5f108-113">Dynamics 365 Commerce giver dig mulighed for at uploade en robots.txt-fil til dit domæne.</span><span class="sxs-lookup"><span data-stu-id="5f108-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="5f108-114">Du kan uploade en robots.txt-fil for hvert domæne i dit Commerce-miljø og knytte den til det pågældende domæne.</span><span class="sxs-lookup"><span data-stu-id="5f108-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="5f108-115">Du finder flere oplysninger om robots-txt-filer på [Siderne om webrobotter](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="5f108-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="5f108-116">Overfør en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="5f108-116">Upload a robots.txt file</span></span>

<span data-ttu-id="5f108-117">Når du har oprettet og redigeret din robots.txt-fil i henhold til [robots exclusion-standarden](https://www.robotstxt.org/orig.html), skal du sørge for, at filen er tilgængelig på den computer, hvor du vil bruge Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="5f108-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="5f108-118">Filen skal have navnet **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5f108-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="5f108-119">Hvis du ønsker de bedste resultater, skal det være i det format, der er angivet i standarden.</span><span class="sxs-lookup"><span data-stu-id="5f108-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="5f108-120">Hver Commerce-kunde er ansvarlig for at validere og vedligeholde indholdet af robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="5f108-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="5f108-121">Hvis du vil overføre en robots.txt-fil, skal du være logget på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5f108-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="5f108-122">Følg disse trin for at overføre en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f108-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5f108-123">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5f108-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5f108-124">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="5f108-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5f108-125">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5f108-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5f108-126">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="5f108-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5f108-127">Vælg **Administrer** for at overføre en robots.txt-fil til et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="5f108-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5f108-128">I menuen til højre skal du vælge knappen **Overfør** (den opadpegende pil) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5f108-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5f108-129">Der vises en dialogboks med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="5f108-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5f108-130">Find og vælg den robots.txt-fil, du vil overføre til det tilknyttede domæne, i dialogboksen, og vælg derefter **Åbn** for at fuldføre overførslen.</span><span class="sxs-lookup"><span data-stu-id="5f108-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="5f108-131">Under overførslen kontrollerer Commerce, at filen er en tekstfil, men den validerer ikke filens indhold.</span><span class="sxs-lookup"><span data-stu-id="5f108-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="5f108-132">Download en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="5f108-132">Download a robots.txt file</span></span>

<span data-ttu-id="5f108-133">Følg disse trin for at downloade en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f108-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5f108-134">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5f108-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5f108-135">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="5f108-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5f108-136">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5f108-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5f108-137">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="5f108-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5f108-138">Vælg **Administrer** for at downloade en robots.txt-fil til et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="5f108-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5f108-139">I menuen til højre skal du vælge knappen **Download** (den nedadpegende pil) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5f108-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5f108-140">Der vises en dialogboks med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="5f108-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5f108-141">Gå til den ønskede placering på det lokale drev i dialogboksen, bekræft eller indtast et filnavn, og vælg derefter **Gem** for at fuldføre downloadet.</span><span class="sxs-lookup"><span data-stu-id="5f108-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="5f108-142">Denne fremgangsmåde kan kun bruges til at hente robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="5f108-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="5f108-143">Slet en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="5f108-143">Delete a robots.txt file</span></span>

<span data-ttu-id="5f108-144">Følg disse trin for at slette en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f108-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5f108-145">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5f108-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5f108-146">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="5f108-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5f108-147">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5f108-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5f108-148">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="5f108-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5f108-149">Vælg **Administrer** for at slette en robots.txt-fil for et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="5f108-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5f108-150">I menuen til højre skal du vælge knappen **Slet** (skraldespandssymbolet) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5f108-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5f108-151">Der vises et vindue med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="5f108-151">A file browser window appears.</span></span>
6. <span data-ttu-id="5f108-152">Find og vælg den robots.txt-fil, du vil slette for det tilknyttede domæne, i filbrowservinduet, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="5f108-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="5f108-153">Der vises en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="5f108-153">A warning message box appears.</span></span>
7. <span data-ttu-id="5f108-154">I meddelelsesfeltet skal du vælge **Slet** for at bekræfte sletningen af robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="5f108-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="5f108-155">Denne fremgangsmåde kan kun bruges til at slette robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="5f108-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f108-156">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5f108-156">Additional resources</span></span>

[<span data-ttu-id="5f108-157">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="5f108-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5f108-158">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="5f108-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5f108-159">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="5f108-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5f108-160">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="5f108-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5f108-161">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="5f108-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5f108-162">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="5f108-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5f108-163">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="5f108-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5f108-164">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="5f108-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5f108-165">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="5f108-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5f108-166">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="5f108-166">Enable location-based store detection</span></span>](enable-store-detection.md)
