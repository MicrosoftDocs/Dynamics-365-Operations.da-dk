---
title: Udvide Talent ved hjælp af PowerApps og Microsoft Flow - eksempelscenarier
description: Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 for Talent ved hjælp af Microsoft PowerApps og Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517596"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="48421-103">Udvide Talent ved hjælp af PowerApps og Microsoft Flow - eksempelscenarier</span><span class="sxs-lookup"><span data-stu-id="48421-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="48421-104">Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 for Talent ved hjælp af Microsoft PowerApps og Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="48421-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="48421-105">Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit PowerApps-miljø.</span><span class="sxs-lookup"><span data-stu-id="48421-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="48421-106">Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.</span><span class="sxs-lookup"><span data-stu-id="48421-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48421-107">Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.</span><span class="sxs-lookup"><span data-stu-id="48421-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="48421-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="48421-108">Prerequisites</span></span>

- <span data-ttu-id="48421-109">For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.</span><span class="sxs-lookup"><span data-stu-id="48421-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="48421-110">For at eksportere eller importere apps skal brugerne have en licens til en PowerApps Plan 2 eller en PowerApps Plan 2-prøveversion.</span><span class="sxs-lookup"><span data-stu-id="48421-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="48421-111">Proces – Tilknyt formular</span><span class="sxs-lookup"><span data-stu-id="48421-111">Flow – Form Connect</span></span>

<span data-ttu-id="48421-112">Skabelonen **Proces – Tilknyt formular** kan anvendes til at læse data fra Microsoft-formularer og lagre det i en Common Data Service-enhed.</span><span class="sxs-lookup"><span data-stu-id="48421-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="48421-113">Denne skabelon kan udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="48421-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="48421-114">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="48421-114">Here are some examples:</span></span>

- <span data-ttu-id="48421-115">Hent kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="48421-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="48421-116">Hent resultater fra kursusspørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="48421-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="48421-117">Kompiler et bibliotek med samtalespørgsmål til personaleansvarlige.</span><span class="sxs-lookup"><span data-stu-id="48421-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="48421-118">Hent en kandidats vurdering af samtaleprocessen</span><span class="sxs-lookup"><span data-stu-id="48421-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="48421-119">I Microsoft Dynamics 365: Attract kan formularer fremgå af en kandidats portal, og kandidaterne kan udfylde detaljerne.</span><span class="sxs-lookup"><span data-stu-id="48421-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="48421-120">Formularerne kan ligeledes indlejres som aktiviteter i en jobskabelon.</span><span class="sxs-lookup"><span data-stu-id="48421-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="48421-121">Når en kandidat indsender en formular, henter Microsoft Flow formularen, læser dataene og lagre den i Common Data Service-enheden.</span><span class="sxs-lookup"><span data-stu-id="48421-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="48421-122">Du kan downloade skabelonen **Proces – Tilknyt formular** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Proces – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="48421-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="48421-123">Påbegyndelse og udtræk af de parametre, der er overført til PowerApps</span><span class="sxs-lookup"><span data-stu-id="48421-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="48421-124">Skabelonen **Påbegyndelse og udtræk af de parametre, der er overført til PowerApps** kan anvendes som udgangspunktet for alle PowerApps-scenarier, der er specifikke for Attract.</span><span class="sxs-lookup"><span data-stu-id="48421-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="48421-125">Den omfatter alle standardparametre, som overføres fra Attract, såsom **Jobansøgning**, **Kandidat-id** og **Job-id**.</span><span class="sxs-lookup"><span data-stu-id="48421-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="48421-126">Denne skabelon kan anvendes til at hente en kandidats vurderingsformular, således at en ansættelsesansvarlig kan gennemgå den vurdering, kandidaten har udfyldt.</span><span class="sxs-lookup"><span data-stu-id="48421-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="48421-127">Apps, der udvikles ved hjælp af PowerApps, kan integreres i jobskabelonen i Attract.</span><span class="sxs-lookup"><span data-stu-id="48421-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="48421-128">Du kan downloade skabelonen **Påbegyndelse og udtræk af parametre, der overføres til PowerApps** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Påbegyndelse og udtræk af parametre, der overføres til PowerApps](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="48421-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="48421-129">Integration med Office 365</span><span class="sxs-lookup"><span data-stu-id="48421-129">Integration with Office 365</span></span>

<span data-ttu-id="48421-130">Appen **Integration med Office 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="48421-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="48421-131">Den henviser arbejdere i Talent til at udtrække detaljer om arbejdsdagens start- og sluttidspunkt samt fortegnelser over undtagelser.</span><span class="sxs-lookup"><span data-stu-id="48421-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="48421-132">Detaljer om arbejdsdagens start- og sluttidspunkt lagres i brugertilpassede Common Data Service-enheder.</span><span class="sxs-lookup"><span data-stu-id="48421-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="48421-133">Det forudsættes, at disse detaljer udfyldes af tredjepartssystemer via integration.</span><span class="sxs-lookup"><span data-stu-id="48421-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="48421-134">Denne app kan udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="48421-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="48421-135">Den kan eksempelvis anvendes til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.</span><span class="sxs-lookup"><span data-stu-id="48421-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="48421-136">Du kan downloade appen **Integration med Office 365** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Integration med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="48421-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="48421-137">Proces – E-mailbesked</span><span class="sxs-lookup"><span data-stu-id="48421-137">Flow – Email Notification</span></span>

<span data-ttu-id="48421-138">Skabelonen **Proces – E-mailbesked** kan anvendes i scenarier omhandlende e-mailbeskeder.</span><span class="sxs-lookup"><span data-stu-id="48421-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="48421-139">Den kan anvendes til at udløse e-mailbeskeder til kandidater vedrørende ansættelsesteamets afslag på alle stadier i rekrutteringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="48421-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="48421-140">Denne skabelon kan udvides til at spore ændringer i kandidatstadiet i hele rekrutteringsprocessen og til at sende beskeder til ansættelsesteamet og kandidaten.</span><span class="sxs-lookup"><span data-stu-id="48421-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="48421-141">Der kan generelt set, for de enheder, som er lagret i Common Data Service, konfigureres processer til at sende beskeder vedrørende hændelser, der finder sted i Core HR, Attract eller Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="48421-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="48421-142">Du kan downloade skabelonen **Proces – E-mailbesked** i Microsoft Download Center ved hjælp af følgende link: [Proces – E-mailbesked](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="48421-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="48421-143">Proces – Forbindelse til SQL og udførelse</span><span class="sxs-lookup"><span data-stu-id="48421-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="48421-144">Skabelonen **Proces – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="48421-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="48421-145">Selv om denne skabelon er designet til at læse og opdatere SQL-tabeller, kan den udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="48421-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="48421-146">Den kan eksempelvis anvendes til at udfylde en stadieinddelt tabel i Common Data Service med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.</span><span class="sxs-lookup"><span data-stu-id="48421-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="48421-147">Du kan downloade skabelonen **Proces – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Proces – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="48421-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="48421-148">Proces – SharePoint-integration</span><span class="sxs-lookup"><span data-stu-id="48421-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="48421-149">Skabelonen **Proces – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked.</span><span class="sxs-lookup"><span data-stu-id="48421-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="48421-150">En organisation har muligvis akut mangel på et bestemt sæt færdigheder.</span><span class="sxs-lookup"><span data-stu-id="48421-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="48421-151">Disse færdigheder kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="48421-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="48421-152">Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint.</span><span class="sxs-lookup"><span data-stu-id="48421-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="48421-153">Derved kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at indlede kontakten og ansætte kandidater på tværs af hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="48421-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="48421-154">Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.</span><span class="sxs-lookup"><span data-stu-id="48421-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="48421-155">Du kan downloade skabelonen **Proces – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Proces – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="48421-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="48421-156">Administrationskonsol til styring af talentpuljer</span><span class="sxs-lookup"><span data-stu-id="48421-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="48421-157">Når du aktiverer integration med LinkedIn, opretter Attract automatisk en LinkedIn-talentgruppe.</span><span class="sxs-lookup"><span data-stu-id="48421-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="48421-158">Når en rekrutteringsmedarbejder udveksler InMail med en rekrutteret via LinkedIn, opretter Attract en profil til den rekrutterede person, og vedkommende bliver medlem af LinkedIn-talentpuljen.</span><span class="sxs-lookup"><span data-stu-id="48421-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="48421-159">Denne PowerApps-app er nyttig til reorganisering af kandidater i talentpuljer baseret på færdigheder.</span><span class="sxs-lookup"><span data-stu-id="48421-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="48421-160">Kør denne PowerApps-app som en administratorkonsol for at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="48421-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="48421-161">Angive kandidater i en talentpulje</span><span class="sxs-lookup"><span data-stu-id="48421-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="48421-162">Føje kandidater til og fjerne kandidater fra en talentpulje</span><span class="sxs-lookup"><span data-stu-id="48421-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="48421-163">Flytte kandidater fra én talentpulje til en anden</span><span class="sxs-lookup"><span data-stu-id="48421-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="48421-164">Afklare, om kandidater allerede er en del af en talentpulje, før de flyttes</span><span class="sxs-lookup"><span data-stu-id="48421-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="48421-165">Kontrollere kandidaternes færdigheder, før du flytter dem til andre talentpuljer</span><span class="sxs-lookup"><span data-stu-id="48421-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="48421-166">Denne PowerApps-app bruger mange-til-mange-relationer, så du kan bruge den som skabelon for andre scenarier, hvor du skal uddrage poster, der har mange-til-mange-relationer.</span><span class="sxs-lookup"><span data-stu-id="48421-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="48421-167">Du kan hente skabelonen **Administrationskonsol til styring af talentpuljer** ved at gå til [Administrationskonsol til styring af talentpuljer](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="48421-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48421-168">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="48421-168">Additional resources</span></span>

[<span data-ttu-id="48421-169">Klientens Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="48421-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="48421-170">Overfør app mellem lejere og miljøer</span><span class="sxs-lookup"><span data-stu-id="48421-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
