---
title: Planlagte vedligeholdelsesjob i arbejdsordrer
description: I dette emne beskrives planlagte vedligeholdelsesjob for arbejdsordrer i Styring af aktiver.
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
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887176"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="d11b8-103">Planlagte vedligeholdelsesjob i arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="d11b8-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="d11b8-104">Siden **Planlagte vedligeholdelsesjob for arbejdsordrer** bruges til at få vist en oversigt over de arbejdsordrer, der er tildelt en ressource.</span><span class="sxs-lookup"><span data-stu-id="d11b8-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="d11b8-105">Arbejdsordrer, der bruger ressourcetyperne "personale", "værktøj" og "maskine", vises på listen.</span><span class="sxs-lookup"><span data-stu-id="d11b8-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="d11b8-106">Listen kan bruges til at få en oversigt over de arbejdsordrer, der er tildelt til en bestemt ressource.</span><span class="sxs-lookup"><span data-stu-id="d11b8-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="d11b8-107">Du kan også bruge den til hurtigt at finde en arbejdsordre, der er tildelt en vedligeholdelsesarbejder, som f.eks. har sygemeldt sig her til morgen, og derefter hurtigt tildele en anden vedligeholdelsesarbejder til jobbet.</span><span class="sxs-lookup"><span data-stu-id="d11b8-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="d11b8-108">Vise planlagte vedligeholdelsesjob for arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="d11b8-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="d11b8-109">Klik på **Aktivstyring** > **Almindeligt** > **Arbejdsordrer** > **Planlagte vedligeholdelsesjob for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="d11b8-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="d11b8-110">Du får vist en liste over alle de arbejdsordrer, hvor livscyklustilstanden for arbejdsordren er indstillet til "planlagt" eller "i gang".</span><span class="sxs-lookup"><span data-stu-id="d11b8-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="d11b8-111">Du kan sortere listen, f.eks. efter vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="d11b8-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="d11b8-112">Du kan også bruge filteret til at begrænse listen, så den kun viser arbejdsordrer, der er tildelt en bestemt ressource eller vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="d11b8-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="d11b8-113">Du kan se noter om arbejdsordren og evt. tilføje nye noter ved at vælge arbejdsordrejobbet på listen og klikke på **Noter**.</span><span class="sxs-lookup"><span data-stu-id="d11b8-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="d11b8-114">Hvis du vil tildele én vedligeholdelsesarbejder til en arbejdsordre, skal du vælge arbejdsordren på listen og klikke på **Arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="d11b8-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="d11b8-115">Siden **Arbejdsordre** åbnes.</span><span class="sxs-lookup"><span data-stu-id="d11b8-115">The **Work order** page opens.</span></span> <span data-ttu-id="d11b8-116">Klik på **Ekspedition** for at planlægge arbejdsordren til en bestemt vedligeholdelsesarbejder.</span><span class="sxs-lookup"><span data-stu-id="d11b8-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="d11b8-117">Du kan læse mere om planlægning af flere arbejdsordrer eller én arbejdsordre i [Planlægge arbejdsordrer](../work-order-scheduling/schedule-work-orders.md) og [Ekspedere arbejdsordre](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="d11b8-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="d11b8-118">I figuren herunder vises et eksempel på siden **Planlagte vedligeholdelsesjob for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="d11b8-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![Figur 1](media/07-work-order-scheduling.png)

