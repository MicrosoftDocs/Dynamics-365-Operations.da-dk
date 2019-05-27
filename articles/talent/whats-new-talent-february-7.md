---
title: Nyheder eller ændringer i Dynamics 365 for Talent (7. februar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b89fc15130755a80b56f26cf7c61674a26f43e36
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517588"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a><span data-ttu-id="e490d-103">Nyheder eller ændringer i Dynamics 365 for Talent (7. februar 2019)</span><span class="sxs-lookup"><span data-stu-id="e490d-103">What's new or changed in Dynamics 365 for Talent (February 7, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e490d-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.</span><span class="sxs-lookup"><span data-stu-id="e490d-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="e490d-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="e490d-105">Changes in Attract</span></span>

### <a name="interview-scheduling-enhancements"></a><span data-ttu-id="e490d-106">Forbedringer af samtaleplanlægning</span><span class="sxs-lookup"><span data-stu-id="e490d-106">Interview scheduling enhancements</span></span>
<span data-ttu-id="e490d-107">Der er foretaget forbedringer af samtaleplanlægningen fra start til slut.</span><span class="sxs-lookup"><span data-stu-id="e490d-107">Improvements have been made to the end-to-end interview scheduling experience.</span></span> <span data-ttu-id="e490d-108">Du kan nu se kalendertilgængeligheden for en intern kandidat og bruge den interne kandidats kalender til anbefalinger i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="e490d-108">You can now see the calendar availability of an internal candidate and use the internal candidate’s calendar for schedule recommendations.</span></span> <span data-ttu-id="e490d-109">Yderligere oplysninger finder du i [Samtaleplanlægning og tilbagemelding](interview-scheduling-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="e490d-109">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a><span data-ttu-id="e490d-110">Jobopslag på LinkedIn – problem med firmauoverensstemmelse er rettet</span><span class="sxs-lookup"><span data-stu-id="e490d-110">Job posting to LinkedIn – company mismatch issue fixed</span></span>
<span data-ttu-id="e490d-111">Et problem er løst, hvor job, der er opslået på LinkedIn fra Attract, blev vist under det forkerte firmanavn.</span><span class="sxs-lookup"><span data-stu-id="e490d-111">An issue has been fixed where jobs posted to LinkedIn from Attract were appearing under the wrong company name.</span></span> <span data-ttu-id="e490d-112">Yderligere oplysninger finder du i [Oprette, godkende og opslå job i Attract](creating-jobs-attract.md).</span><span class="sxs-lookup"><span data-stu-id="e490d-112">For more information, see [Create, approve, and post jobs in Attract](creating-jobs-attract.md).</span></span>

### <a name="career-site-url-displayed-in-admin-settings"></a><span data-ttu-id="e490d-113">URL-adresse til karrierewebsted, der vises i administratorindstillinger</span><span class="sxs-lookup"><span data-stu-id="e490d-113">Career site URL displayed in Admin settings</span></span>
<span data-ttu-id="e490d-114">URL-adressen til startsiden for karrierewebsted vises nu i **Administratorindstillinger** under **Administration af karrierewebsted**.</span><span class="sxs-lookup"><span data-stu-id="e490d-114">The career site home page URL is now displayed in **Admin Settings** under **Career Site management**.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="e490d-115">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="e490d-115">Changes in Core HR</span></span>

<span data-ttu-id="e490d-116">**Build 8.1.2134**</span><span class="sxs-lookup"><span data-stu-id="e490d-116">**Build 8.1.2134**</span></span>

### <a name="multiple-compensation-levels-supported-on-jobs"></a><span data-ttu-id="e490d-117">Flere kompensationsniveauer understøttes for job</span><span class="sxs-lookup"><span data-stu-id="e490d-117">Multiple compensation levels supported on jobs</span></span>
<span data-ttu-id="e490d-118">Denne ændring giver mulighed for, at der kan defineres mere end ét kompensationsniveau for et job og dermed for afgrænsning af medarbejderens faste løn, som kan variere mellem planer, når der bruges samme job.</span><span class="sxs-lookup"><span data-stu-id="e490d-118">This change allows for more than one compensation level to be defined on a job, enabling employee fixed compensation ranges which may differ between plans when using the same job.</span></span> 

<span data-ttu-id="e490d-119">F.eks.:</span><span class="sxs-lookup"><span data-stu-id="e490d-119">For example:</span></span>    
<span data-ttu-id="e490d-120">*Job* - Kontoadministrator *Tilknyttede kompensationsniveauer:* B1 og B2 - Hvert niveau har et defineret interval af værdier.</span><span class="sxs-lookup"><span data-stu-id="e490d-120">*Job* - Account Manager *Associated compensation levels:* B1 and B2 - Each level has a defined range of values.</span></span> <span data-ttu-id="e490d-121">B1 = Min 50.000, Mid 60.000, Maks 75.000 og B2 = Min 65.000, Mid 74.000, Maks 85.000.</span><span class="sxs-lookup"><span data-stu-id="e490d-121">B1 = Min 50,000, Mid 60,000, Max 75,000 and B2 = Min 65,000, Mid 74,000, Max 85,000.</span></span> <span data-ttu-id="e490d-122">Ved oprettelse af fast løn for medarbejdere, der er baseret på de definerede berettigelsesregler, kan hver faste lønstruktur nu henvise til samme job og forskellige niveauer af jobbet.</span><span class="sxs-lookup"><span data-stu-id="e490d-122">When creating fixed compensation for employees, based on the eligibility rules defined, each fixed plan can now point to the same job and to different levels on the job.</span></span> <span data-ttu-id="e490d-123">Dette giver mulighed for, at strukturer kan defineres i forskellige områder/firmaer og henvise til det samme job, men forskellige begrænsninger, uden at det er nødvendigt at duplikere job for at tage højde for disse forskelle.</span><span class="sxs-lookup"><span data-stu-id="e490d-123">This allows for plans to be defined in different regions/companies and point to the same job but different ranges without duplicating jobs to account for these differences.</span></span>

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a><span data-ttu-id="e490d-124">Feltet Kompensationsniveau er føjet til enheden Fast løn til medarbejder</span><span class="sxs-lookup"><span data-stu-id="e490d-124">Compensation level field has been added to the Employee fixed compensation entity</span></span> 
<span data-ttu-id="e490d-125">Med denne opdatering er enheden Fast løn til medarbejder blevet opdateret, så den omfatter feltet **Kompensationsniveau**.</span><span class="sxs-lookup"><span data-stu-id="e490d-125">With this update, the employee fixed compensation entity has been updated to include the **Compensation level** field.</span></span> <span data-ttu-id="e490d-126">Denne tilføjelse gør det nemmere at opdatere medarbejderens faste lønstrukturer.</span><span class="sxs-lookup"><span data-stu-id="e490d-126">This addition makes it easier to update employee fixed compensation plans.</span></span> 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a><span data-ttu-id="e490d-127">Opdatere jobfamilie ved opdatering og oprettelse af nye stillinger</span><span class="sxs-lookup"><span data-stu-id="e490d-127">Update Job family when updating and creating new positions</span></span>
<span data-ttu-id="e490d-128">Når du ændrer jobbet i en stilling, får **Jobfamilie** nu standardindstillingen baseret på det job, der er valgt.</span><span class="sxs-lookup"><span data-stu-id="e490d-128">When changing the job on a position, **Job family** will now default based on the job selected.</span></span>

### <a name="performance-improvements-when-rendering-workspaces"></a><span data-ttu-id="e490d-129">Forbedringer af ydeevnen ved gengivelse af arbejdsområder</span><span class="sxs-lookup"><span data-stu-id="e490d-129">Performance improvements when rendering workspaces</span></span>
<span data-ttu-id="e490d-130">Analysefaner i arbejdsområder indlæses nu kun ved adgang til disse sider.</span><span class="sxs-lookup"><span data-stu-id="e490d-130">Analytics tabs on workspaces will now load only when accessing those pages.</span></span> <span data-ttu-id="e490d-131">Der vises en indikator under den indledende gengivelse af siden i øverste venstre hjørne af siden.</span><span class="sxs-lookup"><span data-stu-id="e490d-131">An indicator will display during the initial rendering of the page in the upper-left corner of the page.</span></span>
