---
title: Introduktion til lønintegrations-API
description: Dette emne beskriver API til Dynamics 365 Human Resources-lønintegration.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022757"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="5b7d7-103">Introduktion til lønintegrations-API</span><span class="sxs-lookup"><span data-stu-id="5b7d7-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5b7d7-104">Dette dokument beskriver API til Dynamics 365 Human Resources-lønintegration.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="5b7d7-105">API muliggør strømlinet totalintegration mellem Human Resources og partnerlønsystemer.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="5b7d7-106">Den integrerede erfaring begynder i Human Resources med medarbejderprofil, løn og fradrag og oplysninger om bidrag.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="5b7d7-107">Når du ansætter en medarbejder og angiver de nødvendige profil- og lønoplysninger i Human Resources, trækkes disse oplysninger ind i lønsystemet, som skal bruges ved behandling af løn.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="5b7d7-108">Opdateringer, der er foretaget for medarbejderen eller lønoplysninger, trækkes også ind til brug i senere lønkørsler.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Lønintegrationsflow](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="5b7d7-110">Human Resources har følgende komponenter for at aktivere integrationen:</span><span class="sxs-lookup"><span data-stu-id="5b7d7-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="5b7d7-111">Funktioner, der markerer en medarbejder som klar til løn</span><span class="sxs-lookup"><span data-stu-id="5b7d7-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="5b7d7-112">En API til integration, der åbner op for de nye funktioner for integration af applikationer</span><span class="sxs-lookup"><span data-stu-id="5b7d7-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="5b7d7-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="5b7d7-113">Microsoft Dataverse</span></span>

<span data-ttu-id="5b7d7-114">Denne API er baseret på Microsoft Dataverse (tidligere Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="5b7d7-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="5b7d7-115">Al RESTful interaktion med denne API sker via Microsoft Dataverse Web-API, der bruger OData.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="5b7d7-116">Denne API er et undersæt af Dataverse Web-API.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="5b7d7-117">Dataverse Web-API definerer egenskaber som f.eks. godkendelse, servicespecifikationer, batch, samtidighedsstyring og håndtering af fejl.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="5b7d7-118">Yderligere generelle oplysninger om Microsoft Dataverse Web-API finder du i:</span><span class="sxs-lookup"><span data-stu-id="5b7d7-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="5b7d7-119">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="5b7d7-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="5b7d7-120">Brug Microsoft Dataverse Web-API</span><span class="sxs-lookup"><span data-stu-id="5b7d7-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="5b7d7-121">Microsoft Dataverse-vejledning for udvikler</span><span class="sxs-lookup"><span data-stu-id="5b7d7-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="5b7d7-122">Denne dokumentation inkluderer oplysninger og udviklervejledning til brug af Dataverse Web-API'en, herunder følgende emner:</span><span class="sxs-lookup"><span data-stu-id="5b7d7-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="5b7d7-123">Godkende med Microsoft Dataverse med Web-API'en</span><span class="sxs-lookup"><span data-stu-id="5b7d7-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="5b7d7-124">Udføre handlinger ved hjælp af Web-API'en</span><span class="sxs-lookup"><span data-stu-id="5b7d7-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="5b7d7-125">Bruge Postman med Web-API'en</span><span class="sxs-lookup"><span data-stu-id="5b7d7-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="5b7d7-126">Bruge sporing af ændringer til at synkronisere data med eksterne systemer</span><span class="sxs-lookup"><span data-stu-id="5b7d7-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="5b7d7-127">Virtuelle tabeller i Dataverse Human Resources</span><span class="sxs-lookup"><span data-stu-id="5b7d7-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="5b7d7-128">Slutpunkterne for lønintegrations-API bruger funktionerne for den virtuelle Microsoft Dataverse-tabelplatform.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="5b7d7-129">Som standard anvendes de virtuelle tabeller og de tilknyttede API-slutpunkter ikke i Human Resources-miljøer, hvilket gør det muligt for organisationer at bestemme, hvilke OData-slutpunkter der vises for miljøet.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="5b7d7-130">Hvis du vil bruge API'en, skal de virtuelle tabeller for Human Resources-enhederne oprettes for miljøet.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="5b7d7-131">Oplysninger om generering af virtuelle tabeller til API finder du i [Konfigurere Dataverse-virtuelle tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="5b7d7-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="5b7d7-132">Datamodel</span><span class="sxs-lookup"><span data-stu-id="5b7d7-132">Data model</span></span>

<span data-ttu-id="5b7d7-133">I følgende diagram vises forholdene i API grafisk.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="5b7d7-134">Flere typer har fremmede nøgler til andre allerede eksisterende enheder i Human Resources, som ikke illustreres her.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="5b7d7-135">Dette dokument indeholder oplysninger om enheder, der er specifikke for scenarier til lønintegration.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="5b7d7-136">Men der er mange andre enheder i Dataverse Web-API til Human Resources, som også kan være relevante for din integration.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="5b7d7-137">Nogle af disse enheder refereres til i relationer med fremmede nøgler eller navigationsegenskaber.</span><span class="sxs-lookup"><span data-stu-id="5b7d7-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Lønintegration, API-datamodel](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="5b7d7-139">Lønmedarbejder og relaterede enheder</span><span class="sxs-lookup"><span data-stu-id="5b7d7-139">Payroll employee and related entities</span></span>

<span data-ttu-id="5b7d7-140">Enheder:</span><span class="sxs-lookup"><span data-stu-id="5b7d7-140">Entities:</span></span>

- [<span data-ttu-id="5b7d7-141">Medarbejders løn</span><span class="sxs-lookup"><span data-stu-id="5b7d7-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="5b7d7-142">Lønarbejderadresse</span><span class="sxs-lookup"><span data-stu-id="5b7d7-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="5b7d7-143">Plan for fast løn</span><span class="sxs-lookup"><span data-stu-id="5b7d7-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="5b7d7-144">Lønstillingsjob</span><span class="sxs-lookup"><span data-stu-id="5b7d7-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="5b7d7-145">Lønstilling</span><span class="sxs-lookup"><span data-stu-id="5b7d7-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="5b7d7-146">Se også</span><span class="sxs-lookup"><span data-stu-id="5b7d7-146">See also</span></span>

[<span data-ttu-id="5b7d7-147">Generere og gennemse lønenheder</span><span class="sxs-lookup"><span data-stu-id="5b7d7-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="5b7d7-148">Konfigurere Human Resources-parametre</span><span class="sxs-lookup"><span data-stu-id="5b7d7-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="5b7d7-149">Konfigurere delte Human Resources-parametre</span><span class="sxs-lookup"><span data-stu-id="5b7d7-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="5b7d7-150">Hvad er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="5b7d7-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="5b7d7-151">Brug Microsoft Dataverse Web-API</span><span class="sxs-lookup"><span data-stu-id="5b7d7-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]