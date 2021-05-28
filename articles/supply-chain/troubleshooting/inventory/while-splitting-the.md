---
title: Når et fastvægtantal opdeles, bruges minimumantallet i stedet for det nominelle antal
description: Når et fastvægtantal opdeles i batches, bruger feltet Plukantal det minimumantal, der er angivet for varen, og ikke det nominelle antal.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026380"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="d3974-103">Når et fastvægtantal opdeles, bruges minimumantallet i stedet for det nominelle antal</span><span class="sxs-lookup"><span data-stu-id="d3974-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="d3974-104">KB-nummer: 4612073</span><span class="sxs-lookup"><span data-stu-id="d3974-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="d3974-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="d3974-105">Symptoms</span></span>

<span data-ttu-id="d3974-106">Når et fastvægtantal opdeles i batches, bruger feltet **Plukantal** det minimumantal, der er angivet for varen, og ikke det nominelle antal.</span><span class="sxs-lookup"><span data-stu-id="d3974-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="d3974-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="d3974-107">Resolution</span></span>

<span data-ttu-id="d3974-108">Systemet fungerer som designet.</span><span class="sxs-lookup"><span data-stu-id="d3974-108">The system is behaving as designed.</span></span> <span data-ttu-id="d3974-109">Systemet bruger den enkelte varens opsætning for minimumantal til plukning.</span><span class="sxs-lookup"><span data-stu-id="d3974-109">The system uses each item's minimum quantity setup for picking.</span></span>
