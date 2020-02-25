---
title: Kopiér en forekomst
description: ''
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
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008440"
---
# <a name="copy-an-instance"></a><span data-ttu-id="0566b-102">Kopiér en forekomst</span><span class="sxs-lookup"><span data-stu-id="0566b-102">Copy an instance</span></span>

<span data-ttu-id="0566b-103">Du kan bruge Microsoft Dynamics Lifecycle Services (LCS) til at kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="0566b-104">Hvis du har et andet sandkasse-miljø, kan du også kopiere databasen fra det pågældende miljø til et målrettet sandkasse-miljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="0566b-105">Hvis du vil kopiere en forekomst, skal du sikre dig følgende:</span><span class="sxs-lookup"><span data-stu-id="0566b-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="0566b-106">Den forekomst af Personale, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="0566b-107">De miljøer, du kopierer fra og til, skal være i samme område.</span><span class="sxs-lookup"><span data-stu-id="0566b-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="0566b-108">Du kan ikke kopiere på tværs af områder.</span><span class="sxs-lookup"><span data-stu-id="0566b-108">You can't copy across regions.</span></span>

- <span data-ttu-id="0566b-109">Du skal være administrator i destinationsmiljøet, så du kan logge på, når du har kopieret forekomsten.</span><span class="sxs-lookup"><span data-stu-id="0566b-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="0566b-110">Når du kopierer Personale-databasen, kopierer du ikke de elementer (apps eller data), der er indeholdt i et Microsoft PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="0566b-111">Yderligere oplysninger om kopiering af elementer i et PowerApps-miljø finder du i [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="0566b-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="0566b-112">Det PowerApps-miljø, du vil overskrive, skal være et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="0566b-113">Du skal være global lejeradministrator for at kunne ændre et PowerApps-produktionsmiljø til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="0566b-114">Yderligere oplysninger om ændring af et PowerApps-miljø finder du [Skifte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance)forekomst.</span><span class="sxs-lookup"><span data-stu-id="0566b-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="0566b-115">Virkninger af kopiering af en Personale-database</span><span class="sxs-lookup"><span data-stu-id="0566b-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="0566b-116">Følgende hændelser indtræffer, når du kopierer en Personale-database:</span><span class="sxs-lookup"><span data-stu-id="0566b-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="0566b-117">Kopieringsprocessen sletter den eksisterende database i destinationsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="0566b-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="0566b-118">Når kopieringsprocessen er fuldført, kan du ikke gendanne den eksisterende database.</span><span class="sxs-lookup"><span data-stu-id="0566b-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="0566b-119">Destinationsmiljøet vil ikke være tilgængeligt, før kopieringsprocessen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="0566b-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="0566b-120">Dokumenter i Microsoft Azure Blob-lager kopieres ikke fra ét miljø til et andet.</span><span class="sxs-lookup"><span data-stu-id="0566b-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="0566b-121">Eventuelle dokumenter og skabeloner, der er vedhæftet, kopieres derfor ikke men forbliver i kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0566b-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="0566b-122">Alle brugere undtagen administratorbrugere og andre interne tjenestebrugerkonti er derfor ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="0566b-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="0566b-123">Administratorbrugeren kan derfor slette eller sløre data, før andre brugere får adgang til systemet igen.</span><span class="sxs-lookup"><span data-stu-id="0566b-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="0566b-124">Administratorbrugeren skal foretage påkrævede konfigurationsændringer, f.eks. genoprette forbindelse mellem integrationsslutpunkter og bestemte tjenester eller URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="0566b-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="0566b-125">Kopiere Personale-databasen</span><span class="sxs-lookup"><span data-stu-id="0566b-125">Copy the Human Resources database</span></span>

<span data-ttu-id="0566b-126">Hvis du vil fuldføre denne opgave, skal du først kopiere en forekomst og derefter logge på Microsoft Power Platform Administration for at kopiere dit PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="0566b-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="0566b-127">Når du kopierer en forekomst, slettes databasen i destinationsforekomsten.</span><span class="sxs-lookup"><span data-stu-id="0566b-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="0566b-128">Destinationsforekomsten er ikke tilgængelig under denne proces.</span><span class="sxs-lookup"><span data-stu-id="0566b-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="0566b-129">Log på LCS, og vælg det LCS-projekt, der indeholder den forekomst, du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="0566b-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="0566b-130">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="0566b-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="0566b-131">Vælg den forekomst, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0566b-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="0566b-132">I opgaveruden **Kopier en forekomst** skal du markere den forekomst, der skal overskrives, og derefter vælge **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0566b-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="0566b-133">Vent, indtil værdien i feltet **Kopieringsstatus** opdateres til **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="0566b-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="0566b-134">Vælg forekomst, der skal overskrives</span><span class="sxs-lookup"><span data-stu-id="0566b-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="0566b-135">Vælg **Power Platform**, og log på Microsoft Power Platform Administration.</span><span class="sxs-lookup"><span data-stu-id="0566b-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="0566b-136">Vælg Power Platform</span><span class="sxs-lookup"><span data-stu-id="0566b-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="0566b-137">Vælg det PowerApps-miljø, der skal kopieres, og vælg derefter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="0566b-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="0566b-138">Når kopieringsprocessen er fuldført, skal du logge på destinationsforekomsten og aktivere Common Data Service-integration.</span><span class="sxs-lookup"><span data-stu-id="0566b-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="0566b-139">Du kan finde flere oplysninger og instruktioner under [Konfigurere Common Data Service-integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="0566b-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="0566b-140">Dataelementer og statusser</span><span class="sxs-lookup"><span data-stu-id="0566b-140">Data elements and statuses</span></span>

<span data-ttu-id="0566b-141">Følgende dataelementer kopieres ikke, når du kopierer en forekomst af Personale:</span><span class="sxs-lookup"><span data-stu-id="0566b-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="0566b-142">E-mailadresser i tabellen **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="0566b-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="0566b-143">Historikken for batchjobbet i tabellerne **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="0566b-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="0566b-144">SMTP-adgangskoden (Simple Mail Transfer Protocol) i tabellen **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="0566b-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="0566b-145">SMTP-Relay-serveren i tabellen **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="0566b-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="0566b-146">Indstillinger for Udskriftsstyring i tabellerne **PrintMgmtSettings** og **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="0566b-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="0566b-147">Miljøspecifikke poster i tabellerne **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="0566b-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="0566b-148">Vedhæftede dokumenter i tabellen DocuValue.</span><span class="sxs-lookup"><span data-stu-id="0566b-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="0566b-149">Disse vedhæftede filer kan omfatte eventuelle Microsoft Office-skabeloner, der er overskrevet i kildemiljøet</span><span class="sxs-lookup"><span data-stu-id="0566b-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="0566b-150">Forbindelsesstrengen i tabellen **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="0566b-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="0566b-151">Nogle af disse elementer kopieres ikke, fordi de er miljøspecifikke.</span><span class="sxs-lookup"><span data-stu-id="0566b-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="0566b-152">Eksempler omfatter posterne **BatchServerConfig** og **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="0566b-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="0566b-153">Andre elementer kopieres ikke på grund af antallet af supportanmodninger.</span><span class="sxs-lookup"><span data-stu-id="0566b-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="0566b-154">Der kan f.eks. sendes duplikerede e-mails, fordi SMTP stadig er aktiveret i testmiljøet til brugeraccept (sandkasse), der kan blive sendt ugyldige integrationsmeddelelser, fordi batchjobbene stadig er aktiveret, og brugerne kan være aktiverede, før administratorer kan udføre handlinger til oprydning efter opdatering.</span><span class="sxs-lookup"><span data-stu-id="0566b-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="0566b-155">Følgende statusser ændres desuden, når du kopierer en forekomst:</span><span class="sxs-lookup"><span data-stu-id="0566b-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="0566b-156">Alle brugere undtagen administrator angives til **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="0566b-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="0566b-157">Alle batchjob, bortset fra visse systemjob, angives til **Tilbagehold.**</span><span class="sxs-lookup"><span data-stu-id="0566b-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="0566b-158">Miljøadmin</span><span class="sxs-lookup"><span data-stu-id="0566b-158">Environment admin</span></span>

<span data-ttu-id="0566b-159">Alle brugere i destinationens sandkassemiljøet, herunder administratorer, erstattes af brugerne af kildemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0566b-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="0566b-160">Før du kopierer en forekomst, skal du sikre dig, at du er administrator i destinationsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="0566b-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="0566b-161">Er du ikke det, kan du ikke logge på destinationens sandkassemiljø, når kopieringen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="0566b-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="0566b-162">Alle brugere, der ikke er administratorer i destinationens sandkassemiljø, er deaktiveret for at forhindre uønsket logon i sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="0566b-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="0566b-163">Administratorer kan genaktivere brugerne, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="0566b-163">Administrators can reenable users if needed.</span></span>
