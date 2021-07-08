---
title: Nyheder eller ændringer i Warehouse Management-mobilappen
description: Dette emne viser de nye og ændrede funktioner for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261768"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="af042-103">Nyheder eller ændringer i Warehouse Management-mobilappen</span><span class="sxs-lookup"><span data-stu-id="af042-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af042-104">Dette emne viser de nye funktioner, rettelser, forbedringer og kendte problemer for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="af042-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="af042-105">Version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="af042-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="af042-106">Nye funktioner, rettelser og forbedringer i version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="af042-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="af042-107">I denne version introduceres følgende nye funktioner, rettelser og forbedringer.</span><span class="sxs-lookup"><span data-stu-id="af042-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="af042-108">I demotilstand vises nu alle etiketter på enhedssproget.</span><span class="sxs-lookup"><span data-stu-id="af042-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="af042-109">Det er mindre sandsynligt, at du får følgende fejlmeddelelse: "Der kan ikke findes en passende visning til den angivne størrelse".</span><span class="sxs-lookup"><span data-stu-id="af042-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="af042-110">Minimumshøjden for arbejdskort er øget (i tilfælde hvor tre eller færre felter konfigureres til at blive vist på opgavelisten).</span><span class="sxs-lookup"><span data-stu-id="af042-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="af042-111">Margener (udtoning) nederst i detaljekort er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="af042-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="af042-112">Ugyldige symboler i XML-filer, der udveksles med serveren, håndteres nu korrekt.</span><span class="sxs-lookup"><span data-stu-id="af042-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="af042-113">(Tegn, der ikke kan udskrives, håndteres for eksempel nu igen korrekt og medfører ikke længere, at appen holder op med at svare).</span><span class="sxs-lookup"><span data-stu-id="af042-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="af042-114">HTTP-fejl (for eksempel "fejl 503"), når der sendes en serveranmodning, håndteres nu korrekt.</span><span class="sxs-lookup"><span data-stu-id="af042-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="af042-115">Mens der vises en fejl, vises indstillingslisten ikke længere automatisk for kontrolelementer af typen kombinationsboks.</span><span class="sxs-lookup"><span data-stu-id="af042-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="af042-116">Appen holder ikke længere op med at svare på grund af den visningsretning, der er valgt i brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="af042-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="af042-117">Produktbilleder vises nu i selvbetjeningsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="af042-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="af042-118">(Denne ændring gælder kun for versioner med lav opløsning.</span><span class="sxs-lookup"><span data-stu-id="af042-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="af042-119">Filstyringstjenesten understøtter ikke billeder i fuld størrelse i selvbetjeningsmiljøer).</span><span class="sxs-lookup"><span data-stu-id="af042-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="af042-120">En fejl, der involverede korte pluk med nul antal, er blevet løst.</span><span class="sxs-lookup"><span data-stu-id="af042-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="af042-121">Appen holder ikke længere op med at svare, når et detaljekort viser flere identiske felter.</span><span class="sxs-lookup"><span data-stu-id="af042-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="af042-122">Kendte problemer i version 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="af042-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="af042-123">Der findes følgende kendte problemer i denne version:</span><span class="sxs-lookup"><span data-stu-id="af042-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="af042-124">Appen (især opgavelisten) bliver langsommere over tid.</span><span class="sxs-lookup"><span data-stu-id="af042-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="af042-125">**Windows-version:** Når en USB-drev bruges til scanning i Windows, medfører uoverensstemmende resultater, at scannede symboler blandes sammen.</span><span class="sxs-lookup"><span data-stu-id="af042-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="af042-126">Version 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="af042-126">Version 2.0.5.0</span></span>

<span data-ttu-id="af042-127">I denne version introduceres følgende nye funktioner, rettelser og forbedringer.</span><span class="sxs-lookup"><span data-stu-id="af042-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="af042-128">Klienthemmeligheden skjules ikke længere i opsætningen af forbindelsesindstillinger.</span><span class="sxs-lookup"><span data-stu-id="af042-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="af042-129">Du kan nu trykke længe på enhver tekst for at se den i fuld længde.</span><span class="sxs-lookup"><span data-stu-id="af042-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="af042-130">Fejlmeddelelsen, når der mangler lagertilladelser, er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="af042-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="af042-131">Der er tilføjet nye kontrolsekvenser for nogle flow.</span><span class="sxs-lookup"><span data-stu-id="af042-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="af042-132">Knappen Send bliver ikke længere tilgængelig på grund af størrelsesvinduet.</span><span class="sxs-lookup"><span data-stu-id="af042-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="af042-133">Skydere kan nu fortsætte på mindre skærme, når der bruges store knapstørrelser.</span><span class="sxs-lookup"><span data-stu-id="af042-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="af042-134">Overlejringen med fire knapper kan ikke længere afskæres.</span><span class="sxs-lookup"><span data-stu-id="af042-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="af042-135">Nu understøttes knappen Delete på tastaturet.</span><span class="sxs-lookup"><span data-stu-id="af042-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="af042-136">Et problem med lysstyrke, der kan forekomme, når der trykkes på tastaturet, er løst.</span><span class="sxs-lookup"><span data-stu-id="af042-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="af042-137">Der er løst forskellige problemer med demodata.</span><span class="sxs-lookup"><span data-stu-id="af042-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="af042-138">Et problem, der havde indflydelse på numeriske felter på detaljesiden, er blevet løst.</span><span class="sxs-lookup"><span data-stu-id="af042-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="af042-139">Skærmtastaturet forsvinder ikke længere fra tid til anden på nogle enheder.</span><span class="sxs-lookup"><span data-stu-id="af042-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="af042-140">Flere forskellige problemer med brugergrænsefladen, for eksempel fejl, der havde indflydelse på baggrundsfarven og positionen, er løst.</span><span class="sxs-lookup"><span data-stu-id="af042-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="af042-141">Den russiske brugergrænseflade er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="af042-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="af042-142">Forskellige problemer, der forårsagede, at systemet ikke længere svarede, er blevet løst.</span><span class="sxs-lookup"><span data-stu-id="af042-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="af042-143">Et problem, der var relateret til genåbningen af regnemaskinen, er blevet løst.</span><span class="sxs-lookup"><span data-stu-id="af042-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="af042-144">**Android-version:** Der er løst et problem, hvor Android 4.4 holdt op med at svare ved start.</span><span class="sxs-lookup"><span data-stu-id="af042-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="af042-145">**Android-version:** Minimumskalering er reduceret til 50 procent.</span><span class="sxs-lookup"><span data-stu-id="af042-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="af042-146">Version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="af042-146">Version 2.0.4.0</span></span>

<span data-ttu-id="af042-147">Version 2.0.4.0 var den første generelt tilgængelige version af Warehouse Management-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="af042-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="af042-148">Nye funktioner, rettelser og forbedringer i version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="af042-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="af042-149">Denne version indeholder følgende nye funktioner, rettelser og forbedringer, som ikke var tilgængelige i forhåndsversionen:</span><span class="sxs-lookup"><span data-stu-id="af042-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="af042-150">Hvis et detaljekort indeholder to etiketter, der har identiske data, skjules den ene af etiketterne.</span><span class="sxs-lookup"><span data-stu-id="af042-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="af042-151">Specialtegn vises nu som standard, og muligheden for at skjule dem er blevet fjernet fra brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="af042-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="af042-152">Deaktiverede send-knapper vises nu som ikke-tilgængelige i håndholdt visning.</span><span class="sxs-lookup"><span data-stu-id="af042-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="af042-153">En ændring i sekvenslogikken for kontroller sikrer en mere problemfri skalering på tværs af enheder.</span><span class="sxs-lookup"><span data-stu-id="af042-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="af042-154">Der er derfor mindre behov for at justere skaleringen af skrifttyper eller knapper.</span><span class="sxs-lookup"><span data-stu-id="af042-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="af042-155">Standardfarvetemaet er ændret til *Mørk*.</span><span class="sxs-lookup"><span data-stu-id="af042-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="af042-156">Det manglende ikon for den deaktiverede send-knap er blevet tilføjet på båndet.</span><span class="sxs-lookup"><span data-stu-id="af042-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="af042-157">Timeoutundtagelser åbner nu forbindelsessiden i stedet for at vise en linjefejl.</span><span class="sxs-lookup"><span data-stu-id="af042-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="af042-158">Hvis der ikke er en tilgængelig send-handling (for eksempel **OK**, **Ja**, **Accepter**, **Udført** eller **Udført**), deaktiveres knappen Send.</span><span class="sxs-lookup"><span data-stu-id="af042-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="af042-159">Appens stabilitet er blevet forbedret.</span><span class="sxs-lookup"><span data-stu-id="af042-159">App stability has been improved.</span></span>
- <span data-ttu-id="af042-160">Der findes en rettelse til sikkerhedsrisikoen [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="af042-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="af042-161">**Windows-version:** Et problem i Windows, hvor menuerne ikke reagerede, efter at størrelsen på vinduet var blevet ændret, er blevet løst.</span><span class="sxs-lookup"><span data-stu-id="af042-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="af042-162">Kendt problem i version 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="af042-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="af042-163">Der findes følgende kendte problem i denne version:</span><span class="sxs-lookup"><span data-stu-id="af042-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="af042-164">Denne version har et problem med enheder, der bruger Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="af042-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="af042-165">Du kan opleve problemer, når du bruger appen på denne version af Android.</span><span class="sxs-lookup"><span data-stu-id="af042-165">You might experience issues when you use the app on this Android version.</span></span>
