---
title: Kopiér en forekomst
description: Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092286"
---
# <a name="copy-an-instance"></a><span data-ttu-id="82de4-103">Kopiér en forekomst</span><span class="sxs-lookup"><span data-stu-id="82de4-103">Copy an instance</span></span>

<span data-ttu-id="82de4-104">Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="82de4-105">Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="82de4-106">Hvis du vil kopiere en forekomst, skal du sikre dig følgende:</span><span class="sxs-lookup"><span data-stu-id="82de4-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="82de4-107">Den forekomst af Personale, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="82de4-108">De miljøer, du kopierer fra og til, skal være i samme område.</span><span class="sxs-lookup"><span data-stu-id="82de4-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="82de4-109">Du kan ikke kopiere på tværs af områder.</span><span class="sxs-lookup"><span data-stu-id="82de4-109">You can't copy across regions.</span></span>

- <span data-ttu-id="82de4-110">Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.</span><span class="sxs-lookup"><span data-stu-id="82de4-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="82de4-111">Når du kopierer Personale-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="82de4-112">Yderligere oplysninger om kopiering af elementer i et PowerApps-miljø finder du i [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="82de4-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="82de4-113">Det PowerApps-miljø, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="82de4-114">Du skal være global lejeradministrator for at kunne ændre et PowerApps-produktionsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="82de4-115">Yderligere oplysninger om ændring af et PowerApps-miljø finder du [Skifte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance)forekomst.</span><span class="sxs-lookup"><span data-stu-id="82de4-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="82de4-116">Virkninger af kopiering af en Personale-database</span><span class="sxs-lookup"><span data-stu-id="82de4-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="82de4-117">Følgende hændelser indtræffer, når du kopierer en Personale-database:</span><span class="sxs-lookup"><span data-stu-id="82de4-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="82de4-118">Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="82de4-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="82de4-119">Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.</span><span class="sxs-lookup"><span data-stu-id="82de4-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="82de4-120">Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="82de4-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="82de4-121">Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet.</span><span class="sxs-lookup"><span data-stu-id="82de4-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="82de4-122">Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="82de4-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="82de4-123">Alle brugere undtagen administratorbrugere og andre interne tjenestebrugerkonti er derfor ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="82de4-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="82de4-124">Administratorbrugeren kan derfor slette eller sløre data, før andre brugere får adgang til systemet igen.</span><span class="sxs-lookup"><span data-stu-id="82de4-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="82de4-125">Administratorbrugeren skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="82de4-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="82de4-126">Kopiere Personale-databasen</span><span class="sxs-lookup"><span data-stu-id="82de4-126">Copy the Human Resources database</span></span>

<span data-ttu-id="82de4-127">Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="82de4-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="82de4-128">Når du kopierer en forekomst, slettes databasen i destinationsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="82de4-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="82de4-129">Destinationsforekomsten er ikke tilgængelig under denne proces.</span><span class="sxs-lookup"><span data-stu-id="82de4-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="82de4-130">Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="82de4-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="82de4-131">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="82de4-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="82de4-132">Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="82de4-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="82de4-133">I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="82de4-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="82de4-134">Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="82de4-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="82de4-135">Vælg en forekomst, der skal overskrives</span><span class="sxs-lookup"><span data-stu-id="82de4-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="82de4-136">Vælg **Power Platform**, og log på Microsoft Power Platform Administration.</span><span class="sxs-lookup"><span data-stu-id="82de4-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="82de4-137">Vælg Power Platform</span><span class="sxs-lookup"><span data-stu-id="82de4-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="82de4-138">Vælg det PowerApps-miljø, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="82de4-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="82de4-139">Når kopieringsprocessen er fuldført, skal du logge på destinationsforekomsten og aktivere Common Data Service-integration.</span><span class="sxs-lookup"><span data-stu-id="82de4-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="82de4-140">Du kan finde flere oplysninger og instruktioner under [Konfigurere Common Data Service-integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="82de4-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="82de4-141">Dataelementer og statusser</span><span class="sxs-lookup"><span data-stu-id="82de4-141">Data elements and statuses</span></span>

<span data-ttu-id="82de4-142">Følgende dataelementer kopieres ikke, når du kopierer en forekomst af Personale:</span><span class="sxs-lookup"><span data-stu-id="82de4-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="82de4-143">E-mailadresser i tabellen **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="82de4-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="82de4-144">Historikken for batchjobbet i tabellerne **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="82de4-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="82de4-145">SMTP-adgangskoden (Simple Mail Transfer Protocol) i tabellen **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="82de4-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="82de4-146">SMTP-Relay-serveren i tabellen **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="82de4-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="82de4-147">Indstillinger for Udskriftsstyring i tabellerne **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="82de4-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="82de4-148">Miljøspecifikke poster i tabellerne **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="82de4-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="82de4-149">Vedhæftede dokumenter i tabellen DocuValue.</span><span class="sxs-lookup"><span data-stu-id="82de4-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="82de4-150">Disse vedhæftede filer kan omfatte eventuelle Microsoft Office-skabeloner, der er overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="82de4-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="82de4-151">Forbindelsesstrengen i tabellen **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="82de4-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="82de4-152">Nogle af disse elementer kopieres ikke, fordi de er miljøspecifikke.</span><span class="sxs-lookup"><span data-stu-id="82de4-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="82de4-153">Eksempler omfatter posterne **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="82de4-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="82de4-154">Andre elementer kopieres ikke på grund af antallet af supportanmodninger.</span><span class="sxs-lookup"><span data-stu-id="82de4-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="82de4-155">Der kan f.eks. sendes duplikerede e-mails, fordi SMTP stadig er aktiveret i testmiljøet til brugeraccept (sandkasse), der kan blive sendt ugyldige integrationsmeddelelser, fordi batchjobbene stadig er aktiveret, og brugerne kan være aktiverede, før administratorer kan udføre handlinger til oprydning efter opdatering.</span><span class="sxs-lookup"><span data-stu-id="82de4-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="82de4-156">Følgende statusser ændres desuden, når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="82de4-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="82de4-157">Alle brugere undtagen administrator angives til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="82de4-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="82de4-158">Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**</span><span class="sxs-lookup"><span data-stu-id="82de4-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="82de4-159">Miljøadmin</span><span class="sxs-lookup"><span data-stu-id="82de4-159">Environment admin</span></span>

<span data-ttu-id="82de4-160">Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="82de4-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="82de4-161">Før du kopierer en forekomst, skal du sikre dig, at du er administrator i destinationsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="82de4-161">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="82de4-162">Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="82de4-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="82de4-163">Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="82de4-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="82de4-164">Administratorer kan genaktivere brugerne, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="82de4-164">Administrators can reenable users if needed.</span></span>
