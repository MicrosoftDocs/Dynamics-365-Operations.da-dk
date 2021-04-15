---
title: Overføre og håndtere statiske filer
description: Dette emne beskriver, hvordan du overfører en statisk fil til Microsoft Dynamics 365 Commerce-webstedsgenerator, og hvordan du opretter en brugerdefineret URL-adresse og et filnavn, der kan bruges til at anmode om filen.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d5f092042b3dda65b041ab2f25f7319dd8e158d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801379"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="e1aa1-103">Overføre og håndtere statiske filer</span><span class="sxs-lookup"><span data-stu-id="e1aa1-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1aa1-104">Dette emne beskriver, hvordan du overfører en statisk fil til Microsoft Dynamics 365 Commerce-webstedsgenerator, og hvordan du opretter en brugerdefineret URL-adresse og et filnavn, der kan bruges til at anmode om filen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="e1aa1-105">Nogle tredjepartsconnectorer kræver, at en fil hostes og behandles på e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="e1aa1-106">Disse connectorer forventer, at filen returneres efter anmodninger til en bestemt URL-adressesti til tilbagekald og filnavn.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="e1aa1-107">I dette emne kan du derfor læse, hvordan du kan overføre og håndtere en statisk fil, der har en brugerdefinerbar URL-adresse og et filnavn på et Dynamics 365 Commerce-e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="e1aa1-108">Oprette en URL-adresse til et websted, der returnerer en statisk fil</span><span class="sxs-lookup"><span data-stu-id="e1aa1-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="e1aa1-109">Udfør følgende trin for at oprette en URL-adresse til et websted, der returnerer en statisk fil i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e1aa1-110">Gå til mediebiblioteket for webstedet, og overfør den fil, der skal behandles af anmodninger til den URL-adresse, du vil definere.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="e1aa1-111">Hvis du allerede har overført filen, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="e1aa1-112">Gå til **URL-adresser** for dit websted.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="e1aa1-113">Vælg **Ny \> Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="e1aa1-114">Vælg **Mediebiblioteksaktiv** i dialogboksen **Ny URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="e1aa1-115">Angiv **URL-stien** i feltet URL-sti.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="e1aa1-116">Medtag filnavnet i stien.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="e1aa1-117">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-117">Select **Next**.</span></span> <span data-ttu-id="e1aa1-118">Mediebiblioteket åbnes og viser alle medieaktiver for den **dokument**-type, der er overført.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="e1aa1-119">Vælg den fil, der skal behandles for anmodninger til den URL-adresse, du har defineret i trin 5.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="e1aa1-120">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-120">Select **Save**.</span></span>

<span data-ttu-id="e1aa1-121">På dette tidspunkt er den URL-adresse, du har oprettet, i kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="e1aa1-122">Den fil, som URL-adressen peger på, bliver ikke returneret, før du publicerer URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="e1aa1-123">Før du publicerer URL-adressen, kan du kontrollere, at den returnerer de korrekte data.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="e1aa1-124">Validere og publicere URL-adresse</span><span class="sxs-lookup"><span data-stu-id="e1aa1-124">Validate and publish a URL</span></span>

<span data-ttu-id="e1aa1-125">Hvis du vil validere en URL-adresse, før du publicerer den, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="e1aa1-126">Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil have vist.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="e1aa1-127">Vælg det korrekte URL-link under knappen **Rediger** i ruden med egenskaber til højre.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="e1aa1-128">Der åbnes et nyt browservindue, og du får vist en 404-fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="e1aa1-129">Tilføj **?preview=inprogress**-forespørgselsstrengen til URL-adressen (f. eks. `https://yoursite.com/callback.html?preview=inprogress`), og genindlæs siden.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="e1aa1-130">Den fil, du har overført til mediebiblioteket, skulle blive returneret med svaret.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="e1aa1-131">Når du har godkendt URL-adressen, kan du publicere den.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="e1aa1-132">Gå til **URL-adresser** for dit websted, og vælg URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="e1aa1-133">Vælg **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="e1aa1-134">Opdater den fil, som en URL-adresse peger på</span><span class="sxs-lookup"><span data-stu-id="e1aa1-134">Update the file that a URL points to</span></span>

<span data-ttu-id="e1aa1-135">Når en URL-adresse publiceres, kan du opdatere den, så den peger på en anden fil.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="e1aa1-136">Du kan også opdatere URL-adressen, så den peger på en anden ressourcetype, som det er beskrevet i næste afsnit.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="e1aa1-137">Du kan f.eks. lade URL-adressen pege på en intern side eller en omdirigering.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="e1aa1-138">Hvis du vil opdatere den fil, som en URL-adresse peger på, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e1aa1-139">Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e1aa1-140">Vælg **Rediger** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e1aa1-141">Under **Tildeling af URL-adresse** skal du markere afkrydsningsfeltet **Trin 2** og derefter vælge et nyt dokument fra mediebiblioteket.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="e1aa1-142">Vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="e1aa1-143">Opdater den aktivtype, som en URL-adresse peger på</span><span class="sxs-lookup"><span data-stu-id="e1aa1-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="e1aa1-144">Du kan også opdatere en URL-adresse, så den peger på en anden type aktiv (ressource), f.eks. en intern side eller en omdirigering.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="e1aa1-145">Hvis du vil opdatere den aktivtype, som en URL-adresse peger på, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e1aa1-146">Gå til **URL-adresser** for dit websted, og vælg den URL-adresse, du vil opdatere.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e1aa1-147">Vælg **Rediger** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e1aa1-148">Under **Tildeling af URL-adresse** skal du vælge en anden aktivtype under **Trin 1**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="e1aa1-149">Marker afkrydsningsfeltet **Trin 2**, og vælg derefter det nye aktiv.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="e1aa1-150">Vælg **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="e1aa1-151">Redigere URL-stien</span><span class="sxs-lookup"><span data-stu-id="e1aa1-151">Change the URL path</span></span>

<span data-ttu-id="e1aa1-152">Når der er oprettet en URL-adresse, kan dens sti ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="e1aa1-153">Hvis du skal ændre den URL-sti, som en fil eller en anden type ressource sendes via, skal du oprette en ny URL-adresse, knytte den til den eksisterende fil eller anden ressource og derefter annullere publiceringen af og slette den gamle URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="e1aa1-154">Benyt følgende fremgangsmåde for at ændre URL-adressestien.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="e1aa1-155">Hvis du vil oprette en ny URL-adresse og knytte den til den eksisterende fil eller en anden ressource, skal du følge instruktionerne i afsnittet [Oprette en URL-adresse til et websted, der returnerer en statisk fil](#create-a-site-url-that-returns-a-static-file) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="e1aa1-156">Vælg den nye URL-adresse, og vælg **Publicer** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="e1aa1-157">Den nye URL-adresse publiceres.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-157">The new URL is published.</span></span>
1. <span data-ttu-id="e1aa1-158">Hvis du vil annullere publiceringen af den gamle URL-adresse, skal du markere den og derefter vælge **Annuller publicering** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="e1aa1-159">Du kan nu evt. slette den gamle URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e1aa1-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1aa1-160">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e1aa1-160">Additional resources</span></span>

[<span data-ttu-id="e1aa1-161">Oversigt over styring af digitale aktiver</span><span class="sxs-lookup"><span data-stu-id="e1aa1-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e1aa1-162">Overføre billeder</span><span class="sxs-lookup"><span data-stu-id="e1aa1-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="e1aa1-163">Uploade videoer</span><span class="sxs-lookup"><span data-stu-id="e1aa1-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="e1aa1-164">Overfør andre filer end billeder og videoer</span><span class="sxs-lookup"><span data-stu-id="e1aa1-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="e1aa1-165">Beskære billeder</span><span class="sxs-lookup"><span data-stu-id="e1aa1-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e1aa1-166">Tilpasse billedets fokuspunkter</span><span class="sxs-lookup"><span data-stu-id="e1aa1-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]