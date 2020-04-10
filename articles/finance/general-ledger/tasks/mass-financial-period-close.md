---
title: Masseafslutning af regnskabsperiode
description: Dette emne viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144976"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="e2ed6-103">Masseafslutning af regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="e2ed6-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2ed6-104">Dette emne viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="e2ed6-105">Desuden viser opgaven, hvordan du kan begrænse bogføring for en brugergruppe til bestemte moduler.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="e2ed6-106">Gå til **Moduler > Finans > Luk periode > Finanskalendere** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="e2ed6-107">Bemærk, at listen over juridiske enheder, der vises, afhænger af den regnskabskalender, der er valgt på siden.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="e2ed6-108">Kun juridiske enheder, der bruger den valgte regnskabskalender, vises.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="e2ed6-109">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-109">Select **Edit**.</span></span>
3. <span data-ttu-id="e2ed6-110">Vælg den periode, du vil ændre status for.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="e2ed6-111">Vælg de juridiske enheder, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="e2ed6-112">Du kan hurtigt markere alle de juridiske enheder ved at markere afkrydsningsfeltet i øverste venstre side af gitteret.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="e2ed6-113">Vælg **Opdater modul adgang** for at definere bogføringsadgang til et bestemt modul.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="e2ed6-114">Modulstatus kan også opdateres én efter én ved at redigere poster i gitteret.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="e2ed6-115">Knappen er nyttig, når du hurtigt vil opdatere flere poster for juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="e2ed6-116">I modulet **Program** skal du vælge det modul, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="e2ed6-117">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-117">Click **Select**.</span></span>
7. <span data-ttu-id="e2ed6-118">På niveauet **Adgang** skal du markere **Alle**, **Ingen** eller en bestemt brugergruppe.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="e2ed6-119">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-119">Click **Select**.</span></span> <span data-ttu-id="e2ed6-120">Alle angiver, at alle brugere med Rediger-adgang til modulet kan bogføre, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="e2ed6-121">Ingen angiver, at ingen brugere kan bogføre til modulet, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="e2ed6-122">En bestemt brugergruppe angiver, at kun brugere i gruppen kan bogføre til modulet, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="e2ed6-123">Vælg **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-123">Select **Update**.</span></span>
9. <span data-ttu-id="e2ed6-124">Vælg en anden periode, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="e2ed6-125">Vælg de juridiske enheder, du vil opdatere periodestatus for.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="e2ed6-126">Vælg **Opdater periodestatus**, og angiv status til **På hold**, **Åben** eller **Permanent lukket**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="e2ed6-127">**Åben** angiver, at der kan bogføres til perioden, hvis brugeren har adgang.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="e2ed6-128">**På hold** betyder, at der ikke kan bogføres på perioden, men perioden kan genåbnes.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="e2ed6-129">**Permanent lukket** betyder, at perioden er lukket og ikke kan åbnes.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="e2ed6-130">Reguleringer kan ikke bogføres.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="e2ed6-131">Det anbefales ikke at indstille en periode til **Permanent lukket**, før alle reguleringer og revisioner er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="e2ed6-132">Vælg **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="e2ed6-132">Select **Update**.</span></span>

