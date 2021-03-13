---
title: Introduktion til API-integration for ansøgersporingssystem
description: Dette emne beskriver Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System).
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125587"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="c702d-103">Introduktion til API-integration for ansøgersporingssystem</span><span class="sxs-lookup"><span data-stu-id="c702d-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="c702d-104">Dette emne beskriver Dynamics 365 Human Resources ATS-integrations-API (Applicant Tracking System).</span><span class="sxs-lookup"><span data-stu-id="c702d-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="c702d-105">Formålet med API er at aktivere strømlinet integration mellem Dynamics 365 Human Resources og partner-ATS'er.</span><span class="sxs-lookup"><span data-stu-id="c702d-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS-integrationsflow](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="c702d-107">Den integrerede erfaring begynder i Human Resources, når en ansættelseschef opretter en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c702d-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="c702d-108">Når anmodningen aktiveres, trækker ATS detaljerne for anmodningen om oprettelse af et rekrutteringsprojekt.</span><span class="sxs-lookup"><span data-stu-id="c702d-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="c702d-109">Derefter følger rekrutteringspipelinen for at vælge og ansætte en kandidat til stillingerne.</span><span class="sxs-lookup"><span data-stu-id="c702d-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="c702d-110">Endelig fuldfører ATS rundtur-integrationen ved at sende den valgte kandidats registrering til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c702d-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="c702d-111">Kandidatposten kan derefter gennemgå flere valideringer og arbejdsgange for at oprette medarbejderposten.</span><span class="sxs-lookup"><span data-stu-id="c702d-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="c702d-112">Human Resources har tilføjet følgende komponenter for at aktivere integrationen:</span><span class="sxs-lookup"><span data-stu-id="c702d-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="c702d-113">Funktioner til oprettelse af en rekrutteringsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c702d-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="c702d-114">En udvidet kandidatprofil og relaterede arbejdsgange.</span><span class="sxs-lookup"><span data-stu-id="c702d-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="c702d-115">En API til integration, der åbner de nye funktioner for integration af applikationer.</span><span class="sxs-lookup"><span data-stu-id="c702d-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="c702d-116">Du kan finde flere oplysninger om, hvordan du konfigurerer og bruger funktionerne til rekrutteringsanmodninger og ansøger, i [Rekrutteringsjobansøgere](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="c702d-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="c702d-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="c702d-117">Microsoft Dataverse</span></span>

<span data-ttu-id="c702d-118">Denne API er baseret på Microsoft Dataverse (tidligere Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="c702d-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="c702d-119">Al RESTful interaktion med denne API sker via Microsoft Dataverse Web-API, der bruger OData.</span><span class="sxs-lookup"><span data-stu-id="c702d-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="c702d-120">Denne API er et undersæt af Dataverse Web-API.</span><span class="sxs-lookup"><span data-stu-id="c702d-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="c702d-121">Dataverse Web-API definerer egenskaber som f.eks. godkendelse, servicespecifikationer, batch, samtidighedsstyring og håndtering af fejl.</span><span class="sxs-lookup"><span data-stu-id="c702d-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="c702d-122">Yderligere generelle oplysninger om Microsoft Dataverse Web-API finder du i:</span><span class="sxs-lookup"><span data-stu-id="c702d-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="c702d-123">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="c702d-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="c702d-124">Brug Microsoft Dataverse Web-API</span><span class="sxs-lookup"><span data-stu-id="c702d-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="c702d-125">Microsoft Dataverse-vejledning for udvikler</span><span class="sxs-lookup"><span data-stu-id="c702d-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="c702d-126">Dokumentationen ovenfor indeholder detaljer og udviklervejledning vedrørende brug af Dataverse Web-API, som f.eks. [administration af godkendelse](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [udførelse af handlinger](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [brug af Postman med API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) og [brug af sporing af ændring eller delta-tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) med API.</span><span class="sxs-lookup"><span data-stu-id="c702d-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="c702d-127">Grupperede indstillinger</span><span class="sxs-lookup"><span data-stu-id="c702d-127">Option sets</span></span>

<span data-ttu-id="c702d-128">Datamodellen for ATS integrations-API, som beskrives i dette dokument, omfatter den indstilling, der er angivet til at indeholde nummererede værdier, der er tilknyttet enhedsegenskaber.</span><span class="sxs-lookup"><span data-stu-id="c702d-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="c702d-129">Yderligere oplysninger om, hvordan du kan arbejde med de indstillinger, der er angivet i Dataverse Web-API, finder du i [Opret og opdater indstillinger, der er angivet ved hjælp af Web-API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="c702d-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="c702d-130">De indstillinger, der skal definere de enkelte Dataverse-miljøer.</span><span class="sxs-lookup"><span data-stu-id="c702d-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="c702d-131">Virtuelle tabeller i Dataverse Human Resources</span><span class="sxs-lookup"><span data-stu-id="c702d-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="c702d-132">Slutpunkterne for ATS integrations-API bruger funktionerne for den virtuelle Microsoft Dataverse-tabelplatform.</span><span class="sxs-lookup"><span data-stu-id="c702d-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="c702d-133">Som standard anvendes de virtuelle tabeller og de tilknyttede API-slutpunkter ikke i Human Resources-miljøer, hvilket gør det muligt for organisationer at bestemme, hvilke OData-slutpunkter der vises for miljøet.</span><span class="sxs-lookup"><span data-stu-id="c702d-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="c702d-134">Hvis du vil bruge API'en, skal de virtuelle tabeller for Human Resources-enhederne oprettes for miljøet.</span><span class="sxs-lookup"><span data-stu-id="c702d-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="c702d-135">Oplysninger om generering af virtuelle tabeller til API finder du i [Konfigurere Dataverse-virtuelle tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="c702d-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="c702d-136">Datamodel</span><span class="sxs-lookup"><span data-stu-id="c702d-136">Data model</span></span>

<span data-ttu-id="c702d-137">Datamodellen er fokuseret på to hovedenheder:</span><span class="sxs-lookup"><span data-stu-id="c702d-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="c702d-138">**RecruitingRequest** repræsenterer en anmodning til ATS om at rekruttere til en eller flere ledige stillinger. Du kan finde en eksempelforespørgsel i [Eksempelforespørgsel til rekrutteringsanmodning](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="c702d-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="c702d-139">**CandidateToHire** repræsenterer oplysninger om en kandidat, der har accepteret et tilbud om en stilling.</span><span class="sxs-lookup"><span data-stu-id="c702d-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="c702d-140">**Person** repræsenterer den person, der er kandidat.</span><span class="sxs-lookup"><span data-stu-id="c702d-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="c702d-141">En person kan have flere roller i firmaet, f.eks. kandidat, ansat, medarbejder eller kontrahent.</span><span class="sxs-lookup"><span data-stu-id="c702d-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="c702d-142">Du kan finde en forespørgsel om et eksempel i [Eksempelforespørgsel til kandidat til ansættelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="c702d-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="c702d-143">I følgende diagram vises forholdene i API grafisk.</span><span class="sxs-lookup"><span data-stu-id="c702d-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="c702d-144">Flere typer har fremmede nøgler til andre allerede eksisterende enheder i Human Resources, som ikke illustreres her.</span><span class="sxs-lookup"><span data-stu-id="c702d-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="c702d-145">Dette dokument indeholder oplysninger om enheder, der er specifikke for scenarier for rekrutteringsintegration.</span><span class="sxs-lookup"><span data-stu-id="c702d-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="c702d-146">Men der er mange andre enheder i Dataverse Web-API til Dynamics 365 Human Resources, som også kan være relevante for din integration.</span><span class="sxs-lookup"><span data-stu-id="c702d-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="c702d-147">Du har f.eks. også brug for detaljer for arbejdere, job, stillinger eller andre enheder, der ikke er defineret her.</span><span class="sxs-lookup"><span data-stu-id="c702d-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="c702d-148">Mange af disse enheder refereres til i relationer med fremmede nøgler eller navigationsegenskaber.</span><span class="sxs-lookup"><span data-stu-id="c702d-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integration, API-datamodel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="c702d-150">Rekrutteringsanmodning og relaterede enheder og indstillinger, der er angivet</span><span class="sxs-lookup"><span data-stu-id="c702d-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="c702d-151">Eksempelforespørgsel:</span><span class="sxs-lookup"><span data-stu-id="c702d-151">Example query:</span></span> 

- [<span data-ttu-id="c702d-152">Eksempelforespørgsel til anmodning om rekruttering</span><span class="sxs-lookup"><span data-stu-id="c702d-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="c702d-153">Enheder:</span><span class="sxs-lookup"><span data-stu-id="c702d-153">Entities:</span></span>

- [<span data-ttu-id="c702d-154">Rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="c702d-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="c702d-155">Stilling til rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="c702d-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="c702d-156">Rekrutteringsanmodningsfærdighed</span><span class="sxs-lookup"><span data-stu-id="c702d-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="c702d-157">Rekrutteringsanmodningsuddannelse</span><span class="sxs-lookup"><span data-stu-id="c702d-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="c702d-158">Lokation af rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="c702d-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="c702d-159">Indstillingssæt:</span><span class="sxs-lookup"><span data-stu-id="c702d-159">Option sets:</span></span>

- [<span data-ttu-id="c702d-160">Status for jobfritagelse</span><span class="sxs-lookup"><span data-stu-id="c702d-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="c702d-161">Status for rekrutteringsanmodningsstilling</span><span class="sxs-lookup"><span data-stu-id="c702d-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="c702d-162">Status for rekrutteringsanmodning</span><span class="sxs-lookup"><span data-stu-id="c702d-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="c702d-163">Kategori af lovpligtigt job</span><span class="sxs-lookup"><span data-stu-id="c702d-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="c702d-164">Kandidat til ansættelse og relaterede enheder og de indstillinger, der er angivet</span><span class="sxs-lookup"><span data-stu-id="c702d-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="c702d-165">Eksempelforespørgsel:</span><span class="sxs-lookup"><span data-stu-id="c702d-165">Example query:</span></span>

- [<span data-ttu-id="c702d-166">Eksempelforespørgsel til ansøger til ansættelse</span><span class="sxs-lookup"><span data-stu-id="c702d-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="c702d-167">Enheder:</span><span class="sxs-lookup"><span data-stu-id="c702d-167">Entities:</span></span>

- [<span data-ttu-id="c702d-168">Kandidat, der kan ansættes</span><span class="sxs-lookup"><span data-stu-id="c702d-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="c702d-169">Person</span><span class="sxs-lookup"><span data-stu-id="c702d-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="c702d-170">Personuddannelse</span><span class="sxs-lookup"><span data-stu-id="c702d-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="c702d-171">Persons erhvervserfaring</span><span class="sxs-lookup"><span data-stu-id="c702d-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="c702d-172">Personadresse</span><span class="sxs-lookup"><span data-stu-id="c702d-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="c702d-173">Kontakt til part</span><span class="sxs-lookup"><span data-stu-id="c702d-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="c702d-174">Personkompetence</span><span class="sxs-lookup"><span data-stu-id="c702d-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="c702d-175">Rangeringsniveau</span><span class="sxs-lookup"><span data-stu-id="c702d-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="c702d-176">Personcertifikat</span><span class="sxs-lookup"><span data-stu-id="c702d-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="c702d-177">Certifikattype</span><span class="sxs-lookup"><span data-stu-id="c702d-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="c702d-178">Personscreening</span><span class="sxs-lookup"><span data-stu-id="c702d-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="c702d-179">Screeningstyper</span><span class="sxs-lookup"><span data-stu-id="c702d-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="c702d-180">Personidentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="c702d-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="c702d-181">Indstillingssæt:</span><span class="sxs-lookup"><span data-stu-id="c702d-181">Option sets:</span></span>

- [<span data-ttu-id="c702d-182">Resultat af ansøgerintegration</span><span class="sxs-lookup"><span data-stu-id="c702d-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="c702d-183">Tomt ja-nej</span><span class="sxs-lookup"><span data-stu-id="c702d-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="c702d-184">Status for færdiggørelse</span><span class="sxs-lookup"><span data-stu-id="c702d-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="c702d-185">Kontakttype</span><span class="sxs-lookup"><span data-stu-id="c702d-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="c702d-186">Uddannelseskreditgrundlag</span><span class="sxs-lookup"><span data-stu-id="c702d-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="c702d-187">Køn</span><span class="sxs-lookup"><span data-stu-id="c702d-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="c702d-188">Ægteskabelig status</span><span class="sxs-lookup"><span data-stu-id="c702d-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="c702d-189">Måneder i året</span><span class="sxs-lookup"><span data-stu-id="c702d-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="c702d-190">Nej Ja</span><span class="sxs-lookup"><span data-stu-id="c702d-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="c702d-191">Periodeenhed</span><span class="sxs-lookup"><span data-stu-id="c702d-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="c702d-192">Screeningfrekvens</span><span class="sxs-lookup"><span data-stu-id="c702d-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="c702d-193">Screeningfrekvensen genereres fra</span><span class="sxs-lookup"><span data-stu-id="c702d-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="c702d-194">Færdighedsniveautype</span><span class="sxs-lookup"><span data-stu-id="c702d-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="c702d-195">Se også</span><span class="sxs-lookup"><span data-stu-id="c702d-195">See also</span></span>

[<span data-ttu-id="c702d-196">Rekruttere jobkandidater</span><span class="sxs-lookup"><span data-stu-id="c702d-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="c702d-197">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="c702d-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="c702d-198">Brug Microsoft Dataverse Web-API</span><span class="sxs-lookup"><span data-stu-id="c702d-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="c702d-199">Opret og opdater de indstillinger, der er angivet ved hjælp af Web-API</span><span class="sxs-lookup"><span data-stu-id="c702d-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>