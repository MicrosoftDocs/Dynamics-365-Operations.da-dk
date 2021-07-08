---
title: Kom i gang med Global Inventory Accounting
description: Dette emne indeholder en beskrivelse af, hvordan du kommer i gang med Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301692"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="ad552-103">Kom i gang med Global Inventory Accounting</span><span class="sxs-lookup"><span data-stu-id="ad552-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="ad552-104">Med Global Inventory Accounting kan du udføre flere lagerregnskaber i de Global Inventory Accounting-finansposter, som du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="ad552-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="ad552-105">Du skal knytte hver Global Inventory Accounting-finanspost til et *princip*.</span><span class="sxs-lookup"><span data-stu-id="ad552-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="ad552-106">En konvention er en samling af følgende typer regnskabspolitikker:</span><span class="sxs-lookup"><span data-stu-id="ad552-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="ad552-107">Omkostningsobjekt</span><span class="sxs-lookup"><span data-stu-id="ad552-107">Cost object</span></span>
- <span data-ttu-id="ad552-108">Basis for inputmål</span><span class="sxs-lookup"><span data-stu-id="ad552-108">Input measurement basis</span></span>
- <span data-ttu-id="ad552-109">Forudsætning for omkostningsforløb</span><span class="sxs-lookup"><span data-stu-id="ad552-109">Cost flow assumption</span></span>
- <span data-ttu-id="ad552-110">Omkostningselement</span><span class="sxs-lookup"><span data-stu-id="ad552-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="ad552-111">Selv efter at du har slået Global Inventory Accounting til, kan du stadig udføre lagerregnskab i Microsoft Dynamics 365 Supply Chain Management, som du plejer.</span><span class="sxs-lookup"><span data-stu-id="ad552-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="ad552-112">Global Inventory Accounting er et tilføjelsesprogram.</span><span class="sxs-lookup"><span data-stu-id="ad552-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="ad552-113">For at gøre dets funktioner tilgængelige skal du installere det fra Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ad552-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ad552-114">Du kan vælge at evaluere det i et testmiljø, før du slår det til i produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="ad552-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="ad552-115">Global Inventory Accounting understøtter i øjeblikket ikke alle funktioner til omkostningsstyring, der er indbygget i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad552-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="ad552-116">Det er derfor vigtigt, at du evaluerer, om det funktionssæt, der aktuelt er tilgængeligt, opfylder dine behov.</span><span class="sxs-lookup"><span data-stu-id="ad552-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="ad552-117">Sådan får du en offentlig forhåndsversion af Global Inventory Accounting</span><span class="sxs-lookup"><span data-stu-id="ad552-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad552-118">Hvis du vil bruge Global Inventory Accounting, skal du have et LCS-aktiveret miljø med høj tilgængelighed (ikke et OneBox-miljø).</span><span class="sxs-lookup"><span data-stu-id="ad552-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="ad552-119">Derudover skal du køre Supply Chain Management version 10.0.19 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="ad552-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="ad552-120">Hvis du vil tilmelde dig en offentlig forhåndsversion af Global Inventory Accounting, skal du sende dit LCS-miljø-id via e-mail til [Global Inventory Accounting-teamet](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ad552-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="ad552-121">Når du er godkendt til programmet, sender teamet dig en opfølgningsmail, der indeholder nøglen til betaversionen af Global Inventory Accounting og dine tjenesteslutpunkter.</span><span class="sxs-lookup"><span data-stu-id="ad552-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="ad552-122">Når du har modtaget nøglen til betaversionen, kan du [installere tilføjelsesprogrammet](#install).</span><span class="sxs-lookup"><span data-stu-id="ad552-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="ad552-123">Licensering</span><span class="sxs-lookup"><span data-stu-id="ad552-123">Licensing</span></span>

<span data-ttu-id="ad552-124">Global Inventory Accounting er givet i licens sammen med standardfunktionerne i lagerregnskabet, der er tilgængelige for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad552-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="ad552-125">Du behøver ikke at købe en ekstra licens for at bruge Global Inventory Accounting.</span><span class="sxs-lookup"><span data-stu-id="ad552-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ad552-126">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="ad552-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="ad552-127">Konfigurer integration med Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="ad552-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="ad552-128">Før du kan aktivere tilføjelsesprogrammets funktioner, skal du integrere det med Microsoft Power Platform ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ad552-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="ad552-129">Åbn det LCS-miljø, hvor du vil tilføje tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ad552-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="ad552-130">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="ad552-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="ad552-131">I sektionen **Integration af Power Platform** skal du vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="ad552-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="ad552-132">I dialogboksen **Opsætning af Power Platform-miljø** skal du markere afkrydsningsfeltet og derefter vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="ad552-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="ad552-133">Det tager normalt mellem 60 og 90 minutter at udføre konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ad552-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="ad552-134">Når opsætningen af Microsoft Power Platform-miljøet er fuldført, vises navnet på miljøet på siden.</span><span class="sxs-lookup"><span data-stu-id="ad552-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="ad552-135">Sektionen **Power Platform-integration** viser desuden sætningen "Opsætning af Power Platform-miljøet er fuldført".</span><span class="sxs-lookup"><span data-stu-id="ad552-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="ad552-136">Global Inventory Accounting kræver ikke et program til dobbeltskrivning.</span><span class="sxs-lookup"><span data-stu-id="ad552-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="ad552-137">Du kan finde flere oplysninger i [Konfigurere efter installation af miljøet](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="ad552-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="ad552-138">Konfigurere Dataverse</span><span class="sxs-lookup"><span data-stu-id="ad552-138">Set up Dataverse</span></span>

<span data-ttu-id="ad552-139">Før du konfigurerer Dataverse, skal du føje Global Inventory Accounting-serviceprincipperne til din lejer ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ad552-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="ad552-140">Installer Azure AD-modul til Windows PowerShell v2 som beskrevet i [Installere Azure Active Directory PowerShell til Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="ad552-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="ad552-141">Kør følgende PowerShell-kommando.</span><span class="sxs-lookup"><span data-stu-id="ad552-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="ad552-142">Derefter skal du oprette programbrugere til Global Inventory Accounting i Dataverse ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ad552-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="ad552-143">Åbn URL-adressen til dit Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="ad552-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="ad552-144">Gå til **Avancerede indstillinger \> System \> Sikkerhed \> Brugere**, og opret en programbruger.</span><span class="sxs-lookup"><span data-stu-id="ad552-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="ad552-145">Brug feltet **Vis** til at ændre sidevisningen til *Applikationsbrugere*.</span><span class="sxs-lookup"><span data-stu-id="ad552-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="ad552-146">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ad552-146">Select **New**.</span></span>
1. <span data-ttu-id="ad552-147">Indstil feltet **Program-id** til *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="ad552-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="ad552-148">Vælg **Tildel rolle**, og vælg derefter *Systemadministrator*.</span><span class="sxs-lookup"><span data-stu-id="ad552-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="ad552-149">Hvis der er en rolle med navnet *Common Data Service Bruger*, skal du også vælge den.</span><span class="sxs-lookup"><span data-stu-id="ad552-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="ad552-150">Gentag de foregående trin, men angiv feltet **Program-id** til *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="ad552-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="ad552-151">Du kan finde flere oplysninger under [Oprette en programbruger](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="ad552-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="ad552-152">Hvis standardsproget for installationen af Dataverse ikke er engelsk, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ad552-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="ad552-153">Gå til **Avancerede indstillinger \> Administration \> Sprog**.</span><span class="sxs-lookup"><span data-stu-id="ad552-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="ad552-154">Vælg *Engelsk* (*LanguageCode=1033*), og vælg derefter **Anvend**.</span><span class="sxs-lookup"><span data-stu-id="ad552-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="ad552-155">Installer tilføjelsesprogrammet</span><span class="sxs-lookup"><span data-stu-id="ad552-155">Install the add-in</span></span>

<span data-ttu-id="ad552-156">Benyt følgende fremgangsmåde for at installere tilføjelsesprogrammet, så du kan bruge Global Inventory Accounting.</span><span class="sxs-lookup"><span data-stu-id="ad552-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="ad552-157">[Tilmeld dig](#sign-up) den offentlige forhåndsversion af Global Inventory Accounting.</span><span class="sxs-lookup"><span data-stu-id="ad552-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="ad552-158">Log på [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="ad552-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="ad552-159">Gå til **Styring af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="ad552-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="ad552-160">Vælg plustegnet (**+**).</span><span class="sxs-lookup"><span data-stu-id="ad552-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="ad552-161">I feltet **Kode** skal du angive betanøglen til tilføjelsesprogrammet for Global Inventory Accounting.</span><span class="sxs-lookup"><span data-stu-id="ad552-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="ad552-162">(Du modtog nøglen pr. mail, da du tilmeldte dig).</span><span class="sxs-lookup"><span data-stu-id="ad552-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="ad552-163">Vælg **Ophæv blokering**.</span><span class="sxs-lookup"><span data-stu-id="ad552-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="ad552-164">Åbn det LCS-miljø, hvor du vil tilføje tjenesten.</span><span class="sxs-lookup"><span data-stu-id="ad552-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="ad552-165">Gå til **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="ad552-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="ad552-166">Gå til **Power Platform-integration**, og vælg **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="ad552-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="ad552-167">I dialogboksen **Opsætning af Power Platform-miljø** skal du markere afkrydsningsfeltet og derefter vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="ad552-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="ad552-168">Det tager normalt mellem 60 og 90 minutter at udføre konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="ad552-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="ad552-169">Når opsætningen af Microsoft Power Platform-miljøet er fuldført, skal du vælge **Installer et nyt tilføjelsesprogram** i oversigtspanelet **Miljøtilføjelsesprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="ad552-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="ad552-170">Vælg **Globalt lagerregnskab**.</span><span class="sxs-lookup"><span data-stu-id="ad552-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="ad552-171">Følg installationsvejledningen, og accepter vilkårene og betingelserne.</span><span class="sxs-lookup"><span data-stu-id="ad552-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="ad552-172">Vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="ad552-172">Select **Install**.</span></span>
1. <span data-ttu-id="ad552-173">I oversigtspanelet **Miljøtilføjelsesprogrammer** kan du se, at Global Inventory Accounting er ved at blive installeret.</span><span class="sxs-lookup"><span data-stu-id="ad552-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="ad552-174">Efter nogle få minutter skal status ændres fra *Installerer* til *Installeret*.</span><span class="sxs-lookup"><span data-stu-id="ad552-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="ad552-175">(Du skal muligvis opdatere siden for at se ændringen). På dette tidspunkt er Global Inventory Accounting klar til brug.</span><span class="sxs-lookup"><span data-stu-id="ad552-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="ad552-176">Konfigurere integrationen</span><span class="sxs-lookup"><span data-stu-id="ad552-176">Set up the integration</span></span>

<span data-ttu-id="ad552-177">Følg disse trin for at konfigurere integrationen mellem Global Inventory Accounting og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad552-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="ad552-178">Log på Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ad552-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="ad552-179">Gå til **Systemadministration \> Funktionsstyring**.</span><span class="sxs-lookup"><span data-stu-id="ad552-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="ad552-180">Vælg **Søg efter opdateringer**.</span><span class="sxs-lookup"><span data-stu-id="ad552-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="ad552-181">Søg efter den funktion, der kaldes *Globalt lagerregnskab*, under fanen **Alle**.</span><span class="sxs-lookup"><span data-stu-id="ad552-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="ad552-182">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="ad552-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="ad552-183">Gå til **Globalt lagerregnskab \> Opsætning \> Parametre for globalt lagerregnskab \> Integrationsparametre**.</span><span class="sxs-lookup"><span data-stu-id="ad552-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="ad552-184">I felterne **Datatjenesteslutpunkt** og **Slutpunkt for globalt lagerregnskab** skal du angive URL-adresserne fra den mail, som Global Inventory Accounting-teamet sendte, da du tilmeldte dig forhåndsversionen.</span><span class="sxs-lookup"><span data-stu-id="ad552-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="ad552-185">Global Inventory Accounting er nu klar til brug.</span><span class="sxs-lookup"><span data-stu-id="ad552-185">Global Inventory Accounting is now ready to use.</span></span>
