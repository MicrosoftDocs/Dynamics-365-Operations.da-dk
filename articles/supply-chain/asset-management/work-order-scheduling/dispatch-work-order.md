---
title: Udsende arbejdsordre
description: Dette emne beskriver, hvordan du udsender en arbejdsordre i Styring af aktiver.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bd3bea647698f76efa5831d0b8b34d3cb0ad479a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825536"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="93e3f-103">Udsende arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="93e3f-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="93e3f-104">Du kan planlægge en arbejdsordre eller arbejdsordrejob til én arbejder ved hjælp af funktionen **Udsend**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="93e3f-105">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="93e3f-106">Vælg arbejdsordren på listen.</span><span class="sxs-lookup"><span data-stu-id="93e3f-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="93e3f-107">Klik på **Udsend** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="93e3f-108">Vælg arbejderen i feltet **Arbejder** i dialogboksen **Planlæg arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="93e3f-109">I feltet **Planlæg timer** kan du indsætte forventede arbejdstimer i tilfælde af, at arbejdstimerne er forskellige fra budgetterede timer.</span><span class="sxs-lookup"><span data-stu-id="93e3f-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="93e3f-110">I feltet **Planlagt start** kan du redigere startdato og -tidspunkt, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="93e3f-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="93e3f-111">Hvis planlægningsprocessen skal overholde kapacitetsbegrænsningerne for ressourcer, der allerede er planlagt på andre job, skal du sørge for, at til/fra-knapperne **Aktiv**, **Værktøj** og **Arbejder** er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="93e3f-112">Hvis du vil have vist detaljerede oplysninger om planlægningsprocessen, skal du vælge **Ja** på knappen **Detaljeret**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="93e3f-113">Det betyder, at der vises detaljerede oplysninger om de beregnede scorer for arbejdsordren i infologgen.</span><span class="sxs-lookup"><span data-stu-id="93e3f-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="93e3f-114">Vælg **Ja** på til/fra-knappen **Ignorer tidsplan** for at ignorere lukkede dage i kalenderen (gælder for aktiv, arbejder og værktøjer).</span><span class="sxs-lookup"><span data-stu-id="93e3f-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="93e3f-115">Vælg **Ja** på til/fra-knappen **Ignorer planlagt udførelse** for at ignorere begrænsninger, der muligvis er valgt på arbejdsordren vedrørende planlægning.</span><span class="sxs-lookup"><span data-stu-id="93e3f-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="93e3f-116">Se afsnittet [Planlagt udførelse](../setup-for-work-orders/scheduled-execution.md) for at få oplysninger om opsætningen af planlagt udførelse.</span><span class="sxs-lookup"><span data-stu-id="93e3f-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="93e3f-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-117">Click **OK**.</span></span> <span data-ttu-id="93e3f-118">Arbejdsordrens livscyklustilstand opdateres automatisk til den **Planlagte** livscyklustilstand, der er angivet for **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Livscyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="93e3f-119">I figuren herunder vises et eksempel på udsendelsesvalg i dialogboksen **Planlægning arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="93e3f-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Figur 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="93e3f-121">Hvis du vil slette tidsplanen på en arbejdsordre, skal du vælge arbejdsordren i **Alle arbejdsordrer** og klikke på **Slet tidsplan** under fanen **Generelt**. Husk at opdatere arbejdsordrens livscyklustilstand manuelt, hvis du sletter tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="93e3f-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]