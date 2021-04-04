---
title: Administrere robots.txt-filer
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
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477702"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="9146f-103">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="9146f-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9146f-104">Dette emne beskriver, hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9146f-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9146f-105">Standarden for "robots exclusion standard" eller robots.txt er en standard, som websteder bruger til at kommunikere med webrobotter.</span><span class="sxs-lookup"><span data-stu-id="9146f-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="9146f-106">Den oplyser webrobotter om alle de områder på et websted, der ikke bør besøges.</span><span class="sxs-lookup"><span data-stu-id="9146f-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="9146f-107">Robotter bruges ofte af søgemaskiner til at indeksere websteder.</span><span class="sxs-lookup"><span data-stu-id="9146f-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="9146f-108">Hvis du vil udelukke robotter fra en server, skal du oprette en fil på serveren.</span><span class="sxs-lookup"><span data-stu-id="9146f-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="9146f-109">I denne fil skal du angive en adgangspolitik for robotter.</span><span class="sxs-lookup"><span data-stu-id="9146f-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="9146f-110">Filen skal være tilgængelig via HTTP på den lokale URL-adresse **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="9146f-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="9146f-111">Robots.txt-filen hjælper søgemaskiner med at indeksere indholdet på dit websted.</span><span class="sxs-lookup"><span data-stu-id="9146f-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="9146f-112">Dynamics 365 Commerce giver dig mulighed for at uploade en robots.txt-fil til dit domæne.</span><span class="sxs-lookup"><span data-stu-id="9146f-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="9146f-113">Du kan uploade en robots.txt-fil for hvert domæne i dit Commerce-miljø og knytte den til det pågældende domæne.</span><span class="sxs-lookup"><span data-stu-id="9146f-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="9146f-114">Du finder flere oplysninger om robots-txt-filer på [Siderne om webrobotter](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="9146f-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="9146f-115">Overfør en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="9146f-115">Upload a robots.txt file</span></span>

<span data-ttu-id="9146f-116">Når du har oprettet og redigeret din robots.txt-fil i henhold til [robots exclusion-standarden](https://www.robotstxt.org/orig.html), skal du sørge for, at filen er tilgængelig på den computer, hvor du vil bruge Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="9146f-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="9146f-117">Filen skal have navnet **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="9146f-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="9146f-118">Hvis du ønsker de bedste resultater, skal det være i det format, der er angivet i standarden.</span><span class="sxs-lookup"><span data-stu-id="9146f-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="9146f-119">Hver Commerce-kunde er ansvarlig for at validere og vedligeholde indholdet af robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="9146f-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="9146f-120">Hvis du vil overføre en robots.txt-fil, skal du være logget på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="9146f-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="9146f-121">Følg disse trin for at overføre en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="9146f-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9146f-122">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="9146f-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="9146f-123">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="9146f-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="9146f-124">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="9146f-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="9146f-125">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="9146f-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="9146f-126">Vælg **Administrer** for at overføre en robots.txt-fil til et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="9146f-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="9146f-127">I menuen til højre skal du vælge knappen **Overfør** (den opadpegende pil) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="9146f-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="9146f-128">Der vises en dialogboks med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="9146f-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="9146f-129">Find og vælg den robots.txt-fil, du vil overføre til det tilknyttede domæne, i dialogboksen, og vælg derefter **Åbn** for at fuldføre overførslen.</span><span class="sxs-lookup"><span data-stu-id="9146f-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="9146f-130">Under overførslen kontrollerer Commerce, at filen er en tekstfil, men den validerer ikke filens indhold.</span><span class="sxs-lookup"><span data-stu-id="9146f-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="9146f-131">Download en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="9146f-131">Download a robots.txt file</span></span>

<span data-ttu-id="9146f-132">Følg disse trin for at downloade en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="9146f-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9146f-133">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="9146f-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="9146f-134">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="9146f-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="9146f-135">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="9146f-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="9146f-136">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="9146f-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="9146f-137">Vælg **Administrer** for at downloade en robots.txt-fil til et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="9146f-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="9146f-138">I menuen til højre skal du vælge knappen **Download** (den nedadpegende pil) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="9146f-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="9146f-139">Der vises en dialogboks med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="9146f-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="9146f-140">Gå til den ønskede placering på det lokale drev i dialogboksen, bekræft eller indtast et filnavn, og vælg derefter **Gem** for at fuldføre downloadet.</span><span class="sxs-lookup"><span data-stu-id="9146f-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="9146f-141">Denne fremgangsmåde kan kun bruges til at hente robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="9146f-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="9146f-142">Slet en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="9146f-142">Delete a robots.txt file</span></span>

<span data-ttu-id="9146f-143">Følg disse trin for at slette en robots.txt-fil i Commerce.</span><span class="sxs-lookup"><span data-stu-id="9146f-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9146f-144">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="9146f-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="9146f-145">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="9146f-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="9146f-146">Under **Lejerindstillinger** skal du vælge **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="9146f-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="9146f-147">En liste over alle de domæner, der er tilknyttet dit miljø, vises i hoveddelen af vinduet.</span><span class="sxs-lookup"><span data-stu-id="9146f-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="9146f-148">Vælg **Administrer** for at slette en robots.txt-fil for et domæne i dit miljø.</span><span class="sxs-lookup"><span data-stu-id="9146f-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="9146f-149">I menuen til højre skal du vælge knappen **Slet** (skraldespandssymbolet) ud for det domæne, der er knyttet til filen robots.txt.</span><span class="sxs-lookup"><span data-stu-id="9146f-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="9146f-150">Der vises et vindue med en filbrowser.</span><span class="sxs-lookup"><span data-stu-id="9146f-150">A file browser window appears.</span></span>
6. <span data-ttu-id="9146f-151">Find og vælg den robots.txt-fil, du vil slette for det tilknyttede domæne, i filbrowservinduet, og vælg derefter **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="9146f-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="9146f-152">Der vises en advarselsmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="9146f-152">A warning message box appears.</span></span>
7. <span data-ttu-id="9146f-153">I meddelelsesfeltet skal du vælge **Slet** for at bekræfte sletningen af robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="9146f-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="9146f-154">Denne fremgangsmåde kan kun bruges til at slette robots.txt-filer, der tidligere er blevet overført via Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="9146f-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9146f-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="9146f-155">Additional resources</span></span>

[<span data-ttu-id="9146f-156">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="9146f-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9146f-157">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="9146f-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9146f-158">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="9146f-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9146f-159">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="9146f-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9146f-160">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="9146f-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9146f-161">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="9146f-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9146f-162">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="9146f-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9146f-163">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="9146f-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9146f-164">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="9146f-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9146f-165">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="9146f-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
