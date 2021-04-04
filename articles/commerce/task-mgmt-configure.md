---
title: Konfigurer opgavestyring
description: Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere funktioner til opgavestyring i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478038"
---
# <a name="configure-task-management"></a><span data-ttu-id="1eb96-103">Konfigurer opgavestyring</span><span class="sxs-lookup"><span data-stu-id="1eb96-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1eb96-104">Dette emne indeholder en beskrivelse af, hvordan du kan konfigurere funktioner til opgavestyring i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1eb96-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1eb96-105">Før Dynamics 365 Commerce-ledere og -medarbejdere kan bruge funktionerne til opgavestyring i Commerce, skal du konfigurere opgavestyring.</span><span class="sxs-lookup"><span data-stu-id="1eb96-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="1eb96-106">Konfigurationstrin omfatter tildeling af rettigheder til ledere og medarbejdere, distribution af tilladelser til POS-klienter, opsætning af POS-beskeder og konfiguration af feltet **Opgave** på startsiden for et POS-program.</span><span class="sxs-lookup"><span data-stu-id="1eb96-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="1eb96-107">Konfigurere rettigheder for butikschefer</span><span class="sxs-lookup"><span data-stu-id="1eb96-107">Configure permissions for store managers</span></span>

<span data-ttu-id="1eb96-108">Alle arbejdere i en bestemt butik kan få vist alle opgaver, der er knyttet til den pågældende butik.</span><span class="sxs-lookup"><span data-stu-id="1eb96-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="1eb96-109">De kan også opdatere status for de opgaver, der er tildelt til dem.</span><span class="sxs-lookup"><span data-stu-id="1eb96-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="1eb96-110">Personer, f.eks. butikschefer, skal imidlertid have rettigheder til styring af opgaver for at kunne administrere de opgaver, der er tildelt til lageret, og til at oprette opgaver med et enkelt formål.</span><span class="sxs-lookup"><span data-stu-id="1eb96-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="1eb96-111">Udfør følgende trin for at konfigurere indstillinger for opgavestyring for butikschefer.</span><span class="sxs-lookup"><span data-stu-id="1eb96-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="1eb96-112">Gå til **Retail og Commerce \> Medarbejdere \> Rettighedsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="1eb96-113">Vælg en bestemt rettighedsgruppe (f.eks **Chef**), og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="1eb96-114">Indstil **Tillad opgavestyring** til **Ja** i oversigtspanelet **Rettigheder**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="1eb96-115">Tilføj handlingen **Opgavestyring** på oversigtspanelet **Beskeder**, og angiv en værdi i feltet **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="1eb96-116">Skriv f.eks. **2**, hvis handlingen **Ordreopfyldelse** allerede har en værdi af **1** for **Visningsrækkefølge**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1eb96-117">Hvis en person, der ikke er chef, skal have tilladelse til styring af opgaver i kasseapparatet, kan du give rettigheder til den person.</span><span class="sxs-lookup"><span data-stu-id="1eb96-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="1eb96-118">Du kan også oprette en ny tilladelsesgruppe for ikke-ledere og angive indstillingen **Tillad Opgavestyring** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="1eb96-119">Følgende illustration viser, hvordan du konfigurerer indstillinger for opgavestyring for butikschefer.</span><span class="sxs-lookup"><span data-stu-id="1eb96-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Konfigurere indstillinger for opgavestyring for butikschefer](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="1eb96-121">Konfigurere rettigheder for medarbejdere</span><span class="sxs-lookup"><span data-stu-id="1eb96-121">Configure permissions for employees</span></span>

<span data-ttu-id="1eb96-122">Medarbejdere skal have rettigheder til at oprette opgavelister, administrere tildelingskriterier og konfigurere gentagelsen af en opgaveliste.</span><span class="sxs-lookup"><span data-stu-id="1eb96-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="1eb96-123">Hvis du vil konfigurere disse rettigheder, skal du tildele medarbejdere rollen **Retail Jobliste**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="1eb96-124">Du kan konfigurere rettigheder for en medarbejder ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1eb96-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="1eb96-125">Gå til **Retail og Commerce \> Medarbejdere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="1eb96-126">Vælg medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="1eb96-126">Select an employee.</span></span>
1. <span data-ttu-id="1eb96-127">Klik på **Tildel roller** i oversigtspanelet **Brugers roller**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="1eb96-128">Vælg rollen **Retail Jobliste** i dialogboksen **Tildel roller til bruger**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="1eb96-129">Distribuere rettigheder til POS-klienter</span><span class="sxs-lookup"><span data-stu-id="1eb96-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="1eb96-130">Før medarbejderne kan bruge POS-klienter, skal rettighederne distribueres og synkroniseres til disse klienter.</span><span class="sxs-lookup"><span data-stu-id="1eb96-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="1eb96-131">Udfør følgende trin for at distribuere rettigheder til POS-klienter:</span><span class="sxs-lookup"><span data-stu-id="1eb96-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="1eb96-132">Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="1eb96-133">Vælg distributionsplanen **1060** (**Human Resources**), og vælg derefter **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="1eb96-134">Vælg distributionsplanen **1070** (**Kanalkonfiguration**), og vælg derefter **Kør nu**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="1eb96-135">Konfigurere POS-beskeder for opgaver</span><span class="sxs-lookup"><span data-stu-id="1eb96-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="1eb96-136">Opgavestyring skal være konfigureret, så beskeder er tilgængelige i POS-programmet.</span><span class="sxs-lookup"><span data-stu-id="1eb96-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="1eb96-137">Du kan konfigurere POS-beskeder for opgaver ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1eb96-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="1eb96-138">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> POS-handlinger**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="1eb96-139">Find handlingen **1400** (**Opgavestyring**), og markér afkrydsningsfeltet **Aktivér beskeder** for den.</span><span class="sxs-lookup"><span data-stu-id="1eb96-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="1eb96-140">I følgende illustration vises handlingen **Opgavestyring** på siden **POS-handlinger**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Handlingen Opgavestyring på siden POS-handlinger](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="1eb96-142">Du kan finde flere oplysninger om, hvordan du konfigurerer POS-beskeder, i [Vis ordrebeskeder på POS](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="1eb96-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="1eb96-143">Konfigurere feltet Opgaver på en startside for POS-programmet</span><span class="sxs-lookup"><span data-stu-id="1eb96-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="1eb96-144">Før du konfigurerer feltet **Opgaver** på startsiden for et POS-program, kan du se [Skærmlayout til POS](pos-screen-layouts.md) for at få oplysninger om, hvordan du konfigurerer og føjer nye knapper til et POS-skærmlayout.</span><span class="sxs-lookup"><span data-stu-id="1eb96-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="1eb96-145">Du konfigurerer feltet **Opgaver** på en startside for POS-programmet ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1eb96-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="1eb96-146">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS \> Screenlayout**.</span><span class="sxs-lookup"><span data-stu-id="1eb96-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="1eb96-147">Vælg et skærmlayout, vælg en layout størrelse, og vælg en knapmatrix.</span><span class="sxs-lookup"><span data-stu-id="1eb96-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="1eb96-148">Vælg **Designer** i oversigtspanelet **Knapmatrix** for at redigere den valgte knapmatrix.</span><span class="sxs-lookup"><span data-stu-id="1eb96-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="1eb96-149">Føj en **Opgave**-flise til det relevante afsnit på startsiden.</span><span class="sxs-lookup"><span data-stu-id="1eb96-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="1eb96-150">Følgende illustration viser et eksempel på et **Opgave**-felt på en POS-startside.</span><span class="sxs-lookup"><span data-stu-id="1eb96-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Opgavefelt på en POS-startside](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="1eb96-152">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1eb96-152">Additional resources</span></span>

[<span data-ttu-id="1eb96-153">Oversigt over opgavestyring</span><span class="sxs-lookup"><span data-stu-id="1eb96-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="1eb96-154">Oprette opgavelister og tilføje opgaver</span><span class="sxs-lookup"><span data-stu-id="1eb96-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1eb96-155">Tildele opgavelister til butikker eller medarbejdere</span><span class="sxs-lookup"><span data-stu-id="1eb96-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="1eb96-156">Opgavestyring i POS</span><span class="sxs-lookup"><span data-stu-id="1eb96-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
