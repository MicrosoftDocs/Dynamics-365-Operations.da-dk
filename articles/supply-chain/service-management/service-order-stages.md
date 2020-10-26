---
title: Serviceordrestadier
description: Ved at definere stadier for en serviceordre og tildele dem til arbejdere styrer du forløbet for en serviceordre gennem de opgaver, som forskellige personer udfører i en serviceorganisation.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978429"
---
# <a name="service-order-stages"></a><span data-ttu-id="e2f49-103">Serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="e2f49-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e2f49-104">Du kan oprette stadier for en serviceordre for at definere de opgaver, der skal udføres, den rækkefølge, hvori de færdiggøres, og de arbejdere, der er ansvarlige for at fuldføre dem.</span><span class="sxs-lookup"><span data-stu-id="e2f49-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="e2f49-105">Ved at definere stadier for en serviceordre og tildele dem til arbejdere kan du styre forløbet for en serviceordre gennem de opgaver, som forskellige personer udfører i en serviceorganisation.</span><span class="sxs-lookup"><span data-stu-id="e2f49-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="e2f49-106">Sekvensen af stadier skal indeholde et indledende stadie.</span><span class="sxs-lookup"><span data-stu-id="e2f49-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="e2f49-107">Du kan også definere de handlinger, der er tilladt i hvert stadie.</span><span class="sxs-lookup"><span data-stu-id="e2f49-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="e2f49-108">Hvis du f.eks. fjerner markeringen i afkrydsningsfeltet **Bogfør** for alle stadier undtagen det endelige stadie, vil ingen serviceordrer blive bogført, før serviceordrerne har gennemgået behandlingen i hele sekvensen af stadier.</span><span class="sxs-lookup"><span data-stu-id="e2f49-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="e2f49-109">Forgrening i serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="e2f49-109">Branching in service order stages</span></span>

<span data-ttu-id="e2f49-110">Når du har oprettet et servicestadie, kan du oprette flere indstillinger, eller grene, som du kan vælge i det næste servicestadie.</span><span class="sxs-lookup"><span data-stu-id="e2f49-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="e2f49-111">Du kan vælge fra alle de grene, du opretter, når det indledende stadie er fuldført.</span><span class="sxs-lookup"><span data-stu-id="e2f49-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="e2f49-112">For eksempel kan du konfigurere **Planlægning** som et indledende stadie.</span><span class="sxs-lookup"><span data-stu-id="e2f49-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="e2f49-113">Du opretter to stadier, **Igangværende** og **Annuller**, og derefter vælger du **Planlægning** som overordnet stadie for dem.</span><span class="sxs-lookup"><span data-stu-id="e2f49-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="e2f49-114">Du kan tildele stadiet **Planlægning** til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="e2f49-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="e2f49-115">Når planlægningen for salgsordren er fuldført, kan du vælge stadiet **Igangværende**, hvis salgsordren er klar til at arbejde på, eller du kan vælge stadiet **Annuller**, hvis ordren er annulleret.</span><span class="sxs-lookup"><span data-stu-id="e2f49-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2f49-116">Se også</span><span class="sxs-lookup"><span data-stu-id="e2f49-116">See also</span></span>

[<span data-ttu-id="e2f49-117">Konfigurer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="e2f49-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="e2f49-118">Ændre serviceordrestadiet</span><span class="sxs-lookup"><span data-stu-id="e2f49-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


