---
title: Konfigurere og administrere databaselogning
description: Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801329"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="05041-103">Konfigurere og administrere databaselogning</span><span class="sxs-lookup"><span data-stu-id="05041-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="05041-104">Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.</span><span class="sxs-lookup"><span data-stu-id="05041-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="05041-105">I dette emne beskrives, hvordan du kan:</span><span class="sxs-lookup"><span data-stu-id="05041-105">This topic describes how to:</span></span>

- <span data-ttu-id="05041-106">Administrere sikkerhed og ydeevne til databaselogning</span><span class="sxs-lookup"><span data-stu-id="05041-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="05041-107">Opret databaselogføring</span><span class="sxs-lookup"><span data-stu-id="05041-107">Set up database logging</span></span>
- <span data-ttu-id="05041-108">Rydde op i databaselogfiler</span><span class="sxs-lookup"><span data-stu-id="05041-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="05041-109">Oversigt over databaselogning</span><span class="sxs-lookup"><span data-stu-id="05041-109">Overview of database logging</span></span>

<span data-ttu-id="05041-110">Databaselogning sporer specifikke ændringer af tabeller og felter i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="05041-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="05041-111">Disse ændringer omfatter indsættelse, opdatering eller sletning.</span><span class="sxs-lookup"><span data-stu-id="05041-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="05041-112">Databaselogning gemmer en post over ændringer af tabeller eller felter i databaseloggens tabel.</span><span class="sxs-lookup"><span data-stu-id="05041-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="05041-113">Forretningsbrug af databaselogning omfatter:</span><span class="sxs-lookup"><span data-stu-id="05041-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="05041-114">Oprette en revisionspost med ændringer af bestemte tabeller, der indeholder følsomme oplysninger.</span><span class="sxs-lookup"><span data-stu-id="05041-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="05041-115">Sporing af enkelte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="05041-115">Tracking single transactions.</span></span> <span data-ttu-id="05041-116">Databaselogning er ikke beregnet til sporing af automatiske transaktioner, der kører i batchjob.</span><span class="sxs-lookup"><span data-stu-id="05041-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="05041-117">Sikkerhed for databaselogning</span><span class="sxs-lookup"><span data-stu-id="05041-117">Security for database logging</span></span>

<span data-ttu-id="05041-118">Databaselogge kan indeholde følsomme data.</span><span class="sxs-lookup"><span data-stu-id="05041-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="05041-119">Begræns adgangen, så den kun omfatter sikkerhedsroller, der skal have adgang til logdata.</span><span class="sxs-lookup"><span data-stu-id="05041-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="05041-120">Databaselogning og ydeevne</span><span class="sxs-lookup"><span data-stu-id="05041-120">Database logging and performance</span></span>

<span data-ttu-id="05041-121">Selvom databaselogning er værdifuld ud fra et forretningsmæssigt perspektiv, kan det være dyrt i ressourceforbrug og administration.</span><span class="sxs-lookup"><span data-stu-id="05041-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="05041-122">Påvirkninger af ydeevne fra databaselogning omfatter:</span><span class="sxs-lookup"><span data-stu-id="05041-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="05041-123">Tabellen i databaselog kan hurtigt vokse og forårsage en forøgelse af størrelsen på databasen.</span><span class="sxs-lookup"><span data-stu-id="05041-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="05041-124">Væksten afhænger af mængden af logførte data, du beslutter at beholde.</span><span class="sxs-lookup"><span data-stu-id="05041-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="05041-125">Tabellen i databaseloggen bevarer som standard kun 30 dages logdata.</span><span class="sxs-lookup"><span data-stu-id="05041-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="05041-126">Databaselogning kan påvirke lange automatiserede processer negativt, f.eks. en langvarig dataimport.</span><span class="sxs-lookup"><span data-stu-id="05041-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="05041-127">Bedste fremgangsmåder</span><span class="sxs-lookup"><span data-stu-id="05041-127">Best practices</span></span>

<span data-ttu-id="05041-128">Du kan forbedre ydeevnen ved at udvælge bestemte felter til loggen i stedet for hele tabeller.</span><span class="sxs-lookup"><span data-stu-id="05041-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="05041-129">Databaselogning er begrænset til 20 tabeller for at hjælpe med at opretholde den overordnede ydeevne.</span><span class="sxs-lookup"><span data-stu-id="05041-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="05041-130">Det er kun muligt at logføre opdateringer for individuelle felter.</span><span class="sxs-lookup"><span data-stu-id="05041-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="05041-131">Opret databaselogføring</span><span class="sxs-lookup"><span data-stu-id="05041-131">Set up database logging</span></span>

<span data-ttu-id="05041-132">Du kan bruge guiden **Registrering af databaseændringer** til at konfigurere databaselogning.</span><span class="sxs-lookup"><span data-stu-id="05041-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="05041-133">Guiden giver en fleksibel måde at konfigurere logføring for tabeller eller felter.</span><span class="sxs-lookup"><span data-stu-id="05041-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="05041-134">Gå til **Systemadministration > Links > Database > Opsætning af databaselog**.</span><span class="sxs-lookup"><span data-stu-id="05041-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="05041-135">Vælg **Ny** for at starte guiden **Registrering af databaseændringer**.</span><span class="sxs-lookup"><span data-stu-id="05041-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="05041-136">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="05041-136">Select **Next**.</span></span> 
3. <span data-ttu-id="05041-137">På siden **Tabeller og felter** i guiden skal du vælge de tabeller og felter, hvor du vil aktivere databaselogføring, og vælge **Næste**.</span><span class="sxs-lookup"><span data-stu-id="05041-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="05041-138">Databaselogføring er ikke tilgængelig i alle tabeller i Human Resources-databasen.</span><span class="sxs-lookup"><span data-stu-id="05041-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="05041-139">Hvis du vælger **Vis alle tabeller** under listen, udvides listen over tabeller og felter til at vise alle databasetabeller, som databaselogføring er tilgængelig for, men dette vil være en delmængde af den fulde liste over databasetabeller.</span><span class="sxs-lookup"><span data-stu-id="05041-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="05041-140">På siden **Typer af ændringer** i guiden skal du vælge de datahandlinger, du vil spore ændringer for i hver af tabellerne og felterne, og vælge **Næste**.</span><span class="sxs-lookup"><span data-stu-id="05041-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="05041-141">I tabellen nedenfor kan du se en beskrivelse af de datahandlinger, der er tilgængelige til logføring.</span><span class="sxs-lookup"><span data-stu-id="05041-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="05041-142">Gennemse de ændringer, der vil blive foretaget, på siden **Udfør**, og vælg **Udfør**.</span><span class="sxs-lookup"><span data-stu-id="05041-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="05041-143">Operation</span><span class="sxs-lookup"><span data-stu-id="05041-143">Operation</span></span> | <span data-ttu-id="05041-144">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="05041-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="05041-145">Spor nye transaktioner</span><span class="sxs-lookup"><span data-stu-id="05041-145">Track new transactions</span></span> | <span data-ttu-id="05041-146">Opret en log for nye poster, der er oprettet i tabellen.</span><span class="sxs-lookup"><span data-stu-id="05041-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="05041-147">Opdater</span><span class="sxs-lookup"><span data-stu-id="05041-147">Update</span></span> | <span data-ttu-id="05041-148">Opret en log for opdateringer af tabelposter eller opdateringer af individuelt valgte felter i tabellen.</span><span class="sxs-lookup"><span data-stu-id="05041-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="05041-149">Hvis du vælger at logføre opdateringer for tabellen, oprettes der en logpost, hver gang der foretages en opdatering af et felt i en vilkårlig post i tabellen.</span><span class="sxs-lookup"><span data-stu-id="05041-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="05041-150">Hvis du vælger at logføre opdateringer for bestemte felter, oprettes der kun en logpost, når der foretages opdateringer af disse felter med tabelposter.</span><span class="sxs-lookup"><span data-stu-id="05041-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="05041-151">Slet</span><span class="sxs-lookup"><span data-stu-id="05041-151">Delete</span></span> | <span data-ttu-id="05041-152">Opret en log for poster, der er slettet fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="05041-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="05041-153">Omdøb nøgle</span><span class="sxs-lookup"><span data-stu-id="05041-153">Rename key</span></span> | <span data-ttu-id="05041-154">Opret en logpost, når en tabelnøgle omdøbes.</span><span class="sxs-lookup"><span data-stu-id="05041-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="05041-155">Rydde op i databaselogfiler</span><span class="sxs-lookup"><span data-stu-id="05041-155">Clean up database logs</span></span>

<span data-ttu-id="05041-156">Du kan slette alle eller en del af databaseloggene ved hjælp af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="05041-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="05041-157">Vælg alle logge for en bestemt tabel.</span><span class="sxs-lookup"><span data-stu-id="05041-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="05041-158">Vælg bestemte typer af databaselog.</span><span class="sxs-lookup"><span data-stu-id="05041-158">Select specific types of database log.</span></span>
- <span data-ttu-id="05041-159">Vælg en dato og et klokkeslæt for oprettelse af en log.</span><span class="sxs-lookup"><span data-stu-id="05041-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="05041-160">Benyt følgende fremgangsmåde for at konfigurere oprydning af databaselog:</span><span class="sxs-lookup"><span data-stu-id="05041-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="05041-161">Gå til **Systemadministration > Links > Database > Databaselog**.</span><span class="sxs-lookup"><span data-stu-id="05041-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="05041-162">Vælg **Oprydning i log**.</span><span class="sxs-lookup"><span data-stu-id="05041-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="05041-163">Vælg en metode til valg af logge, der skal slettes, ved at angive en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="05041-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="05041-164">Tabel-ID</span><span class="sxs-lookup"><span data-stu-id="05041-164">Table ID</span></span>
   - <span data-ttu-id="05041-165">Logtype</span><span class="sxs-lookup"><span data-stu-id="05041-165">Type of log</span></span>
   - <span data-ttu-id="05041-166">Dato og klokkeslæt for oprettelse</span><span class="sxs-lookup"><span data-stu-id="05041-166">Created date and time</span></span>

3. <span data-ttu-id="05041-167">Brug fanen **Oprydning i databaselog** til at bestemme, hvornår du vil køre oprydningsopgaven for log.</span><span class="sxs-lookup"><span data-stu-id="05041-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="05041-168">Databaselogge er som standard tilgængelige i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="05041-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
