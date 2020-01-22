---
title: Udvid Talent med Power Apps og Power Automate
description: Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898311"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="b1598-103">Udvid Talent med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="b1598-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="b1598-104">Dette emne beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent ved hjælp af Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="b1598-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="b1598-105">Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="b1598-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="b1598-106">Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.</span><span class="sxs-lookup"><span data-stu-id="b1598-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1598-107">Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.</span><span class="sxs-lookup"><span data-stu-id="b1598-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="b1598-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="b1598-108">Prerequisites</span></span>

- <span data-ttu-id="b1598-109">For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.</span><span class="sxs-lookup"><span data-stu-id="b1598-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="b1598-110">For at eksportere eller importere apps skal brugerne have en licens til en Power Apps Plan 2 eller en Power Apps Plan 2-prøveversion.</span><span class="sxs-lookup"><span data-stu-id="b1598-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="b1598-111">Power Automate – Tilknyt formular</span><span class="sxs-lookup"><span data-stu-id="b1598-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="b1598-112">Skabelonen **Power Automate – Tilknyt formular** kan anvendes til at læse data fra Microsoft Forms og lagre dem i en Common Data Service-enhed.</span><span class="sxs-lookup"><span data-stu-id="b1598-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="b1598-113">Denne skabelon kan udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="b1598-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b1598-114">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="b1598-114">Here are some examples:</span></span>

- <span data-ttu-id="b1598-115">Hent kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="b1598-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="b1598-116">Hent resultater fra kursusspørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="b1598-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="b1598-117">Kompiler et bibliotek med samtalespørgsmål til personaleansvarlige.</span><span class="sxs-lookup"><span data-stu-id="b1598-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="b1598-118">Hent en kandidats vurdering af samtaleprocessen</span><span class="sxs-lookup"><span data-stu-id="b1598-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="b1598-119">I Microsoft Dynamics 365: Attract kan formularer fremgå af en kandidats portal, og kandidaterne kan udfylde detaljerne.</span><span class="sxs-lookup"><span data-stu-id="b1598-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="b1598-120">Formularerne kan ligeledes indlejres som aktiviteter i en jobskabelon.</span><span class="sxs-lookup"><span data-stu-id="b1598-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="b1598-121">Når en kandidat indsender en formular, henter Microsoft Power Automate formularen, læser dataene og lagre den i Common Data Service-enheden.</span><span class="sxs-lookup"><span data-stu-id="b1598-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="b1598-122">Du kan downloade skabelonen **Power Automate – Tilknyt formular** og Brugertilpasset enhedsstruktur i [Power Automate – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="b1598-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="b1598-123">Påbegyndelse og udtræk af de parametre, der er overført til Power Apps</span><span class="sxs-lookup"><span data-stu-id="b1598-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="b1598-124">Skabelonen **Påbegyndelse og udtræk af de parametre, der er overført til Power Apps** kan anvendes som udgangspunktet for alle Power Apps-scenarier, der er specifikke for Attract.</span><span class="sxs-lookup"><span data-stu-id="b1598-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="b1598-125">Den omfatter alle standardparametre, som overføres fra Attract, såsom **Jobansøgning**, **Kandidat-id** og **Job-id**.</span><span class="sxs-lookup"><span data-stu-id="b1598-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="b1598-126">Denne skabelon kan anvendes til at hente en kandidats vurderingsformular, således at en ansættelsesansvarlig kan gennemgå den vurdering, kandidaten har udfyldt.</span><span class="sxs-lookup"><span data-stu-id="b1598-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="b1598-127">Apps, der er oprettet ved hjælp af Power Apps, kan integreres i jobskabelonen i Attract.</span><span class="sxs-lookup"><span data-stu-id="b1598-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="b1598-128">Du kan downloade skabelonen **Påbegyndelse og udtræk af parametre, der overføres til Power Apps** under [Påbegyndelse og udtræk af parametre, der overføres til Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="b1598-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="b1598-129">Integration med Office 365</span><span class="sxs-lookup"><span data-stu-id="b1598-129">Integration with Office 365</span></span>

<span data-ttu-id="b1598-130">Appen **Integration med Office 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1598-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="b1598-131">Den henviser arbejdere i Talent til at udtrække detaljer om arbejdsdagens start- og sluttidspunkt samt fortegnelser over undtagelser.</span><span class="sxs-lookup"><span data-stu-id="b1598-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="b1598-132">Detaljer om arbejdsdagens start- og sluttidspunkt lagres i brugertilpassede Common Data Service-enheder.</span><span class="sxs-lookup"><span data-stu-id="b1598-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="b1598-133">Det forudsættes, at disse detaljer udfyldes af tredjepartssystemer via integration.</span><span class="sxs-lookup"><span data-stu-id="b1598-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="b1598-134">Denne app kan udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="b1598-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b1598-135">Den kan eksempelvis anvendes til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.</span><span class="sxs-lookup"><span data-stu-id="b1598-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="b1598-136">Du kan downloade appen **Integration med Office 365** og "Brugertilpasset enhedsstruktur" i Microsoft Download Center ved hjælp af følgende link: [Integration med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="b1598-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="b1598-137">Power Automate – E-mailbesked</span><span class="sxs-lookup"><span data-stu-id="b1598-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="b1598-138">Skabelonen **Power Automate– E-mailbesked** kan anvendes i scenarier omhandlende e-mailbeskeder.</span><span class="sxs-lookup"><span data-stu-id="b1598-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="b1598-139">Den kan anvendes til at udløse e-mailbeskeder til kandidater vedrørende ansættelsesteamets afslag på alle stadier i rekrutteringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="b1598-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="b1598-140">Denne skabelon kan udvides til at spore ændringer i kandidatstadiet i hele rekrutteringsprocessen og til at sende beskeder til ansættelsesteamet og kandidaten.</span><span class="sxs-lookup"><span data-stu-id="b1598-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="b1598-141">Der kan generelt set, for de enheder, som er lagret i Common Data Service, konfigureres processer til at sende beskeder vedrørende hændelser, der finder sted i Core HR, Attract eller Onboard.</span><span class="sxs-lookup"><span data-stu-id="b1598-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="b1598-142">Du kan downloade skabelonen **Power Automate – E-mailbesked** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – E-mailbesked](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="b1598-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="b1598-143">Power Automate – Forbindelse til SQL og udførelse</span><span class="sxs-lookup"><span data-stu-id="b1598-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="b1598-144">Skabelonen **Power Automate – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="b1598-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="b1598-145">Selv om denne skabelon er designet til at læse og opdatere SQL-tabeller, kan den udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="b1598-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="b1598-146">Den kan eksempelvis anvendes til at udfylde en stadieinddelt tabel i Common Data Service med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.</span><span class="sxs-lookup"><span data-stu-id="b1598-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="b1598-147">Du kan downloade skabelonen **Power Automate – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="b1598-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="b1598-148">Power Automate – SharePoint-integration</span><span class="sxs-lookup"><span data-stu-id="b1598-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="b1598-149">Skabelonen **Power Automate – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked.</span><span class="sxs-lookup"><span data-stu-id="b1598-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="b1598-150">En organisation har muligvis akut mangel på et bestemt sæt færdigheder.</span><span class="sxs-lookup"><span data-stu-id="b1598-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="b1598-151">Disse færdigheder kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="b1598-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="b1598-152">Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b1598-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="b1598-153">Derved kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at indlede kontakten og ansætte kandidater på tværs af hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="b1598-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="b1598-154">Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.</span><span class="sxs-lookup"><span data-stu-id="b1598-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="b1598-155">Du kan downloade skabelonen **Power Automate – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="b1598-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="b1598-156">Appen Henvisning</span><span class="sxs-lookup"><span data-stu-id="b1598-156">Referral App</span></span>
<span data-ttu-id="b1598-157">Du kan bruge appen Henvisning til at føje kandidater til en delt talentpulje.</span><span class="sxs-lookup"><span data-stu-id="b1598-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="b1598-158">Den, der henviser, kan angive **Fornavn**, **Efternavn**, **Mail** og **URL-adresse til LinkedIn** ved indsendelse af en kandidat.</span><span class="sxs-lookup"><span data-stu-id="b1598-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="b1598-159">Metadata til kandidatkilden udfyldes derefter med oplysningerne fra den, der henviser.</span><span class="sxs-lookup"><span data-stu-id="b1598-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="b1598-160">Du kan integrere denne app i Medarbejderselvbetjening (ESS) for at sende henvisninger, eller du kan bruge den som et link i firmaportalen og køre den som en fritstående app.</span><span class="sxs-lookup"><span data-stu-id="b1598-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="b1598-161">Du kan downloade **appen Henvisning** ved at gå til [Dynamics 365 Talent-udvidelsesløsning: appen Henvisning](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="b1598-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="b1598-162">Du kan importere denne app og tilpasse den for at tilføje yderligere funktioner.</span><span class="sxs-lookup"><span data-stu-id="b1598-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1598-163">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b1598-163">Additional resources</span></span>

[<span data-ttu-id="b1598-164">Klientens Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="b1598-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="b1598-165">Overfør app mellem lejere og miljøer</span><span class="sxs-lookup"><span data-stu-id="b1598-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
