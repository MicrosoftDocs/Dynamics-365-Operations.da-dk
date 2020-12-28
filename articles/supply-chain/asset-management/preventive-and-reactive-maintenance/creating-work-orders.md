---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424668"
---
# <a name="creating-work-orders"></a><span data-ttu-id="d4d64-103">Oprette arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="d4d64-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d4d64-104">Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer for jobbene.</span><span class="sxs-lookup"><span data-stu-id="d4d64-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="d4d64-105">Du kan gøre det i en af vedligeholdelsestidsplanerne.</span><span class="sxs-lookup"><span data-stu-id="d4d64-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="d4d64-106">De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper:</span><span class="sxs-lookup"><span data-stu-id="d4d64-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="d4d64-107">Referencetype</span><span class="sxs-lookup"><span data-stu-id="d4d64-107">Reference type</span></span> | <span data-ttu-id="d4d64-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d4d64-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d64-109">Vedligeholdelsesplaner</span><span class="sxs-lookup"><span data-stu-id="d4d64-109">Maintenance plans</span></span>     | <span data-ttu-id="d4d64-110">Præventivee vedligeholdelsesjob baseret på vedligeholdelsesplantyperne "Tid" eller "Tæller".</span><span class="sxs-lookup"><span data-stu-id="d4d64-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="d4d64-111">Vedligeholdelsesrunder</span><span class="sxs-lookup"><span data-stu-id="d4d64-111">Maintenance rounds</span></span>    | <span data-ttu-id="d4d64-112">Præventive vedligeholdelsesjob med flere aktiver, der kræver en lignende form for vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="d4d64-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="d4d64-113">Vedligeholdelsesanmodning</span><span class="sxs-lookup"><span data-stu-id="d4d64-113">Maintenance request</span></span>   | <span data-ttu-id="d4d64-114">Manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv, som kan konverteres til en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="d4d64-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="d4d64-115">Klik på **Styring af aktiver** > **Generelt** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="d4d64-116">Vælg de planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for, og klik på **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="d4d64-117">Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer** i dialogboksen **Opret arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="d4d64-118">Vælg, hvor mange arbejdsordrer der skal oprettes, i sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="d4d64-119">Du kan oprette én arbejdsordre pr. vedligeholdelsestidsplanslinje eller et antal arbejdsordrer ud fra dine valg i sektionen **Én arbejdsordre pr.**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="d4d64-120">Vælg en **Arbejdsordretype**, der skal bruges på alle de arbejdsordrer, du opretter.</span><span class="sxs-lookup"><span data-stu-id="d4d64-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="d4d64-121">I illustrationen nedenfor vises et eksempel på dialogboksen **Opret arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Figur 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="d4d64-123">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4d64-123">Click **OK**.</span></span> <span data-ttu-id="d4d64-124">Der oprettes en eller flere arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="d4d64-124">One or more work orders are created.</span></span>

