---
title: Konfigurere en arbejder ved hjælp af den mobile jobenhed
description: Denne procedure viser, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "327383"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="f3b49-103">Konfigurere en arbejder ved hjælp af den mobile jobenhed</span><span class="sxs-lookup"><span data-stu-id="f3b49-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3b49-104">Denne procedure viser, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.</span><span class="sxs-lookup"><span data-stu-id="f3b49-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="f3b49-105">Tildele roller til brugerkonto</span><span class="sxs-lookup"><span data-stu-id="f3b49-105">Assign roles to user account</span></span>
1. <span data-ttu-id="f3b49-106">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="f3b49-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f3b49-107">Brug af Quick Filter til at filtrere på navnet på en arbejder, hvor brugerkontoen er tilknyttet rollen Maskinpasser.</span><span class="sxs-lookup"><span data-stu-id="f3b49-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="f3b49-108">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="f3b49-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="f3b49-109">Fremhæv brugerkontoposten.</span><span class="sxs-lookup"><span data-stu-id="f3b49-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="f3b49-110">Klik på linket "Navn" i den markerede række på listen for at få vist oplysningerne om brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="f3b49-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="f3b49-111">Vælg Roles\Machine operator i træet.</span><span class="sxs-lookup"><span data-stu-id="f3b49-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="f3b49-112">Luk siden med detaljer om brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="f3b49-112">Close the user account details page.</span></span>
7. <span data-ttu-id="f3b49-113">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3b49-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="f3b49-114">Konfigurer arbejderkonto.</span><span class="sxs-lookup"><span data-stu-id="f3b49-114">Configure worker account.</span></span>
1. <span data-ttu-id="f3b49-115">Gå til Personale > Arbejdere > Arbejdere.</span><span class="sxs-lookup"><span data-stu-id="f3b49-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="f3b49-116">Brug af Quick Filter til at filtrere på navnet på en arbejder, hvor brugerkontoen er tilknyttet rollen Maskinpasser.</span><span class="sxs-lookup"><span data-stu-id="f3b49-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="f3b49-117">I eksempeldataene er navnet Shannon.</span><span class="sxs-lookup"><span data-stu-id="f3b49-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="f3b49-118">Fremhæv brugerkontoposten.</span><span class="sxs-lookup"><span data-stu-id="f3b49-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="f3b49-119">Klik på linket "Navn" i den markerede række på listen for at få vist oplysningerne om brugerkontoen.</span><span class="sxs-lookup"><span data-stu-id="f3b49-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="f3b49-120">Klik på fanen Ansættelse.</span><span class="sxs-lookup"><span data-stu-id="f3b49-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="f3b49-121">Udvid oversigtspanelet Tidsregistrering, og klik på Aktivér på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="f3b49-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="f3b49-122">Klik på Aktivér på registreringsterminaler.</span><span class="sxs-lookup"><span data-stu-id="f3b49-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="f3b49-123">Skriv eller vælg en værdi i feltet Beregningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3b49-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="f3b49-124">Skriv eller vælg en værdi i feltet Standardberegningsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3b49-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="f3b49-125">Indtast eller vælg en værdi i feltet Godkendelsesgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3b49-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="f3b49-126">Indtast eller vælg en værdi i feltet Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f3b49-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="f3b49-127">Indtast eller vælg en værdi i feltet Profilgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3b49-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="f3b49-128">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3b49-128">Click OK.</span></span>
14. <span data-ttu-id="f3b49-129">Klik på Rediger for at angive et kortnummer for den nye tidsregistreringsarbejder.</span><span class="sxs-lookup"><span data-stu-id="f3b49-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="f3b49-130">Skriv en værdi i feltet Kort-id.</span><span class="sxs-lookup"><span data-stu-id="f3b49-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="f3b49-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="f3b49-131">Click Save.</span></span>
17. <span data-ttu-id="f3b49-132">Brug genvejen SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="f3b49-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="f3b49-133">Luk siden med detaljer om arbejderen.</span><span class="sxs-lookup"><span data-stu-id="f3b49-133">Close the worker details page.</span></span>
19. <span data-ttu-id="f3b49-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3b49-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="f3b49-135">Tildel arbejder til enhedsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f3b49-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="f3b49-136">Gå til Produktionsstyring > Konfiguration > Produktionsudførelse > Konfigurer jobkort for enheder.</span><span class="sxs-lookup"><span data-stu-id="f3b49-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="f3b49-137">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="f3b49-137">Click Add.</span></span>
3. <span data-ttu-id="f3b49-138">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="f3b49-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f3b49-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="f3b49-139">Click OK.</span></span>
5. <span data-ttu-id="f3b49-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="f3b49-140">Click Edit.</span></span>
6. <span data-ttu-id="f3b49-141">Du kan angive standardfilteret for arbejderen i feltet Produktionsenhed.</span><span class="sxs-lookup"><span data-stu-id="f3b49-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="f3b49-142">Dette sikrer, at kun produktionsjob for den valgte produktionsenhed vises, når arbejderen logger på enheden.</span><span class="sxs-lookup"><span data-stu-id="f3b49-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="f3b49-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="f3b49-143">Close the page.</span></span>

