---
title: Ofte stillede spørgsmål om arbejdsgang
description: Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/01/2019
ms.locfileid: "773201"
---
# <a name="workflow-system"></a><span data-ttu-id="f74a8-103">Arbejdsgangsystem</span><span class="sxs-lookup"><span data-stu-id="f74a8-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f74a8-104">Dette emne besvar ofte stillede spørgsmål om arbejdsgangssystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f74a8-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="f74a8-105">Beskeder</span><span class="sxs-lookup"><span data-stu-id="f74a8-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="f74a8-106">Hvorfor modtages flere beskeder, når en workflowopgave afvises?</span><span class="sxs-lookup"><span data-stu-id="f74a8-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="f74a8-107">Når en workflowopgave afvises, fuldføres den som afvist.</span><span class="sxs-lookup"><span data-stu-id="f74a8-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="f74a8-108">Der oprettes en anden workflowopgave, som tildeles til igangsætteren.</span><span class="sxs-lookup"><span data-stu-id="f74a8-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="f74a8-109">Det betyder, at der er en besked til igangsætteren af den afviste workflowopgave, og en særskilt besked til den bruger, der er tildelt til den nye workflowopgave med "ændringsanmodning".</span><span class="sxs-lookup"><span data-stu-id="f74a8-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="f74a8-110">Hver besked er for en særskilt workflowopgave, men lighedspunkter kan medføre forvirring.</span><span class="sxs-lookup"><span data-stu-id="f74a8-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="f74a8-111">Vi ser på forskellige måder at forbedre dette i en senere version.</span><span class="sxs-lookup"><span data-stu-id="f74a8-111">We are looking at ways to improve this in a future release.</span></span>
