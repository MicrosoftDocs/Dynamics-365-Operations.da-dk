---
title: Konfigurere en mailbeskedprofil
description: Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9378fb200a239433f2023bb90f72840dace1c0eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000818"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="6bc32-103">Konfigurere en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="6bc32-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6bc32-104">Dette emne beskriver, hvordan du opretter en mailbeskedprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6bc32-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6bc32-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="6bc32-105">Overview</span></span>

<span data-ttu-id="6bc32-106">Før du opretter kanaler, skal du oprette en profil for at sikre, at mailbeskeder kan sendes ud fra forskellige hændelser, f.eks. ordreoprettelse, ordreforsendelsesstatus og betalingsfejl.</span><span class="sxs-lookup"><span data-stu-id="6bc32-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="6bc32-107">Du kan finde yderligere oplysninger om mailkonfiguration i [Konfigurere og sende e-mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6bc32-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="6bc32-108">Oprette en mailbeskedprofil</span><span class="sxs-lookup"><span data-stu-id="6bc32-108">Create an email notification profile</span></span>

<span data-ttu-id="6bc32-109">Benyt følgende fremgangsmåde for at oprette en mailbeskedprofil.</span><span class="sxs-lookup"><span data-stu-id="6bc32-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="6bc32-110">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6bc32-111">Klik på **Ny** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6bc32-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="6bc32-112">Angiv et navn, der identificerer profilen, i feltet **Profil til e-mail-besked**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="6bc32-113">Indtast en relevant beskrivelse i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="6bc32-114">Angiv parameteren **Aktiv** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="6bc32-115">Opret en mailskabelon</span><span class="sxs-lookup"><span data-stu-id="6bc32-115">Create an email template</span></span>

<span data-ttu-id="6bc32-116">Før du kan oprette en mailbesked, skal du oprette en mailskabelon for organisationen, der indeholder oplysninger om afsenderens mail og mailskabelonen.</span><span class="sxs-lookup"><span data-stu-id="6bc32-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="6bc32-117">Benyt følgende fremgangsmåde for at oprette en mailskabelon.</span><span class="sxs-lookup"><span data-stu-id="6bc32-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="6bc32-118">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Skabelon til organisationsmail**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="6bc32-119">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6bc32-120">I feltet **Mail-id** sal du angive et id, der kan hjælpe med at identificere denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="6bc32-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="6bc32-121">Indtast navnet på afsenderen i feltet **Afsenders e-mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="6bc32-122">Indtast en meningsfuld beskrivelse i feltet **E-mail-beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="6bc32-123">I feltet **Afsenders e-mailadresse** skal du angive afsenderens mailadresse.</span><span class="sxs-lookup"><span data-stu-id="6bc32-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="6bc32-124">I sektionen **Generelt** kan du angive eventuelle valgfrie oplysninger, der er nødvendige (f.eks. prioriteringen af mail).</span><span class="sxs-lookup"><span data-stu-id="6bc32-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="6bc32-125">Udvid sektionen **E-mailbeskedens indhold**, og vælg **Ny** for at oprette skabelonindholdet.</span><span class="sxs-lookup"><span data-stu-id="6bc32-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="6bc32-126">Vælg sproget for hvert indholdselement, og angiv emnelinjen i mailen.</span><span class="sxs-lookup"><span data-stu-id="6bc32-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="6bc32-127">Hvis der skal være indhold i mailen, skal du sørge for at markere afkrydsningsfeltet **Har indhold**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="6bc32-128">Vælg **E-mail-besked** i handlingsruden for at oprette en skabelon til mailindholdet.</span><span class="sxs-lookup"><span data-stu-id="6bc32-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="6bc32-129">Følgende billede viser eksempler på indstillinger for mailskabeloner.</span><span class="sxs-lookup"><span data-stu-id="6bc32-129">The following image shows some example email template settings.</span></span>

![Mailskabelonindstillinger](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="6bc32-131">Opret en mailhændelse</span><span class="sxs-lookup"><span data-stu-id="6bc32-131">Create an email event</span></span>

<span data-ttu-id="6bc32-132">Benyt følgende fremgangsmåde for at oprette en mailhændelse.</span><span class="sxs-lookup"><span data-stu-id="6bc32-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="6bc32-133">I navigationsruden skal du gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Commerce-profil for mailbesked**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6bc32-134">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6bc32-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="6bc32-135">Vælg mailskabelonen fra rullelisten **Mail-id**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="6bc32-136">Vælg den relevante **E-mailbeskedtype** på rullelisten.</span><span class="sxs-lookup"><span data-stu-id="6bc32-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="6bc32-137">Marker afkrydsningsfeltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="6bc32-138">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6bc32-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6bc32-139">Følgende billede viser eksempler på indstillinger for hændelsesbeskeder.</span><span class="sxs-lookup"><span data-stu-id="6bc32-139">The following image shows some example event notification settings.</span></span>

![Indstillinger for hændelsesbesked](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="6bc32-141">Næste trin</span><span class="sxs-lookup"><span data-stu-id="6bc32-141">Next steps</span></span>

<span data-ttu-id="6bc32-142">Før du kan sende mails, skal du konfigurere tjenesten til udgående mail og konfigurere et batchjob.</span><span class="sxs-lookup"><span data-stu-id="6bc32-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="6bc32-143">Du kan få flere oplysninger under [Konfigurere og sende mail](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6bc32-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6bc32-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6bc32-144">Additional resources</span></span>

[<span data-ttu-id="6bc32-145">Konfigurere og sende mail</span><span class="sxs-lookup"><span data-stu-id="6bc32-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6bc32-146">Oversigt over kanaler</span><span class="sxs-lookup"><span data-stu-id="6bc32-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6bc32-147">Forudsætninger for konfiguration af kanal</span><span class="sxs-lookup"><span data-stu-id="6bc32-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6bc32-148">Oversigt over organisationer og organisationshierarkier</span><span class="sxs-lookup"><span data-stu-id="6bc32-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
