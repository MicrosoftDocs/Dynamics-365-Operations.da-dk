---
title: Udvide Talent med Power Apps og Power Automate
description: Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent - Attract ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029905"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="24f47-103">Udvide Talent med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="24f47-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="24f47-104">Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Talent: Attract ved hjælp af Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="24f47-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="24f47-105">Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="24f47-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="24f47-106">Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.</span><span class="sxs-lookup"><span data-stu-id="24f47-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24f47-107">Såfremt du ønsker at anvende de i denne artikel beskrevne skabeloner og appen "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.</span><span class="sxs-lookup"><span data-stu-id="24f47-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="24f47-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="24f47-108">Prerequisites</span></span>

- <span data-ttu-id="24f47-109">For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.</span><span class="sxs-lookup"><span data-stu-id="24f47-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="24f47-110">For at eksportere eller importere apps skal brugerne have en licens til en Power Apps Plan 2 eller en Power Apps Plan 2-prøveversion.</span><span class="sxs-lookup"><span data-stu-id="24f47-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="24f47-111">Power Automate – Tilknyt formular</span><span class="sxs-lookup"><span data-stu-id="24f47-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="24f47-112">Skabelonen **Power Automate – Tilknyt formular** kan anvendes til at læse data fra Microsoft Forms og lagre dem i en Common Data Service-enhed.</span><span class="sxs-lookup"><span data-stu-id="24f47-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="24f47-113">Denne skabelon kan udvides, således at den kan anvendes i andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="24f47-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="24f47-114">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="24f47-114">Here are some examples:</span></span>

- <span data-ttu-id="24f47-115">Hent kandidatvurderinger.</span><span class="sxs-lookup"><span data-stu-id="24f47-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="24f47-116">Hent resultater fra kursusspørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="24f47-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="24f47-117">Kompiler et bibliotek med samtalespørgsmål til personaleansvarlige.</span><span class="sxs-lookup"><span data-stu-id="24f47-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="24f47-118">Hent en kandidats vurdering af samtaleprocessen</span><span class="sxs-lookup"><span data-stu-id="24f47-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="24f47-119">I Microsoft Dynamics 365: Attract, du kan bruge formularer i kandidatportalen, hvor kandidaterne udfylder detaljerne.</span><span class="sxs-lookup"><span data-stu-id="24f47-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="24f47-120">Du kan ligeledes integrere formularer som aktiviteter i en jobskabelon.</span><span class="sxs-lookup"><span data-stu-id="24f47-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="24f47-121">Når en kandidat indsender en formular, henter Microsoft Power Automate formularen, læser dataene og lagre den i Common Data Service-enheden.</span><span class="sxs-lookup"><span data-stu-id="24f47-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="24f47-122">Du kan downloade skabelonen **Power Automate – Tilknyt formular** og Brugertilpasset enhedsstruktur i [Power Automate – Tilknyt formular](https://go.microsoft.com/fwlink/?linkid=2081988) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="24f47-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="24f47-123">Power Automate – SharePoint-integration</span><span class="sxs-lookup"><span data-stu-id="24f47-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="24f47-124">Skabelonen **Power Automate – SharePoint-integration** kan anvendes til at læse data fra en Microsoft SharePoint-liste, sammenligne listen med feltværdierne for alle Common Data Service-enheder og sende resultaterne af sammenligningen som en e-mailbesked.</span><span class="sxs-lookup"><span data-stu-id="24f47-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="24f47-125">En organisation har muligvis akut mangel på et bestemt sæt færdigheder.</span><span class="sxs-lookup"><span data-stu-id="24f47-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="24f47-126">Disse færdigheder kan lagres i SharePoint som en SharePoint-liste.</span><span class="sxs-lookup"><span data-stu-id="24f47-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="24f47-127">Når en kandidat søger et hvilket som helst job, som indeholder det sæt færdigheder, der er anført på listen, fremsendes en e-mailbesked, såfremt der er væsentligt sammenfald mellem kandidatens færdigheder og de færdigheder, der er lagret i SharePoint.</span><span class="sxs-lookup"><span data-stu-id="24f47-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="24f47-128">På den måde kan stillinger, hvor der er akut behov for ansættelse, hurtigere besættes, da beskeden hjælper rekrutteringsmedarbejdere med at ansætte kandidater på tværs af hele organisationen.</span><span class="sxs-lookup"><span data-stu-id="24f47-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="24f47-129">Denne skabelon kan udvides, så den kan anvendes i alle scenarier, der omfatter SharePoint-integration.</span><span class="sxs-lookup"><span data-stu-id="24f47-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="24f47-130">Du kan downloade skabelonen **Power Automate – SharePoint-integration** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – SharePoint-integration](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="24f47-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="24f47-131">Appen Henvisning</span><span class="sxs-lookup"><span data-stu-id="24f47-131">Referral App</span></span>

<span data-ttu-id="24f47-132">Du kan bruge appen Henvisning til at føje kandidater til en delt talentpulje.</span><span class="sxs-lookup"><span data-stu-id="24f47-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="24f47-133">Den, der henviser, kan angive **Fornavn**, **Efternavn**, **Mail** og **URL-adresse til LinkedIn** ved indsendelse af en kandidat.</span><span class="sxs-lookup"><span data-stu-id="24f47-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="24f47-134">Metadata til kandidatkilden udfyldes derefter med oplysningerne fra den, der henviser.</span><span class="sxs-lookup"><span data-stu-id="24f47-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="24f47-135">Du kan integrere denne app i Medarbejderselvbetjening (ESS) for at sende henvisninger, eller du kan bruge den som et link i firmaportalen og køre den som en enkeltstående app.</span><span class="sxs-lookup"><span data-stu-id="24f47-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="24f47-136">Du kan downloade **appen Henvisning** ved at gå til [Dynamics 365 Talent-udvidelsesløsning: appen Henvisning](https://www.microsoft.com/download/details.aspx?id=58497) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="24f47-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="24f47-137">Du kan importere denne app og tilpasse den for at tilføje yderligere funktioner.</span><span class="sxs-lookup"><span data-stu-id="24f47-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24f47-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="24f47-138">Additional resources</span></span>

[<span data-ttu-id="24f47-139">Klientens Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="24f47-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="24f47-140">Overfør app mellem lejere og miljøer</span><span class="sxs-lookup"><span data-stu-id="24f47-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
