---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvarer ofte stillede spørgsmål om arbejdsgangssystemet.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14aa9b56da005e8e3ca121589d0e22c60f34343b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189769"
---
# <a name="workflow-faq"></a><span data-ttu-id="debe5-103">Ofte stillede spørgsmål om arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="debe5-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="debe5-104">Dette emne besvarer ofte stillede spørgsmål om arbejdsgangssystemet.</span><span class="sxs-lookup"><span data-stu-id="debe5-104">This topic answers frequently asked questions about the workflow system.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="debe5-105">Hvorfor modtages flere beskeder, når en workflowopgave afvises?</span><span class="sxs-lookup"><span data-stu-id="debe5-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="debe5-106">Når en workflowopgave afvises, fuldføres den som afvist.</span><span class="sxs-lookup"><span data-stu-id="debe5-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="debe5-107">Der oprettes en anden workflowopgave, som tildeles til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="debe5-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="debe5-108">Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning".</span><span class="sxs-lookup"><span data-stu-id="debe5-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="debe5-109">Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring.</span><span class="sxs-lookup"><span data-stu-id="debe5-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="debe5-110">Vi ser på forskellige måder at forbedre dette i en senere version.</span><span class="sxs-lookup"><span data-stu-id="debe5-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="debe5-111">Hvorfor mislykkes eksporten af mine arbejdsgange?</span><span class="sxs-lookup"><span data-stu-id="debe5-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="debe5-112">Der er i øjeblikket en begrænsning i funktionen til eksport af arbejdsgange, som forhindrer, at arbejdsgangens navne overstiger 48 tegn.</span><span class="sxs-lookup"><span data-stu-id="debe5-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="debe5-113">Hvis du bruger et navn, der er længere end 48 tegn, kan det resultere i, at fejlen "Serveren kunne ikke godkende anmodningen", og/eller forhindre, at en fil kan eksporteres uden en filtype.</span><span class="sxs-lookup"><span data-stu-id="debe5-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="debe5-114">Følgende blogindlæg indeholder flere detaljer [Fejlfinding i forbindelse med eksport af arbejdsgang](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="debe5-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="debe5-115">Kan afsenderen af en arbejdsgang også godkende arbejdsgangen?</span><span class="sxs-lookup"><span data-stu-id="debe5-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="debe5-116">Ja, en afsender af en arbejdsgang kan også godkende arbejdsgangen, hvis den er konfigureret på denne måde.</span><span class="sxs-lookup"><span data-stu-id="debe5-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="debe5-117">Hvis du vil undgå dette, skal du angive **Arbejdsgangsparametre > Generelt > Godkender > Tillad ikke afsenders godkendelse** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="debe5-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="debe5-118">Kan jeg føje påmindelser til arbejdsgange for at sende beskeder til brugerne?</span><span class="sxs-lookup"><span data-stu-id="debe5-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="debe5-119">Her er nogle få nøgleområder, du kan bemærke om tilføjelse af påmindelser til arbejdsgange for at give beskeder:</span><span class="sxs-lookup"><span data-stu-id="debe5-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="debe5-120">Påmindelser for mekanismer til arbejdsgangsbeskeder</span><span class="sxs-lookup"><span data-stu-id="debe5-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="debe5-121">Påmindelser kan konfigureres til postændringer.</span><span class="sxs-lookup"><span data-stu-id="debe5-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="debe5-122">Arbejdsgange ændrer poster, så det er muligt at oprette en påmindelse, der relaterer til en post, der er blevet ændret pga. en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="debe5-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="debe5-123">Men da arbejdsgange har forskellige indbyggede beskedindstillinger, er brug af påmindelser ikke ideel.</span><span class="sxs-lookup"><span data-stu-id="debe5-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="debe5-124">Standardbeskeder fra arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="debe5-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="debe5-125">Arbejdsgange har indbyggede mailbeskeder.</span><span class="sxs-lookup"><span data-stu-id="debe5-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="debe5-126">En kunde kan konfigurere beskederne, så brugerne sendes som mails.</span><span class="sxs-lookup"><span data-stu-id="debe5-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="debe5-127">Disse beskeder resulterer ikke i Handlingscenter-meddelelser for brugere.</span><span class="sxs-lookup"><span data-stu-id="debe5-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="debe5-128">I en fremtidig opdatering vil vi tilføje en Handlingscenter-meddelelse, så en bruger får tildelt et arbejdsgangsopgave.</span><span class="sxs-lookup"><span data-stu-id="debe5-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="debe5-129">Føje beskeder til arbejdsgange</span><span class="sxs-lookup"><span data-stu-id="debe5-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="debe5-130">Handlingscenter-meddelelser kan oprettes for bestemte brugere, f.eks. en meddelelse, der er oprettet fra en arbejdsgang i X++.</span><span class="sxs-lookup"><span data-stu-id="debe5-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="debe5-131">[Arbejdsgangsforretningshændelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), som kunden kan bruge til at udløse flows, har de beskeder, de søger.</span><span class="sxs-lookup"><span data-stu-id="debe5-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="debe5-132">Hvis en bruger kort sagt ikke får den rigtige besked fra Handlingscenter, når vedkommende er blevet tildelt en arbejdsgangsopgave, så brug [Arbejdsgangsforretningshændelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) med Microsoft Flow til at give flere eller andre beskeder.</span><span class="sxs-lookup"><span data-stu-id="debe5-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
