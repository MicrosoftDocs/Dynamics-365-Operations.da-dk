---
title: Konfigurere arbejdsgange for leasinggodkendelse
description: I emnet forklares det, hvordan du opretter en godkendelsesarbejdsgang, der skal køres, når der oprettes en ny leasingaftale.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1eaa2f5cc191ec93c30f4f10a662a87e501a341d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249575"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="f366a-103">Konfigurere arbejdsgange for leasinggodkendelse</span><span class="sxs-lookup"><span data-stu-id="f366a-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f366a-104">I emnet forklares det, hvordan du opretter en godkendelsesarbejdsgang, der skal køres, når der oprettes en ny leasingaftale.</span><span class="sxs-lookup"><span data-stu-id="f366a-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="f366a-105">Du kan finde flere oplysninger om, hvordan du bruger arbejdsgangen, i [Bruge arbejdsgange for leasinggodkendelse](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="f366a-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="f366a-106">Gå til **Aktivleasing \> Konfiguration \> Leasingarbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="f366a-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="f366a-107">På siden **Leasingarbejdsproces** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f366a-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="f366a-108">I den dialogboks, der vises, skal du under **Arbejdsprocestype** vælge linket **Leasingarbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="f366a-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="f366a-109">Ansøgningen åbnes.</span><span class="sxs-lookup"><span data-stu-id="f366a-109">The application is opened.</span></span> <span data-ttu-id="f366a-110">Når den er kørt, skal du logge på Azure Active Directory (Azure AD) for at blive omdirigeret til arbejdsprocesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="f366a-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="f366a-111">Træk **Godkendelse af leasingarbejdsproces** til arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f366a-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="f366a-112">Forbind en node fra **Start** til **Godkendelse af leasingarbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="f366a-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="f366a-113">Forbind derefter **Godkendelse af leasingarbejdsproces** til **Slut**.</span><span class="sxs-lookup"><span data-stu-id="f366a-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="f366a-114">Dobbeltklik på **Godkendelse af leasingarbejdsproces**.</span><span class="sxs-lookup"><span data-stu-id="f366a-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="f366a-115">Vælg **Egenskaber** og angiv derefter under **Grundlæggende indstillinger** et navn til arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="f366a-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="f366a-116">På denne side kan du også angive flere parametre for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="f366a-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="f366a-117">Hvis du har aktiveret **Automatiske aktioner**, vil systemet automatisk udføre en bestemt handling.</span><span class="sxs-lookup"><span data-stu-id="f366a-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="f366a-118">Notifikationer kan sendes, hvis de er angivet under fanen **Notifikationer**. Under fanen **Avancerede indstillinger** kan du angive en endelig godkender, angive en tidsgrænse og angive bestemte handlinger, der skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="f366a-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="f366a-119">Vælg **Luk**, når du er færdig med at angive arbejdsprocesparametrene.</span><span class="sxs-lookup"><span data-stu-id="f366a-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="f366a-120">Vælg **Trin 1** og derefter **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="f366a-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="f366a-121">Angiv et navn til trinnet under **Grundlæggende indstillinger**, opret en emnelinje til godkendelsen, og angiv instruktioner til godkendelsen.</span><span class="sxs-lookup"><span data-stu-id="f366a-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="f366a-122">Vælg tildelingstypen på siden **Tildeling**.</span><span class="sxs-lookup"><span data-stu-id="f366a-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="f366a-123">Hvis du vil tildele specifikke brugere til godkendelsen, skal du vælge **Bruger**, vælge de brugere, der godkender leasingaftaler og derefter vælge **Luk**.</span><span class="sxs-lookup"><span data-stu-id="f366a-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="f366a-124">Vælg **Gem og luk** for at oprette arbejdsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f366a-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="f366a-125">Vælg derefter **OK**, når du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="f366a-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="f366a-126">På siden **Opret arbejdsproces** skal du vælge **luk**.</span><span class="sxs-lookup"><span data-stu-id="f366a-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="f366a-127">Vælg den nye arbejdsproces, og vælg derefter **Versioner**.</span><span class="sxs-lookup"><span data-stu-id="f366a-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="f366a-128">Vælg derefter **Gør aktiv** for at sikre, at arbejdsgangen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="f366a-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="f366a-129">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="f366a-129">Select **Close**.</span></span> <span data-ttu-id="f366a-130">Den nye aktive version vises.</span><span class="sxs-lookup"><span data-stu-id="f366a-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]