---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509285"
---
# <a name="workflow-system"></a><span data-ttu-id="e9201-103">Arbejdsgangsystem</span><span class="sxs-lookup"><span data-stu-id="e9201-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9201-104">Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9201-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="e9201-105">Beskeder</span><span class="sxs-lookup"><span data-stu-id="e9201-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="e9201-106">Hvorfor modtages flere beskeder, når en workflowopgave afvises?</span><span class="sxs-lookup"><span data-stu-id="e9201-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="e9201-107">Når en workflowopgave afvises, fuldføres den som afvist.</span><span class="sxs-lookup"><span data-stu-id="e9201-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="e9201-108">Der oprettes en anden workflowopgave, som tildeles til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="e9201-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="e9201-109">Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning".</span><span class="sxs-lookup"><span data-stu-id="e9201-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="e9201-110">Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring.</span><span class="sxs-lookup"><span data-stu-id="e9201-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="e9201-111">Vi ser på forskellige måder at forbedre dette i en senere version.</span><span class="sxs-lookup"><span data-stu-id="e9201-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="e9201-112">Hvorfor mislykkes eksporten af mine arbejdsgange?</span><span class="sxs-lookup"><span data-stu-id="e9201-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="e9201-113">Der er i øjeblikket en begrænsning i funktionen til eksport af arbejdsgange, som forhindrer, at arbejdsgangens navne overstiger 48 tegn.</span><span class="sxs-lookup"><span data-stu-id="e9201-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="e9201-114">Hvis du bruger et navn, der er længere end 48 tegn, kan det resultere i, at fejlen "Serveren kunne ikke godkende anmodningen", og/eller forhindre, at en fil kan eksporteres uden en filtype.</span><span class="sxs-lookup"><span data-stu-id="e9201-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="e9201-115">Følgende blogindlæg indeholder flere detaljer [Fejlfinding i forbindelse med eksport af arbejdsgang](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="e9201-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
