---
title: Konfigurere og administrere databaselogning
description: Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8057ebd0bc061c6bf78d8674c45e0885ffce681c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467643"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="eec59-103">Konfigurere og administrere databaselogning</span><span class="sxs-lookup"><span data-stu-id="eec59-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eec59-104">Du kan spore ændringer af tabeller og felter i Dynamics 365 Human Resources med databaselogning.</span><span class="sxs-lookup"><span data-stu-id="eec59-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="eec59-105">I dette emne beskrives, hvordan du kan:</span><span class="sxs-lookup"><span data-stu-id="eec59-105">This topic describes how to:</span></span>

- <span data-ttu-id="eec59-106">Administrere sikkerhed og ydeevne til databaselogning</span><span class="sxs-lookup"><span data-stu-id="eec59-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="eec59-107">Opret databaselogføring</span><span class="sxs-lookup"><span data-stu-id="eec59-107">Set up database logging</span></span>
- <span data-ttu-id="eec59-108">Rydde op i databaselogfiler</span><span class="sxs-lookup"><span data-stu-id="eec59-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="eec59-109">Oversigt over databaselogning</span><span class="sxs-lookup"><span data-stu-id="eec59-109">Overview of database logging</span></span>

<span data-ttu-id="eec59-110">Databaselogning sporer specifikke ændringer af tabeller og felter i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eec59-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="eec59-111">Disse ændringer omfatter indsættelse, opdatering eller sletning.</span><span class="sxs-lookup"><span data-stu-id="eec59-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="eec59-112">Databaselogning gemmer en post over ændringer af tabeller eller felter i databaseloggens tabel.</span><span class="sxs-lookup"><span data-stu-id="eec59-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="eec59-113">Forretningsbrug af databaselogning omfatter:</span><span class="sxs-lookup"><span data-stu-id="eec59-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="eec59-114">Oprette en revisionspost med ændringer af bestemte tabeller, der indeholder følsomme oplysninger.</span><span class="sxs-lookup"><span data-stu-id="eec59-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="eec59-115">Sporing af enkelte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="eec59-115">Tracking single transactions.</span></span> <span data-ttu-id="eec59-116">Databaselogning er ikke beregnet til sporing af automatiske transaktioner, der kører i batchjob.</span><span class="sxs-lookup"><span data-stu-id="eec59-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="eec59-117">Sikkerhed for databaselogning</span><span class="sxs-lookup"><span data-stu-id="eec59-117">Security for database logging</span></span>

<span data-ttu-id="eec59-118">Databaselogge kan indeholde følsomme data.</span><span class="sxs-lookup"><span data-stu-id="eec59-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="eec59-119">Begræns adgangen, så den kun omfatter sikkerhedsroller, der skal have adgang til logdata.</span><span class="sxs-lookup"><span data-stu-id="eec59-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="eec59-120">Databaselogning og ydeevne</span><span class="sxs-lookup"><span data-stu-id="eec59-120">Database logging and performance</span></span>

<span data-ttu-id="eec59-121">Selvom databaselogning er værdifuld ud fra et forretningsmæssigt perspektiv, kan det være dyrt i ressourceforbrug og administration.</span><span class="sxs-lookup"><span data-stu-id="eec59-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="eec59-122">Påvirkninger af ydeevne fra databaselogning omfatter:</span><span class="sxs-lookup"><span data-stu-id="eec59-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="eec59-123">Tabellen i databaselog kan hurtigt vokse og forårsage en forøgelse af størrelsen på databasen.</span><span class="sxs-lookup"><span data-stu-id="eec59-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="eec59-124">Væksten afhænger af mængden af logførte data, du beslutter at beholde.</span><span class="sxs-lookup"><span data-stu-id="eec59-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="eec59-125">Tabellen i databaseloggen bevarer som standard kun 30 dages logdata.</span><span class="sxs-lookup"><span data-stu-id="eec59-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="eec59-126">Databaselogning kan påvirke lange automatiserede processer negativt, f.eks. en langvarig dataimport.</span><span class="sxs-lookup"><span data-stu-id="eec59-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="eec59-127">Bedste fremgangsmåder</span><span class="sxs-lookup"><span data-stu-id="eec59-127">Best practices</span></span>

<span data-ttu-id="eec59-128">Du kan forbedre ydeevnen ved at udvælge bestemte felter til loggen i stedet for hele tabeller.</span><span class="sxs-lookup"><span data-stu-id="eec59-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="eec59-129">Databaselogning er begrænset til 20 tabeller for at hjælpe med at opretholde den overordnede ydeevne.</span><span class="sxs-lookup"><span data-stu-id="eec59-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="eec59-130">Det er kun muligt at logføre opdateringer for individuelle felter.</span><span class="sxs-lookup"><span data-stu-id="eec59-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="eec59-131">Opret databaselogføring</span><span class="sxs-lookup"><span data-stu-id="eec59-131">Set up database logging</span></span>

<span data-ttu-id="eec59-132">Du kan bruge guiden **Registrering af databaseændringer** til at konfigurere databaselogning.</span><span class="sxs-lookup"><span data-stu-id="eec59-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="eec59-133">Guiden giver en fleksibel måde at konfigurere logføring for tabeller eller felter.</span><span class="sxs-lookup"><span data-stu-id="eec59-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="eec59-134">Gå til **Systemadministration > Links > Database > Opsætning af databaselog**.</span><span class="sxs-lookup"><span data-stu-id="eec59-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="eec59-135">Vælg **Ny** for at starte guiden **Registrering af databaseændringer**.</span><span class="sxs-lookup"><span data-stu-id="eec59-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="eec59-136">Fuldfør guiden.</span><span class="sxs-lookup"><span data-stu-id="eec59-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="eec59-137">Rydde op i databaselogfiler</span><span class="sxs-lookup"><span data-stu-id="eec59-137">Clean up database logs</span></span>

<span data-ttu-id="eec59-138">Du kan slette alle eller en del af databaseloggene ved hjælp af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="eec59-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="eec59-139">Vælg alle logge for en bestemt tabel.</span><span class="sxs-lookup"><span data-stu-id="eec59-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="eec59-140">Vælg bestemte typer af databaselog.</span><span class="sxs-lookup"><span data-stu-id="eec59-140">Select specific types of database log.</span></span>
- <span data-ttu-id="eec59-141">Vælg en dato og et klokkeslæt for oprettelse af en log.</span><span class="sxs-lookup"><span data-stu-id="eec59-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="eec59-142">Benyt følgende fremgangsmåde for at konfigurere oprydning af databaselog:</span><span class="sxs-lookup"><span data-stu-id="eec59-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="eec59-143">Gå til **Systemadministration > Links > Database > Databaselog**.</span><span class="sxs-lookup"><span data-stu-id="eec59-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="eec59-144">Vælg **Oprydning i log**.</span><span class="sxs-lookup"><span data-stu-id="eec59-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="eec59-145">Vælg en metode til valg af logge, der skal slettes, ved at angive en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="eec59-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="eec59-146">Tabel-ID</span><span class="sxs-lookup"><span data-stu-id="eec59-146">Table ID</span></span>
   - <span data-ttu-id="eec59-147">Logtype</span><span class="sxs-lookup"><span data-stu-id="eec59-147">Type of log</span></span>
   - <span data-ttu-id="eec59-148">Dato og klokkeslæt for oprettelse</span><span class="sxs-lookup"><span data-stu-id="eec59-148">Created date and time</span></span>

3. <span data-ttu-id="eec59-149">Brug fanen **Oprydning i databaselog** til at bestemme, hvornår du vil køre oprydningsopgaven for log.</span><span class="sxs-lookup"><span data-stu-id="eec59-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="eec59-150">Databaselogge er som standard tilgængelige i 30 dage.</span><span class="sxs-lookup"><span data-stu-id="eec59-150">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]