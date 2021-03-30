---
title: Konfigurere en arbejder ved hjælp af den mobile jobenhed
description: I dette emne beskrives, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6210cdeed99f26a6b58b75d9f5405c0e1ee5aef1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213324"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="6f2d2-103">Konfigurere en arbejder ved hjælp af den mobile jobenhed</span><span class="sxs-lookup"><span data-stu-id="6f2d2-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f2d2-104">I dette emne beskrives, hvordan du tildeler de korrekte roller til brugerkontoen for en arbejder og derefter gør det muligt for arbejderen at foretage shop floor-registreringer.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="6f2d2-105">Kontroller, at en arbejder er tildelt en bestemt rolle</span><span class="sxs-lookup"><span data-stu-id="6f2d2-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="6f2d2-106">I dette eksempel skal du kontrollere, at brugeren "SHANNON" er tildelt rollen maskinoperatør, før du konfigurerer arbejderens konto.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="6f2d2-107">Gå til **Navigationsrude > Moduler > Systemadministration > Brugere > Brugere**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="6f2d2-108">Søg efter en bruger i quick-filteret.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="6f2d2-109">Skriv eksempelvis `shannon`.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="6f2d2-110">Vælg linket i kolonnen **Bruger-ID** for den brugerkonto, der vises.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="6f2d2-111">Vælg træet **Brugerens roller** og dernæst **Roller > Maskinoperatør**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="6f2d2-112">Luk siderne **Brugeroplysninger** og **Brugere** for at vende tilbage til startsiden.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="6f2d2-113">Konfigurer arbejderkonto</span><span class="sxs-lookup"><span data-stu-id="6f2d2-113">Configure worker account</span></span>
1. <span data-ttu-id="6f2d2-114">Gå til **Navigationsrude > Moduler > Personale > Arbejdere >** Arbejdere.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="6f2d2-115">Søg efter en bruger i quick-filteret.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="6f2d2-116">Skriv eksempelvis `shannon`.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="6f2d2-117">Vælg linket i kolonnen **Navn** for den brugerkonto, der vises.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="6f2d2-118">Vælg fanen **Tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="6f2d2-119">Vælg **Aktivér på registreringsterminaler**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="6f2d2-120">Indtast eller vælg værdier i følgende felter:</span><span class="sxs-lookup"><span data-stu-id="6f2d2-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="6f2d2-121">**Beregningsgruppe**</span><span class="sxs-lookup"><span data-stu-id="6f2d2-121">**Calculation group**</span></span>  
    - <span data-ttu-id="6f2d2-122">**Standardberegningsgruppe**</span><span class="sxs-lookup"><span data-stu-id="6f2d2-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="6f2d2-123">**Godkendelsesgruppe**</span><span class="sxs-lookup"><span data-stu-id="6f2d2-123">**Approval group**</span></span>  
    - <span data-ttu-id="6f2d2-124">**Standardprofil**</span><span class="sxs-lookup"><span data-stu-id="6f2d2-124">**Standard profile**</span></span>  
    - <span data-ttu-id="6f2d2-125">**Profilgruppe**</span><span class="sxs-lookup"><span data-stu-id="6f2d2-125">**Profile group**</span></span>  

7. <span data-ttu-id="6f2d2-126">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-126">Select **OK**.</span></span>
8. <span data-ttu-id="6f2d2-127">Vælg **Rediger** for at angive et kortnummer for den nye tidsregistreringsarbejder.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="6f2d2-128">Indtast en værdi i feltet **Kort-ID**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="6f2d2-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-129">Select **Save**.</span></span>
10. <span data-ttu-id="6f2d2-130">Luk siderne **Detaljer om arbejder** og **Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="6f2d2-131">Tildel arbejder til enhedsgruppe</span><span class="sxs-lookup"><span data-stu-id="6f2d2-131">Assign worker to device group</span></span>
1. <span data-ttu-id="6f2d2-132">Gå til **Produktionsstyring > Opsætning > Produktionsudførelse > Konfigurer jobkort for enheder**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="6f2d2-133">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-133">Select **Add**.</span></span>
3. <span data-ttu-id="6f2d2-134">Vælg den ønskede arbejder på listen.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-134">In the list, select the desired worker.</span></span> <span data-ttu-id="6f2d2-135">Vælg i dette eksempel **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="6f2d2-136">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-136">Select **OK**.</span></span>
5. <span data-ttu-id="6f2d2-137">Vælg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-137">Select **Edit**.</span></span>
6. <span data-ttu-id="6f2d2-138">Du kan angive standardfilteret for arbejderen i feltet **Produktionsenhed**.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="6f2d2-139">Dette sikrer, at kun produktionsjob for den valgte produktionsenhed vises, når arbejderen logger på enheden.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="6f2d2-140">Indtast den ønskede værdi.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-140">Enter the desired value.</span></span>
7. <span data-ttu-id="6f2d2-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="6f2d2-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]