---
title: Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410975"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8d9c3-103">Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d9c3-104">I dette emne beskrives det, hvordan du konfigurerer valgfrie funktioner for et Microsoft Dynamics 365 Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d9c3-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="8d9c3-105">Prerequisites</span></span>

<span data-ttu-id="8d9c3-106">Hvis du vil evaluere transaktionsfunktionerne for mail, skal følgende forudsætninger være opfyldt:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="8d9c3-107">Du har en tilgængelig mailserver (Simple Mail Transfer Protocol \[SMTP\]-server), som kan bruges fra Microsoft Azure-abonnementet, hvor du har klargjort evalueringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="8d9c3-108">Du har serverens fulde domænenavn (FQDN)/IP-adresse, SMTP-portnummer og godkendelsesdetaljer ved hånden.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="8d9c3-109">Konfigurer backend-billedet</span><span class="sxs-lookup"><span data-stu-id="8d9c3-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="8d9c3-110">Find din URL-basisadresse til dit medie</span><span class="sxs-lookup"><span data-stu-id="8d9c3-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="8d9c3-111">Før du kan fuldføre denne procedure, skal du udføre trinnene i [Konfigurer dit websted i Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="8d9c3-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="8d9c3-112">Log på Commerce-webstedsgenerator ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="8d9c3-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="8d9c3-113">Åbn webstedet **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="8d9c3-114">Vælg **Mediebibliotek** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="8d9c3-115">Vælg et enkelt billedaktiv.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-115">Select any single image asset.</span></span>
1. <span data-ttu-id="8d9c3-116">Find egenskaben **Offentlig URL-adresse** i egenskabsfremviseren til højre.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="8d9c3-117">Værdien er en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-117">The value is a URL.</span></span> <span data-ttu-id="8d9c3-118">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-118">Here is an example:</span></span>

    <span data-ttu-id="8d9c3-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="8d9c3-120">Erstat den sidste identifikator i URL-adressen (**MA1nQC** i det foregående eksempel) med følgende streng **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="8d9c3-121">Eksempel-URL-adressen ser således ud, når denne ændring er foretaget:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="8d9c3-122">Denne URL-adresse er URL-basisadressen til dit medie.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-122">This URL is your media base URL.</span></span> <span data-ttu-id="8d9c3-123">Notér det.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="8d9c3-124">Opdater URL-basisadressen til mediet</span><span class="sxs-lookup"><span data-stu-id="8d9c3-124">Update the media base URL</span></span>

1. <span data-ttu-id="8d9c3-125">Log på Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8d9c3-126">Anvend menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af kanal \> Kanalprofiler**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="8d9c3-127">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-127">Select **Edit**.</span></span>
1. <span data-ttu-id="8d9c3-128">Under **Profilegenskaber** skal du erstatte egenskabsværdien for **URL-basisadressen til medieserveren** med den URL-basisadresse til medie, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="8d9c3-129">Vælg den kanal, der hedder **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="8d9c3-130">Under **Profilegenskaber** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="8d9c3-131">For den egenskab, der blev tilføjet, skal du vælge **URL-basisadresse til medieserver** som egenskabsnøglen.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="8d9c3-132">Angiv som egenskabsværdi den URL-basisadresse til mediet, som du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="8d9c3-133">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="8d9c3-134">Konfigurer og test mailserveren</span><span class="sxs-lookup"><span data-stu-id="8d9c3-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="8d9c3-135">SMTP-serveren eller mailtjenesten, du angiver her, skal være tilgængelig fra det Azure-abonnement, som du bruger til miljøet.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="8d9c3-136">Log på Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8d9c3-137">Brug menuen til venstre, og gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> E-mailparametre**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="8d9c3-138">På fanen **SMTP-indstillinger** i feltet **Udgående mailserver** skal du indtaste FQDN- eller IP-adressen på din SMTP-server eller e-mailtjeneste.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="8d9c3-139">I feltet **SMTP-portnummer** skal du indtaste portnummeret.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="8d9c3-140">(Hvis du ikke bruger SSL-certifikater (Secure Sockets Layer) \[SSL\], er standardportnummeret **25**.)</span><span class="sxs-lookup"><span data-stu-id="8d9c3-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="8d9c3-141">Hvis der kræves godkendelse, skal du angive værdier i felterne **Brugernavn** og **Adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="8d9c3-142">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-142">Select **Save**.</span></span>
1. <span data-ttu-id="8d9c3-143">Vælg **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="8d9c3-144">På fanen **Test e-mail** i feltet **E-mailudbyder** skal du vælge **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="8d9c3-145">Angiv den mailadresse, som testmailen skal leveres til, i feltet **Send til**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="8d9c3-146">Vælg **Send testmail**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="8d9c3-147">Konfigurer mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="8d9c3-147">Configure email templates</span></span>

<span data-ttu-id="8d9c3-148">For hver transaktionshændelse, du vil sende mails for, skal du opdatere mailskabelonen med en gyldig afsendermailadresse.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="8d9c3-149">Log på Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="8d9c3-150">Brug menuen til venstre, og gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabeloner til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="8d9c3-151">Vælg **Vis liste**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-151">Select **Show list**.</span></span>
1. <span data-ttu-id="8d9c3-152">Benyt følgende fremgangsmåde for hver skabelon på listen:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="8d9c3-153">I feltet **Afsenders e-mailadresse** skal du angive afsenderens e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="8d9c3-154">Valgfrit: I feltet **Afsenders navn** skal du indtaste det navn, der skal bruges som afsendernavnet.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="8d9c3-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="8d9c3-156">Tilpas mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="8d9c3-156">Customize email templates</span></span>

<span data-ttu-id="8d9c3-157">Du ønsker måske at tilpasse e-mail-skabelonerne, så de bruger forskellige billeder.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="8d9c3-158">Du kan også opdatere links i skabelonerne, så de fører til dit evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="8d9c3-159">Denne procedure beskriver, hvordan du henter standardskabelonerne, tilpasser dem og opdaterer skabelonerne i systemet.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="8d9c3-160">I en browser kan du downloade [Microsoft Dynamics 365 Commerce-evalueringens .zip-fil med standardmailskabeloner](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) til din lokale computer.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="8d9c3-161">Denne fil indeholder følgende HTML-dokumenter:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="8d9c3-162">Skabelon til ordrebekræftelse</span><span class="sxs-lookup"><span data-stu-id="8d9c3-162">Order confirmation template</span></span>
    - <span data-ttu-id="8d9c3-163">Skabelon til udstedelse af gavekort</span><span class="sxs-lookup"><span data-stu-id="8d9c3-163">Issue gift card template</span></span>
    - <span data-ttu-id="8d9c3-164">Skabelon til ny ordre</span><span class="sxs-lookup"><span data-stu-id="8d9c3-164">New order template</span></span>
    - <span data-ttu-id="8d9c3-165">Skabelon til pakkeordre</span><span class="sxs-lookup"><span data-stu-id="8d9c3-165">Pack order template</span></span>
    - <span data-ttu-id="8d9c3-166">Skabelon til plukordre</span><span class="sxs-lookup"><span data-stu-id="8d9c3-166">Pick order template</span></span>

1. <span data-ttu-id="8d9c3-167">Tilpas skabelonerne ved hjælp af en tekst- eller HTML-editor.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="8d9c3-168">Se listen over [understøttede tokens](#supported-tokens-in-the-email-template) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="8d9c3-169">Log på Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="8d9c3-170">Brug menuen til venstre for at gå til **Moduler \> Organisationsadministration \> Konfiguration \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="8d9c3-171">Udvid listen til venstre for at få vist alle skabelonerne.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="8d9c3-172">Følg disse trin for hver skabelon, du vil tilpasse:</span><span class="sxs-lookup"><span data-stu-id="8d9c3-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="8d9c3-173">Vælg skabelonen på listen.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="8d9c3-174">Vælg den relevante sprogversion på listen under **E-mailbeskedens indhold**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="8d9c3-175">(Standardsproget er **da-dk**.)</span><span class="sxs-lookup"><span data-stu-id="8d9c3-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="8d9c3-176">Under **E-mailbeskedens indhold** skal du vælge **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="8d9c3-177">Ruden **Overfør mailskabelon** vises.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="8d9c3-178">Vælg **Gennemse**, og find den HTML-fil, der har det tilpassede indhold.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="8d9c3-179">Vælg **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-179">Select **Upload**.</span></span> <span data-ttu-id="8d9c3-180">Skabelonen overføres til systemet, og der vises et eksempel.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="8d9c3-181">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-181">Select **OK**.</span></span>
    1. <span data-ttu-id="8d9c3-182">Valgfrit: Tilpas egenskaben **Emne** for skabelonen.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="8d9c3-183">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="8d9c3-184">Understøttede tokens i mailskabelonen</span><span class="sxs-lookup"><span data-stu-id="8d9c3-184">Supported tokens in the email template</span></span>

<span data-ttu-id="8d9c3-185">Når e-mail er gengivet, vil disse tokens blive erstattet af de faktiske værdier, der gælder for kunden og kundens ordre.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="8d9c3-186">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="8d9c3-186">Sales order</span></span>

<span data-ttu-id="8d9c3-187">Følgende tokens gælder for den overordnede salgsordre.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="8d9c3-188">Navn på token</span><span class="sxs-lookup"><span data-stu-id="8d9c3-188">Name of the token</span></span> | <span data-ttu-id="8d9c3-189">Tokenet</span><span class="sxs-lookup"><span data-stu-id="8d9c3-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="8d9c3-190">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="8d9c3-190">Order number</span></span>      | <span data-ttu-id="8d9c3-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-191">%salesid%</span></span> |
| <span data-ttu-id="8d9c3-192">Debitors navn</span><span class="sxs-lookup"><span data-stu-id="8d9c3-192">Customer's name</span></span>   | <span data-ttu-id="8d9c3-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-193">%customername%</span></span> |
| <span data-ttu-id="8d9c3-194">Leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="8d9c3-194">Delivery address</span></span>  | <span data-ttu-id="8d9c3-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="8d9c3-196">Faktureringsadresse</span><span class="sxs-lookup"><span data-stu-id="8d9c3-196">Billing address</span></span>   | <span data-ttu-id="8d9c3-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-197">%customeraddress%</span></span> |
| <span data-ttu-id="8d9c3-198">Bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="8d9c3-198">Order date</span></span>        | <span data-ttu-id="8d9c3-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-199">%shipdate%</span></span> |
| <span data-ttu-id="8d9c3-200">Leveringstilstand</span><span class="sxs-lookup"><span data-stu-id="8d9c3-200">Delivery mode</span></span>     | <span data-ttu-id="8d9c3-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="8d9c3-202">Diskontering</span><span class="sxs-lookup"><span data-stu-id="8d9c3-202">Discount</span></span>          | <span data-ttu-id="8d9c3-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-203">%discount%</span></span> |
| <span data-ttu-id="8d9c3-204">Moms</span><span class="sxs-lookup"><span data-stu-id="8d9c3-204">Sales tax</span></span>         | <span data-ttu-id="8d9c3-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-205">%tax%</span></span> |
| <span data-ttu-id="8d9c3-206">Ordretotal</span><span class="sxs-lookup"><span data-stu-id="8d9c3-206">Order total</span></span>       | <span data-ttu-id="8d9c3-207">%total%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="8d9c3-208">Salgslinje</span><span class="sxs-lookup"><span data-stu-id="8d9c3-208">Sales line</span></span>

<span data-ttu-id="8d9c3-209">For hvert produkt i ordren erstattes følgende tokens med værdier.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="8d9c3-210">Placer token for **Produktlisten - start** i begyndelsen af den HTML-blok, der gentages for hvert produkt, og placer token for **Produktliste - slut** i slutningen af blokken.</span><span class="sxs-lookup"><span data-stu-id="8d9c3-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="8d9c3-211">Navn på token</span><span class="sxs-lookup"><span data-stu-id="8d9c3-211">Name of the token</span></span>      | <span data-ttu-id="8d9c3-212">Token</span><span class="sxs-lookup"><span data-stu-id="8d9c3-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="8d9c3-213">Produktliste - start</span><span class="sxs-lookup"><span data-stu-id="8d9c3-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="8d9c3-214">Produktliste - slut</span><span class="sxs-lookup"><span data-stu-id="8d9c3-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="8d9c3-215">Produktnavn</span><span class="sxs-lookup"><span data-stu-id="8d9c3-215">Product name</span></span>           | <span data-ttu-id="8d9c3-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-216">%lineproductname%</span></span> |
| <span data-ttu-id="8d9c3-217">Beskrivende tekst</span><span class="sxs-lookup"><span data-stu-id="8d9c3-217">Description</span></span>            | <span data-ttu-id="8d9c3-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="8d9c3-219">Mængde</span><span class="sxs-lookup"><span data-stu-id="8d9c3-219">Quantity</span></span>               | <span data-ttu-id="8d9c3-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-220">%linequantity%</span></span> |
| <span data-ttu-id="8d9c3-221">Linjeprisenhed</span><span class="sxs-lookup"><span data-stu-id="8d9c3-221">Line unit price</span></span>        | <span data-ttu-id="8d9c3-222">%lineprice% (verify)</span><span class="sxs-lookup"><span data-stu-id="8d9c3-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="8d9c3-223">linjevaretotal</span><span class="sxs-lookup"><span data-stu-id="8d9c3-223">line item total</span></span>        | <span data-ttu-id="8d9c3-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-224">%linenetamount%</span></span> |
| <span data-ttu-id="8d9c3-225">linjerabat</span><span class="sxs-lookup"><span data-stu-id="8d9c3-225">line discount</span></span>          | <span data-ttu-id="8d9c3-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-226">%linediscount%</span></span> |
| <span data-ttu-id="8d9c3-227">Afsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="8d9c3-227">Ship date</span></span>              | <span data-ttu-id="8d9c3-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-228">%lineshipdate%</span></span> |
| <span data-ttu-id="8d9c3-229">Indkøbsmetode</span><span class="sxs-lookup"><span data-stu-id="8d9c3-229">Procurement method</span></span>     | <span data-ttu-id="8d9c3-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="8d9c3-231">leveringsadresse</span><span class="sxs-lookup"><span data-stu-id="8d9c3-231">delivery address</span></span>       | <span data-ttu-id="8d9c3-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="8d9c3-233">Salgsenhed for linjen</span><span class="sxs-lookup"><span data-stu-id="8d9c3-233">Sales unit of the line</span></span> | <span data-ttu-id="8d9c3-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="8d9c3-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="8d9c3-235">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="8d9c3-235">Additional resources</span></span>

[<span data-ttu-id="8d9c3-236">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8d9c3-237">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="8d9c3-238">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8d9c3-239">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8d9c3-240">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="8d9c3-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8d9c3-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8d9c3-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8d9c3-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="8d9c3-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8d9c3-243">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="8d9c3-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8d9c3-244">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="8d9c3-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
