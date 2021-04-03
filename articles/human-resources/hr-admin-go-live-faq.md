---
title: Ofte stillede spørgsmål om udgivelse
description: Dette emne indeholder ofte stillede spørgsmål om, hvordan du udgiver et Dynamics 365 Human Resources-implementeringsprojekt.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d667d94983d5c8f8e6140259922396d4299a15e3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467575"
---
# <a name="go-live-faq"></a><span data-ttu-id="1a511-103">Ofte stillede spørgsmål om udgivelse</span><span class="sxs-lookup"><span data-stu-id="1a511-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1a511-104">Dette emne indeholder ofte stillede spørgsmål om, hvordan du udgiver et Dynamics 365 Human Resources-implementeringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="1a511-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="1a511-105">Hvornår kan jeg konfigurere og anmode om mit produktionsmiljø?</span><span class="sxs-lookup"><span data-stu-id="1a511-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="1a511-106">Et produktionsmiljø kan i de fleste tilfælde implementeres, når følgende kriterier er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="1a511-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="1a511-107">Alle tilpasninger er code-complete (kræver ikke tilføjelse af helt ny kildekode).</span><span class="sxs-lookup"><span data-stu-id="1a511-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="1a511-108">Når test af brugeraccept (UAT) er fuldført.</span><span class="sxs-lookup"><span data-stu-id="1a511-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="1a511-109">Kunden har godkendt løsningen.</span><span class="sxs-lookup"><span data-stu-id="1a511-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="1a511-110">Ingen problemer blokerer for udgivelsen.</span><span class="sxs-lookup"><span data-stu-id="1a511-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="1a511-111">Når kvalificerede kunder er på dette trin, kan Microsoft FastTrack-teamet samarbejde med projektteamet om at foretage en udgivelsesvurdering.</span><span class="sxs-lookup"><span data-stu-id="1a511-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="1a511-112">Hvad er forudsætningerne for at implementere et produktionsmiljø?</span><span class="sxs-lookup"><span data-stu-id="1a511-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="1a511-113">Du kan se en liste over forudsætninger under  [Forberede til udgivelse](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="1a511-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="1a511-114">Hvad er en udgivelsesvurdering?</span><span class="sxs-lookup"><span data-stu-id="1a511-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="1a511-115">En udgivelsesvurdering er en del af  [Microsoft FastTrack-programmet](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="1a511-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="1a511-116">Under denne gennemgang vurderer en løsningsarkitekt, om et implementeringsprojekt er klar til cutover-overgangsfasen og udgivelse.</span><span class="sxs-lookup"><span data-stu-id="1a511-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="1a511-117">Denne gennemgang er obligatorisk for ethvert implementeringsprojekt, før du kan anmode om udgivelse i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="1a511-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="1a511-118">Vores sandkassemiljøer implementeres i det centrale USA's datacenter.</span><span class="sxs-lookup"><span data-stu-id="1a511-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="1a511-119">Vi ønsker, at vores produktionsmiljøer skal implementeres i det vestlige USA's datacenter.</span><span class="sxs-lookup"><span data-stu-id="1a511-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="1a511-120">Kan jeg vælge Det vestlige USA som datacenter i min produktionskonfiguration?</span><span class="sxs-lookup"><span data-stu-id="1a511-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="1a511-121">LCS forhindrer ikke valg af et andet datacenter, når du implementerer et Human Resources-miljø, men det kan ikke anbefales at vælge et andet datacenter.</span><span class="sxs-lookup"><span data-stu-id="1a511-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="1a511-122">Hvis du vil placere dit produktionsmiljø i Det vestlige USA's datacenter, skal du først geninstallere dine sandkassemiljøer i Det vestlige USA's datacenter, teste dem og derefter godkende.</span><span class="sxs-lookup"><span data-stu-id="1a511-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="1a511-123">Oplysninger om, hvordan du vælger det korrekte datacenter, finder du under [Netværkskrav](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="1a511-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="1a511-124">Hvilket adgangsniveau skal jeg bruge til Azure-ressourcerne i mine Human Resources-miljøer?</span><span class="sxs-lookup"><span data-stu-id="1a511-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="1a511-125">Adgang til Human Resources-miljøer er begrænset.</span><span class="sxs-lookup"><span data-stu-id="1a511-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="1a511-126">Du kan ikke få adgang til den virtuelle maskine (VM) eller Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="1a511-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="1a511-127">Du kan heller ikke få adgang til databasen via Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="1a511-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="1a511-128">Selvom du ikke kan få adgang til dine Azure-ressourcer eller Dynamics 365 Human Resources-miljøer direkte, er der flere funktioner, du kan bruge til at få adgang til dine data:</span><span class="sxs-lookup"><span data-stu-id="1a511-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="1a511-129">Du kan installere en Azure SQL-database i din egen Azure-lejer og bruge BYOD-funktionen (Bring Your Own Database) til at synkronisere data.</span><span class="sxs-lookup"><span data-stu-id="1a511-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="1a511-130">Yderligere oplysninger finder du i afsnittet [Bruge din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="1a511-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="1a511-131">Du kan bruge Dataverse-integration til at synkronisere udvalgte enheder i Dataverse-databasen.</span><span class="sxs-lookup"><span data-stu-id="1a511-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="1a511-132">Yderligere oplysninger finder du i [Dataverse-tabeller](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="1a511-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="1a511-133">Hvor ofte sikkerhedskopieres min produktionsdatabase?</span><span class="sxs-lookup"><span data-stu-id="1a511-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="1a511-134">Databaser beskyttes gennem automatiske sikkerhedskopieringer med følgende frekvens:</span><span class="sxs-lookup"><span data-stu-id="1a511-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="1a511-135">Backuptype</span><span class="sxs-lookup"><span data-stu-id="1a511-135">Type of backup</span></span> | <span data-ttu-id="1a511-136">Frekvens</span><span class="sxs-lookup"><span data-stu-id="1a511-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="1a511-137">Fuld sikkerhedskopiering af database</span><span class="sxs-lookup"><span data-stu-id="1a511-137">Full database backup</span></span> | <span data-ttu-id="1a511-138">Ugentligt</span><span class="sxs-lookup"><span data-stu-id="1a511-138">Weekly</span></span> |
| <span data-ttu-id="1a511-139">Differentieret sikkerhedskopiering af database</span><span class="sxs-lookup"><span data-stu-id="1a511-139">Differential database backup</span></span> | <span data-ttu-id="1a511-140">Hver 12-24. time</span><span class="sxs-lookup"><span data-stu-id="1a511-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="1a511-141">Sikkerhedskopiering af transaktionslog</span><span class="sxs-lookup"><span data-stu-id="1a511-141">Transaction log backup</span></span> | <span data-ttu-id="1a511-142">Hvert 5. til 10. minut</span><span class="sxs-lookup"><span data-stu-id="1a511-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="1a511-143">Microsoft opbevarer et tilstrækkeligt antal sikkerhedskopier, der giver mulighed for gendannelse til bestemt tidspunkt (PITR) inden for de seneste 14 dage.</span><span class="sxs-lookup"><span data-stu-id="1a511-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="1a511-144">Du kan finde flere oplysninger i  [Få mere at vide om automatiske sikkerhedskopieringer af SQL Database](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="1a511-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="1a511-145">Kan jeg anmode om en kopi af sikkerhedskopien af min produktionsdatabase?</span><span class="sxs-lookup"><span data-stu-id="1a511-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="1a511-146">Nej</span><span class="sxs-lookup"><span data-stu-id="1a511-146">No.</span></span> <span data-ttu-id="1a511-147">Du kan dog sende en serviceanmodning om en databaseopdatering for at kopiere dit produktionsmiljø til dit sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="1a511-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="1a511-148">Du kan installere en Azure SQL-database i din egen Azure-lejer og bruge BYOD-funktionen til at synkronisere data fra dit produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="1a511-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="1a511-149">Yderligere oplysninger finder du i afsnittet [Bruge din egen database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="1a511-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="1a511-150">Hvordan flytter jeg mit sandkassemiljø til produktion med henblik på udgivelse?</span><span class="sxs-lookup"><span data-stu-id="1a511-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="1a511-151">Da der ikke findes en kopieringsfunktion, som kan flytte miljøet fra en sandkasse til et produktionsmiljø, skal du bruge datapakker til at flytte data til produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="1a511-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="1a511-152">Vi anbefaler, at du udarbejder en tydelig liste over enheder, der er konfigureret i sandkassen, under hele projektet.</span><span class="sxs-lookup"><span data-stu-id="1a511-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="1a511-153">Test derefter cutover- og migreringsprocessen for eventuelle datapakker, der er nødvendige, før du kan iværksætte udgivelsen.</span><span class="sxs-lookup"><span data-stu-id="1a511-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="1a511-154">Du skal manuelt flytte datapakker ind i produktionsmiljøet, når du er klar til udgivelse.</span><span class="sxs-lookup"><span data-stu-id="1a511-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="1a511-155">Hvad skal jeg gøre, hvis mit produktionsmiljø er nede?</span><span class="sxs-lookup"><span data-stu-id="1a511-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="1a511-156">Hvis du vil rapportere en produktionsafbrydelse, skal du følge den proces, der er beskrevet under  [Rapportere en produktionsafbrydelse](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="1a511-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="1a511-157">Se også</span><span class="sxs-lookup"><span data-stu-id="1a511-157">See also</span></span>

 [<span data-ttu-id="1a511-158">Forberede til udgivelse</span><span class="sxs-lookup"><span data-stu-id="1a511-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]