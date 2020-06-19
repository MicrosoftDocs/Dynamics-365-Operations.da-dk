---
title: Klargøre et Dynamics 365 Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.
author: psimolin
manager: annbe
ms.date: 06/02/2020
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
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426459"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="14fd6-103">Klargøre et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="14fd6-104">I dette emne beskrives det, hvordan du klargør et Dynamics 365 Commerce-prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="14fd6-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="14fd6-105">Før du går i gang, anbefales det, at du hurtigt gennemgår dette emne for at få et indtryk af, hvad processen kræver.</span><span class="sxs-lookup"><span data-stu-id="14fd6-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="14fd6-106">Hvis du endnu ikke har fået adgang til Dynamics 365 Commerce-prøveversionen, kan du anmode om adgang fra [Dynamics 365 Commerce-webstedet](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="14fd6-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="14fd6-107">Oversigt</span><span class="sxs-lookup"><span data-stu-id="14fd6-107">Overview</span></span>

<span data-ttu-id="14fd6-108">Hvis du vil kunne klargør dit Commerce-prøveversionsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type.</span><span class="sxs-lookup"><span data-stu-id="14fd6-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="14fd6-109">Miljøet og Commerce Scale Unit (CSU) har nogle specifikke parametre, du skal bruge, når du senere klargør dit e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="14fd6-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="14fd6-110">Instruktionerne i dette emne beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="14fd6-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="14fd6-111">Nå du har klargjort dit Commerce-prøveversionsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit prøveversionsmiljø klar.</span><span class="sxs-lookup"><span data-stu-id="14fd6-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="14fd6-112">Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="14fd6-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="14fd6-113">Du kan altid udføre de valgfrie trin senere.</span><span class="sxs-lookup"><span data-stu-id="14fd6-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="14fd6-114">For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-prøveversionsmiljø, efter du har klargjort det, se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="14fd6-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="14fd6-115">For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="14fd6-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="14fd6-116">Hvis du har spørgsmål til klargøringstrinnene, eller du oplever problemer, bedes du fortælle det til Microsoft i [Microsoft Dynamics 365 Commerce-prøveversionens-Yammer-gruppen](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="14fd6-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="14fd6-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="14fd6-117">Prerequisites</span></span>

<span data-ttu-id="14fd6-118">Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-prøveversionsmiljø:</span><span class="sxs-lookup"><span data-stu-id="14fd6-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="14fd6-119">Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="14fd6-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="14fd6-120">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan oprette et Dynamics 365 Commerce-projekt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="14fd6-121">Du er blevet godkendt til Dynamics 365 Commerce-prøveversionsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="14fd6-122">Du har de nødvendige rettigheder til at oprette et projekt til **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="14fd6-123">Du er medlem af rollen **Miljøadministrator** eller **Projektejer** i det projekt, hvor du skal klargøre miljøet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="14fd6-124">Du har administratoradgang til dit Microsoft Azure-abonnement eller du er i kontakt med en abonnementsadministrator, der kan fuldføre de to trin, der kræver administratorrettigheder, på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="14fd6-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="14fd6-125">Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.</span><span class="sxs-lookup"><span data-stu-id="14fd6-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="14fd6-126">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="14fd6-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="14fd6-127">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="14fd6-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="14fd6-128">(Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)</span><span class="sxs-lookup"><span data-stu-id="14fd6-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="14fd6-129">Klargøring af dit Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="14fd6-130">Disse procedurer forklarer, hvordan du klargør et Commerce-prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="14fd6-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="14fd6-131">Når du har fuldført dem, vil Commerce-prøveversionsmiljøet være klar til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="14fd6-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="14fd6-132">Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14fd6-133">Forhåndsadgang er knyttet til den LCS-konto og -organisation, som du angav i Commerce-prøveversionsansøgningen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="14fd6-134">Du skal bruge den samme konto til at klargøre Commerce-prøveversionmiljøet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="14fd6-135">Hvis du skal bruge en anden LCS-konto eller -lejer til Commerce-prøveversionsmiljøet, skal du oplyse Microsoft herom.</span><span class="sxs-lookup"><span data-stu-id="14fd6-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="14fd6-136">Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="14fd6-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="14fd6-137">Bekræft, at prøveversionens funktioner er tilgængelige og aktiverede i LCS</span><span class="sxs-lookup"><span data-stu-id="14fd6-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="14fd6-138">For at bekræfte, at prøveversionens funktioner er tilgængelige og aktiverede i LCS, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="14fd6-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-139">Log på [LCS-portalen](https://lcs.dynamics.com) ved at bruge den samme LCS-konto, som du brugte til at anmode om adgang til prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="14fd6-140">Rul helt til højre på LCS-startsiden, og vælg feltet **Styring af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Feltet Styring af prøveversionsfunktion](./media/preview1.png)

1. <span data-ttu-id="14fd6-142">Rul ned til **Funktioner i private prøveversioner**, bekræft, at følgende funktioner er tilgængelige og aktiverede:</span><span class="sxs-lookup"><span data-stu-id="14fd6-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="14fd6-143">Evaluering af e-handel</span><span class="sxs-lookup"><span data-stu-id="14fd6-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="14fd6-144">Programmiljøer til Commerce-prøveversion</span><span class="sxs-lookup"><span data-stu-id="14fd6-144">Commerce Preview Program Environments</span></span>

    ![Funktioner i private prøveversioner](./media/preview2.png)

1. <span data-ttu-id="14fd6-146">Hvis disse funktioner ikke vises på listen, skal du kontakte Microsoft og angive din arbejdsmailadresse, LCS-konto og lejeroplysninger.</span><span class="sxs-lookup"><span data-stu-id="14fd6-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="14fd6-147">Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="14fd6-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="14fd6-148">Opret et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="14fd6-148">Create a new project</span></span>

<span data-ttu-id="14fd6-149">Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="14fd6-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-150">På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="14fd6-151">Benyt en af følgende fremgangsmåder i højre rude:</span><span class="sxs-lookup"><span data-stu-id="14fd6-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="14fd6-152">Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="14fd6-153">Hvis du er en kunde, skal du vælge **Mulige førsalg**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="14fd6-154">Angiv et navn, beskrivelse og branche.</span><span class="sxs-lookup"><span data-stu-id="14fd6-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="14fd6-155">I feltet **Produktnavn** skal du vælge **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="14fd6-156">I feltet **Produktversion** skal du vælge **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="14fd6-157">I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="14fd6-158">Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="14fd6-159">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-159">Select **Create**.</span></span> <span data-ttu-id="14fd6-160">Projektoversigten vises.</span><span class="sxs-lookup"><span data-stu-id="14fd6-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="14fd6-161">Tilføj Azure Connector</span><span class="sxs-lookup"><span data-stu-id="14fd6-161">Add the Azure Connector</span></span>

<span data-ttu-id="14fd6-162">Hvis du vil tilføje Azure Connector til dit LCS-projekt, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="14fd6-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-163">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="14fd6-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="14fd6-164">Hvis du er en partner, skal du vælge feltet **Projektindstillinger** længst til højre.</span><span class="sxs-lookup"><span data-stu-id="14fd6-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="14fd6-165">Hvis du er en kunde, skal du vælge **Projektindstillinger** i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="14fd6-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="14fd6-166">Vælg **Azure-connectorer**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="14fd6-167">Vælg **Tilføj** for at tilføje Azure Connector'en.</span><span class="sxs-lookup"><span data-stu-id="14fd6-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="14fd6-168">Skriv et navn.</span><span class="sxs-lookup"><span data-stu-id="14fd6-168">Enter a name.</span></span>
1. <span data-ttu-id="14fd6-169">Angiv dit Azure-abonnements-ID.</span><span class="sxs-lookup"><span data-stu-id="14fd6-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="14fd6-170">Aktiver indstillingen **Konfigurer til at bruge Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="14fd6-171">Kontrollér, at værdien **Azure-abonnement AAD-lejerdomæne (eller ID)** er korrekt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="14fd6-172">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="14fd6-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="14fd6-173">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-173">Select **Next**.</span></span>
1. <span data-ttu-id="14fd6-174">Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="14fd6-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="14fd6-175">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="14fd6-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="14fd6-176">Log på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="14fd6-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="14fd6-177">Sørg for, at den korrekte mappe er valgt, og vælg derefter **Abonnementer** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="14fd6-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="14fd6-178">Find det korrekte abonnement på listen, og vælg det.</span><span class="sxs-lookup"><span data-stu-id="14fd6-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="14fd6-179">Brug søgefunktionen efter behov.</span><span class="sxs-lookup"><span data-stu-id="14fd6-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="14fd6-180">Vælg **Adgangskontrol (IAM)** i menuen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="14fd6-181">Til højre under **Tilføj en rolletildeling** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="14fd6-182">Ruden **Tilføj rolletildeling** vises.</span><span class="sxs-lookup"><span data-stu-id="14fd6-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="14fd6-183">I feltet **Rolle** skal du vælge **Bidragsyder**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="14fd6-184">I feltet **Tildel adgang** skal du lade standardværdien for **Azure AD-bruger, gruppe eller tjenesteprincipal** være.</span><span class="sxs-lookup"><span data-stu-id="14fd6-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="14fd6-185">Under **Vælg** skal du angive **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="14fd6-186">Vælg **Dynamics-installationstjenester \[wsfed-enabled\]** på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="14fd6-187">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-187">Select **Save**.</span></span>

1. <span data-ttu-id="14fd6-188">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-188">Select **Next**.</span></span>
1. <span data-ttu-id="14fd6-189">Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="14fd6-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="14fd6-190">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="14fd6-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="14fd6-191">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-191">Select **Next**.</span></span>
1. <span data-ttu-id="14fd6-192">I feltet **Azure-region** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="14fd6-193">Vælg **Forbind**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-193">Select **Connect**.</span></span> <span data-ttu-id="14fd6-194">Din Azure-connector bør blive vist på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="14fd6-195">Importer Demobasisudvidelse til Commerce-prøveversion</span><span class="sxs-lookup"><span data-stu-id="14fd6-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="14fd6-196">Følg disse trin for at importere Demobasisudvidelse til Commerce-prøveversion i projektet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-197">Åbn startsiden for dit projekt ved at vælge projektets navn øverst.</span><span class="sxs-lookup"><span data-stu-id="14fd6-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="14fd6-198">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="14fd6-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="14fd6-199">Hvis du er en partner, skal du vælge feltet **Aktivbibliotek** længst til højre.</span><span class="sxs-lookup"><span data-stu-id="14fd6-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="14fd6-200">Hvis du er en kunde, skal du vælge **Aktivbibliotek** i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="14fd6-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="14fd6-201">Vælg **Installerbar softwarepakke** fra listen til venstre.</span><span class="sxs-lookup"><span data-stu-id="14fd6-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="14fd6-202">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-202">Select **Import**.</span></span>
1. <span data-ttu-id="14fd6-203">Under **Delt aktivbibliotek** skal du vælge **Demobasisudvidelse til Commerce-prøveversion** fra aktivlisten.</span><span class="sxs-lookup"><span data-stu-id="14fd6-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="14fd6-204">Vælg **Pluk**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-204">Select **Pick**.</span></span> <span data-ttu-id="14fd6-205">Du kommer tilbage til aktivbiblioteket, og du bør kunne se udvidelsen på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="14fd6-206">I følgende illustration vises de handlinger, der skal udføres på LCS-siden **Aktivbibliotek**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Import af Demobasisudvidelse til Commerce-prøveversion](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="14fd6-208">Installer miljøet</span><span class="sxs-lookup"><span data-stu-id="14fd6-208">Deploy the environment</span></span>

<span data-ttu-id="14fd6-209">Følg disse trin for at installere miljøet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="14fd6-210">Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over.</span><span class="sxs-lookup"><span data-stu-id="14fd6-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="14fd6-211">Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce - Demo (10.0.* x* med platformsopdatering *xx*)\*\* vises direkte over feltet **Miljønavn**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="14fd6-212">Se detaljer på den illustration, der vises efter trin 8.</span><span class="sxs-lookup"><span data-stu-id="14fd6-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="14fd6-213">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="14fd6-214">Vælg **Tilføj** for at tilføje et miljø.</span><span class="sxs-lookup"><span data-stu-id="14fd6-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="14fd6-215">Vælg den seneste version i feltet **Programversion**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="14fd6-216">Hvis du har et specifikt behov for at vælge en anden programversion end den seneste version, skal du ikke vælge en version før **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="14fd6-217">I feltet **Platformsversion** skal du bruge den platformsversion, der automatisk vælges for den programversion, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Valg af program- og platformsversioner](./media/project1.png)

1. <span data-ttu-id="14fd6-219">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-219">Select **Next**.</span></span>
1. <span data-ttu-id="14fd6-220">Vælg **Demo** miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="14fd6-220">Select **Demo** as the environment topology.</span></span>

    ![Valg af miljøtopologi 1](./media/project2.png)

1. <span data-ttu-id="14fd6-222">Vælg **Dynamics 365 Commerce - Demo** som miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="14fd6-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="14fd6-223">Hvis du har konfigureret en enkelt Azure Connector tidligere, bruges denne til dette miljø.</span><span class="sxs-lookup"><span data-stu-id="14fd6-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="14fd6-224">Hvis du har konfigureret flere Azure Connector'er, kan du vælge, hvilken connector der skal bruges: **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="14fd6-225">(For at opnå den bedste altomfattende præstation anbefaler vi, at du vælger **Det vestlige USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="14fd6-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Valg af miljøtopologi 2](./media/project3.png)

1. <span data-ttu-id="14fd6-227">Angiv et miljønavn på side **Installer miljø**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="14fd6-228">Lad de avancerede indstillinger være, som de er.</span><span class="sxs-lookup"><span data-stu-id="14fd6-228">Leave the advanced settings as they are.</span></span>

    ![Siden Installer miljø](./media/project4.png)

1. <span data-ttu-id="14fd6-230">Juster VM-størrelsen efter behov.</span><span class="sxs-lookup"><span data-stu-id="14fd6-230">Adjust the VM size as required.</span></span> <span data-ttu-id="14fd6-231">(Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)</span><span class="sxs-lookup"><span data-stu-id="14fd6-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="14fd6-232">Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.</span><span class="sxs-lookup"><span data-stu-id="14fd6-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="14fd6-233">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-233">Select **Next**.</span></span>
1. <span data-ttu-id="14fd6-234">Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="14fd6-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="14fd6-235">Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="14fd6-236">Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation.</span><span class="sxs-lookup"><span data-stu-id="14fd6-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="14fd6-237">Det vil tage nogen tid at fuldføre miljø arbejdsgangene.</span><span class="sxs-lookup"><span data-stu-id="14fd6-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="14fd6-238">Kom derfor tilbage efter ca. seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="14fd6-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="14fd6-239">Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="14fd6-240">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="14fd6-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="14fd6-241">Følg disse trin for at påbegynde CSU.</span><span class="sxs-lookup"><span data-stu-id="14fd6-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-242">Vælg dit miljø på listen i visningen **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="14fd6-243">Vælg **Alle detaljer** i miljøvisningen til højre.</span><span class="sxs-lookup"><span data-stu-id="14fd6-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="14fd6-244">Visningen med miljødetaljer vises.</span><span class="sxs-lookup"><span data-stu-id="14fd6-244">The environment details view appears.</span></span>
1. <span data-ttu-id="14fd6-245">Under **Miljøfunktioner** skal du vælge **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="14fd6-246">På fanen **Commerce** skal du vælge **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="14fd6-247">CSU-initialiseringsparametrene bliver vist.</span><span class="sxs-lookup"><span data-stu-id="14fd6-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="14fd6-248">I feltet **Tegion** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="14fd6-249">I feltet **Version** skal du vælge **Angiv en Version** på listen og derefter angive **9.18.20014.4** i det felt, der vises.</span><span class="sxs-lookup"><span data-stu-id="14fd6-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="14fd6-250">Sørg for at angive den nøjagtige version, der er angivet her.</span><span class="sxs-lookup"><span data-stu-id="14fd6-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="14fd6-251">Ellers skal du opdatere RCSU til den korrekte version senere.</span><span class="sxs-lookup"><span data-stu-id="14fd6-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="14fd6-252">Aktivér indstillingen **Anvend udvidelse**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="14fd6-253">Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over udvidelser.</span><span class="sxs-lookup"><span data-stu-id="14fd6-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="14fd6-254">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="14fd6-255">Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="14fd6-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="14fd6-256">Visningen **Commerce-administration** vises igen, hvor fanen **Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="14fd6-257">Din CSU er sat i kø til klargøring.</span><span class="sxs-lookup"><span data-stu-id="14fd6-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="14fd6-258">Før du fortsætter, skal du kontrollere, at din statussen for dit CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="14fd6-259">Initialiseringen tager ca. to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="14fd6-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="14fd6-260">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="14fd6-260">Initialize e-Commerce</span></span>

<span data-ttu-id="14fd6-261">Følg disse trin for at påbegynde e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="14fd6-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="14fd6-262">Under fanen **e-Commerce** skal du gennemgå samtykket for prøveversionen og derefter vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="14fd6-263">Angiv et navn for **e-Commerce-lejernavn** i feltet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="14fd6-264">Bemærk dog, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.</span><span class="sxs-lookup"><span data-stu-id="14fd6-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="14fd6-265">I feltet **Commerce Scale Unit-navn** skal du vælge din CSU på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="14fd6-266">(Listen bør kun have én indstilling.)</span><span class="sxs-lookup"><span data-stu-id="14fd6-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="14fd6-267">Feltet **e-Commerce-geografi** angives automatisk, og værdien kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="14fd6-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="14fd6-268">Vælg **Næste** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="14fd6-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="14fd6-269">I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="14fd6-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="14fd6-270">I feltet **AAD-sikkerhedsgruppe for systemadministrator** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge.</span><span class="sxs-lookup"><span data-stu-id="14fd6-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="14fd6-271">Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="14fd6-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="14fd6-272">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="14fd6-273">I feltet **AAD-sikkerhedsgruppen for redaktører for vurderinger og anmeldelser** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge.</span><span class="sxs-lookup"><span data-stu-id="14fd6-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="14fd6-274">Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="14fd6-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="14fd6-275">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="14fd6-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="14fd6-276">Lad indstillingen **Aktivér tjenesten vurderinger og anmeldelser** være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="14fd6-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="14fd6-277">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-277">Select **Initialize**.</span></span> <span data-ttu-id="14fd6-278">Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="14fd6-279">Din initialisering af e-Commerce er påbegyndt.</span><span class="sxs-lookup"><span data-stu-id="14fd6-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="14fd6-280">Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.</span><span class="sxs-lookup"><span data-stu-id="14fd6-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="14fd6-281">Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:</span><span class="sxs-lookup"><span data-stu-id="14fd6-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="14fd6-282">**e-Commerce-websted** – linket til roden af dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="14fd6-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="14fd6-283">**Værktøj til administration af e-Commerce-websted** – linket til administrationsværktøjet for webstedet.</span><span class="sxs-lookup"><span data-stu-id="14fd6-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="14fd6-284">Support til Commerce-prøveversionsmiljøet</span><span class="sxs-lookup"><span data-stu-id="14fd6-284">Commerce preview environment support</span></span>

<span data-ttu-id="14fd6-285">Hvis der opstår problemer under din fuldførelse af klargøringstrinnene, kan du gå til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="14fd6-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="14fd6-286">Næste trin</span><span class="sxs-lookup"><span data-stu-id="14fd6-286">Next steps</span></span>

<span data-ttu-id="14fd6-287">For at fortsætte processen med klargøring og konfigurering af dit Commerce-prøveversionsmiljø se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="14fd6-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14fd6-288">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="14fd6-288">Additional resources</span></span>

[<span data-ttu-id="14fd6-289">Oversigt over Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="14fd6-290">Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="14fd6-291">Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="14fd6-292">Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="14fd6-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="14fd6-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="14fd6-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="14fd6-294">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="14fd6-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="14fd6-295">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="14fd6-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="14fd6-296">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="14fd6-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

