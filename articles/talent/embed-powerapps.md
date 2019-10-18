---
title: Integrere PowerApps-apps i Dynamics 365 - Core HR
description: I dette emne beskrives, hvordan du kan løse problemet, når PowerApps-menupunktet er forsvundet fra modulet Systemadministration.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008424"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="52aae-103">Integrer PowerApps-apps i Core HR</span><span class="sxs-lookup"><span data-stu-id="52aae-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52aae-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="52aae-104">**Issue**</span></span>

<span data-ttu-id="52aae-105">Menupunktet **PowerApps** er forsvundet fra modulet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="52aae-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="52aae-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="52aae-106">**Cause**</span></span>

<span data-ttu-id="52aae-107">Brugergrænsefladens design er blevet ændret, og Microsoft PowerApps er nu inkluderet i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="52aae-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="52aae-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="52aae-108">**Resolution**</span></span>

<span data-ttu-id="52aae-109">Den måde, PowerApps-apps er integreret på, er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="52aae-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="52aae-110">PowerApps-apps tilføjes nu via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="52aae-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="52aae-111">Du kan tilføje PowerApps-apps på næsten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="52aae-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="52aae-112">Du kan finde oplysninger om, hvordan du integrerer PowerApps-apps i Talent, under [Integrer PowerApps-apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="52aae-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="52aae-113">Enhver PowerApps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.</span><span class="sxs-lookup"><span data-stu-id="52aae-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="52aae-114">Knappen **PowerApps** findes i øverste højre hjørne af næsten alle sider i Talent.</span><span class="sxs-lookup"><span data-stu-id="52aae-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="52aae-115">Du kan bruge denne knap til at indsætte en PowerApps-app.</span><span class="sxs-lookup"><span data-stu-id="52aae-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="52aae-116">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="52aae-116">Here is an example.</span></span>

1. <span data-ttu-id="52aae-117">Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="52aae-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="52aae-118">Vælg knappen **PowerApps**, og vælg derefter **Indsæt en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="52aae-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-knap](media/png.png)

3. <span data-ttu-id="52aae-120">Udfyld felterne i dialogboksen **Indsæt en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="52aae-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogboksen Indsæt en PowerApp.](media/insert-powerapp.png)

<span data-ttu-id="52aae-122">Du kan også følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="52aae-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="52aae-123">I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Personaliser denne formular**.</span><span class="sxs-lookup"><span data-stu-id="52aae-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    <span data-ttu-id="52aae-125">Tilpasningsværktøjslinjen vises.</span><span class="sxs-lookup"><span data-stu-id="52aae-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="52aae-126">Vælg **Indsæt \> PowerApp** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="52aae-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Tilføje en PowerApps-app ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
