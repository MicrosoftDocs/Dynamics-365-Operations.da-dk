---
title: Nyheder eller ændringer i Dynamics 365 for Talent Core HR (16. oktober 2018)
description: Dette emne beskriver funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 51cfe8a92d1ac611e946934fe8ebbc99053788f1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517637"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a><span data-ttu-id="a6cd4-103">Nyheder eller ændringer i Dynamics 365 for Talent Core HR (19. oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="a6cd4-103">What's new or changed in Dynamics 365 for Talent Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="a6cd4-104">**Build 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="a6cd4-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="a6cd4-105">Dette emne beskriver funktioner, der enten er nye eller ændrede i Core HR.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="a6cd4-106">Tillade, at ledere kan opdatere anmodninger om fridage</span><span class="sxs-lookup"><span data-stu-id="a6cd4-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="a6cd4-107">Medarbejderens anmodninger fridage skal muligvis opdateres, når de er godkendt via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="a6cd4-108">I mange tilfælde udfører lederen selv disse opdateringer på medarbejderens vegne.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="a6cd4-109">Denne nye funktion giver lederne muligheden for at opdatere planlagte fridage eller annullere anmodninger om fridage på vegne af deres medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="a6cd4-110">Denne funktion styres af parameteren **Arbejde på vegne af**, der kan angives på siden **Parametre for personale**.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="a6cd4-111">Tillade, at HR kan opdatere anmodninger om fridage</span><span class="sxs-lookup"><span data-stu-id="a6cd4-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="a6cd4-112">I lighed med funktionen ovenfor skal medarbejderes anmodninger om fridage muligvis opdateres af personale, når de tidligere er blevet godkendt via arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="a6cd4-113">Denne funktion gør det muligt for personale at opdatere anmodninger om fridage.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="a6cd4-114">Funktionen aktiveres i arbejdsområdet **Personer** og på siden **Arbejder** ved hjælp af en ny indstilling, **Vis fridag**.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="a6cd4-115">HR-brugere kan på disse sider få vist anmodninger og opdatere fridagstransaktioner svarende til, hvordan administratorer kan udføre disse handlinger.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="a6cd4-116">Den sikkerhedsprogramadgangsrettighed, som styrer adgangen til denne funktion, er:</span><span class="sxs-lookup"><span data-stu-id="a6cd4-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="a6cd4-117">Programadgangsrettighed: Vedligehold arbejderspecifikke orlovs- og fraværsprocesser.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="a6cd4-118">Rettighed: Vedligehold anmodninger om orlov og fravær for alle arbejdere.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="a6cd4-119">Andre ændringer</span><span class="sxs-lookup"><span data-stu-id="a6cd4-119">Other changes</span></span>
<span data-ttu-id="a6cd4-120">Der er foretaget følgende opdateringer i denne version:</span><span class="sxs-lookup"><span data-stu-id="a6cd4-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="a6cd4-121">Ændringer af ansættelseshandlinger for arbejdere, så de er ikke længere "hænger fast" i tilstanden **Arbejdsgang er fuldført**.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="a6cd4-122">Ansættelsesposter kan nu oprettes uden en startdato for ansættelse.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="a6cd4-123">Registreringsdatoen i Dynamics 365 Talent for et kursus, der vises i medarbejderselvbetjeningsportalen, anvender nu tidszoneforskydning for datoen.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="a6cd4-124">Excel-filer kan importeres flere gange uden fejl ved hjælp af **medarbejderenhed**.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="a6cd4-125">Kendt problem</span><span class="sxs-lookup"><span data-stu-id="a6cd4-125">Known issue</span></span>

- <span data-ttu-id="a6cd4-126">**Problem**: Når du føjer en ny vedhæftet fil til en arbejder, bliver knapperne **Ny** og **Rediger** nedtonet.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="a6cd4-127">**Løsning:** Før du åbner siden Vedhæftet fil, skal du sørge for, at faktaboksene på siden **Arbejder** er lukket.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="a6cd4-128">Hvis faktaboksene lukkes, når siden **Arbejder** indlæses, vil knapperne for vedhæftede filer blive aktiveret.</span><span class="sxs-lookup"><span data-stu-id="a6cd4-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="a6cd4-129">(Dette problem vil blive løst i den næste platformsopdatering).</span><span class="sxs-lookup"><span data-stu-id="a6cd4-129">(This issue will be fixed in the next platform update.)</span></span>
