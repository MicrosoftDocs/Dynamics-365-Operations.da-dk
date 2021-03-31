---
title: Arbejd med CSS-tilsidesættelsesfiler
description: Dette emne indeholder en beskrivelse af hvorfor, hvornår og hvordan du bruger CSS-tilsidesættelsesfiler (Cascading Style Sheets) i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 41fb0be51f7af25faba1b860319aea84ae7a8b56
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207793"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="e7d44-103">Arbejde med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="e7d44-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e7d44-104">Dette emne indeholder en beskrivelse af hvorfor, hvornår og hvordan du bruger CSS-tilsidesættelsesfiler (Cascading Style Sheets) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7d44-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7d44-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="e7d44-105">Overview</span></span>

<span data-ttu-id="e7d44-106">Permanente webstedstypografier skal normalt håndteres via et websteds tema.</span><span class="sxs-lookup"><span data-stu-id="e7d44-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="e7d44-107">Temaerne indeholder de grundlæggende indstillinger for CSS og typografi, der er gældende for modulerne på siderne på dit websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="e7d44-108">Temaer oprettes ved hjælp af det online SDK (Software Development Kit) til Dynamics 365 Commerce, og implementeres på dine websteder via Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e7d44-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e7d44-109">Temafejlfindingsfunktioner og modulgrænsefladekonfigurationer i SDK hjælper webstedsudviklere med at oprette tilpassede og sammenhængende webstedsdesignpakker.</span><span class="sxs-lookup"><span data-stu-id="e7d44-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="e7d44-110">Når disse designpakker installeres på et websted, kan webstedsforfatterne fokusere på at oprette, redigere og udgive indhold i stedet for at udvikle webstederne.</span><span class="sxs-lookup"><span data-stu-id="e7d44-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="e7d44-111">Som følge af et temas sædvanlige livscyklus kan afhængigheden af udviklere til at foretage typografiændringer ved hjælp af SDK- og LCS-installationspipeline være uoverkommelig i nogle scenarier.</span><span class="sxs-lookup"><span data-stu-id="e7d44-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="e7d44-112">Webstedsprototyper eller hotfixes kan virke besværlige, hvis SDK'et ikke er konfigureret, eller hvis du ikke har tid til at vente på en LCS-installation.</span><span class="sxs-lookup"><span data-stu-id="e7d44-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="e7d44-113">I disse scenarier kan CSS-tilsidesættelsesfiler hjælpe.</span><span class="sxs-lookup"><span data-stu-id="e7d44-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="e7d44-114">I Commerce-oprettelsesværktøjerne kan godkendte brugere uploade en CSS-fil, få den vist og derefter aktivere den for at tilsidesætte et websteds tema.</span><span class="sxs-lookup"><span data-stu-id="e7d44-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="e7d44-115">Der er ikke behov for overordnet installation af SDK eller LCS.</span><span class="sxs-lookup"><span data-stu-id="e7d44-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="e7d44-116">De tilsidesættelser, der er angivet i en CSS-tilsidesættelsesfil, kan være lige så små som en ændring af en enkelt teksttypografi eller så omfattende som et fuldstændigt eftersyn af varemærket.</span><span class="sxs-lookup"><span data-stu-id="e7d44-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="e7d44-117">Før du bruger CSS-tilsidesættelsesfiler, skal du være opmærksom på følgende begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="e7d44-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="e7d44-118">Der kan kun aktiveres én CSS-tilsidesættelsesfil på et websted ad gangen.</span><span class="sxs-lookup"><span data-stu-id="e7d44-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="e7d44-119">Alle aktive tilsidesættelser skal derfor være indeholdt i en enkelt tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="e7d44-120">Selvom du kan få vist tilsidesættelser i Commerce-oprettelsesværktøjerne, er der ingen dedikerede fejlfindingsfunktioner, som kan hjælpe med at identificere eventuelle fejl, som skyldes tilsidesættelserne.</span><span class="sxs-lookup"><span data-stu-id="e7d44-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="e7d44-121">Når du bruger CSS-tilsidesættelsesfiler har du med andre ord ikke det samme værktøjsæt, som SDK indeholder til validering af moduler og oprettelse.</span><span class="sxs-lookup"><span data-stu-id="e7d44-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="e7d44-122">Ikke desto mindre giver CSS-tilsidesættelsesfiler dig en hurtig måde, hvorpå du kan prototype et design eller implementere et hotfix, før der udvikles og implementeres en fuldstændig temaopdatering.</span><span class="sxs-lookup"><span data-stu-id="e7d44-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="e7d44-123">Opret en CSS-tilsidesættelsesfil</span><span class="sxs-lookup"><span data-stu-id="e7d44-123">Create a CSS override file</span></span>

<span data-ttu-id="e7d44-124">Du kan bruge et hvilket som helst IDE (integreret udviklingsmiljø), teksteditor eller kildekodeeditor til at oprette en CSS-tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="e7d44-125">En typisk fremgangsmåde er at bruge din browsers standard webfejlfindingsprogram til at identificere typografivælgere, egenskaber og værdier på dit eksisterende websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="e7d44-126">De fleste browsere giver dig mulighed for at ændre værdier og få vist dem i fejlfindingsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="e7d44-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="e7d44-127">Når du har identificeret de ændringer, du vil foretage, kan du gemme dem i din egen CSS-fil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="e7d44-128">Overfør en CSS-tilsidesættelsesfil</span><span class="sxs-lookup"><span data-stu-id="e7d44-128">Upload a CSS override file</span></span>

<span data-ttu-id="e7d44-129">Følg disse trin for at overføre en CSS-fil til dit websted i Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7d44-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e7d44-130">Gå til dit websted i oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="e7d44-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="e7d44-131">Vælg **Design** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="e7d44-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7d44-132">Afhængigt af versionen af de Commerce-oprettelsesværktøjer du bruger, skal du muligvis udvide **Indstillingerne** i navigationsruden, før du kan vælge **Design**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="e7d44-133">Øverst i den primære designrude skal du vælge fanen **CSS-tilsidesættelse**, hvis den ikke allerede er valgt.</span><span class="sxs-lookup"><span data-stu-id="e7d44-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="e7d44-134">Vælg **Tilgængelige CSS-tilsidesættelser** skal du vælge **Overfør CSS-fil**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="e7d44-135">Der vises et Stifinder-vindue.</span><span class="sxs-lookup"><span data-stu-id="e7d44-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="e7d44-136">Søg i Stifinder, og vælg en CSS-fil, og vælg dernæst **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="e7d44-137">Den overførte CSS-fil vises nu under **Tilgængelige CSS-tilsidesættelse**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="e7d44-138">Få vist en CSS-tilsidesættelsesfil</span><span class="sxs-lookup"><span data-stu-id="e7d44-138">Preview a CSS override file</span></span>

<span data-ttu-id="e7d44-139">Følg disse trin for at få vist en CSS-tilsidesættelsesfil, før du gør den aktiv på dit aktive websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="e7d44-140">I navigationsruden til venstre skal du vælge **Design** og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil have vist.</span><span class="sxs-lookup"><span data-stu-id="e7d44-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="e7d44-141">Ud for CSS-filnavnet skal du vælge **Vis websted**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="e7d44-142">I dialogboksen **Vælg en URL-adresse** skal du vælge URL-adressen for det websted, hvorpå du ønsker at se den anvendte tilsidesættelse, og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="e7d44-143">Hvis der er flere varianter for den valgte URL-adresse, skal du vælge den ønskede variant i den viste dialogboks **Se variationer**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="e7d44-144">En ny browserfane eller et nyt vindue åbnes, hvor du kan validere dine typografitilsidesættelser mod dit websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="e7d44-145">Du kan derefter dele URL-adressen med andre godkendte Commerce-brugere til gennemsyn og feedback.</span><span class="sxs-lookup"><span data-stu-id="e7d44-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="e7d44-146">Aktivér en CSS-tilsidesættelsesfil på dit aktive websted</span><span class="sxs-lookup"><span data-stu-id="e7d44-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="e7d44-147">Når du har set og godkendt CSS-tilsidesættelsesfilen, kan du aktivere den på dit aktive websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="e7d44-148">Der kan kun aktiveres én CSS-tilsidesættelsesfil på dit websted ad gangen.</span><span class="sxs-lookup"><span data-stu-id="e7d44-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="e7d44-149">Hvis du aktiverer en ny tilsidesættelsesfil, deaktiveres den forrige tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="e7d44-150">Sørg derfor for, at alle påkrævede tilsidesættelser findes i en enkelt CSS-tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="e7d44-151">Følg disse trin for at aktivere en CSS-tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="e7d44-152">I navigationsruden til venstre skal du vælge **Design** og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil aktivere.</span><span class="sxs-lookup"><span data-stu-id="e7d44-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="e7d44-153">Under CSS-filnavnet skal du vælge **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="e7d44-154">Tilsidesættelsesfilen bliver straks aktiveret på dit aktive websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="e7d44-155">Deaktivér en CSS-tilsidesættelsesfil på dit aktive websted</span><span class="sxs-lookup"><span data-stu-id="e7d44-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="e7d44-156">Følg disse trin for at deaktivere en CSS-tilsidesættelsesfil på dit websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="e7d44-157">I navigationsruden til venstre skal du vælge **Design** og derefter på fanen **CSS-tilsidesættelse** under **Tilgængelige CSS-tilsidesættelser** finde den CSS-fil, du vil deaktivere.</span><span class="sxs-lookup"><span data-stu-id="e7d44-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="e7d44-158">Under CSS-filnavnet skal du vælge **Deaktivér**.</span><span class="sxs-lookup"><span data-stu-id="e7d44-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="e7d44-159">Tilsidesættelsesfilen bliver straks deaktiveret på dit aktive websted.</span><span class="sxs-lookup"><span data-stu-id="e7d44-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="e7d44-160">Hvis du vil tilgå yderligere indstillinger for CSS-tilsidesættelsesfiler, skal du vælge ellipsen (**...**) ud for CSS-filnavnet.</span><span class="sxs-lookup"><span data-stu-id="e7d44-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="e7d44-161">Indstillingerne **Download**, **Omdøb** og **Erstat** er nyttige til hurtige ændringer af en eksisterende CSS-tilsidesættelsesfil.</span><span class="sxs-lookup"><span data-stu-id="e7d44-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7d44-162">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e7d44-162">Additional resources</span></span>

[<span data-ttu-id="e7d44-163">Tilføje et logo</span><span class="sxs-lookup"><span data-stu-id="e7d44-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e7d44-164">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="e7d44-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e7d44-165">Arbejde med forudindstillinger for typografier</span><span class="sxs-lookup"><span data-stu-id="e7d44-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="e7d44-166">Tilføje en favicon</span><span class="sxs-lookup"><span data-stu-id="e7d44-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e7d44-167">Tilføje en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="e7d44-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e7d44-168">Tilføje en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="e7d44-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e7d44-169">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="e7d44-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e7d44-170">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="e7d44-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]