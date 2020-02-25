---
title: Eksportere data fra Attract og Onboard
description: Eksportere data fra Dynamics 365 Talent - Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975928"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="9d677-103">Eksportere data fra Attract og Onboard</span><span class="sxs-lookup"><span data-stu-id="9d677-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d677-104">Som annonceret i [Tilbagetrækningen af Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) tilbagetrækker vi Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard d. 1. februar 2022.</span><span class="sxs-lookup"><span data-stu-id="9d677-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="9d677-105">Begge apps kan nu tilbyde funktioner til dataeksport for at hjælpe med migreringen til et andet produkt.</span><span class="sxs-lookup"><span data-stu-id="9d677-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="9d677-106">Eksportér data fra Attract</span><span class="sxs-lookup"><span data-stu-id="9d677-106">Export data from Attract</span></span>

<span data-ttu-id="9d677-107">Du kan eksportere dine data uden at begrænse adgangen til dit miljø.</span><span class="sxs-lookup"><span data-stu-id="9d677-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="9d677-108">Det kan være en god ide at gøre dette med henblik på test eller for at forstå vores datastruktur.</span><span class="sxs-lookup"><span data-stu-id="9d677-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="9d677-109">Når du er klar til at overføre, skal du begrænse adgangen til dit Attract-miljø vha. instruktionerne efter denne procedure.</span><span class="sxs-lookup"><span data-stu-id="9d677-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="9d677-110">Sørg for at eksportere dataene igen.</span><span class="sxs-lookup"><span data-stu-id="9d677-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="9d677-111">Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="9d677-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="9d677-112">Vælg **Anmod om en dataeksport** under **Dataeksport**.</span><span class="sxs-lookup"><span data-stu-id="9d677-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="9d677-113">Anmode om en dataeksport fra Attract</span><span class="sxs-lookup"><span data-stu-id="9d677-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="9d677-114">Når meddelelsen **Din anmodning behandles**, skal du klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d677-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="9d677-115">Dataeksporten kan vare op til 20 minutter, afhængigt af eksportens størrelsen.</span><span class="sxs-lookup"><span data-stu-id="9d677-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="9d677-116">Når eksporten er fuldført, skal du vælge knappen **Download** ud for den.</span><span class="sxs-lookup"><span data-stu-id="9d677-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="9d677-117">Alle dataeksporter er tilgængelige i syv dage, hvorefter linket **Download** udløber.</span><span class="sxs-lookup"><span data-stu-id="9d677-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="9d677-118">Downloaden indeholder en .zip-fil med dine Attract-data, herunder følgende mapper:</span><span class="sxs-lookup"><span data-stu-id="9d677-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="9d677-119">Mappenavn</span><span class="sxs-lookup"><span data-stu-id="9d677-119">Folder name</span></span> | <span data-ttu-id="9d677-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="9d677-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="9d677-121">Administratorindstillinger</span><span class="sxs-lookup"><span data-stu-id="9d677-121">Admin settings</span></span> | <span data-ttu-id="9d677-122">Konfigurationer af Attract-administrationscenter.</span><span class="sxs-lookup"><span data-stu-id="9d677-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="9d677-123">Kandidater</span><span class="sxs-lookup"><span data-stu-id="9d677-123">Candidates</span></span> | <span data-ttu-id="9d677-124">Alle kandidater, der er føjet til job eller talentpuljer.</span><span class="sxs-lookup"><span data-stu-id="9d677-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="9d677-125">Mailskabeloner</span><span class="sxs-lookup"><span data-stu-id="9d677-125">Email templates</span></span> | <span data-ttu-id="9d677-126">Alle mailskabeloner, der er konfigureret for miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d677-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="9d677-127">Skabeloner til jobtilbudspakker</span><span class="sxs-lookup"><span data-stu-id="9d677-127">Job offer package templates</span></span> | <span data-ttu-id="9d677-128">Alle job tilbyder pakkeskabeloner, der er oprettet, plus de tilknyttede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="9d677-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="9d677-129">Job, der tilbyder regelsæt</span><span class="sxs-lookup"><span data-stu-id="9d677-129">Job offer rule sets</span></span> |  <span data-ttu-id="9d677-130">Alle filer med regelsæt, der er uploadet til tilbudsstyring.</span><span class="sxs-lookup"><span data-stu-id="9d677-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="9d677-131">Skabeloner til jobtilbud</span><span class="sxs-lookup"><span data-stu-id="9d677-131">Job offer templates</span></span> | <span data-ttu-id="9d677-132">Alle jobtilbudsdokumentskabeloner, der er oprettet for miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d677-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="9d677-133">Jobtilbud</span><span class="sxs-lookup"><span data-stu-id="9d677-133">Job openings</span></span> | <span data-ttu-id="9d677-134">Alle oprettede job.</span><span class="sxs-lookup"><span data-stu-id="9d677-134">All created jobs.</span></span> <span data-ttu-id="9d677-135">Slettede job eksporteres ikke.</span><span class="sxs-lookup"><span data-stu-id="9d677-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="9d677-136">Undermapperne indeholder kandidatansøgninger med undermapper til vedhæftninger af kandidatansøgninger og tilbyder evt. pakker.</span><span class="sxs-lookup"><span data-stu-id="9d677-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="9d677-137">Skabeloner til jobtilbud</span><span class="sxs-lookup"><span data-stu-id="9d677-137">Job opening templates</span></span> | <span data-ttu-id="9d677-138">Skabeloner til jobtilbud, der er konfigureret i miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d677-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="9d677-139">Talentpuljer</span><span class="sxs-lookup"><span data-stu-id="9d677-139">Talent pools</span></span> | <span data-ttu-id="9d677-140">Alle oprettede talentpuljer, deres bidragyderelister og kandidatlister til talentgrupperne.</span><span class="sxs-lookup"><span data-stu-id="9d677-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="9d677-141">Arbejdere</span><span class="sxs-lookup"><span data-stu-id="9d677-141">Workers</span></span> | <span data-ttu-id="9d677-142">Liste over alle de arbejdere, der findes i miljøet, plus deres roller.</span><span class="sxs-lookup"><span data-stu-id="9d677-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="9d677-143">(rodmappe)</span><span class="sxs-lookup"><span data-stu-id="9d677-143">(root folder)</span></span> | <span data-ttu-id="9d677-144">En JSON-skemafil, der beskriver datastrukturfelterne.</span><span class="sxs-lookup"><span data-stu-id="9d677-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="9d677-145">Begræns adgangen til Attract</span><span class="sxs-lookup"><span data-stu-id="9d677-145">Restrict access to Attract</span></span>

<span data-ttu-id="9d677-146">Når du er klar til at overføre, skal du begrænse ikke-administratorer i at få adgang til dit Attract-miljø og eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="9d677-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="9d677-147">Begrænsning af adgangen til dit Attract-miljø er permanent og kan ikke fortrydes.</span><span class="sxs-lookup"><span data-stu-id="9d677-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="9d677-148">Hvis brugere uden administratorrettigheder fortsat skal have adgang til dit miljø, kan du springe dette trin over.</span><span class="sxs-lookup"><span data-stu-id="9d677-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="9d677-149">Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="9d677-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="9d677-150">Hvis du vil forhindre, at ikke-administratorer får adgang til dit Attract-miljø, skal du vælge **Begræns adgang nu** under **Begræns adgang nu til denne app**.</span><span class="sxs-lookup"><span data-stu-id="9d677-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="9d677-151">Hvis du begrænser adgangen, medfører det også, at aktive job, der er bogført, ikke bogføres.</span><span class="sxs-lookup"><span data-stu-id="9d677-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="9d677-152">Begræns ikke-administratoradgang til Attract</span><span class="sxs-lookup"><span data-stu-id="9d677-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="9d677-153">Når advarslen **Dette er en permanent ændringe** vises, skal du vælge **Begræns adgang** for permanent at begrænse brugere, der ikke er administratorer, ud af dette miljø.</span><span class="sxs-lookup"><span data-stu-id="9d677-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="9d677-154">Vælg **Annuller**, hvis du ikke er klar til at fuldføre dette trin.</span><span class="sxs-lookup"><span data-stu-id="9d677-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="9d677-155">Advarsel om, at begrænsende adgang er en permanent ændring</span><span class="sxs-lookup"><span data-stu-id="9d677-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="9d677-156">Administratorer kan fortsætte med at få adgang til dataeksport- og personrapportsiderne, når du har begrænset adgangen til Attract-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d677-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="9d677-157">Eksportér data fra Onboard</span><span class="sxs-lookup"><span data-stu-id="9d677-157">Export data from Onboard</span></span>

<span data-ttu-id="9d677-158">Når du er klar, kan du downloade skabeloner, guider og kandidatdata fra Onboard.</span><span class="sxs-lookup"><span data-stu-id="9d677-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="9d677-159">Gå til [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="9d677-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="9d677-160">Vælg **Anmod om en dataeksport** under **Dataeksport**.</span><span class="sxs-lookup"><span data-stu-id="9d677-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="9d677-161">Anmode om en dataeksport fra Onboard</span><span class="sxs-lookup"><span data-stu-id="9d677-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="9d677-162">Når meddelelsen **Din anmodning behandles**, skal du klikke på **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d677-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="9d677-163">Dataeksporten kan vare op til 20 minutter, afhængigt af eksportens størrelsen.</span><span class="sxs-lookup"><span data-stu-id="9d677-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="9d677-164">Når eksporten er fuldført, skal du vælge knappen **Download** ud for den.</span><span class="sxs-lookup"><span data-stu-id="9d677-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="9d677-165">Download data, som er eksporteret fra Onboard</span><span class="sxs-lookup"><span data-stu-id="9d677-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="9d677-166">Dataeksporten er tilgængelig i syv dage.</span><span class="sxs-lookup"><span data-stu-id="9d677-166">Your data export is available for seven days.</span></span> <span data-ttu-id="9d677-167">Efter syv dage udløber linket **Download**, og du skal anmode om en ny eksport, hvis du har brug for at downloade dataene igen.</span><span class="sxs-lookup"><span data-stu-id="9d677-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="9d677-168">Når du starter en ny dataeksport, udløber eventuelle eksisterende downloads, efter at den nye eksport er fuldført.</span><span class="sxs-lookup"><span data-stu-id="9d677-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="9d677-169">Downloaden er en .zip-fil, der indeholder:</span><span class="sxs-lookup"><span data-stu-id="9d677-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="9d677-170">En **Skabelon**mappe, der indeholder dine indbyggede Onboard-skabeloner i Word-dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="9d677-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="9d677-171">En **Guides**mappe, der indeholder dine indbyggede Onboard-guides i Word-dokumentformat.</span><span class="sxs-lookup"><span data-stu-id="9d677-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d677-172">Se også</span><span class="sxs-lookup"><span data-stu-id="9d677-172">See also</span></span>

[<span data-ttu-id="9d677-173">Tilbagetrækning af Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apps</span><span class="sxs-lookup"><span data-stu-id="9d677-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)