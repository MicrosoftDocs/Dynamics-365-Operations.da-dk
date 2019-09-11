---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875562"
---
# <a name="creating-work-orders"></a><span data-ttu-id="26b73-103">Oprette arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="26b73-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="26b73-104">Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer for jobbene.</span><span class="sxs-lookup"><span data-stu-id="26b73-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="26b73-105">Du kan gøre det i en af vedligeholdelsestidsplanerne.</span><span class="sxs-lookup"><span data-stu-id="26b73-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="26b73-106">De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper:</span><span class="sxs-lookup"><span data-stu-id="26b73-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="26b73-107">Referencetype</span><span class="sxs-lookup"><span data-stu-id="26b73-107">Reference type</span></span> | <span data-ttu-id="26b73-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="26b73-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b73-109">Vedligeholdelsesplaner</span><span class="sxs-lookup"><span data-stu-id="26b73-109">Maintenance plans</span></span>     | <span data-ttu-id="26b73-110">Præventivee vedligeholdelsesjob baseret på vedligeholdelsesplantyperne "Tid" eller "Tæller".</span><span class="sxs-lookup"><span data-stu-id="26b73-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="26b73-111">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="26b73-111">Maintenance rounds</span></span>    | <span data-ttu-id="26b73-112">Præventive vedligeholdelsesjob med flere aktiver, der kræver en lignende form for vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="26b73-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="26b73-113">Vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="26b73-113">Maintenance request</span></span>   | <span data-ttu-id="26b73-114">Manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv, som kan konverteres til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="26b73-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="26b73-115">Klik på **Styring af aktiver** > **Generelt** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="26b73-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="26b73-116">Vælg de planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for, og klik på **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="26b73-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="26b73-117">Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer**.</span><span class="sxs-lookup"><span data-stu-id="26b73-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="26b73-118">Vælg, hvor mange arbejdsordrer der skal oprettes, i sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="26b73-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="26b73-119">Du kan oprette én arbejdsordre pr. vedligeholdelsestidsplanslinje eller et antal arbejdsordrer ud fra dine valg i sektionen **Én arbejdsordre pr.**.</span><span class="sxs-lookup"><span data-stu-id="26b73-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="26b73-120">Vælg en **Arbejdsordretype**, der skal bruges på alle de arbejdsordrer, du opretter.</span><span class="sxs-lookup"><span data-stu-id="26b73-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="26b73-121">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="26b73-121">Click **OK**.</span></span> <span data-ttu-id="26b73-122">Der oprettes en eller flere arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="26b73-122">One or more work orders are created.</span></span>

![Figur 1](media/18-preventive-maintenance.png)

