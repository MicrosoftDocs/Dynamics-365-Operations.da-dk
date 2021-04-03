---
title: Udvide Talent med Power Apps og Power Automate
description: Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Human Resources ved hjælp af Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: tfehr
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edc2352fa53ac93c582b608b65fc624ff5dcd2a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467067"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="668a4-103">Udvide med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="668a4-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="668a4-104">Denne artikel beskriver nogle eksempler på udvidelsesmulighederne for Microsoft Dynamics 365 Human Resources ved hjælp af Microsoft Power Apps og Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="668a4-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="668a4-105">Du kan importere løsningspakken, der er tilknyttet hvert eksempel, til dit Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="668a4-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="668a4-106">Du kan dernæst anvende pakkerne enten som vejledning eller som udgangspunktet for at implementere scenarier, der er anvendelige for din organisation.</span><span class="sxs-lookup"><span data-stu-id="668a4-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="668a4-107">Såfremt du ønsker at anvende de i dette emne beskrevne skabeloner og apps "som de er", skal du afprøve dem for at sikre dig, at de omfatter alle de scenarier, der er specifikke for din implementering.</span><span class="sxs-lookup"><span data-stu-id="668a4-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="668a4-108">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="668a4-108">Prerequisites</span></span>

- <span data-ttu-id="668a4-109">For at importere pakker skal brugerne have rettigheden **Miljøoprettelse**.</span><span class="sxs-lookup"><span data-stu-id="668a4-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="668a4-110">For at eksportere eller importere apps skal brugerne have en licens til en Power Apps Plan 2 eller en Power Apps Plan 2-prøveversion.</span><span class="sxs-lookup"><span data-stu-id="668a4-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="668a4-111">Integration med Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="668a4-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="668a4-112">Appen **Integration med Microsoft 365** kan anvendes til at udtrække teamoplysninger for brugere, der er logget på Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="668a4-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="668a4-113">Den refererer til arbejdere i personale for at udtrække medarbejderidentifikationstyper.</span><span class="sxs-lookup"><span data-stu-id="668a4-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="668a4-114">Ledere kan kontrollere udløbsdatoer for medarbejder-id-typer.</span><span class="sxs-lookup"><span data-stu-id="668a4-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="668a4-115">De kan også sende en påmindelse via mail, hvis medarbejder-id-typen udløber.</span><span class="sxs-lookup"><span data-stu-id="668a4-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="668a4-116">Power Automate kan integreres med Power Apps for at sende denne påmindelse.</span><span class="sxs-lookup"><span data-stu-id="668a4-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="668a4-117">Der sendes en bekræftelse tilbage til Power Apps fra Power Automate, når påmindelsen er sendt.</span><span class="sxs-lookup"><span data-stu-id="668a4-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="668a4-118">Identifikationstyper omfatter chaufførens kørekort, pas og andre acceptable former for id.</span><span class="sxs-lookup"><span data-stu-id="668a4-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="668a4-119">Du kan udvide denne app til andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="668a4-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="668a4-120">Du kan eksempelvis anvende den til at vise oplysninger om teamets ferie, kalenderhændelser og alle teamspecifikke hændelser.</span><span class="sxs-lookup"><span data-stu-id="668a4-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="668a4-121">Du kan downloade appen **Integration med Microsoft 365, Power Automate** ved at gå til [Integration med Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) i Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="668a4-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="668a4-122">Power Automate – Forbindelse til SQL og udførelse</span><span class="sxs-lookup"><span data-stu-id="668a4-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="668a4-123">Skabelonen **Power Automate – Forbindelse til SQL og udførelse** forbinder til Microsoft SQL Server og gør det muligt at køre SQL-forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="668a4-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="668a4-124">Selvom denne skabelon læser og opdaterer SQL-tabeller, kan du udvide den og bruge den til andre scenarier.</span><span class="sxs-lookup"><span data-stu-id="668a4-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="668a4-125">Du kan eksempelvis anvende den til at udfylde en stadieinddelt tabel i Dataverse med poster fra SQL-serveren og til at synkronisere den stadieinddelte tabel periodisk ved hjælp af en trinvis overførelse fra SQL-serveren.</span><span class="sxs-lookup"><span data-stu-id="668a4-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="668a4-126">En avanceret forespørgsel er integreret med flow, der muliggør datatransformation og trinvis push.</span><span class="sxs-lookup"><span data-stu-id="668a4-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="668a4-127">Du kan downloade skabelonen **Power Automate – Forbindelse til SQL og udførelse** i Microsoft Download Center ved hjælp af følgende link: [Power Automate – Forbindelse til SQL og udførelse](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="668a4-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="668a4-128">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="668a4-128">Additional resources</span></span>

[<span data-ttu-id="668a4-129">Klientens Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="668a4-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]