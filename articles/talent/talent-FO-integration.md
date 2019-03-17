---
title: Ofte stillede spørgsmål om integration af Dynamics 365 for Talent med Dynamics 365 for Finance and Operations
description: I dette emne beskrives, hvilke data der synkroniseres i en integration af Talent og Finance and Operations.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303767"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="61378-103">Ofte stillede spørgsmål om integration af Dynamics 365 for Talent med Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="61378-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61378-104">Dette emne indeholder svar på almindelige spørgsmål om, hvilke data der synkroniseres, når Dynamics 365 for Talent integreres med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="61378-105">Synkroniseres alle data eller bare nogle dataenheder?</span><span class="sxs-lookup"><span data-stu-id="61378-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="61378-106">Med Core HR (Human Resources) synkroniseres et undersæt af dataene.</span><span class="sxs-lookup"><span data-stu-id="61378-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="61378-107">Du kan finde en liste over alle enheder i [Integration fra Dynamics 365 for Talent til Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="61378-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="61378-108">I Attract og Onboard er alle data indbygget i Common Data Service (CDS) for Apps.</span><span class="sxs-lookup"><span data-stu-id="61378-108">For Attract and Onboard, all data is native to Common Data Services (CDS) for Apps.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="61378-109">Kan jeg oprette en ny tilknytning uden at bruge skabelonerne?</span><span class="sxs-lookup"><span data-stu-id="61378-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="61378-110">Skabeloner bruges som udgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="61378-110">Templates are the starting point.</span></span> <span data-ttu-id="61378-111">Du kan oprette din egen skabelon, men der skal altid bruges en skabelon ved oprettelse af et integrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="61378-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="61378-112">Du kan finde flere oplysninger om dataintegrator (DI), skabeloner og projekter i [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="61378-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="61378-113">Kan jeg tilknytte økonomiske dimensioner for at overføre mellem Talent og Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="61378-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="61378-114">Økonomiske dimensioner findes ikke aktuelt i CDS for Apps og er derfor ikke del af standardskabelonen.</span><span class="sxs-lookup"><span data-stu-id="61378-114">Financial dimensions aren’t currently in CDS for Apps and as a result aren’t part of the default template.</span></span> <span data-ttu-id="61378-115">Denne enhed er planlagt, men i øjeblikket er der ingen versionstidslinje.</span><span class="sxs-lookup"><span data-stu-id="61378-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="61378-116">For data i Finance and Operations, som ikke findes i Talent, kan du sammenkæde de to systemer ved hjælp af **Konfigurer links** i Talent.</span><span class="sxs-lookup"><span data-stu-id="61378-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="61378-117">Du kan finde flere oplysninger om, hvordan du konfigurerer links mellem Talent og Finance and Operations, i [Nyheder eller ændringer i Dynamics 365 for Talent Core HR (31. oktober 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="61378-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="61378-118">Når jeg importerer medarbejdere, bliver de sommetider placeret blandt inaktive arbejdere i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-118">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="61378-119">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="61378-119">Why?</span></span>

<span data-ttu-id="61378-120">Denne fejl kan opstå, hvis medarbejderne ikke har en aktiv post med ansættelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="61378-120">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="61378-121">Du kan løse dette ved at gå til **Personalestyring \> Medarbejdere \> Ansættelseshistorik \> Datoadministrator** og kontrollere, at der findes en aktiv post med ansættelsesoplysninger.</span><span class="sxs-lookup"><span data-stu-id="61378-121">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="61378-122">Hvis jeg vælger kun at tilknytte et undersæt af felter, udløser ændringer af ikke-tilknyttede felter så en synkronisering?</span><span class="sxs-lookup"><span data-stu-id="61378-122">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="61378-123">Synkronisering af data følger tidsplanen for udførelse.</span><span class="sxs-lookup"><span data-stu-id="61378-123">Data sync follows the execution schedule.</span></span> <span data-ttu-id="61378-124">Integrationen henter en post, hvis et felt i posten ændres, uanset om feltet er en del af integrationstilknytningen.</span><span class="sxs-lookup"><span data-stu-id="61378-124">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="61378-125">Hvordan kan jeg nøjes med at sende ændringer, der kun gælder en aktiv arbejder og ikke de afsluttede poster?</span><span class="sxs-lookup"><span data-stu-id="61378-125">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="61378-126">Ved hjælp af "Avanceret forespørgsel" kan du filtrere og omforme kildedata, før du overfører dem til destinationen.</span><span class="sxs-lookup"><span data-stu-id="61378-126">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="61378-127">Kan jeg angive, hvilke felter der skal sendes til Finance and Operations for en bestemt enhed?</span><span class="sxs-lookup"><span data-stu-id="61378-127">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="61378-128">Felter kan tilføjes eller fjernes fra integrationsopgaven.</span><span class="sxs-lookup"><span data-stu-id="61378-128">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="61378-129">Ikke alle datafelter, der findes på CDS for Apps (CDS 2.0)-enheden udfyldes fra Core HR.</span><span class="sxs-lookup"><span data-stu-id="61378-129">Not all data fields that exist on the CDS for Apps (CDS 2.0) entity will be populated from Core HR.</span></span>
<span data-ttu-id="61378-130">Yderligere data kan udfyldes via PowerApps.</span><span class="sxs-lookup"><span data-stu-id="61378-130">Additional data can be populated via PowerApps.</span></span>

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="61378-131">Jeg konfigurerede integration som et batchjob, men så mistede Talent forbindelsen til destinationssystemet.</span><span class="sxs-lookup"><span data-stu-id="61378-131">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="61378-132">Hvordan kan jeg sende det samme sæt ændringer til destinationssystemet?</span><span class="sxs-lookup"><span data-stu-id="61378-132">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="61378-133">Der kræves ingen speciel opsætning for undtagelseshåndtering.</span><span class="sxs-lookup"><span data-stu-id="61378-133">No special setup is required for exception handling.</span></span> <span data-ttu-id="61378-134">Dataintegrator registrerer og rapporterer automatisk fejl, der finder sted på kilde og destination og giver mulighed for nye manuelle forsøg.</span><span class="sxs-lookup"><span data-stu-id="61378-134">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="61378-135">Men det tillader ikke manuel rettelse af data.</span><span class="sxs-lookup"><span data-stu-id="61378-135">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="61378-136">Hvis det er nødvendigt at opdatere data, skal det foregå ved kilden eller destinationen.</span><span class="sxs-lookup"><span data-stu-id="61378-136">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="61378-137">Kan jeg konfigurere tovejsintegration?</span><span class="sxs-lookup"><span data-stu-id="61378-137">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="61378-138">Nej, integration går i øjeblikket kun fra Talent til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-138">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="61378-139">Der er dog en tilgængelig standardskabelon, som kan bruges til at sende data fra Talent til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-139">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="61378-140">Kan jeg tillade sletning af poster som en del af integrationen?</span><span class="sxs-lookup"><span data-stu-id="61378-140">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="61378-141">Nej, Dataintegrator henter ikke slettede poster til dataoverførsel.</span><span class="sxs-lookup"><span data-stu-id="61378-141">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="61378-142">Kun oprettelse og opdateringer af data (UPSERT) er inkluderet i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="61378-142">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="61378-143">Kan jeg foretage den kørsel, der mislykkedes, igen?</span><span class="sxs-lookup"><span data-stu-id="61378-143">Can I rerun the errored execution?</span></span> <span data-ttu-id="61378-144">Vil den i så fald sende en komplet fil eller kun ændringerne?</span><span class="sxs-lookup"><span data-stu-id="61378-144">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="61378-145">Den første kørsel af Dataintegrator er altid en fuld kørsel.</span><span class="sxs-lookup"><span data-stu-id="61378-145">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="61378-146">Efterfølgende kørsler er baseret på registrering af ændringer.</span><span class="sxs-lookup"><span data-stu-id="61378-146">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="61378-147">Når der er foretaget en fejlkørsel, pakkes posterne, der er medtaget i kørslen, ud og de seneste ændringer fra CDS udsendes.</span><span class="sxs-lookup"><span data-stu-id="61378-147">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from CDS.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="61378-148">Når jeg gemmer projektet, får jeg fejlmeddelelsen: "Projektet har tilknytningsfejl".</span><span class="sxs-lookup"><span data-stu-id="61378-148">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="61378-149">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-149">What do I do?</span></span>

<span data-ttu-id="61378-150">Kontroller konfiguration af integrationsnøglerne, foretag eventuelle nødvendige ændringer i opsætningen, og opdater derefter objekterne i projektet.</span><span class="sxs-lookup"><span data-stu-id="61378-150">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="61378-151">Når standardskabelonen bruges, importeres integrationsnøglerne automatisk.</span><span class="sxs-lookup"><span data-stu-id="61378-151">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="61378-152">Dette problem kan opstå, når der føjes nye opgaver til den eksisterende skabelon.</span><span class="sxs-lookup"><span data-stu-id="61378-152">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="61378-153">Hvis jeg har N antal juridiske enheder, hvor arbejdere har ansættelse, skal jeg så oprette en tilknytning for hver af dem?</span><span class="sxs-lookup"><span data-stu-id="61378-153">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="61378-154">Ja, du skal bruge et separat integrationsprojekt i dataintegrationen for hver juridisk enhed i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-154">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="61378-155">Jeg har brug at overføre data, ikke der er en del af den standardskabelon, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61378-155">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="61378-156">Kan jeg gøre det?</span><span class="sxs-lookup"><span data-stu-id="61378-156">Can I do this?</span></span>

<span data-ttu-id="61378-157">Ja, du kan tilføje felter i eller fjerne dem fra den eksisterende skabelon.</span><span class="sxs-lookup"><span data-stu-id="61378-157">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="61378-158">Skabelonen kan ændres, så der medtages yderligere data fra andre CDS for Apps-enheder.</span><span class="sxs-lookup"><span data-stu-id="61378-158">The template can be modified to include additional data from other CDS for Apps entities.</span></span> <span data-ttu-id="61378-159">Enheden skal være i CDS for Apps, hvis den skal medtages i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="61378-159">The entity must be in CDS for Apps for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="61378-160">Jeg har netop oprettet nye Finance and Operations- og Talent-miljøer, og jeg får fejlmeddelelsen "Dataværdien overtræder integritetsbegrænsningerne".</span><span class="sxs-lookup"><span data-stu-id="61378-160">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="61378-161">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="61378-161">Why?</span></span>

<span data-ttu-id="61378-162">Årsager til denne fejl kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="61378-162">Reasons for this error can include:</span></span>

- <span data-ttu-id="61378-163">Dataoverførslen medførte, at der blev udtrukket dubletposter ved kilden (CDS).</span><span class="sxs-lookup"><span data-stu-id="61378-163">The data transfer resulted in duplicate records extraction at the source (CDS).</span></span>

- <span data-ttu-id="61378-164">Dataoverførslen har null-værdier for felter, der kræves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-164">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="61378-165">Kontroller de data, der er i CDS, og at de opfylder kravene i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-165">Verify the data that is in CDS and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="61378-166">Hvis der er kørselsfejl, og medarbejder-id'et ikke synkroniseres, hvordan finder jeg så historikjobbet med den mislykkede medarbejderpost?</span><span class="sxs-lookup"><span data-stu-id="61378-166">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="61378-167">Dataintegrator opretter flere projekter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-167">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="61378-168">Forholdet mellem Dataintegrator-opgaven og Finance and Operations-projektet er 1 til 1.</span><span class="sxs-lookup"><span data-stu-id="61378-168">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="61378-169">Spor tiden fra historikken for Dataintegrator-udførelse, og se efter indeks -1-projektet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-169">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="61378-170">Hvis opgavenummeret er 9 i Dataintegrator, er indekset i Finance and Operations 8.</span><span class="sxs-lookup"><span data-stu-id="61378-170">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="61378-171">Hent opgaveindekset fra Dataintegrator (i dette eksempel er det "9").</span><span class="sxs-lookup"><span data-stu-id="61378-171">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Hent opgaveindeks fra Dataintegrator](media/CaptureTaskIndex.png)

2. <span data-ttu-id="61378-173">Spor projektets kørselstidspunkt.</span><span class="sxs-lookup"><span data-stu-id="61378-173">Track the execution time of the project.</span></span>

![Spor projektets kørselstidspunkt](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="61378-175">Identificer indeks - 1 i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-175">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="61378-176">I dette eksempel matcher projektet med suffikset "8" og kørselstidspunkt for indeks "0" udførelsestidspunktet i trin 2.</span><span class="sxs-lookup"><span data-stu-id="61378-176">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Identifikation af indeks](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="61378-178">Jeg kan ikke se dataene i Finance and Operations efter at have integreret Talent og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-178">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="61378-179">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-179">What do I do?</span></span>

<span data-ttu-id="61378-180">Integrationen i Finance and Operations er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="61378-180">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="61378-181">Kontroller først, at Talent-dataene er opdaterede og tilgængelige i CDS.</span><span class="sxs-lookup"><span data-stu-id="61378-181">First, verify that the Talent data is updated and available in CDS.</span></span> <span data-ttu-id="61378-182">Dette er en synkronisering i nær-realtid, som du kan kontrollere i PowerApps ved at se på dataene i dataenhederne.</span><span class="sxs-lookup"><span data-stu-id="61378-182">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Data i CDS](media/DataInCDS.png)

<span data-ttu-id="61378-184">Hvis dataene ikke vises som forventet i CDS, kan du kontrollere, om enheden understøttes i integrationen.</span><span class="sxs-lookup"><span data-stu-id="61378-184">If the data is not appearing as expected in CDS, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="61378-185">For at medtage flere data i CDS kræver det en ændring fra Microsofts side.</span><span class="sxs-lookup"><span data-stu-id="61378-185">To include additional data in CDS, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="61378-186">Hvis enheden understøttes, og dataene er tilgængelige i CDS, skal du kontrollere, at tilknytningen er korrekt i Dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="61378-186">If the entity is supported and the data is available in CDS, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="61378-187">Hvis integratortilknytningen ser ud til at være i orden, skal du kontrollere, at datastyringsjobbet er kørt korrekt.</span><span class="sxs-lookup"><span data-stu-id="61378-187">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="61378-188">Fejl kan opstå under kørsel af batchjob.</span><span class="sxs-lookup"><span data-stu-id="61378-188">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="61378-189">Du kan finde flere oplysninger om datastyring i [Datastyring](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="61378-189">For more information about Data Management, see [Data management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="61378-190">Adresserne for mine medarbejdere er forkerte, når jeg har importeret dem i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-190">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="61378-191">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-191">What should I do?</span></span>

<span data-ttu-id="61378-192">Nummerserien for **Lokations-id** bruger det samme mønster i Finance and Operations som i Talent.</span><span class="sxs-lookup"><span data-stu-id="61378-192">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="61378-193">Nummerserien skal være entydig på begge sider, så der ikke opstår adressekollisioner under integration af data fra CDS til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-193">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from CDS to Finance and Operations.</span></span>

<span data-ttu-id="61378-194">Ved implementering af Talent skal du kontrollere, at nummerserierne ikke de samme i Talent og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-194">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="61378-195">Kontroller, at alle nummerserier ikke er ens, hvor data kan vedligeholdes i begge systemer.</span><span class="sxs-lookup"><span data-stu-id="61378-195">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="61378-196">Når jeg opretter mit forbindelsessæt, kan jeg ikke se forbindelsen i rullelisten Forbindelse.</span><span class="sxs-lookup"><span data-stu-id="61378-196">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="61378-197">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-197">What do I do?</span></span>

<span data-ttu-id="61378-198">Sørg for, når du opretter forbindelser, at vælge Dynamics 365 for Finance and Operations (i øjeblikket som prøveversion) og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="61378-198">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="61378-199">Når jeg synkroniserer ansættelser, vises fejlmeddelelserne "CompanyInfo_FK findes ikke", eller "Værdien '31/12/2154 23:59:59' i feltet 'Slutdato for ansættelse' bliver ikke fundet i den relaterede tabel 'Ansættelse'". Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-199">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="61378-200">Kontroller, at det er de korrekte juridiske enheder, du opretter tilknytning til.</span><span class="sxs-lookup"><span data-stu-id="61378-200">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="61378-201">Synkronisering af juridisk enhed er ikke en del af standardskabelonen, så det forventes, at de enkelte juridiske enheder, der findes i Talent og CDS, også findes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61378-201">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and CDS is also present in Finance and Operations.</span></span>
<span data-ttu-id="61378-202">Kontroller også, at det er de korrekte juridiske enheder for det tilknyttede forbindelsessæt, du vælger.</span><span class="sxs-lookup"><span data-stu-id="61378-202">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="61378-203">Når jeg har oprettet projektet, ser felttilknytningen for Finance and Operations ud til at være tom.</span><span class="sxs-lookup"><span data-stu-id="61378-203">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="61378-204">Hvad skal jeg gøre?</span><span class="sxs-lookup"><span data-stu-id="61378-204">What should I do?</span></span>

<span data-ttu-id="61378-205">Opdater dataenhederne i Finance and Operations ved at gå til **Datastyring \> Rammeparametre \> Indstillinger for enhed \> Opdater liste over enheder.**</span><span class="sxs-lookup"><span data-stu-id="61378-205">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="61378-206">Dette tager et par minutter, og derefter bør du kunne se disse tilknytninger.</span><span class="sxs-lookup"><span data-stu-id="61378-206">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="61378-207">Dette problem opstår, når der oprettes nye projekter.</span><span class="sxs-lookup"><span data-stu-id="61378-207">This issue occurs when new projects are created.</span></span>

![Manglende felttilknytning](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="61378-209">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="61378-209">Additional resources</span></span>

- <span data-ttu-id="61378-210">Dataintegrator (DI):</span><span class="sxs-lookup"><span data-stu-id="61378-210">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="61378-211">Integrere data i Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="61378-211">Integrate data into Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="61378-212">Dataintegrator-fejlstyring og fejlfinding</span><span class="sxs-lookup"><span data-stu-id="61378-212">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="61378-213">Svar på DSR-anmodninger om systemgenererede logfiler i PowerApps, Microsoft Flow og Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="61378-213">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="61378-214">Datastyring:</span><span class="sxs-lookup"><span data-stu-id="61378-214">Data Management:</span></span>

  - [<span data-ttu-id="61378-215">Datastyring</span><span class="sxs-lookup"><span data-stu-id="61378-215">Data management</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)