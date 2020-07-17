---
title: Procesautomatisering
description: Dette emne indeholder oplysninger om, hvordan procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508179"
---
# <a name="process-automation"></a><span data-ttu-id="7a206-103">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="7a206-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7a206-104">Procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren.</span><span class="sxs-lookup"><span data-stu-id="7a206-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="7a206-105">Den opdaterede kalendervisning af det planlagte arbejde giver slutbrugere mulighed for at få vist og reagere på planlagt og afsluttet arbejde.</span><span class="sxs-lookup"><span data-stu-id="7a206-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="7a206-106">Administration</span><span class="sxs-lookup"><span data-stu-id="7a206-106">Administration</span></span>

<span data-ttu-id="7a206-107">Den centrale administrationsside for alle procesautomatiseringer findes i modulet Systemadministration under menuen **Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="7a206-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="7a206-108">På denne side vises en liste over alle automatiserede processer (serier), der er oprettet i systemet.</span><span class="sxs-lookup"><span data-stu-id="7a206-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="7a206-109">Du kan også tilføje nye procesautomatiseringer direkte fra denne side.</span><span class="sxs-lookup"><span data-stu-id="7a206-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="7a206-110">Når en serie er konfigureret, kan du administrere hver serie på denne liste.</span><span class="sxs-lookup"><span data-stu-id="7a206-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="7a206-111">Du kan vælge at redigere hele serien, slette den, få vist alle forekomster i en listevisning eller deaktivere serien, hvis du midlertidigt vil stoppe det planlagte arbejde i en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="7a206-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="7a206-112">Kalendervisning</span><span class="sxs-lookup"><span data-stu-id="7a206-112">Calendar view</span></span> 
<span data-ttu-id="7a206-113">En af de vigtigste fordele ved procesautomatisering er muligheden for at se det planlagte arbejde i en simpel kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="7a206-113">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="7a206-114">Du kan bruge denne visning til at få vist arbejde for en uge ad gangen.</span><span class="sxs-lookup"><span data-stu-id="7a206-114">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="7a206-115">Du kan se denne visning i højre side af siden **Procesautomatisering**.</span><span class="sxs-lookup"><span data-stu-id="7a206-115">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="7a206-116">Den vil blive udfyldt med det planlagte arbejde for den valgte serie.</span><span class="sxs-lookup"><span data-stu-id="7a206-116">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="7a206-117">[![Kalender for procesautomatisering](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="7a206-117">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="7a206-118">Forekomster ændres</span><span class="sxs-lookup"><span data-stu-id="7a206-118">Occurrence changes</span></span>
<span data-ttu-id="7a206-119">Hver forekomst kan redigeres uden at påvirke andre forekomster, der er defineret af den serie, der har oprettet dem.</span><span class="sxs-lookup"><span data-stu-id="7a206-119">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="7a206-120">Forekomster af planlagt arbejde kan redigeres i kalendervisningen ved at vælge knappen **Vis/Rediger** og vælge **Forekomst**.</span><span class="sxs-lookup"><span data-stu-id="7a206-120">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="7a206-121">Dette giver dig adgang til alle de indstillinger, der oprindeligt blev vist i guiden til konfiguration af serie, og giver mulighed for at foretage en engangsændring for den valgte forekomst.</span><span class="sxs-lookup"><span data-stu-id="7a206-121">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="7a206-122">En forekomst af planlagt arbejde kan også slås fra ved at vælge knappen **Deaktiver** i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="7a206-122">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="7a206-123">Udviklerdokumentation</span><span class="sxs-lookup"><span data-stu-id="7a206-123">Developer documentation</span></span> 
<span data-ttu-id="7a206-124">Dokumentationen til udviklere skrives i øjeblikket for at give udviklere mulighed for at udvide procesautomatiseringsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="7a206-124">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="7a206-125">Denne dokumentation indeholder oplysninger om, hvordan du kan oprette brugerdefinerede processer, som du skal køre på den batchserver, der er planlagt med guiden til procesautomatisering, og som automatisk vises i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="7a206-125">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
