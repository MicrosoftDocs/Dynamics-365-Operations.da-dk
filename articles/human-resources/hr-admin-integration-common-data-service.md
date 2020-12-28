---
title: Konfigurere Common Data Service-integration
description: Du kan slå integration mellem Common Data Service og Dynamics 365 Human Resources til eller fra. Du kan også få vist synkroniseringsdetaljer, rydde sporingsdata og synkronisere en enhed som hjælp til fejlfinding af dataproblemer mellem de to miljøer.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
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
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527912"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="a871b-104">Konfigurere Common Data Service-integration</span><span class="sxs-lookup"><span data-stu-id="a871b-104">Configure Common Data Service integration</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a871b-105">Du kan slå integration mellem Common Data Service og Dynamics 365 Human Resources til eller fra.</span><span class="sxs-lookup"><span data-stu-id="a871b-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="a871b-106">Du kan også få vist synkroniseringsdetaljerne, rydde sporingsdata og synkronisere en enhed som hjælp til fejlfinding af dataproblemer mellem de to miljøer.</span><span class="sxs-lookup"><span data-stu-id="a871b-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="a871b-107">Når du deaktiverer integration, kan brugere foretage ændringer i Personale eller Common Data Service, men disse ændringer synkroniseres ikke mellem de to miljøer.</span><span class="sxs-lookup"><span data-stu-id="a871b-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="a871b-108">Som standard er dataintegration mellem Human Resources og Common Data Service slået fra.</span><span class="sxs-lookup"><span data-stu-id="a871b-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="a871b-109">Du kan eventuelt deaktivere integration i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="a871b-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="a871b-110">Du er ved at udfylde data via Data Management Framework og skal importere dataene flere gange for at få dem i korrekt tilstand.</span><span class="sxs-lookup"><span data-stu-id="a871b-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="a871b-111">Der er problemer med dataene i enten Personale eller Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="a871b-112">Hvis du deaktiverer integration, kan du slette en post i ét miljø uden at slette den i det andet.</span><span class="sxs-lookup"><span data-stu-id="a871b-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="a871b-113">Når du slår integrationen til igen, vil posten i det miljø, hvor den ikke blev slettet, blive synkroniseret til det miljø, hvor den blev slettet.</span><span class="sxs-lookup"><span data-stu-id="a871b-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="a871b-114">Synkroniseringen starter, næste gang batchjobbet **Common Data Service-integration mistet anmodningssynk.** køres.</span><span class="sxs-lookup"><span data-stu-id="a871b-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="a871b-115">Når du slår dataintegration fra, skal du sørge for ikke at redigere den samme post i begge miljøer.</span><span class="sxs-lookup"><span data-stu-id="a871b-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="a871b-116">Når du slår integration til igen, vil den post, du senest har redigeret, blive synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="a871b-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="a871b-117">Hvis du derfor ikke har foretaget de samme ændringer i posten i begge miljøer, kan der opstå datatab.</span><span class="sxs-lookup"><span data-stu-id="a871b-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="a871b-118">Adgang til siden Common Data Service-integration</span><span class="sxs-lookup"><span data-stu-id="a871b-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="a871b-119">I den Personale-forekomst, hvor du vil se eller konfigurere indstillinger for integrationen med Common Data Service, skal du vælge feltet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="a871b-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="a871b-120">[![Feltet Systemadministration](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="a871b-121">Vælg fanen **Links**.</span><span class="sxs-lookup"><span data-stu-id="a871b-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="a871b-122">[![Fanen Links](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="a871b-123">Under **Integrationer** skal du vælge **Common Data Service-konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a871b-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="a871b-124">[![Common Data Service-konfigurationslink](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="a871b-125">Slå dataintegration mellem Personale og Common Data Service til eller fra</span><span class="sxs-lookup"><span data-stu-id="a871b-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="a871b-126">Hvis du vil aktivere integration, skal du angive indstillingen **Aktivér integration med Common Data Service** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a871b-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a871b-127">Når du slår integration til, synkroniseres data, næste gang batchjobbet **Common Data Service-integration mistet anmodningssynk** køres.</span><span class="sxs-lookup"><span data-stu-id="a871b-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="a871b-128">Alle data bør være tilgængelige, når batchjobbet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="a871b-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="a871b-129">Hvis du vil deaktivere integration, skal du angive indstillingen til **Nej**.</span><span class="sxs-lookup"><span data-stu-id="a871b-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="a871b-130">[![Slå Common Data Service-integration til eller fra](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="a871b-131">Det anbefales kraftigt, at du deaktiverer Common Data Service-integration, mens du udfører dataoverførselsopgaver.</span><span class="sxs-lookup"><span data-stu-id="a871b-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="a871b-132">Store dataoverførsler kan påvirke ydeevnen betydeligt.</span><span class="sxs-lookup"><span data-stu-id="a871b-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="a871b-133">Overførsel af 2000 arbejdere kan f.eks. tage flere timer, når integration er aktiveret, og mindre end en time, når den deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="a871b-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="a871b-134">De tal, der er i dette eksempel, er udelukkende til demonstrationsformål.</span><span class="sxs-lookup"><span data-stu-id="a871b-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="a871b-135">Det nøjagtige tidsforbrug med at importere poster kan variere meget afhængigt af mange faktorer.</span><span class="sxs-lookup"><span data-stu-id="a871b-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="a871b-136">Vis dataintegrationsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a871b-136">View data integration details</span></span>

<span data-ttu-id="a871b-137">I oversigtspanelet **Administration** på siden **Common Data Service-integration** kan du se, hvordan poster er sammenkædet mellem Personale og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="a871b-138">Hvis du vil have vist posterne for en enhed, skal du vælge enheden i feltet **CDS-enhedsnavn**.</span><span class="sxs-lookup"><span data-stu-id="a871b-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="a871b-139">Gitteret viser alle de poster, der er knyttet til den valgte enhed.</span><span class="sxs-lookup"><span data-stu-id="a871b-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="a871b-140">[![Visning af posterne for en enhed](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a871b-141">Ikke alle Common Data Service-enheder er angivet i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="a871b-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="a871b-142">Kun enheder, der understøtter brugen af brugerdefinerede felter, vises i gitteret.</span><span class="sxs-lookup"><span data-stu-id="a871b-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="a871b-143">Nye enheder bliver tilgængelige via løbende frigivelser af Personale.</span><span class="sxs-lookup"><span data-stu-id="a871b-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="a871b-144">Gitteret indeholder følgende felter:</span><span class="sxs-lookup"><span data-stu-id="a871b-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="a871b-145">**CDS-enhedsnavn** – Navnet på enheden i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="a871b-146">**CD-enhedsreference** – den identifikator, som Common Data Service bruges til at identificere en post.</span><span class="sxs-lookup"><span data-stu-id="a871b-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="a871b-147">Denne værdi svarer til en **RecId**-værdi i Personale.</span><span class="sxs-lookup"><span data-stu-id="a871b-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="a871b-148">Du kan finde identifikatoren, når du åbner Common Data Service-enheden i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a871b-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="a871b-149">**Personaleenhedsnavn** – Den enhed, der sidst synkroniserede data til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="a871b-150">Enheden kan enten have Common Data Service-præfikset eller et andet præfiks.</span><span class="sxs-lookup"><span data-stu-id="a871b-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="a871b-151">**Personale-reference** – Den **RecId**-værdi, der er tilknyttet posten i Personale.</span><span class="sxs-lookup"><span data-stu-id="a871b-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="a871b-152">**Blev slettet fra CDS** – En værdi, der angiver, om posten blev slettet fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="a871b-153">Fjern tilknytningen af en post i Personale fra Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a871b-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="a871b-154">Hvis du får problemer under datasynkronisering mellem Personale og Common Data Service, kan du muligvis løse dem ved at rydde sporingen og lade sporingstabellen blive synkroniseret igen.</span><span class="sxs-lookup"><span data-stu-id="a871b-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="a871b-155">Hvis du fjerner tilknytningen og derefter ændrer eller sletter en post i Common Data Service, synkroniseres ændringerne ikke med Personale.</span><span class="sxs-lookup"><span data-stu-id="a871b-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="a871b-156">Hvis du foretager ændringer i Personale, oprettes der en ny sporingspost, og posten opdateres i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a871b-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="a871b-157">Hvis du vil fjerne tilknytningen af en post mellem Personale og Common Data Service, skal du vælge enheden i **CDS-enhedsnavn** og derefter vælge **Ryd sporingsoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a871b-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="a871b-158">[![Rydning af sporingsoplysninger](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="a871b-159">Se den næste procedure, hvis du vil køre en fuld synkronisering af enheden, når du har ryddet sporingen.</span><span class="sxs-lookup"><span data-stu-id="a871b-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="a871b-160">Synkronisere en enhed mellem Personale og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a871b-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="a871b-161">Benyt denne fremgangsmåde, når:</span><span class="sxs-lookup"><span data-stu-id="a871b-161">Use this procedure when:</span></span>

- <span data-ttu-id="a871b-162">Ændringerne fra Common Data Service er for længe om at blive vist i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a871b-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="a871b-163">Du skal opdatere sporingstabellen, efter at du har ryddet registreringen.</span><span class="sxs-lookup"><span data-stu-id="a871b-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="a871b-164">Sådan kører du en fuld synkronisering af en enhed mellem Human Resources og Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="a871b-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="a871b-165">Vælg enheden i feltet **CDS-enhedsnavn**.</span><span class="sxs-lookup"><span data-stu-id="a871b-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="a871b-166">Vælg **Synkroniser nu**.</span><span class="sxs-lookup"><span data-stu-id="a871b-166">Select **Sync now**.</span></span>

<span data-ttu-id="a871b-167">[![Køre en fuld synkronisering](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="a871b-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


