--- 
title: Masseafslutning af regnskabsperiode
description: "Denne procedure viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 847a4fd675096bc8a13cfc756e75a1878f092406
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="mass-financial-period-close"></a><span data-ttu-id="9e028-103">Masseafslutning af regnskabsperiode</span><span class="sxs-lookup"><span data-stu-id="9e028-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e028-104">Denne procedure viser, hvordan du kan sætte en periode på hold eller permanent lukke en periode eller mere end én juridisk enhed ad gangen.</span><span class="sxs-lookup"><span data-stu-id="9e028-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="9e028-105">Desuden viser opgaven, hvordan du kan begrænse bogføring for en brugergruppe til bestemte moduler.</span><span class="sxs-lookup"><span data-stu-id="9e028-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="9e028-106">Gå til Finans > Luk periode > Finanskalendere.</span><span class="sxs-lookup"><span data-stu-id="9e028-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="9e028-107">Bemærk, at listen over juridiske enheder, der vises, afhænger af den regnskabskalender, der er valgt på siden.</span><span class="sxs-lookup"><span data-stu-id="9e028-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="9e028-108">Kun juridiske enheder, der bruger den valgte regnskabskalender, vises.</span><span class="sxs-lookup"><span data-stu-id="9e028-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="9e028-109">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="9e028-109">Click Edit.</span></span>
3. <span data-ttu-id="9e028-110">Vælg den periode, du vil ændre status for.</span><span class="sxs-lookup"><span data-stu-id="9e028-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="9e028-111">Vælg de juridiske enheder, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="9e028-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="9e028-112">Du kan hurtigt markere alle de juridiske enheder ved at markere afkrydsningsfeltet i øverste venstre side af gitteret.</span><span class="sxs-lookup"><span data-stu-id="9e028-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="9e028-113">Vælg Opdater modul adgang for at definere bogføringsadgang til et bestemt modul.</span><span class="sxs-lookup"><span data-stu-id="9e028-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="9e028-114">Modulstatus kan også opdateres én efter én ved at redigere poster i gitteret.</span><span class="sxs-lookup"><span data-stu-id="9e028-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="9e028-115">Knappen er nyttig, når du hurtigt vil opdatere flere poster for juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="9e028-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="9e028-116">I Programmodul skal du vælge det modul, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="9e028-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="9e028-117">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="9e028-117">Click Select.</span></span>
7. <span data-ttu-id="9e028-118">I Adgangsniveau skal du markere Alle, Ingen eller en bestemt brugergruppe.</span><span class="sxs-lookup"><span data-stu-id="9e028-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="9e028-119">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="9e028-119">Click Select.</span></span>
    * <span data-ttu-id="9e028-120">Alle angiver, at alle brugere med Rediger-adgang til modulet kan bogføre, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="9e028-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="9e028-121">Ingen angiver, at ingen brugere kan bogføre til modulet, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="9e028-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="9e028-122">En bestemt brugergruppe angiver, at kun brugere i gruppen kan bogføre til modulet, hvis perioden er åben.</span><span class="sxs-lookup"><span data-stu-id="9e028-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="9e028-123">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="9e028-123">Click Update.</span></span>
9. <span data-ttu-id="9e028-124">Vælg en anden periode, du vil opdatere status for.</span><span class="sxs-lookup"><span data-stu-id="9e028-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="9e028-125">Vælg de juridiske enheder, du vil opdatere periodestatus for.</span><span class="sxs-lookup"><span data-stu-id="9e028-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="9e028-126">Vælg Opdater periodestatus, og angiv status til På hold, Åben eller Permanent lukket.</span><span class="sxs-lookup"><span data-stu-id="9e028-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="9e028-127">Åben angiver, at der kan bogføres til perioden, hvis brugeren har adgang.</span><span class="sxs-lookup"><span data-stu-id="9e028-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="9e028-128">På hold betyder, at der ikke kan bogføres på perioden, men perioden kan genåbnes.</span><span class="sxs-lookup"><span data-stu-id="9e028-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="9e028-129">Permanent lukket betyder, at perioden er lukket og ikke kan åbnes.</span><span class="sxs-lookup"><span data-stu-id="9e028-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="9e028-130">Reguleringer kan ikke bogføres.</span><span class="sxs-lookup"><span data-stu-id="9e028-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="9e028-131">Det anbefales ikke at indstille en periode til Permanent lukket, før alle reguleringer og revisioner er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="9e028-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="9e028-132">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="9e028-132">Click Update.</span></span>


