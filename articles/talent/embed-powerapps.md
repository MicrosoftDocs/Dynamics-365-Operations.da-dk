---
title: Integrere Power Apps-apps i Dynamics 365 Human Resources
description: I dette emne beskrives, hvordan du kan løse problemet, når Microsoft Power Apps-menupunktet er forsvundet fra modulet Systemadministration.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017867"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="3be70-103">Integrere Power Apps-apps i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="3be70-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="3be70-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="3be70-104">**Issue**</span></span>

<span data-ttu-id="3be70-105">Menupunktet **Power Apps** er forsvundet fra modulet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="3be70-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="3be70-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="3be70-106">**Cause**</span></span>

<span data-ttu-id="3be70-107">Brugergrænsefladens design er blevet ændret, og Microsoft Power Apps er nu inkluderet i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3be70-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="3be70-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="3be70-108">**Resolution**</span></span>

<span data-ttu-id="3be70-109">Den måde, Power Apps er integreret på, er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="3be70-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="3be70-110">Power Apps tilføjes nu via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="3be70-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="3be70-111">Du kan tilføje Power Apps på næsten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="3be70-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="3be70-112">Du kan finde oplysninger om, hvordan du integrerer Power Apps i Talent, under [Integrer Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="3be70-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="3be70-113">Enhver Power Apps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.</span><span class="sxs-lookup"><span data-stu-id="3be70-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="3be70-114">Knappen **Power Apps** findes i øverste højre hjørne af næsten alle sider i Talent.</span><span class="sxs-lookup"><span data-stu-id="3be70-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="3be70-115">Du kan bruge denne knap til at indsætte apps.</span><span class="sxs-lookup"><span data-stu-id="3be70-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="3be70-116">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="3be70-116">Here is an example.</span></span>

1. <span data-ttu-id="3be70-117">Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="3be70-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="3be70-118">Vælg knappen **Power Apps**, og vælg derefter **Tilføj en app fra Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="3be70-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps-knap](media/png.png)

3. <span data-ttu-id="3be70-120">Udfyld felterne i dialogboksen **Tilføj en app fra Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="3be70-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Dialogboksen Tilføj en app fra Power Apps](media/insert-powerapp.png)

<span data-ttu-id="3be70-122">Du kan også følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3be70-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="3be70-123">I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Tilpas denne side**.</span><span class="sxs-lookup"><span data-stu-id="3be70-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    <span data-ttu-id="3be70-125">Tilpasningsværktøjslinjen vises.</span><span class="sxs-lookup"><span data-stu-id="3be70-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="3be70-126">Vælg **Tilføj en app fra Power Apps** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="3be70-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Tilføje en app fra Power Apps ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
