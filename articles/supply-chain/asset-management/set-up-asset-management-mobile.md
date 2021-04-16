---
title: Konfigurere arbejdsområdet til aktivstyring på mobilenhed
description: Dette emne beskriver, hvordan Microsoft Dynamics 365 Supply Chain Management- og Finance and Operations (Dynamics 365)-mobilappen konfigureres til at køre et mobilarbejdsområde til aktivstyring, som arbejderne kan bruge til at udføre opgaver i forbindelse med aktivstyring.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837771"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="a4414-103">Konfigurere arbejdsområdet til aktivstyring på mobilenhed</span><span class="sxs-lookup"><span data-stu-id="a4414-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4414-104">Dette emne beskriver, hvordan Microsoft Dynamics 365 Supply Chain Management- og Finance and Operations (Dynamics 365)-mobilappen konfigureres til at køre et mobilarbejdsområde til **aktivstyring**, som arbejderne kan bruge til at udføre opgaver i forbindelse med aktivstyring.</span><span class="sxs-lookup"><span data-stu-id="a4414-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="a4414-105">Konfigurere vedligeholdelsesarbejderbrugere i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a4414-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="a4414-106">For hver bruger, der skal have adgang til det mobile arbejdsområde til **aktivstyring**, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a4414-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="a4414-107">I Supply Chain Management skal du gå til **Personale \> Arbejdere** og sørge for, at der findes en arbejderpost for den bruger, du vil konfigurere.</span><span class="sxs-lookup"><span data-stu-id="a4414-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="a4414-108">Opret en ny arbejderpost efter behov.</span><span class="sxs-lookup"><span data-stu-id="a4414-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="a4414-109">Gå til **Aktivstyring \> Konfiguration \> Arbejdere \> Arbejdere**, og kontrollér, at den arbejderpost, du har identificeret (eller oprettet) i det forrige trin, er knyttet til en vedligeholdelsesarbejderpost.</span><span class="sxs-lookup"><span data-stu-id="a4414-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="a4414-110">Opret en ny vedligeholdelsesarbejderpost efter behov, og angiv feltet **Arbejder** til arbejderposten fra det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="a4414-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="a4414-111">Gå til **Aktivstyring \> Konfiguration \> Arbejdere \> Vedligeholdelsesarbejdergrupper**, og kontrollér, at den vedligeholdelsesarbejder, du har identificeret (eller oprettet) i det forrige trin, er knyttet til en vedligeholdelsesarbejdergruppe.</span><span class="sxs-lookup"><span data-stu-id="a4414-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="a4414-112">Gå til **Systemadministration \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="a4414-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="a4414-113">Vælg den relevante bruger i gitteret.</span><span class="sxs-lookup"><span data-stu-id="a4414-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="a4414-114">På oversigtspanelet **Brugeroplysninger** skal du angive feltet **Person** til den arbejderkonto, du vil knytte til den aktuelle brugerkonto.</span><span class="sxs-lookup"><span data-stu-id="a4414-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="a4414-115">Denne arbejderkonto skal være den arbejderpost, du har identificeret (eller oprettet) i trin 1 og knyttet til en vedligeholdelsesarbejderpost i trin 2.</span><span class="sxs-lookup"><span data-stu-id="a4414-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="a4414-116">Brugerrettigheder og sikkerhedsroller gælder for funktionerne i mobilarbejdsområdet til **aktivstyring** på samme måde, som de gælder for funktionerne i brugergrænsefladen til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4414-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="a4414-117">Derfor skal alle brugere, du konfigurerer adgangen til mobilarbejdsområdet til **aktivstyring** for, have de sikkerhedsroller, der er nødvendige for at udføre lignende handlinger direkte i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a4414-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="a4414-118">Publicere mobilarbejdsområdet til aktivstyring</span><span class="sxs-lookup"><span data-stu-id="a4414-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="a4414-119">Du kan gøre funktioner for aktivstyring tilgængelige i Finance and Operations (Dynamics 365)-mobilappen ved at publicere mobilarbejdsområdet til **aktivstyring**.</span><span class="sxs-lookup"><span data-stu-id="a4414-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="a4414-120">I Supply Chain Management skal du vælge knappen **Indstillinger** (tandhjulsymbolet øverst til højre) og derefter vælge **Mobilapp** i menuen.</span><span class="sxs-lookup"><span data-stu-id="a4414-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="a4414-121">I dialogboksen **Administrer mobilapp** skal du finde feltet **Aktivstyring**.</span><span class="sxs-lookup"><span data-stu-id="a4414-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="a4414-122">Hvis det indeholder teksten "I metadata – ikke publiceret", er arbejdsområdet endnu ikke publiceret.</span><span class="sxs-lookup"><span data-stu-id="a4414-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="a4414-123">Hvis det indeholder teksten "I metadata – publiceret", er arbejdsområdet allerede blevet publiceret, og du kan springe resten af denne procedure over.</span><span class="sxs-lookup"><span data-stu-id="a4414-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="a4414-124">![Dialogboksen Administrer mobilapp](media/mobile-workspaces.png "Dialogboksen Administrer mobilapp")</span><span class="sxs-lookup"><span data-stu-id="a4414-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="a4414-125">Vælg feltet **Aktivstyring**, og vælg derefter **Publicer** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="a4414-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="a4414-126">Efter nogle få sekunder burde du modtage en besked om, at arbejdsområdet er blevet publiceret korrekt.</span><span class="sxs-lookup"><span data-stu-id="a4414-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="a4414-127">Teksten i feltet burde desuden ændres til "I metadata – publiceret".</span><span class="sxs-lookup"><span data-stu-id="a4414-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="a4414-128">Installere og konfigurere Finance and Operations (Dynamics 365)-mobilappen</span><span class="sxs-lookup"><span data-stu-id="a4414-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="a4414-129">Gå til en af følgende appbutikker for at installere **Microsoft Finance and Operations (Dynamics 365)**-appen på din mobilenhed:</span><span class="sxs-lookup"><span data-stu-id="a4414-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="a4414-130">For Google Android-enheder</span><span class="sxs-lookup"><span data-stu-id="a4414-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="a4414-131">For Apple iOS-enheder</span><span class="sxs-lookup"><span data-stu-id="a4414-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="a4414-132">Åbn Finance and Operations (Dynamics 365)-appen.</span><span class="sxs-lookup"><span data-stu-id="a4414-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="a4414-133">Logonsiden vises.</span><span class="sxs-lookup"><span data-stu-id="a4414-133">The sign-in page should appear.</span></span> <span data-ttu-id="a4414-134">I feltet **Log på** skal du angive URL-adressen til Supply Chain Management eller vælge en ny URL-adresse på listen **Seneste miljøer** og derefter trykke på **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="a4414-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="a4414-135">![Logonside](media/mobile-app-sign-in.png "Logonside")</span><span class="sxs-lookup"><span data-stu-id="a4414-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="a4414-136">Hvis du bliver bedt om at bekræfte forbindelsen, skal du markere afkrydsningsfeltet **Jeg forstår** og derefter trykke på **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="a4414-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="a4414-137">På siden **Vælg en konto** skal du bruge din Microsoft-konto til at logge på mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a4414-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="a4414-138">Siden **Arbejdsområder** vises.</span><span class="sxs-lookup"><span data-stu-id="a4414-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="a4414-139">Den viser alle mobilarbejdsområder, der er publiceret af din Supply Chain Management-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a4414-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="a4414-140">![Liste over arbejdsområder](media/mobile-app-workspaces.png "Liste over arbejdsområder")</span><span class="sxs-lookup"><span data-stu-id="a4414-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="a4414-141">Hvis du skal ændre den juridiske enhed (firma), skal du trykke på menuknappen (nogle gange kaldet hamburger eller hamburgerknappen) i øverste venstre hjørne og derefter trykke på **Skift firma**.</span><span class="sxs-lookup"><span data-stu-id="a4414-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="a4414-142">![Skifte den juridiske enhed](media/mobile-app-change-comp.png "Skifte den juridiske enhed")</span><span class="sxs-lookup"><span data-stu-id="a4414-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="a4414-143">På siden **Arbejdsområder** skal du vælge det arbejdsområde, du vil arbejde med, for at åbne det.</span><span class="sxs-lookup"><span data-stu-id="a4414-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="a4414-144">![Arbejdsområde til aktivstyring på mobilenhed](media/mobile-app-asset-workspace.png "Arbejdsområde til aktivstyring på mobilenhed")</span><span class="sxs-lookup"><span data-stu-id="a4414-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="a4414-145">Arbejde med mobilarbejdsområdet til aktivstyring</span><span class="sxs-lookup"><span data-stu-id="a4414-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="a4414-146">Du kan finde flere oplysninger om, hvordan du arbejder med mobilarbejdsområdet til **aktivstyring**, under [Bruge mobilarbejdsområdet til aktivstyring](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="a4414-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="a4414-147">Yderligere oplysninger om Finance and Operations (Dynamics 365)-mobilappen finder du på [Mobilapp-startside](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="a4414-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]