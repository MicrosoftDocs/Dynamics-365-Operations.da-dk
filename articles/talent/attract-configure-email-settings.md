---
title: Konfigurer mailindstillinger i Attract
description: I dette emne beskrives, hvordan du kan konfigurere indstillinger for mails, der sendes af Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124721"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="a3502-103">Konfigurer mailindstillinger i Attract</span><span class="sxs-lookup"><span data-stu-id="a3502-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a3502-104">Dit varemærke skaber tillid og hjælper dig med at opbygge en relation til kandidater, selv før de ansøger om dine stillinger.</span><span class="sxs-lookup"><span data-stu-id="a3502-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="a3502-105">Positiv opfattelse af et brand tiltrækker de bedste talenter og øger eksisterende medarbejderes loyalitet.</span><span class="sxs-lookup"><span data-stu-id="a3502-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="a3502-106">Microsoft Dynamics 365 Talent: Attract giver dig mulighed for at konfigurere mails, så de afspejler virksomhedens brand.</span><span class="sxs-lookup"><span data-stu-id="a3502-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="a3502-107">Du kan derfor give jobkandidater en gennemført oplevelse, når de gennemgår ansøgningsprocessen.</span><span class="sxs-lookup"><span data-stu-id="a3502-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="a3502-108">Med Attract kan du udføre disse handlinger:</span><span class="sxs-lookup"><span data-stu-id="a3502-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="a3502-109">Konfigurer mailindstillinger, så dit firmas Microsoft Exchange-mailtjenestekonto bruges.</span><span class="sxs-lookup"><span data-stu-id="a3502-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="a3502-110">På denne måde ved ansøgere, at mails kommer fra dit firma.</span><span class="sxs-lookup"><span data-stu-id="a3502-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="a3502-111">Du kan f.eks. konfigurere dine indstillinger, så kandidater modtager mails fra `recruiting@contoso.com` i stedet for `contoso@microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="a3502-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="a3502-112">Opret en gennemført branding til al mailkommunikation ved at angive det globale sidehoved og den globale sidefod til alle mailskabeloner.</span><span class="sxs-lookup"><span data-stu-id="a3502-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="a3502-113">Hvis du vil konfigurere Attract, så det bruger dit firmas mailtjenestekonto til at sende mail, skal du bruge tilføjelsesprogrammet Omfattende ansættelser.</span><span class="sxs-lookup"><span data-stu-id="a3502-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="a3502-114">Forbinde en mailtjenestekonto</span><span class="sxs-lookup"><span data-stu-id="a3502-114">Connect an email service account</span></span>

<span data-ttu-id="a3502-115">Ved at forbinde dit firmas mailtjenestekonto kan du oprette en brandet mailoplevelse for dine jobkandidater.</span><span class="sxs-lookup"><span data-stu-id="a3502-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="a3502-116">Hvis du ikke tilslutter dit firmas konto, bruger Attract den Microsoft-brandede mailtjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="a3502-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="a3502-117">Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.</span><span class="sxs-lookup"><span data-stu-id="a3502-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a3502-118">Vælg **Tilslut en firmakonto** under **Mailtjenestekonti** under fanen **Mailindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a3502-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Tilslutte dit firmas mailtjenestekonto i Attract](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="a3502-120">Du kan finde flere oplysninger om, hvordan du opretter en delt mailkonto, i [Delte postkasser i Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="a3502-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="a3502-121">Log på ved hjælp af dine firmalegitimationsoplysninger i Microsoft-vinduet til logon.</span><span class="sxs-lookup"><span data-stu-id="a3502-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="a3502-122">Hvis du endnu ikke har oprettet en mailtjenestekonto, eller hvis du vil tilføje en ny, skal du vælge **Tilføj ny tjenestekonto** og derefter angive dine mailoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a3502-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="a3502-123">Hvis du allerede har konfigureret den mailtjenestekonto, du vil bruge, skal du vælge den.</span><span class="sxs-lookup"><span data-stu-id="a3502-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="a3502-124">Når din mailtjenestekonto er konfigureret korrekt, kan du se den på listen under **Mailtjenestekonti**.</span><span class="sxs-lookup"><span data-stu-id="a3502-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="a3502-125">Frakoble en mailtjenestekonto</span><span class="sxs-lookup"><span data-stu-id="a3502-125">Disconnect an email service account</span></span>

<span data-ttu-id="a3502-126">Hvis du ikke længere vil bruge dit firmas domæne i mailkommunikation via Attract, kan du frakoble en mailtjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="a3502-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="a3502-127">Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.</span><span class="sxs-lookup"><span data-stu-id="a3502-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a3502-128">Vælg knappen **Mere** (tre lodrette prikker) under **Mailtjenestekonti** under fanen **Mailindstillinger** ud for den mailtjenestekonto, du vil frakoble.</span><span class="sxs-lookup"><span data-stu-id="a3502-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="a3502-129">Vælg **Afbryd forbindelsen til mailkonto**.</span><span class="sxs-lookup"><span data-stu-id="a3502-129">Select **Disconnect email account**.</span></span>

    ![Frakobling af dit firmas mailtjenestekonto](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="a3502-131">Når du bliver bedt om at bekræfte handlingen, skal du vælge **Afbryd forbindelsen**.</span><span class="sxs-lookup"><span data-stu-id="a3502-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Bekræftelse af frakobling af dit firmas mailtjenestekonto](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="a3502-133">Hvis du ikke tilslutter en anden mailtjenestekonto, vil mails, der sendes fra Attract, bruge den Microsoft-brandede mailtjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="a3502-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="a3502-134">Konfigurere mailskabelonindstillinger</span><span class="sxs-lookup"><span data-stu-id="a3502-134">Configure email template settings</span></span>

<span data-ttu-id="a3502-135">Du kan uploade et billede af dit firmas logo og andre oplysninger som et brandet sidehoved til dine mails.</span><span class="sxs-lookup"><span data-stu-id="a3502-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="a3502-136">Du kan også angive links til politikken for beskyttelse af personlige oplysninger og vilkår for anvendelse i mailsidefødder.</span><span class="sxs-lookup"><span data-stu-id="a3502-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="a3502-137">Du skal overholde alle gældende love i dit land eller område samt lovene i det land eller område, der er styrende for mailmodtageren.</span><span class="sxs-lookup"><span data-stu-id="a3502-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="a3502-138">Disse love omfatter antispamregler.</span><span class="sxs-lookup"><span data-stu-id="a3502-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="a3502-139">Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.</span><span class="sxs-lookup"><span data-stu-id="a3502-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="a3502-140">Træk det billede, du vil bruge som mailsidehoved, til billedfeltet under **Mailskabelonindstillinger** under fanen **Mailindstillinger**, eller klik i billedfeltet for at navigere til filen.</span><span class="sxs-lookup"><span data-stu-id="a3502-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="a3502-141">Hvis du vil erstatte et eksisterende billede, skal du først vælge **Fjern** ud for det.</span><span class="sxs-lookup"><span data-stu-id="a3502-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="a3502-142">Billedet skal være en JPEG-, JPG-, PNG-eller SVG-fil.</span><span class="sxs-lookup"><span data-stu-id="a3502-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="a3502-143">Den anbefalede størrelse på billeder er mellem 25 og 800 pixelbredde og mellem 25 og 150 pixelhøje.</span><span class="sxs-lookup"><span data-stu-id="a3502-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="a3502-144">Den maksimale filstørrelse for sidehovedet er 1 megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="a3502-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Tilføjelse af et billede til firmaets mailsidehoved](./media/attract-admin-email-header.png)

3. <span data-ttu-id="a3502-146">Under **Din politik om beskyttelse af personlige oplysninger for kommunikation** skal du angive et link til din virksomheds politik for beskyttelse af personlige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a3502-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="a3502-147">Under **Dine Vilkår og betingelser for kommunikation** skal du angive et link til dit firmas vilkår for anvendelse.</span><span class="sxs-lookup"><span data-stu-id="a3502-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Tilføjelse af links til firmaets politik for beskyttelse af personlige oplysninger og vilkår for anvendelse i mailsidefod](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="a3502-149">Vælg **Gem** for at gemme mailskabelonindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="a3502-149">Select **Save** to save your email template settings.</span></span>
