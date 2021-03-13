---
title: Konfigurere Dataverse-integration
description: Du kan slå integration mellem Microsoft Dataverse og Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljer, rydde sporingsdata og synkronisere en tabel som hjælp til fejlfinding af dataproblemer mellem de to miljøer.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111974"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="09160-104">Konfigurere Dataverse-integration</span><span class="sxs-lookup"><span data-stu-id="09160-104">Configure Dataverse integration</span></span>

<span data-ttu-id="09160-105">Du kan slå integration mellem Microsoft Dataverse og Dynamics 365 Human Resources til eller fra.</span><span class="sxs-lookup"><span data-stu-id="09160-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="09160-106">Du kan også få vist synkroniseringsdetaljer, rydde sporingsdata og synkronisere en tabel som hjælp til fejlfinding af dataproblemer mellem de to miljøer.</span><span class="sxs-lookup"><span data-stu-id="09160-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="09160-107">Yderligere oplysninger om Dataverse (tidligere Common Data Service) og terminologiopdateringer finder du i [Hvad er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="09160-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="09160-108">Når du deaktiverer integration, kan brugere foretage ændringer i Human Resources eller Dataverse, men disse ændringer synkroniseres ikke mellem de to miljøer.</span><span class="sxs-lookup"><span data-stu-id="09160-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="09160-109">Som standard er dataintegration mellem Human Resources og Dataverse slået fra.</span><span class="sxs-lookup"><span data-stu-id="09160-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="09160-110">Du kan eventuelt deaktivere integration i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="09160-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="09160-111">Du er ved at udfylde data via Data Management Framework og skal importere dataene flere gange for at få dem i korrekt tilstand.</span><span class="sxs-lookup"><span data-stu-id="09160-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="09160-112">Der er problemer med dataene i enten Human Resources eller Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="09160-113">Hvis du deaktiverer integration, kan du slette en post i ét miljø uden at slette den i det andet.</span><span class="sxs-lookup"><span data-stu-id="09160-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="09160-114">Når du slår integrationen til igen, vil posten i det miljø, hvor den ikke blev slettet, blive synkroniseret til det miljø, hvor den blev slettet.</span><span class="sxs-lookup"><span data-stu-id="09160-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="09160-115">Synkroniseringen starter, næste gang batchjobbet **Dataverse-integration mistet anmodningssynk.** køres.</span><span class="sxs-lookup"><span data-stu-id="09160-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="09160-116">Når du slår dataintegration fra, skal du sørge for ikke at redigere den samme post i begge miljøer.</span><span class="sxs-lookup"><span data-stu-id="09160-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="09160-117">Når du slår integration til igen, vil den post, du senest har redigeret, blive synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="09160-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="09160-118">Hvis du derfor ikke har foretaget de samme ændringer i posten i begge miljøer, kan der opstå datatab.</span><span class="sxs-lookup"><span data-stu-id="09160-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="09160-119">Adgang til siden Dataverse-integration</span><span class="sxs-lookup"><span data-stu-id="09160-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="09160-120">I den Human Resources-forekomst, hvor du vil se eller konfigurere indstillinger for integrationen med Dataverse, skal du vælge feltet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="09160-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="09160-121">[![Feltet Systemadministration](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="09160-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="09160-122">Vælg fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="09160-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="09160-123">[![Fanen Links](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="09160-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="09160-124">Under **Integrationer** skal du vælge **Dataverse-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="09160-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="09160-125">[![Dataverse-konfigurationslink](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="09160-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="09160-126">Slå dataintegration mellem Human Resources og Dataverse til eller fra</span><span class="sxs-lookup"><span data-stu-id="09160-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="09160-127">Hvis du vil aktivere integration, skal du angive indstillingen **Aktivere Dataverse-integration** til **Ja** på siden **Microsoft Dataverse-integration**.</span><span class="sxs-lookup"><span data-stu-id="09160-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="09160-128">Når du slår integration til, synkroniseres data, næste gang batchjobbet **Dataverse-integration mistet anmodningssynk** køres.</span><span class="sxs-lookup"><span data-stu-id="09160-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="09160-129">Alle data bør være tilgængelige, når batchjobbet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="09160-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="09160-130">Hvis du vil deaktivere integration, skal du angive indstillingen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="09160-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="09160-131">[![Slå Dataverse-integration til eller fra](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="09160-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="09160-132">Det anbefales kraftigt, at du deaktiverer Dataverse-integration, mens du udfører dataoverførselsopgaver.</span><span class="sxs-lookup"><span data-stu-id="09160-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="09160-133">Store dataoverførsler kan påvirke ydeevnen betydeligt.</span><span class="sxs-lookup"><span data-stu-id="09160-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="09160-134">Overførsel af 2000 arbejdere kan f.eks. tage flere timer, når integration er aktiveret, og mindre end en time, når den deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="09160-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="09160-135">De tal, der er i dette eksempel, er udelukkende til demonstrationsformål.</span><span class="sxs-lookup"><span data-stu-id="09160-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="09160-136">Det nøjagtige tidsforbrug med at importere poster kan variere meget afhængigt af mange faktorer.</span><span class="sxs-lookup"><span data-stu-id="09160-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="09160-137">Vis dataintegrationsdetaljer</span><span class="sxs-lookup"><span data-stu-id="09160-137">View data integration details</span></span>

<span data-ttu-id="09160-138">I oversigtspanelet **Administration** på siden **Microsoft Dataverse-integration** kan du se, hvordan rækkerne er sammenkædet mellem Human Resources og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="09160-139">Hvis du vil se rækkerne for en tabel, skal du vælge tabellen i feltet **Dataverse-tabel**.</span><span class="sxs-lookup"><span data-stu-id="09160-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="09160-140">Gitteret viser alle de rækker, der er knyttet til den valgte tabel.</span><span class="sxs-lookup"><span data-stu-id="09160-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="09160-141">Ikke alle Dataverse-tabeller er angivet i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="09160-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="09160-142">Kun tabeller, der understøtter brugen af brugerdefinerede felter, vises i gitteret.</span><span class="sxs-lookup"><span data-stu-id="09160-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="09160-143">Nye tabeller bliver tilgængelige via løbende frigivelser af Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09160-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="09160-144">Gitteret indeholder følgende felter:</span><span class="sxs-lookup"><span data-stu-id="09160-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="09160-145">**Dataverse-tabel** – Navn på tabellen i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="09160-146">**Dataverse-tabelreference** – Den identifikation, som Dataverse bruger til at identificere en post.</span><span class="sxs-lookup"><span data-stu-id="09160-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="09160-147">Denne værdi svarer til en **RecId**-værdi i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09160-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="09160-148">Du kan finde identifikatoren, når du åbner Dataverse-tabellen i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="09160-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="09160-149">**Human Resources-enhedsnavn** – Den Human Resources-enhed, der sidst synkroniserede data til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="09160-150">Enheden kan enten have Dataverse-præfikset eller et andet præfiks.</span><span class="sxs-lookup"><span data-stu-id="09160-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="09160-151">**Human Resources-reference** – Den **RecId**-værdi, der er tilknyttet posten i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09160-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="09160-152">**Slettet fra Dataverse** – En værdi, der angiver, om rækken blev slettet fra Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="09160-153">Poster i Human Resources svarer til rækker i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="09160-154">Fjerne tilknytningen af en post i Human resources fra en Dataverse-række</span><span class="sxs-lookup"><span data-stu-id="09160-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="09160-155">Hvis du får problemer under datasynkronisering mellem Human Resources og Dataverse, kan du muligvis løse dem ved at rydde sporingen og lade sporingstabellen blive synkroniseret igen.</span><span class="sxs-lookup"><span data-stu-id="09160-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="09160-156">Hvis du fjerner tilknytningen og derefter ændrer eller sletter en række i Dataverse, synkroniseres ændringerne ikke med Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09160-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="09160-157">Hvis du foretager ændringer i Human Resources, oprettes der en ny sporingspost, og rækken opdateres i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="09160-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="09160-158">Hvis du vil fjerne tilknytningen af en post mellem Human Resources og en Dataverse-række, skal du vælge tabellen i feltet **Dataverse-tabel** og derefter vælge **Ryd sporingsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="09160-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="09160-159">[![Rydning af sporingsoplysninger](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="09160-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="09160-160">Se den næste procedure, hvis du vil køre en fuld synkronisering af tabellen, når du har ryddet sporingen.</span><span class="sxs-lookup"><span data-stu-id="09160-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="09160-161">Synkronisere en tabel mellem Human Resources og Dataverse</span><span class="sxs-lookup"><span data-stu-id="09160-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="09160-162">Benyt denne fremgangsmåde, når:</span><span class="sxs-lookup"><span data-stu-id="09160-162">Use this procedure when:</span></span>

- <span data-ttu-id="09160-163">Ændringerne fra Dataverse er for længe om at blive vist i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09160-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="09160-164">Du skal opdatere sporingstabellen, efter at du har ryddet registreringen.</span><span class="sxs-lookup"><span data-stu-id="09160-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="09160-165">Sådan kører du en fuld synkronisering af en tabel mellem Human Resources og Dataverse:</span><span class="sxs-lookup"><span data-stu-id="09160-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="09160-166">Vælg tabellen i feltet **Dataverse-tabel**.</span><span class="sxs-lookup"><span data-stu-id="09160-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="09160-167">Vælg **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="09160-167">Select **Sync now**.</span></span>

<span data-ttu-id="09160-168">[![Køre en fuld synkronisering](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="09160-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="09160-169">Se også</span><span class="sxs-lookup"><span data-stu-id="09160-169">See also</span></span>

[<span data-ttu-id="09160-170">Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="09160-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="09160-171">Konfigurere virtuelle Dataverse-tabeller</span><span class="sxs-lookup"><span data-stu-id="09160-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="09160-172">Ofte stillede spørgsmål om Virtuelle tabeller i Human Resources</span><span class="sxs-lookup"><span data-stu-id="09160-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="09160-173">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="09160-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="09160-174">Terminologiopdateringer</span><span class="sxs-lookup"><span data-stu-id="09160-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
