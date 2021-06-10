---
title: Kopiér en forekomst
description: Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8961b7156f52e48dbfcf7efb14e50316e81fcfff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053677"
---
# <a name="copy-an-instance"></a><span data-ttu-id="3d5d1-103">Kopiér en forekomst</span><span class="sxs-lookup"><span data-stu-id="3d5d1-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3d5d1-104">Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="3d5d1-105">Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="3d5d1-106">Hvis du vil kopiere en forekomst, skal du huske at følge nedenstående tip:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="3d5d1-107">Den forekomst af Human Resources, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="3d5d1-108">De miljøer, du kopierer fra og til, skal være i samme område.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="3d5d1-109">Du kan ikke kopiere på tværs af områder.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-109">You can't copy across regions.</span></span>

- <span data-ttu-id="3d5d1-110">Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="3d5d1-111">Når du kopierer Human Resources-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="3d5d1-112">Yderligere oplysninger om kopiering af elementer i et Power Apps-miljø finder du i [Kopiere et miljø](/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="3d5d1-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="3d5d1-113">Det Power Apps-miljø, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="3d5d1-114">Du skal være global lejeradministrator for at kunne ændre et Power Apps-produktionsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="3d5d1-115">Yderligere oplysninger om ændring af et Power Apps-miljø finder du [Skifte en forekomst](/dynamics365/admin/switch-instance)forekomst.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-115">For more information about changing a Power Apps environment, see [Switch an instance](/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="3d5d1-116">Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Dataverse, skal du genanvende brugerdefinerede felter på Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="3d5d1-117">Se [Anvende brugerdefinerede felter i Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="3d5d1-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="3d5d1-118">Virkninger af kopiering af en Human Resources-database</span><span class="sxs-lookup"><span data-stu-id="3d5d1-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="3d5d1-119">Følgende hændelser indtræffer, når du kopierer en Human Resources-database:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="3d5d1-120">Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="3d5d1-121">Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="3d5d1-122">Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="3d5d1-123">Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="3d5d1-124">Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="3d5d1-125">Alle brugere undtagen administratorbrugere og andre interne tjenestebrugerkonti er derfor ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="3d5d1-126">Administratorbrugeren kan derfor slette eller sløre data, før andre brugere får adgang til systemet igen.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="3d5d1-127">Administratorbrugeren skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="3d5d1-128">Kopiere Human Resources-databasen</span><span class="sxs-lookup"><span data-stu-id="3d5d1-128">Copy the Human Resources database</span></span>

<span data-ttu-id="3d5d1-129">Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="3d5d1-130">Når du kopierer en forekomst, slettes databasen i destinationsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="3d5d1-131">Destinationsforekomsten er ikke tilgængelig under denne proces.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="3d5d1-132">Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="3d5d1-133">I LCS-projektet skal du vælge feltet **Administration af Human Resources-app**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="3d5d1-134">Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="3d5d1-135">I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="3d5d1-136">Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="3d5d1-137">Vælg forekomst, der skal overskrives</span><span class="sxs-lookup"><span data-stu-id="3d5d1-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="3d5d1-138">Vælg **Power Platform**, og log på Microsoft Power Platform Administration.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="3d5d1-139">Vælg Power Platform</span><span class="sxs-lookup"><span data-stu-id="3d5d1-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="3d5d1-140">Vælg det Power Apps-miljø, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="3d5d1-141">Når kopieringsprocessen er fuldført, skal du logge på destinationsforekomsten og aktivere Dataverse-integration.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="3d5d1-142">Du kan finde flere oplysninger og instruktioner under [Konfigurere Dataverse-integration](./hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="3d5d1-142">For more information and instructions, see [Configure Dataverse integration](./hr-admin-integration-common-data-service.md).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="3d5d1-143">Dataelementer og statusser</span><span class="sxs-lookup"><span data-stu-id="3d5d1-143">Data elements and statuses</span></span>

<span data-ttu-id="3d5d1-144">Følgende dataelementer kopieres ikke, når du kopierer en forekomst af Human Resources:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="3d5d1-145">E-mailadresser i tabellen **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="3d5d1-146">Historikken for batchjobbet i tabellerne **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="3d5d1-147">SMTP-adgangskoden (Simple Mail Transfer Protocol) i tabellen **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="3d5d1-148">SMTP-Relay-serveren i tabellen **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="3d5d1-149">Indstillinger for Udskriftsstyring i tabellerne **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="3d5d1-150">Miljøspecifikke poster i tabellerne **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="3d5d1-151">Vedhæftede dokumenter i tabellen DocuValue.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="3d5d1-152">Disse vedhæftede filer kan omfatte eventuelle Microsoft Office-skabeloner, der er overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="3d5d1-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="3d5d1-153">Forbindelsesstrengen i tabellen **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="3d5d1-154">Nogle af disse elementer kopieres ikke, fordi de er miljøspecifikke.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="3d5d1-155">Eksempler omfatter posterne **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="3d5d1-156">Andre elementer kopieres ikke på grund af antallet af supportanmodninger.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="3d5d1-157">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-157">For example:</span></span>

- <span data-ttu-id="3d5d1-158">Der kan sendes duplikerede mails, fordi SMTP stadig er aktiveret i miljøet til test af brugeraccept (sandkasse).</span><span class="sxs-lookup"><span data-stu-id="3d5d1-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="3d5d1-159">Der kan sendes ugyldige integrationsmeddelelser, fordi batchjobbene stadig er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="3d5d1-160">Brugere kan være aktiveret, før administratorer kan udføre oprydningshandlinger efter opdatering.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="3d5d1-161">Følgende statusser ændres også, når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="3d5d1-162">Alle brugere undtagen administrator angives til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="3d5d1-163">Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**</span><span class="sxs-lookup"><span data-stu-id="3d5d1-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="3d5d1-164">Miljøadmin</span><span class="sxs-lookup"><span data-stu-id="3d5d1-164">Environment admin</span></span>

<span data-ttu-id="3d5d1-165">Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="3d5d1-166">Før du kopierer en forekomst, skal du sikre dig, at du er administrator i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="3d5d1-167">Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="3d5d1-168">Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="3d5d1-169">Administratorer kan genaktivere brugerne, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="3d5d1-170">Anvende brugerdefinerede felter i Dataverse</span><span class="sxs-lookup"><span data-stu-id="3d5d1-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="3d5d1-171">Hvis du kopierer en forekomst til dit sandkassemiljø og vil integrere dit sandkassemiljø med Dataverse, skal du genanvende brugerdefinerede felter på Dataverse-tabeller.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="3d5d1-172">Udfør følgende trin for hvert brugerdefineret felt, der vises i Dataverse-tabeller:</span><span class="sxs-lookup"><span data-stu-id="3d5d1-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="3d5d1-173">Gå til det brugerdefinerede felt, og vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="3d5d1-174">Fjern markeringen i feltet **Aktiveret** for hver cdm_\*-enhed, som det brugerdefinerede felt er aktiveret i.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="3d5d1-175">Vælg **Anvend ændringer**.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="3d5d1-176">Vælg **Rediger** igen.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="3d5d1-177">Vælg feltet **Aktiveret** for hver cdm_\*-enhed, som det brugerdefinerede felt er aktiveret i.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="3d5d1-178">Vælg **Anvend ændringer** igen.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="3d5d1-179">Ved at fravælge, anvende ændringer, vælge igen og genanvende ændringer vil det skema, der opdateres i Dataverse, indeholde de brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="3d5d1-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="3d5d1-180">Du kan finde flere oplysninger om brugerdefinerede felter under [Oprette og arbejde med brugerdefinerede felter](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span><span class="sxs-lookup"><span data-stu-id="3d5d1-180">For more information about custom fields, see [Create and work with custom fields](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d5d1-181">Se også</span><span class="sxs-lookup"><span data-stu-id="3d5d1-181">See also</span></span>

[<span data-ttu-id="3d5d1-182">Klargør Human Resources</span><span class="sxs-lookup"><span data-stu-id="3d5d1-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="3d5d1-183">Fjern en forekomst</span><span class="sxs-lookup"><span data-stu-id="3d5d1-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="3d5d1-184">Opdater proces</span><span class="sxs-lookup"><span data-stu-id="3d5d1-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]