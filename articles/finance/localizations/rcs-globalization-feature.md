---
title: Regulatory Configuration Service (RCS) – globaliseringsfunktioner
description: Dette emne forklarer, hvordan du bruger Microsoft Regulatory Configuration Services (RCS) og det globale lager for at oprette og bruge globaliseringsfunktioner.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002777"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="4bfe2-103">Regulatory Configuration Service (RCS) – globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4bfe2-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bfe2-104">Du kan bruge RCS (Microsoft Regulatory Configuration Services) til at oprette en globaliseringsfunktion, der kan bruges i globaliseringstjenester, f.eks. en e-faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="4bfe2-105">RCS giver dig mulighed for at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="4bfe2-106">Definere relaterede komponenter i en funktion.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-106">Define related components of a feature.</span></span>
- <span data-ttu-id="4bfe2-107">Administrere funktionens livscyklus via en funktionsstatus.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="4bfe2-108">Gøre en funktion tilgængelig for definerede miljøer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="4bfe2-109">Dele en funktion med andre organisationer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="4bfe2-110">I de følgende procedurer forklares det, hvordan en bruger i RCS kan tilføje en globaliseringsfunktion og relaterede komponenter, opdatere funktionens status og gøre funktionen tilgængelig, så den kan bruges i globaliseringstjenester.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="4bfe2-111">Før du fuldfører procedurerne, skal du udføre de trin, der er knyttet til følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="4bfe2-112">Adgang til en RCS-forekomst.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="4bfe2-113">Oprettelse og aktivering af en konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="4bfe2-114">Få flere oplysninger i [Oprette konfigurationsudbydere og markere dem som aktive](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="4bfe2-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="4bfe2-115">I din Finance and Operations-appforekomst skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="4bfe2-116">Gå til **Organisationsadministration** \> **Arbejdsområder** \> **Elektronisk rapportering**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4bfe2-117">Hvis der ikke er klargjort noget RCS-miljø til dit firma, skal du vælge **Regulatory services – Konfiguration** og derefter følge vejledningen for at klargøre et miljø.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="4bfe2-118">Hvis der allerede er klargjort et RCS-miljø til dit firma, kan du bruge siden med URL-adresser til at få adgang til miljøet ved at vælge indstillingen til logon.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="4bfe2-119">Slå globaliseringsfunktionerne til</span><span class="sxs-lookup"><span data-stu-id="4bfe2-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="4bfe2-120">I RCS-forekomsten skal du vælge feltet **Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="4bfe2-121">I området **Funktionsstyring** skal du vælge **Globaliseringsfunktioner** på listen og derefter **Aktivér nu**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globaliseringsfunktioner i funktionsstyring](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="4bfe2-123">Globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4bfe2-123">Globalization features</span></span>

<span data-ttu-id="4bfe2-124">Hvis du vil bruge en globaliseringsfunktion, skal du importere den fra det globale lager og oprette din egen version af den.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="4bfe2-125">Du kan tilføje globaliseringsfunktioner på to måder:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="4bfe2-126">Tilføj en afledt funktion, som er baseret på en eksisterende funktion, der er publiceret eller delt.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="4bfe2-127">Tilføj en ny funktion, som du har oprettet fra bunden.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="4bfe2-128">Tilgå globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4bfe2-128">Access Globalization features</span></span>

1. <span data-ttu-id="4bfe2-129">Sørg for, at funktionen **Globaliseringsfunktioner** er aktiveret i funktionsstyring, som beskrevet tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="4bfe2-130">Åbn det nye arbejdsområde **Globaliseringsfunktioner**, og under **Funktioner** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Arbejdsområde til globale funktioner](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="4bfe2-132">Siden **e-faktureringsfunktioner** åbnes.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Side med e-faktureringsfunktioner](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="4bfe2-134">Tilføje en afledt globaliseringsfunktion</span><span class="sxs-lookup"><span data-stu-id="4bfe2-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="4bfe2-135">Du kan tilføje en ny globaliseringsfunktion ved at aflede den fra en eksisterende funktion, der er publiceret eller delt.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="4bfe2-136">Vælg **Importér** for at åbne siden **Importér funktion fra globalt lager**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Siden Importér funktion fra globalt lager](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="4bfe2-138">Vælg **Synkroniser** for at hente de nyeste funktioner.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="4bfe2-139">Den synkroniserede liste indeholder funktioner, som enten er tilgængelige, fordi de blev publiceret af Microsoft, eller fordi de blev delt med dig af en anden konfigurationsudbyder.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Synkroniseret liste over funktioner](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="4bfe2-141">Vælg de funktioner, der skal importeres, på listen, og vælg derefter **Importér**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="4bfe2-142">Du modtager en meddelelse, når de valgte funktioner er blevet importeret.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Meddelelse om vellykket import](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="4bfe2-144">Vælg **Tilføj**, og derefter skal du i rulledialogboksen vælge indstillingen **Baseret på eksisterende version**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="4bfe2-145">Angiv et navn til og en beskrivelse af funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="4bfe2-146">Vælg funktionens basisversion på listen over tilgængelige funktioner og derefter **Opret funktion**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Tilføje en afledt funktion](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="4bfe2-148">Den funktion, du har tilføjet, er oprettet og har statussen **Kladde**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Afledt funktion med kladdestatus](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="4bfe2-150">Gennemse funktionskomponenterne for at finde ud af, om der kræves opdateringer:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="4bfe2-151">Gennemse konfigurationerne, hvis du skal tilpasse ER-formaterne (Electronic Reporting) og deres binding med formattilknytninger til funktionsversionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="4bfe2-152">Gennemse opsætningen, hvis du har brug for at tilpasse fanen **Handlinger**, fanen **Anvendelighedsregler** eller fanen **Variabler** for funktionsversionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="4bfe2-153">På fanen **Versioner** skal du vælge en **Ikrafttrædelsesdato** og angive en beskrivelse, hvis feltet **Beskrivelse** er tomt.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="4bfe2-154">Vælg **Skift status** for at fuldføre funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="4bfe2-155">Fuldførte funktioner kan gøres tilgængelige for et bestemt miljø, så de kan bruges i globaliseringstjenester, eller de kan publiceres til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="4bfe2-156">Funktioner, der har en **Funktionsversionsstatus**-værdi for **Publiceret**, kan deles med eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="4bfe2-157">Tilføje en ny globaliseringsfunktion</span><span class="sxs-lookup"><span data-stu-id="4bfe2-157">Add a new Globalization feature</span></span>

<span data-ttu-id="4bfe2-158">Du kan tilføje en ny globaliserings funktion ved at oprette den fra bunden.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="4bfe2-159">På siden **Importér funktion fra globalt lager** skal du vælge **Tilføj** og derefter i rulledialogboksen vælge indstillingen **Ny funktion**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="4bfe2-160">Angiv et navn til og en beskrivelse af funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="4bfe2-161">Vælg **Opret funktion**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-161">Select **Create feature**.</span></span>

    ![Tilføje en ny funktion](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="4bfe2-163">På fanen **Versioner** skal du vælge en **Ikrafttrædelsesdato** og derefter **Skift status** for at fuldføre funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="4bfe2-164">Fuldførte funktioner kan gøres tilgængelige for et bestemt miljø, så de kan bruges i globaliseringstjenester, eller de kan publiceres til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="4bfe2-165">Funktioner, der har en **Funktionsversionsstatus**-værdi for **Publiceret**, kan deles med eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="4bfe2-166">Oversigt over funktionskomponenter</span><span class="sxs-lookup"><span data-stu-id="4bfe2-166">Feature component overview</span></span>

<span data-ttu-id="4bfe2-167">Globaliseringsfunktioner har flere forskellige komponenter:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-167">Globalization features have several components:</span></span>

- <span data-ttu-id="4bfe2-168">**Version** – Denne komponent understøtter styring af funktionens livscyklus og giver brugerne mulighed for at styre status for forskellige versioner af funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="4bfe2-169">**Konfigurationer** – Denne komponent giver brugerne mulighed for at administrere, få vist og redigere relaterede ER-formater og formattilknytninger.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="4bfe2-170">**Opsætninger** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere opsætningen af den relaterede funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="4bfe2-171">Den understøtter derfor den fleksible konstruktion af kommunikations- og svarregler.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="4bfe2-172">**Miljø** – Denne komponent giver brugerne af globaliseringstjenester, f.eks. en e-faktureringstjeneste, mulighed for at administrere det miljø, hvor opsætningen af funktionsversionen bruges, og give tilladelse til de brugere, der skal have adgang til miljøet.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="4bfe2-173">**Organisationer** – Denne komponent giver brugerne mulighed for at dele funktionen med eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="4bfe2-174">Konfigurere funktionskomponenter</span><span class="sxs-lookup"><span data-stu-id="4bfe2-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="4bfe2-175">Version og status</span><span class="sxs-lookup"><span data-stu-id="4bfe2-175">Version and status</span></span>

<span data-ttu-id="4bfe2-176">Versionen bruges til at administrere globaliseringsfunktionens livscyklus.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="4bfe2-177">Status kan ændres i feltet **Status** på fanen **Version**. Følgende statusser er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="4bfe2-178">**Kladde** – Funktionen kan kun redigeres, når den er i denne status.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="4bfe2-179">**Fuldført** – Funktionen og alle relaterede komponenter er blevet færdiggjort (fuldført) og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="4bfe2-180">**Publiceret** – Funktionen og alle relaterede komponenter er blevet publiceret til det globale lager.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="4bfe2-181">**Delt** – Funktionen og alle relaterede komponenter er blevet delt med eksterne organisationer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="4bfe2-182">**Aktiveret** – Funktionen og alle relaterede komponenter er aktiveret til brug i en globaliseringstjeneste, f.eks. en e-faktureringstjeneste.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="4bfe2-183">Funktioner skal flyttes sekventielt gennem nogle af disse statusser.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="4bfe2-184">Derfor er det ikke alle statusser, der kan være tilgængelige i alle livscyklusser.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="4bfe2-185">Varianter</span><span class="sxs-lookup"><span data-stu-id="4bfe2-185">Configurations</span></span>

<span data-ttu-id="4bfe2-186">De følgende handligner er tilgængelige for konfigurationer:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="4bfe2-187">**Vis** – Få vist de underliggende funktionskonfigurationer, der ikke kræver opdatering.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="4bfe2-188">**Rediger** – Opretfe en kladdeversion af en valgt konfiguration, så du kan redigere formatet eller formattilknytningen i formatdesigneren.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="4bfe2-189">**Slet** – Slette en valgt konfiguration fra funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="4bfe2-190">**Rebasér** – Rebasere funktionen.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="4bfe2-191">Du kan finde flere oplysninger i afsnittet [Rebasér delte globaliseringsfunktioner](#rebase) nedenfor i dette emne.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="4bfe2-192">Konfigurationer</span><span class="sxs-lookup"><span data-stu-id="4bfe2-192">Setups</span></span>

<span data-ttu-id="4bfe2-193">Følgende handlinger er tilgængelige for funkionsopsætninger:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="4bfe2-194">**Tilføj** – Oprette en ny funktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="4bfe2-195">Denne funktionsopsætning kan afledes fra en eksisterende funktionsopsætning eller oprettes fra bunden.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="4bfe2-196">**Slet** – Slette en valgt funktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="4bfe2-197">**Vis** – Få vist en underliggende funktionsopsætning, der ikke kræver nogen ændringer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="4bfe2-198">**Rediger** – Oprette, slette eller redigere attributterne for de tre hovedkomponenter i en funktionsopsætning:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="4bfe2-199">Handlinger og deres parametre</span><span class="sxs-lookup"><span data-stu-id="4bfe2-199">Actions and their parameters</span></span>
    - <span data-ttu-id="4bfe2-200">Anvendelighedsregler</span><span class="sxs-lookup"><span data-stu-id="4bfe2-200">Applicability rules</span></span>
    - <span data-ttu-id="4bfe2-201">Variabler</span><span class="sxs-lookup"><span data-stu-id="4bfe2-201">Variables</span></span>

![Siden Opsætning af funktionsversion](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="4bfe2-203">Miljøer</span><span class="sxs-lookup"><span data-stu-id="4bfe2-203">Environments</span></span>

<span data-ttu-id="4bfe2-204">De følgende handlinger er tilgængelige for miljøer:</span><span class="sxs-lookup"><span data-stu-id="4bfe2-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="4bfe2-205">**Aktivér** – For en valgt funktionsversion skal du vælge et publiceret miljø og vælge en **Ikrafttrædelsesdato**, når den skal være tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="4bfe2-206">Du kan finde flere oplysninger i afsnittet [Konfigurer miljøer til aktivering](#configureenvironment) nedenfor i dette emne.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="4bfe2-207">**Annuller** – Fjerne et miljø for en funktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="4bfe2-208">Organisationer</span><span class="sxs-lookup"><span data-stu-id="4bfe2-208">Organizations</span></span>

<span data-ttu-id="4bfe2-209">Udfør følgende trin for at dele en globaliseringsfunktion med en ekstern organisation.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="4bfe2-210">På siden **e-faktureringsfunktioner** skal du vælge den funktion og den funktionsversion, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="4bfe2-211">På fanen **Organisationer** skal du vælge **Del med** og derefter i rulledialogboksen angive organisationens domænenavn.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="4bfe2-212">Vælg **Del**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-212">Select **Share**.</span></span>

    ![Deling af en funktion med en organisation](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="4bfe2-214">Funktionen deles med den valgte organisation og er tilgængelig for denne organisation i det globale lager.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="4bfe2-215">Derfra kan funktionen importeres til organisationens forekomst af RCS eller Dynamics 365 Finance, så den kan bruges.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="4bfe2-216">Rebasér afledte globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4bfe2-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="4bfe2-217">Du kan rebasere en afledt globaliseringsfunktion til den nye eller opdaterede basisfunktionsversion.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="4bfe2-218">På denne måde kan ændringer, der er foretaget i basisversionen, opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="4bfe2-219">Den opdaterede basisfunktionsversion oprettes af den oprindelige konfigurationsudbyder, og den publiceres eller deles derefter.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Opdateret basisfunktionsversion](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="4bfe2-221">Hvis du f eks. vil rebasere den afledte version af en funktion, du har oprettet, skal du først hente den seneste version af funktionen ved at importere den fra det globale lager.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="4bfe2-222">På siden **e-faktureringsfunktioner** skal du vælge **Importér**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="4bfe2-223">Vælg **Synkroniser** for at hente de nyeste funktioner.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="4bfe2-224">På listen over funktioner skal du vælge de funktioner, der skal importeres, og derefter **Importér**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Import af den seneste version af en funktion](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="4bfe2-226">Vælg den funktion, der skal rebaseres, på listen over funktioner.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="4bfe2-227">På fanen **Version** skal du vælge **Ny** for at oprette en kladdeversion.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Ny kladdeversion oprettet](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="4bfe2-229">Vælg **Rebaśer**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="4bfe2-230">I dialogboksen **Rebasér** skal du vælge den seneste version af funktionen, der skal rebaseres til.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialogboksen Rebasér](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="4bfe2-232">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-232">Select **OK**.</span></span>
9. <span data-ttu-id="4bfe2-233">Gennemgå funktionskomponenterne, og foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="4bfe2-234">Vælg **Skift status** for at fuldføre den rebaserede funktion.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="4bfe2-235">Når rebaseringen er fuldført, kan du udføre yderligere handlinger.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="4bfe2-236">Du kan f.eks. publicere funktionen og gøre den tilgængelig for brug i globaliseringstjenester.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Funktionsstatus er opdateret til Fuldført](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="4bfe2-238">Konfigurere miljøer til globaliseringsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4bfe2-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="4bfe2-239">Brugere af globaliseringstjenester kan administrere miljøet for at konfigurere en globaliseringsfunktion og give godkendelse til andre brugere, der skal have adgang til den.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="4bfe2-240">I arbejdsområdet **Globaliseringsfunktioner** under **Miljøer** skal du vælge feltet **e-fakturering**.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Arbejdsområdet for globale funktioner](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="4bfe2-242">Vælg **Parametre for Key Vault** og derefter **Ny** for at oprette en Azure Key Vault-hemmelighed.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="4bfe2-243">Angiv et navn til og en beskrivelse af Key Vault, og angiv derefter i feltet **Key Vault URI** den URL-adresse, der identificerer Key Vault-ressourcen i Azure.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="4bfe2-244">I oversigtspanelet **Certifikater** skal du vælge **Tilføj** for at tilføje certifikatet og angive et navn til og en beskrivelse af hvert certifikat.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Certifikat tilføjet](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="4bfe2-246">Vælg **Ny** for at oprette et nyt miljø.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="4bfe2-247">Angiv et navn, en beskrivelse og det hemmelige token for signaturer til delt adgang, der er nødvendigt til lagring.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="4bfe2-248">I oversigtspanelet **Brugere** skal du vælge **Ny** for at tilføje en bruger, der ønsker tilladelse til at få adgang til dette miljø.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="4bfe2-249">Angiv brugerens bruger-id og e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="4bfe2-250">Gentag trin 7 og 8 for at tilføje flere brugere.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="4bfe2-251">Vælg **Publicer** for at publicere miljøet.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-251">Select **Publish** to publish the environment.</span></span>

    ![Publiceret miljø](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
