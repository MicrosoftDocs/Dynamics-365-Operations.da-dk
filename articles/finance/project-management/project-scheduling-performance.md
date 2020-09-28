---
title: Ydeevne af projektressourceplanlægning
description: Dette emne beskriver, hvordan du kan forbedre ydeevnen af ressourceplanlægningen for et større antal projekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760509"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="6e221-103">Ydeevne af projektressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="6e221-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="6e221-104">Ydeevneproblemer relateret til ressourceplanlægning kan forekomme, når antallet af projekter når op på tusinder.</span><span class="sxs-lookup"><span data-stu-id="6e221-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="6e221-105">For at forbedre ydeevnen i ressourceplanlægningen er der en tilgængelig funktion, der giver brugerne mulighed for at reducere den tid, det tager at starte formularen Ressourcetilgængelighed.</span><span class="sxs-lookup"><span data-stu-id="6e221-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="6e221-106">Dette fjerner specifikt synkroniseringsprocessen til akkumuleringer af ressourcekapacitet og bruger tabellen **ResProjectResource** til at øge ressourceopslaget.</span><span class="sxs-lookup"><span data-stu-id="6e221-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="6e221-107">Bemærk, at tabellen **ResRollup** ikke længere vil blive brugt.</span><span class="sxs-lookup"><span data-stu-id="6e221-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e221-108">Hvis der er en afhængighed af enten synkroniseringsprocessen til akkumuleringer af ressourcekapacitet eller tabellen **ResProjectResource**, skal du ikke bruge denne funktion.</span><span class="sxs-lookup"><span data-stu-id="6e221-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="6e221-109">Aktivere forbedring af ydeevne for ressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="6e221-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="6e221-110">Hvis du vil aktivere forbedringer af ydeevnen for ressourceplanlægning, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="6e221-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="6e221-111">Gå til **Funktionsstyring** > **Alle**, og find **Aktivér funktionen til forbedring af ydeevnen for projekt ressourceplanlægning** på funktionslisten.</span><span class="sxs-lookup"><span data-stu-id="6e221-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="6e221-112">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="6e221-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="6e221-113">Hvis du ikke kan finde funktionen på listen, skal du vælge **Søg efter opdateringer** for at opdatere listen.</span><span class="sxs-lookup"><span data-stu-id="6e221-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="6e221-114">Opdater browseren, og gå derefter til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Synkroniser ressourcekalenderkapacitet på tværs af alle firmaer**.</span><span class="sxs-lookup"><span data-stu-id="6e221-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="6e221-115">Angiv **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="6e221-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="6e221-116">Hvis du vil oprette trinvise data, skal du angive den til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="6e221-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="6e221-117">Vælg den periode, hvor der skal genereres data, i feltet **Periodekode**.</span><span class="sxs-lookup"><span data-stu-id="6e221-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="6e221-118">Hvis du vælger en periodekode, skal der ikke defineres en start- og slutdato.</span><span class="sxs-lookup"><span data-stu-id="6e221-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="6e221-119">Hvis du ikke udfylder feltet **Periodekode**, skal du vælge bestemte start- og slutdatoer for at oprette data.</span><span class="sxs-lookup"><span data-stu-id="6e221-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="6e221-120">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e221-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6e221-121">Dette vil distribuere generelle data til tabellen **ResCalendarCapacity** på tværs af alle firmaer i dit miljø, så batchjobbet kun skal køres i én juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6e221-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="6e221-122">Dataene i dette batchjob skal bruges til at beregne ressourcekapaciteten via den tilknyttede kalender.</span><span class="sxs-lookup"><span data-stu-id="6e221-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="6e221-123">Gå til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Udfyld projektressourcer på tværs af alle firmaer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e221-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="6e221-124">Dette er scriptet til dataopgradering for generelle data i tabellerne **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="6e221-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="6e221-125">Værdierne for feltet **PSAPRojSchedRole.RootActivity** opdateres også.</span><span class="sxs-lookup"><span data-stu-id="6e221-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="6e221-126">Hvis dette ikke køres, vises der en advarsel, når du forsøger at udføre ressourceplanlægningshandlinger.</span><span class="sxs-lookup"><span data-stu-id="6e221-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="6e221-127">Deaktivere forbedring af ydeevne for ressourceplanlægning</span><span class="sxs-lookup"><span data-stu-id="6e221-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="6e221-128">Gå til **Funktionsstyring** > **Alle**, og søg efter **Aktivér funktionen til forbedring af ydeevnen for projekt ressourceplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="6e221-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="6e221-129">Vælg funktionen, og vælg derefter knappen **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="6e221-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="6e221-130">Opdater browseren.</span><span class="sxs-lookup"><span data-stu-id="6e221-130">Refresh your browser.</span></span>
4. <span data-ttu-id="6e221-131">Gå til **Projektstyring og regnskab** > **Periodisk** > **Kapacitetssynkronisering** > **Synkroniser ressourcekapacitet, opkøb**.</span><span class="sxs-lookup"><span data-stu-id="6e221-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="6e221-132">På siden **Kapacitetsopkøb, synkronisering** skal du angive **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data.</span><span class="sxs-lookup"><span data-stu-id="6e221-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="6e221-133">Hvis du vil oprette trinvise data, skal du angive den til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="6e221-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="6e221-134">Vælg den periode, hvor der skal genereres data, i feltet **Periodekode**.</span><span class="sxs-lookup"><span data-stu-id="6e221-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="6e221-135">Hvis du vælger en periodekode, skal der ikke defineres en start- og slutdato.</span><span class="sxs-lookup"><span data-stu-id="6e221-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="6e221-136">Hvis du ikke udfylder feltet **Periodekode**, skal du vælge bestemte start- og slutdatoer for at oprette data.</span><span class="sxs-lookup"><span data-stu-id="6e221-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="6e221-137">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e221-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6e221-138">Dette vil distribuere generelle data til tabellen **ResRollup** på tværs af alle firmaer i dit miljø, så batchjobbet kun skal køres i én juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6e221-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="6e221-139">Dette batchjob er nødvendigt for alle visninger af **Ressourcetilgængelighed**.</span><span class="sxs-lookup"><span data-stu-id="6e221-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="6e221-140">Hvis dette batchjob ikke køres, vil **ResRollup**-data blive genereret løbende, hvilket kan tage lang tid.</span><span class="sxs-lookup"><span data-stu-id="6e221-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
