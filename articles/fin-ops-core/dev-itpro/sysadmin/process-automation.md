---
title: Procesautomatisering
description: Dette emne indeholder oplysninger om, hvordan procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 479f621ef05519f4f2c97112a0115dccdbf24c52
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682503"
---
# <a name="process-automation"></a><span data-ttu-id="b5f4d-103">Procesautomatisering</span><span class="sxs-lookup"><span data-stu-id="b5f4d-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b5f4d-104">Procesautomatisering tillader enkel planlægning af processer, der køres af batchserveren.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="b5f4d-105">Den opdaterede kalendervisning af det planlagte arbejde giver slutbrugere mulighed for at få vist og reagere på planlagt og afsluttet arbejde.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="b5f4d-106">Administration</span><span class="sxs-lookup"><span data-stu-id="b5f4d-106">Administration</span></span>

<span data-ttu-id="b5f4d-107">Den centrale administrationsside for alle procesautomatiseringer findes i modulet Systemadministration under menuen **Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b5f4d-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="b5f4d-108">På denne side vises en liste over alle automatiserede processer (serier), der er oprettet i systemet.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="b5f4d-109">Du kan også tilføje nye procesautomatiseringer direkte fra denne side.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="b5f4d-110">Når en serie er konfigureret, kan du administrere hver serie på denne liste.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="b5f4d-111">Du kan vælge at redigere hele serien, slette den, få vist alle forekomster i en listevisning eller deaktivere serien, hvis du vil stoppe det planlagte arbejde i et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="b5f4d-112">Processer, der er deaktiveret i funktionsstyringen, vises ikke, når funktionen er deaktiveret.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="b5f4d-113">Derudover vil planlægningsprogrammet for procesautomatisering ikke planlægge nogen forekomster eller baggrundsprocesser for en deaktiveret funktion.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="b5f4d-114">Hvis du genaktiverer funktionen, vil eventuelle planlagte forekomster eller baggrundsprocesser fra tidligere straks blive kørt.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="b5f4d-115">Kalendervisning</span><span class="sxs-lookup"><span data-stu-id="b5f4d-115">Calendar view</span></span>

<span data-ttu-id="b5f4d-116">En af de vigtigste fordele ved procesautomatisering er muligheden for at se det planlagte arbejde i en simpel kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="b5f4d-117">Du kan bruge denne visning til at få vist arbejde for en uge ad gangen.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="b5f4d-118">Du kan se denne visning i højre side af siden **Procesautomatisering**.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="b5f4d-119">Den vil blive udfyldt med det planlagte arbejde for den valgte serie.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="b5f4d-120">[![Kalender for procesautomatisering](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="b5f4d-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="b5f4d-121">Forekomster ændres</span><span class="sxs-lookup"><span data-stu-id="b5f4d-121">Occurrence changes</span></span>

<span data-ttu-id="b5f4d-122">Hver forekomst kan redigeres uden at påvirke andre forekomster, der er defineret af den serie, der har oprettet dem.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="b5f4d-123">Forekomster af planlagt arbejde kan redigeres i kalendervisningen ved at vælge knappen **Vis/Rediger** og vælge **Forekomst**.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="b5f4d-124">Denne side giver dig adgang til alle de indstillinger, der oprindeligt blev vist i guiden til konfiguration af serie, og giver mulighed for at foretage en engangsændring for den valgte forekomst.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="b5f4d-125">En forekomst af planlagt arbejde kan også slås fra ved at vælge knappen **Deaktiver** i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="b5f4d-126">Udviklerdokumentation</span><span class="sxs-lookup"><span data-stu-id="b5f4d-126">Developer documentation</span></span>

<span data-ttu-id="b5f4d-127">Procesautomatiseringsstrukturen giver udviklere mulighed for at udvide procesautomatiseringsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="b5f4d-128">Dokumentation til [procesautomatiseringsstrukturen](../process-automation/process-automation-framework.md) indeholder oplysninger om, hvordan du kan oprette brugerdefinerede processer, som du skal køre på den batchserver, der er planlagt med guiden til procesautomatisering, og som automatisk vises i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="b5f4d-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
