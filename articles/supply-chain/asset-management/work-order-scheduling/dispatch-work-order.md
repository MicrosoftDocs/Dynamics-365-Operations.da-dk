---
title: Udsende arbejdsordre
description: Dette emne beskriver, hvordan du udsender en arbejdsordre i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887199"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="ad8ca-103">Udsende arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="ad8ca-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ad8ca-104">Du kan planlægge en arbejdsordre eller arbejdsordrejob til én arbejder ved hjælp af funktionen **Udsend**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="ad8ca-105">Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ad8ca-106">Vælg arbejdsordren på listen.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="ad8ca-107">Klik på **Udsend** under fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="ad8ca-108">Vælg arbejderen i feltet **Arbejder** i dialogboksen **Planlæg arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-108">n the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="ad8ca-109">I feltet **Planlæg timer** kan du indsætte forventede arbejdstimer i tilfælde af, at arbejdstimerne er forskellige fra budgetterede timer.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="ad8ca-110">I feltet **Planlagt start** kan du redigere startdato og -tidspunkt, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="ad8ca-111">Hvis planlægningsprocessen skal overholde kapacitetsbegrænsningerne for ressourcer, der allerede er planlagt på andre job, skal du sørge for, at til/fra-knapperne **Aktiv**, **Værktøj** og **Arbejder** er indstillet til "Ja".</span><span class="sxs-lookup"><span data-stu-id="ad8ca-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to "Yes".</span></span> <span data-ttu-id="ad8ca-112">Hvis du vil have vist detaljerede oplysninger om planlægningsprocessen, skal du vælge "Ja" på knappen **Detaljeret**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-112">If you want to see detailed information about the scheduling process, select "Yes" on the **Verbose** toggle button.</span></span> <span data-ttu-id="ad8ca-113">Det betyder, at der vises detaljerede oplysninger om de beregnede scorer for arbejdsordren i infologgen.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="ad8ca-114">Vælg "Ja" på til/fra-knappen **Ignorer tidsplan** at ignorere lukkede dage i kalenderen (gælder for aktiv, arbejder og værktøjer).</span><span class="sxs-lookup"><span data-stu-id="ad8ca-114">Select "Yes" on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="ad8ca-115">Vælg "Ja" på til/fra-knappen **Ignorer planlagt udførelse** for at ignorere begrænsninger, der muligvis er valgt på arbejdsordren vedrørende planlægning.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-115">Select "Yes" on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> <span data-ttu-id="ad8ca-116">Se afsnittet [Planlagt udførelse](../setup-for-work-orders/scheduled-execution.md) for at få oplysninger om opsætningen af planlagt udførelse.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-116">Refer to the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section for information on the setup of scheduled execution.</span></span>

9. <span data-ttu-id="ad8ca-117">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-117">Click **OK**.</span></span> <span data-ttu-id="ad8ca-118">Arbejdsordrens livscyklustilstand opdateres automatisk til den "Planlagte" livscyklustilstand, der er angivet for **Styring af aktiver** > **Opsætning** > **Arbejdsordrer** > **Livscyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-118">The work order lifecycle state is automatically updated to the "Scheduled" lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="ad8ca-119">I figuren herunder vises et eksempel på udsendelsesvalg i dialogboksen **Planlægning arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Figur 1](media/04-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="ad8ca-121">Hvis du vil slette tidsplanen på en arbejdsordre, skal dette gøres ved at vælge arbejdsordren i **Alle arbejdsordrer** og klikke **Slet tidsplan** under fanen **Generelt**. Husk at opdatere arbejdsordrens livscyklustilstand manuelt, hvis du sletter tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="ad8ca-121">If you want to delete the schedule on a work order, this is done by selecting the work order in **All work orders** and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

