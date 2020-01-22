---
title: Konfigurer valgfrie funktioner for et miljø til prøveversion af Commerce
description: I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et miljø til prøveversionen af Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906110"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a><span data-ttu-id="fe05e-103">Konfigurer valgfrie funktioner for et miljø til prøveversion af Commerce</span><span class="sxs-lookup"><span data-stu-id="fe05e-103">Configure optional features for a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fe05e-104">I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et miljø til prøveversionen af Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe05e-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe05e-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="fe05e-105">Prerequisites</span></span>

<span data-ttu-id="fe05e-106">Hvis du vil evaluere transaktionsfunktionerne for mail, skal følgende forudsætninger være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="fe05e-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="fe05e-107">Du har en tilgængelig mailserver (Simple Mail Transfer Protocol \[SMTP\]-server), som kan bruges fra Microsoft Azure-abonnementet, hvor du har klargjort prøveversionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="fe05e-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="fe05e-108">Du har serverens fulde domænenavn (FQDN)/IP-adresse, SMTP-portnummer og godkendelsesdetaljer ved hånden.</span><span class="sxs-lookup"><span data-stu-id="fe05e-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="fe05e-109">Hvis du vil evaluere funktionerne til administration af digitale aktiver ved at inddrage nye omni-kanalbilleder, skal du have navnet på din CMS-lejer (Content Management System) ved hånden.</span><span class="sxs-lookup"><span data-stu-id="fe05e-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="fe05e-110">Der findes en vejledning til at finde dette navn senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="fe05e-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="fe05e-111">>>>(Q: hvor er instruktionerne?)</span><span class="sxs-lookup"><span data-stu-id="fe05e-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="fe05e-112">Konfigurer backend-billedet</span><span class="sxs-lookup"><span data-stu-id="fe05e-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="fe05e-113">Find din URL-basisadresse til dit medie</span><span class="sxs-lookup"><span data-stu-id="fe05e-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="fe05e-114">Før du kan fuldføre denne procedure, skal du udføre trinnene i [Konfigurer dit websted i Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="fe05e-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="fe05e-115">Log på værktøjet til administration af Commerce-webstedet ved hjælp af den webadresse, du har noteret ned, da du initialiserede e-Commerce under klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="fe05e-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="fe05e-116">Åbn webstedet **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="fe05e-117">Vælg **Aktiver** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="fe05e-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="fe05e-118">Vælg et enkelt billedaktiv.</span><span class="sxs-lookup"><span data-stu-id="fe05e-118">Select any single image asset.</span></span>
1. <span data-ttu-id="fe05e-119">Find egenskaben **Offentlig URL-adresse** i egenskabsfremviseren til højre.</span><span class="sxs-lookup"><span data-stu-id="fe05e-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="fe05e-120">Værdien er en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="fe05e-120">The value is a URL.</span></span> <span data-ttu-id="fe05e-121">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="fe05e-121">Here is an example:</span></span>

    <span data-ttu-id="fe05e-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="fe05e-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="fe05e-123">Erstat den sidste identifikator i URL-adressen (**MA1nQC** i det foregående eksempel) med følgende streng **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="fe05e-124">Eksempel-URL-adressen ser således ud, når denne ændring er foretaget:</span><span class="sxs-lookup"><span data-stu-id="fe05e-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="fe05e-125">Denne URL-adresse er URL-basisadressen til dit medie.</span><span class="sxs-lookup"><span data-stu-id="fe05e-125">This URL is your media base URL.</span></span> <span data-ttu-id="fe05e-126">Notér det.</span><span class="sxs-lookup"><span data-stu-id="fe05e-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="fe05e-127">Opdater URL-basisadressen til mediet</span><span class="sxs-lookup"><span data-stu-id="fe05e-127">Update the media base URL</span></span>

1. <span data-ttu-id="fe05e-128">Log på Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="fe05e-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="fe05e-129">anvend menuen til venstre for at gå til **Moduler \> Retail \> Konfiguration af kanal \> Kanalprofiler**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="fe05e-130">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-130">Select **Edit**.</span></span>
1. <span data-ttu-id="fe05e-131">Under **Profilegenskaber** skal du erstatte egenskabsværdien for **URL-basisadressen til medieserveren** med den URL-basisadresse til medie, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="fe05e-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="fe05e-132">Vælg den anden kanal på listen til venstre under **Standard**-kanal.</span><span class="sxs-lookup"><span data-stu-id="fe05e-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="fe05e-133">Under **Profilegenskaber** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="fe05e-134">For den egenskab, der blev tilføjet, skal du vælge **URL-basisadresse til medieserver** som egenskabsnøglen.</span><span class="sxs-lookup"><span data-stu-id="fe05e-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="fe05e-135">Angiv som egenskabsværdi den URL-basisadresse til mediet, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="fe05e-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="fe05e-136">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="fe05e-137">Konfigurer mailserveren</span><span class="sxs-lookup"><span data-stu-id="fe05e-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="fe05e-138">SMTP-serveren eller mailtjenesten, du angiver her, skal være tilgængelig fra det Azure-abonnement, som du bruger til miljøet.</span><span class="sxs-lookup"><span data-stu-id="fe05e-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="fe05e-139">Log på Retail.</span><span class="sxs-lookup"><span data-stu-id="fe05e-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="fe05e-140">Brug menuen til venstre for at gå til **Moduler \> Systemadministration \> Konfiguration \> E-mail \> E-mailparametre**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="fe05e-141">På fanen **SMTP-indstillinger** i feltet **Udgående mailserver** skal du indtaste FQDN- eller IP-adressen på din SMTP-server eller e-mailtjeneste.</span><span class="sxs-lookup"><span data-stu-id="fe05e-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="fe05e-142">I feltet **SMTP-portnummer** skal du indtaste portnummeret.</span><span class="sxs-lookup"><span data-stu-id="fe05e-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="fe05e-143">(Hvis du ikke bruger SSL-certifikater (Secure Sockets Layer) \[SSL\], er standardportnummeret **25**.)</span><span class="sxs-lookup"><span data-stu-id="fe05e-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="fe05e-144">Hvis der kræves godkendelse, skal du angive værdier i felterne **Brugernavn** og **Adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="fe05e-145">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-145">Select **Save**.</span></span>
1. <span data-ttu-id="fe05e-146">Vælg **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="fe05e-147">På fanen **Test e-mail** i feltet **E-mailudbyder** skal du vælge **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="fe05e-148">Angiv den mailadresse, som testmailen skal leveres til, i feltet **Send til**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="fe05e-149">Vælg **Send testmail**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="fe05e-150">Konfigurer mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="fe05e-150">Configure email templates</span></span>

<span data-ttu-id="fe05e-151">For hver transaktionshændelse, du vil sende mails for, skal du opdatere mailskabelonen med en gyldig afsendermailadresse.</span><span class="sxs-lookup"><span data-stu-id="fe05e-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="fe05e-152">Log på Retail.</span><span class="sxs-lookup"><span data-stu-id="fe05e-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="fe05e-153">Brug menuen til venstre for at gå til **Moduler \> Organisationsadministration \> Konfiguration \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="fe05e-154">Vælg **Vis liste**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-154">Select **Show list**.</span></span>
1. <span data-ttu-id="fe05e-155">Benyt følgende fremgangsmåde for hver skabelon på listen:</span><span class="sxs-lookup"><span data-stu-id="fe05e-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="fe05e-156">I feltet **Afsenders e-mailadresse** skal du angive afsenderens e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="fe05e-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="fe05e-157">Valgfrit: I feltet **Afsenders navn** skal du indtaste det navn, der skal bruges som afsendernavnet.</span><span class="sxs-lookup"><span data-stu-id="fe05e-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="fe05e-158">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="fe05e-159">Tilpas mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="fe05e-159">Customize email templates</span></span>

<span data-ttu-id="fe05e-160">Du ønsker måske at tilpasse e-mail-skabelonerne, så de bruger forskellige billeder.</span><span class="sxs-lookup"><span data-stu-id="fe05e-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="fe05e-161">Du kan også opdatere links i skabelonerne, så de fører til dit prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="fe05e-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="fe05e-162">Denne procedure beskriver, hvordan du henter standardskabelonerne, tilpasser dem og opdaterer skabelonerne i systemet.</span><span class="sxs-lookup"><span data-stu-id="fe05e-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="fe05e-163">I en browser kan du downloade [Microsoft Dynamics 365 Commerce-prøveversionens .zip-fil med standardmailskabeloner](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="fe05e-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="fe05e-164">Denne fil indeholder følgende HTML-dokumenter:</span><span class="sxs-lookup"><span data-stu-id="fe05e-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="fe05e-165">Skabelon til ordrebekræftelse</span><span class="sxs-lookup"><span data-stu-id="fe05e-165">Order confirmation template</span></span>
    - <span data-ttu-id="fe05e-166">Skabelon til udstedelse af gavekort</span><span class="sxs-lookup"><span data-stu-id="fe05e-166">Issue gift card template</span></span>
    - <span data-ttu-id="fe05e-167">Skabelon til ny ordre</span><span class="sxs-lookup"><span data-stu-id="fe05e-167">New order template</span></span>
    - <span data-ttu-id="fe05e-168">Skabelon til pakkeordre</span><span class="sxs-lookup"><span data-stu-id="fe05e-168">Pack order template</span></span>
    - <span data-ttu-id="fe05e-169">Skabelon til plukordre</span><span class="sxs-lookup"><span data-stu-id="fe05e-169">Pick order template</span></span>

1. <span data-ttu-id="fe05e-170">Tilpas skabelonerne ved hjælp af en tekst- eller HTML-editor.</span><span class="sxs-lookup"><span data-stu-id="fe05e-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="fe05e-171">Se listen over [understøttede tokens](#supported-tokens-in-the-email-template) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="fe05e-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="fe05e-172">Log på Retail.</span><span class="sxs-lookup"><span data-stu-id="fe05e-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="fe05e-173">Brug menuen til venstre for at gå til **Moduler \> Organisationsadministration \> Konfiguration \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="fe05e-174">Udvid listen til venstre for at få vist alle skabelonerne.</span><span class="sxs-lookup"><span data-stu-id="fe05e-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="fe05e-175">Følg disse trin for hver skabelon, du vil tilpasse:</span><span class="sxs-lookup"><span data-stu-id="fe05e-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="fe05e-176">Vælg skabelonen på listen.</span><span class="sxs-lookup"><span data-stu-id="fe05e-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="fe05e-177">Vælg den relevante sprogversion på listen under **E-mailbeskedens indhold**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="fe05e-178">(Standardsproget er **da-dk**.)</span><span class="sxs-lookup"><span data-stu-id="fe05e-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="fe05e-179">Under **E-mailbeskedens indhold** skal du vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="fe05e-180">Ruden **Overfør mailskabelon** vises.</span><span class="sxs-lookup"><span data-stu-id="fe05e-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="fe05e-181">Vælg **Gennemse**, og find den HTML-fil, der har det tilpassede indhold.</span><span class="sxs-lookup"><span data-stu-id="fe05e-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="fe05e-182">Vælg **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-182">Select **Upload**.</span></span> <span data-ttu-id="fe05e-183">Skabelonen overføres til systemet, og der vises et eksempel.</span><span class="sxs-lookup"><span data-stu-id="fe05e-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="fe05e-184">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-184">Select **OK**.</span></span>
    1. <span data-ttu-id="fe05e-185">Valgfrit: Tilpas egenskaben **Emne** for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="fe05e-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="fe05e-186">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="fe05e-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="fe05e-187">Understøttede tokens i mailskabelonen</span><span class="sxs-lookup"><span data-stu-id="fe05e-187">Supported tokens in the email template</span></span>

<span data-ttu-id="fe05e-188">Når e-mail er gengivet, vil disse tokens blive erstattet af de faktiske værdier, der gælder for kunden og kundens ordre.</span><span class="sxs-lookup"><span data-stu-id="fe05e-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="fe05e-189">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="fe05e-189">Sales order</span></span>

<span data-ttu-id="fe05e-190">Følgende tokens gælder for den overordnede salgsordre.</span><span class="sxs-lookup"><span data-stu-id="fe05e-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="fe05e-191">Navn på token</span><span class="sxs-lookup"><span data-stu-id="fe05e-191">Name of the token</span></span> | <span data-ttu-id="fe05e-192">Tokenet</span><span class="sxs-lookup"><span data-stu-id="fe05e-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="fe05e-193">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="fe05e-193">Order number</span></span>      | <span data-ttu-id="fe05e-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="fe05e-194">%salesid%</span></span> |
| <span data-ttu-id="fe05e-195">Debitors navn</span><span class="sxs-lookup"><span data-stu-id="fe05e-195">Customer's name</span></span>   | <span data-ttu-id="fe05e-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="fe05e-196">%customername%</span></span> |
| <span data-ttu-id="fe05e-197">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="fe05e-197">Delivery address</span></span>  | <span data-ttu-id="fe05e-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="fe05e-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="fe05e-199">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="fe05e-199">Billing address</span></span>   | <span data-ttu-id="fe05e-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="fe05e-200">%customeraddress%</span></span> |
| <span data-ttu-id="fe05e-201">Bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="fe05e-201">Order date</span></span>        | <span data-ttu-id="fe05e-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="fe05e-202">%shipdate%</span></span> |
| <span data-ttu-id="fe05e-203">Leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="fe05e-203">Delivery mode</span></span>     | <span data-ttu-id="fe05e-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="fe05e-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="fe05e-205">Diskontering</span><span class="sxs-lookup"><span data-stu-id="fe05e-205">Discount</span></span>          | <span data-ttu-id="fe05e-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="fe05e-206">%discount%</span></span> |
| <span data-ttu-id="fe05e-207">Moms</span><span class="sxs-lookup"><span data-stu-id="fe05e-207">Sales tax</span></span>         | <span data-ttu-id="fe05e-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="fe05e-208">%tax%</span></span> |
| <span data-ttu-id="fe05e-209">Ordretotal</span><span class="sxs-lookup"><span data-stu-id="fe05e-209">Order total</span></span>       | <span data-ttu-id="fe05e-210">%total%</span><span class="sxs-lookup"><span data-stu-id="fe05e-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="fe05e-211">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="fe05e-211">Sales line</span></span>

<span data-ttu-id="fe05e-212">For hvert produkt i ordren erstattes følgende tokens med værdier.</span><span class="sxs-lookup"><span data-stu-id="fe05e-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="fe05e-213">Placer token for **Produktlisten - start** i begyndelsen af den HTML-blok, der gentages for hvert produkt, og placer token for **Produktliste - slut** i slutningen af blokken.</span><span class="sxs-lookup"><span data-stu-id="fe05e-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="fe05e-214">Navn på token</span><span class="sxs-lookup"><span data-stu-id="fe05e-214">Name of the token</span></span>      | <span data-ttu-id="fe05e-215">Tokenet</span><span class="sxs-lookup"><span data-stu-id="fe05e-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="fe05e-216">Produktliste - start</span><span class="sxs-lookup"><span data-stu-id="fe05e-216">Product list - start</span></span>   | <span data-ttu-id="fe05e-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="fe05e-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="fe05e-218">Produktliste - slut</span><span class="sxs-lookup"><span data-stu-id="fe05e-218">Product list - end</span></span>     | <span data-ttu-id="fe05e-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="fe05e-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="fe05e-220">Produktnavn</span><span class="sxs-lookup"><span data-stu-id="fe05e-220">Product name</span></span>           | <span data-ttu-id="fe05e-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="fe05e-221">%lineproductname%</span></span> |
| <span data-ttu-id="fe05e-222">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fe05e-222">Description</span></span>            | <span data-ttu-id="fe05e-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="fe05e-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="fe05e-224">Mængde</span><span class="sxs-lookup"><span data-stu-id="fe05e-224">Quantity</span></span>               | <span data-ttu-id="fe05e-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="fe05e-225">%linequantity%</span></span> |
| <span data-ttu-id="fe05e-226">Linjeprisenhed</span><span class="sxs-lookup"><span data-stu-id="fe05e-226">Line unit price</span></span>        | <span data-ttu-id="fe05e-227">%lineprice% (verify)</span><span class="sxs-lookup"><span data-stu-id="fe05e-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="fe05e-228">linjevaretotal</span><span class="sxs-lookup"><span data-stu-id="fe05e-228">line item total</span></span>        | <span data-ttu-id="fe05e-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="fe05e-229">%linenetamount%</span></span> |
| <span data-ttu-id="fe05e-230">linjerabat</span><span class="sxs-lookup"><span data-stu-id="fe05e-230">line discount</span></span>          | <span data-ttu-id="fe05e-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="fe05e-231">%linediscount%</span></span> |
| <span data-ttu-id="fe05e-232">Afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="fe05e-232">Ship date</span></span>              | <span data-ttu-id="fe05e-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="fe05e-233">%lineshipdate%</span></span> |
| <span data-ttu-id="fe05e-234">Indkøbsmetode</span><span class="sxs-lookup"><span data-stu-id="fe05e-234">Procurement method</span></span>     | <span data-ttu-id="fe05e-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="fe05e-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="fe05e-236">leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="fe05e-236">delivery address</span></span>       | <span data-ttu-id="fe05e-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="fe05e-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="fe05e-238">Salgsenhed for linjen</span><span class="sxs-lookup"><span data-stu-id="fe05e-238">Sales unit of the line</span></span> | <span data-ttu-id="fe05e-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="fe05e-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="fe05e-240">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="fe05e-240">Additional resources</span></span>

[<span data-ttu-id="fe05e-241">Oversigt over miljø til prøveversion af Commerce</span><span class="sxs-lookup"><span data-stu-id="fe05e-241">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="fe05e-242">Klargøring af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="fe05e-242">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="fe05e-243">Konfigurering af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="fe05e-243">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="fe05e-244">Ofte stillede spørgsmål om Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="fe05e-244">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="fe05e-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="fe05e-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="fe05e-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="fe05e-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="fe05e-247">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="fe05e-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="fe05e-248">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="fe05e-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="fe05e-249">Hjælp-ressourcer til Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="fe05e-249">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
