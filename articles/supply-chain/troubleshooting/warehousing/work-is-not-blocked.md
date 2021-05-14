---
title: Arbejde er ikke blokeret
description: Arbejde er ikke blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924198"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="81057-103">Arbejde er ikke blokeret</span><span class="sxs-lookup"><span data-stu-id="81057-103">Work isn't blocked</span></span>

<span data-ttu-id="81057-104">Fejlkode: WSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="81057-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="81057-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="81057-105">Symptoms</span></span>

<span data-ttu-id="81057-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="81057-106">The system shows the following error message:</span></span>

> <span data-ttu-id="81057-107">Arbejde med id'et %1 er ikke blokeret.</span><span class="sxs-lookup"><span data-stu-id="81057-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="81057-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="81057-108">Cause</span></span>

<span data-ttu-id="81057-109">Indstillingen **Blokeret bølge** for bølgen er angivet til *Nej*.</span><span class="sxs-lookup"><span data-stu-id="81057-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="81057-110">Blokering af arbejdet kan ikke fjernes, da arbejdet ikke er blokeret i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="81057-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="81057-111">Løsning</span><span class="sxs-lookup"><span data-stu-id="81057-111">Resolution</span></span>

 <span data-ttu-id="81057-112">Det er kun arbejde, hvor indstillingen **Blokeret bølge** er angivet til *Ja*, hvor blokering kan fjernes.</span><span class="sxs-lookup"><span data-stu-id="81057-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
