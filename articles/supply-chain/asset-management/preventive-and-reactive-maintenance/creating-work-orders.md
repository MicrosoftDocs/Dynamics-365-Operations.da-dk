---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922108"
---
# <a name="creating-work-orders"></a><span data-ttu-id="51103-103">Oprette arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="51103-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="51103-104">Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer for jobbene.</span><span class="sxs-lookup"><span data-stu-id="51103-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="51103-105">Du kan gøre det i en af vedligeholdelsestidsplanerne.</span><span class="sxs-lookup"><span data-stu-id="51103-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="51103-106">De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper:</span><span class="sxs-lookup"><span data-stu-id="51103-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="51103-107">Referencetype</span><span class="sxs-lookup"><span data-stu-id="51103-107">Reference type</span></span> | <span data-ttu-id="51103-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="51103-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51103-109">Vedligeholdelsesplaner</span><span class="sxs-lookup"><span data-stu-id="51103-109">Maintenance plans</span></span>     | <span data-ttu-id="51103-110">Præventivee vedligeholdelsesjob baseret på vedligeholdelsesplantyperne "Tid" eller "Tæller".</span><span class="sxs-lookup"><span data-stu-id="51103-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="51103-111">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="51103-111">Maintenance rounds</span></span>    | <span data-ttu-id="51103-112">Præventive vedligeholdelsesjob med flere aktiver, der kræver en lignende form for vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="51103-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="51103-113">Vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="51103-113">Maintenance request</span></span>   | <span data-ttu-id="51103-114">Manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv, som kan konverteres til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="51103-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="51103-115">Klik på **Styring af aktiver** > **Generelt** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="51103-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="51103-116">Vælg de planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for, og klik på **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="51103-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="51103-117">Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer** i dialogboksen **Opret arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="51103-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="51103-118">Vælg, hvor mange arbejdsordrer der skal oprettes, i sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="51103-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="51103-119">Du kan oprette én arbejdsordre pr. vedligeholdelsestidsplanslinje eller et antal arbejdsordrer ud fra dine valg i sektionen **Én arbejdsordre pr.**.</span><span class="sxs-lookup"><span data-stu-id="51103-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="51103-120">Vælg en **Arbejdsordretype**, der skal bruges på alle de arbejdsordrer, du opretter.</span><span class="sxs-lookup"><span data-stu-id="51103-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="51103-121">I illustrationen nedenfor vises et eksempel på dialogboksen **Opret arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="51103-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Figur 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="51103-123">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="51103-123">Click **OK**.</span></span> <span data-ttu-id="51103-124">Der oprettes en eller flere arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="51103-124">One or more work orders are created.</span></span>

