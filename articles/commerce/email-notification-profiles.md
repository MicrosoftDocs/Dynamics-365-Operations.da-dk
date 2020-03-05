---
title: Konfigurere en mailbeskedprofil
description: Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: feb28b9c801786f63282c4189d3eeb6d53ed07e1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003136"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="a15e4-103">Konfigurere en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="a15e4-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a15e4-104">Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a15e4-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a15e4-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="a15e4-105">Overview</span></span>

<span data-ttu-id="a15e4-106">Før du opretter kanaler, skal du oprette en profil for at sikre, at mailbeskeder kan sendes ud fra forskellige hændelser, f.eks. ordreoprettelse, ordreforsendelsesstatus og betalingsfejl.</span><span class="sxs-lookup"><span data-stu-id="a15e4-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="a15e4-107">Du kan finde yderligere oplysninger om mailkonfiguration i [Konfigurere og sende e-mail](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="a15e4-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="a15e4-108">Oprette en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="a15e4-108">Create an email notification profile</span></span>

<span data-ttu-id="a15e4-109">Benyt følgende fremgangsmåde for at oprette en mailbeskedprofil.</span><span class="sxs-lookup"><span data-stu-id="a15e4-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="a15e4-110">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Retail-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="a15e4-111">Klik på **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a15e4-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="a15e4-112">Angiv et navn, der identificerer profilen, i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="a15e4-113">Indtast en relevant beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="a15e4-114">Angiv parameteren **Aktiv** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="a15e4-115">Opret en mailskabelon</span><span class="sxs-lookup"><span data-stu-id="a15e4-115">Create an email template</span></span>

<span data-ttu-id="a15e4-116">Før du kan oprette en mailbesked, skal du oprette en mailskabelon for organisationen, der indeholder oplysninger om afsenderens mail og mailskabelonen.</span><span class="sxs-lookup"><span data-stu-id="a15e4-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="a15e4-117">Benyt følgende fremgangsmåde for at oprette en mailskabelon.</span><span class="sxs-lookup"><span data-stu-id="a15e4-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="a15e4-118">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="a15e4-119">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a15e4-120">I feltet **Mail-id** sal du angive et id, der kan hjælpe med at identificere denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="a15e4-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="a15e4-121">Indtast navnet på afsenderen i feltet **Afsenders e-mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="a15e4-122">Indtast en meningsfuld beskrivelse i feltet **E-mail-beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="a15e4-123">I feltet **Afsenders e-mailadresse** skal du angive afsenderens mailadresse.</span><span class="sxs-lookup"><span data-stu-id="a15e4-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="a15e4-124">I sektionen **Generelt** kan du angive eventuelle valgfrie oplysninger, der er nødvendige (f.eks. prioriteringen af mail).</span><span class="sxs-lookup"><span data-stu-id="a15e4-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="a15e4-125">Udvid sektionen **E-mailbeskedens indhold**, og vælg **Ny** for at oprette skabelonindholdet.</span><span class="sxs-lookup"><span data-stu-id="a15e4-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="a15e4-126">Vælg sproget for hvert indholdselement, og angiv emnelinjen i mailen.</span><span class="sxs-lookup"><span data-stu-id="a15e4-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="a15e4-127">Hvis der skal være indhold i mailen, skal du sørge for at markere afkrydsningsfeltet **Har indhold**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="a15e4-128">Vælg **E-mail-besked** i handlingsruden for at oprette en skabelon til mailindholdet.</span><span class="sxs-lookup"><span data-stu-id="a15e4-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="a15e4-129">Følgende billede viser eksempler på indstillinger for mailskabeloner.</span><span class="sxs-lookup"><span data-stu-id="a15e4-129">The following image shows some example email template settings.</span></span>

![Mailskabelonindstillinger](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="a15e4-131">Opret en mailhændelse</span><span class="sxs-lookup"><span data-stu-id="a15e4-131">Create an email event</span></span>

<span data-ttu-id="a15e4-132">Benyt følgende fremgangsmåde for at oprette en mailhændelse.</span><span class="sxs-lookup"><span data-stu-id="a15e4-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="a15e4-133">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Retail-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Retail Email notification profile**.</span></span>
1. <span data-ttu-id="a15e4-134">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="a15e4-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="a15e4-135">Vælg mailskabelonen fra rullelisten **Mail-id**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="a15e4-136">Vælg den relevante **E-mailbeskedtype** på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="a15e4-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="a15e4-137">Marker afkrydsningsfeltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="a15e4-138">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a15e4-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a15e4-139">Følgende billede viser eksempler på indstillinger for detailhændelsesbeskeder.</span><span class="sxs-lookup"><span data-stu-id="a15e4-139">The following image shows some example retail event notification settings.</span></span>

![Indstillinger for besked om detailhændelse](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="a15e4-141">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a15e4-141">Additional resources</span></span>

[<span data-ttu-id="a15e4-142">Konfigurere og sende mail</span><span class="sxs-lookup"><span data-stu-id="a15e4-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="a15e4-143">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="a15e4-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a15e4-144">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="a15e4-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a15e4-145">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="a15e4-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)