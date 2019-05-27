---
title: Nyheder eller ændringer i Dynamics 365 for Talent (14. februar 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517590"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="b342f-103">Nyheder eller ændringer i Dynamics 365 for Talent (14. februar 2019)</span><span class="sxs-lookup"><span data-stu-id="b342f-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b342f-104">I dette emne beskrives funktioner, der enten er nye eller ændrede i Talent.</span><span class="sxs-lookup"><span data-stu-id="b342f-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="b342f-105">Ændringer i Attract</span><span class="sxs-lookup"><span data-stu-id="b342f-105">Changes in Attract</span></span>
<span data-ttu-id="b342f-106">Der indgår mindre fejlrettelser i denne version.</span><span class="sxs-lookup"><span data-stu-id="b342f-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="b342f-107">Ændringer i Onboarding</span><span class="sxs-lookup"><span data-stu-id="b342f-107">Changes in Onboarding</span></span>
<span data-ttu-id="b342f-108">Der indgår mindre fejlrettelser i denne version.</span><span class="sxs-lookup"><span data-stu-id="b342f-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="b342f-109">Ændringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="b342f-109">Changes in Core HR</span></span> 
<span data-ttu-id="b342f-110">**Build 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="b342f-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="b342f-111">Enheden Fast løn til medarbejder eksportere ikke alle poster</span><span class="sxs-lookup"><span data-stu-id="b342f-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="b342f-112">Med denne ændring eksporterer enheden **Fast løn til medarbejder** nu alle poster.</span><span class="sxs-lookup"><span data-stu-id="b342f-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="b342f-113">Enheden kan bruges til at oprette og opdatere eksisterende faste lønposter for medarbejdere.</span><span class="sxs-lookup"><span data-stu-id="b342f-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="b342f-114">Slutdatoen for ansættelsen bruger ikke indstillinger for medarbejders foretrukken tidszone</span><span class="sxs-lookup"><span data-stu-id="b342f-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="b342f-115">Slutdato for ansættelser bruger nu den tidszone, brugeren foretrækker til at oprette eller afslutte ansættelse i et firma.</span><span class="sxs-lookup"><span data-stu-id="b342f-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="b342f-116">Britiske adresser vises i Analyser som adresser i den østlige del af Schweiz</span><span class="sxs-lookup"><span data-stu-id="b342f-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="b342f-117">Der er foretaget en ændring i denne version for at rette fejljustering i adresser i **Personalestyring** "antal beskæftigede pr. lokalitet"-rapporten.</span><span class="sxs-lookup"><span data-stu-id="b342f-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="b342f-118">Fratrædelseskode udfyldes ikke i posten for tildeling af arbejderstilling, når stillingen afsluttes</span><span class="sxs-lookup"><span data-stu-id="b342f-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="b342f-119">Der er foretaget en ændring for at anvende standardkoden for "Årsag til fratrædelse", når medarbejderens stillingstildeling afsluttes.</span><span class="sxs-lookup"><span data-stu-id="b342f-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="b342f-120">Ny enhed, der er oprettet for jobkompensationsniveauer</span><span class="sxs-lookup"><span data-stu-id="b342f-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="b342f-121">Et nyt datastyringsobjekt (DMF) er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="b342f-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="b342f-122">Objektet bruges til oprettelse og opdatering til kompensationsniveauer, markedsværdier og undersøgelsesoplysninger for hvert job, der er defineret i systemet.</span><span class="sxs-lookup"><span data-stu-id="b342f-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
