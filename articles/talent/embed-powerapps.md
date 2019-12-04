---
title: Integrere Power Apps-apps i Dynamics 365 - Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830203"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="c9b1a-103">Integrere Power Apps-apps i Dynamics 365 - Core HR</span><span class="sxs-lookup"><span data-stu-id="c9b1a-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9b1a-104">**Udsted**</span><span class="sxs-lookup"><span data-stu-id="c9b1a-104">**Issue**</span></span>

<span data-ttu-id="c9b1a-105">Menupunktet **Power Apps** er forsvundet fra modulet **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="c9b1a-106">**Årsag**</span><span class="sxs-lookup"><span data-stu-id="c9b1a-106">**Cause**</span></span>

<span data-ttu-id="c9b1a-107">Brugergrænsefladens design er blevet ændret, og Microsoft Power Apps er nu inkluderet i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="c9b1a-108">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="c9b1a-108">**Resolution**</span></span>

<span data-ttu-id="c9b1a-109">Den måde, Power Apps er integreret på, er blevet ændret.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="c9b1a-110">Power Apps tilføjes nu via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="c9b1a-111">Du kan tilføje Power Apps på næsten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="c9b1a-112">Du kan finde oplysninger om, hvordan du integrerer Power Apps i Talent, under [Integrer Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="c9b1a-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="c9b1a-113">Enhver Power Apps-kunde, der har integreret apps inden ændringen, bør være blevet opgraderet til den nye model.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="c9b1a-114">Knappen **Power Apps** findes i øverste højre hjørne af næsten alle sider i Talent.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="c9b1a-115">Du kan bruge denne knap til at indsætte Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="c9b1a-116">Her er et eksempel.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-116">Here is an example.</span></span>

1. <span data-ttu-id="c9b1a-117">Gå til **Personalestyring \> Links \> Arbejdere \> Medarbejdere**.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="c9b1a-118">Vælg knappen **Power Apps**, og vælg derefter **Indsæt en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-knap](media/png.png)

3. <span data-ttu-id="c9b1a-120">Udfyld felterne i dialogboksen **Indsæt en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogboksen Indsæt en PowerApp.](media/insert-powerapp.png)

<span data-ttu-id="c9b1a-122">Du kan også følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="c9b1a-123">I handlingsruden på siden skal du under fanen **Indstillinger** i gruppen **Personaliser** vælge **Personaliser denne formular**.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Gruppen Personaliser under fanen Indstillinger](media/options.png)

    <span data-ttu-id="c9b1a-125">Tilpasningsværktøjslinjen vises.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="c9b1a-126">Vælg **Indsæt \> PowerApp** på værktøjslinjen.</span><span class="sxs-lookup"><span data-stu-id="c9b1a-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Tilføje en Power Apps-app ved hjælp af tilpasningsværktøjslinjen](media/powerapp-bar.png)
