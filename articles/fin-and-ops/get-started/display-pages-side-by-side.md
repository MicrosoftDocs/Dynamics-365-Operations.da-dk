---
title: "Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue"
description: "I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Finance and Operations."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f19ca5e9642b5a8222ee7bf23fdd228ab75d2ed1
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a><span data-ttu-id="68ec7-103">Vise sider side om side ved hjælp af ikonet Åbn i et nyt vindue</span><span class="sxs-lookup"><span data-stu-id="68ec7-103">Display pages side-by-side using the Open in New Window icon</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="68ec7-104">I denne artikel beskrives det, hvordan du får vist siderne side om side i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68ec7-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="68ec7-105">Microsoft Dynamics 365 for Finance and Operations hjælper dig med at udføre opgaver effektivt.</span><span class="sxs-lookup"><span data-stu-id="68ec7-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="68ec7-106">I nogle tilfælde kan du få vist flere sider side om side for at udføre opgaver hurtigt.</span><span class="sxs-lookup"><span data-stu-id="68ec7-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="68ec7-107">Som et eksempel vil du måske validere eller angive linjer i mere end én kladde.</span><span class="sxs-lookup"><span data-stu-id="68ec7-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="68ec7-108">For at gøre det vil du typisk være nødt til at gå skulle gå frem og tilbage mellem den side, der viser en liste over kladder, og den side, der viser linjer for en given kladde.</span><span class="sxs-lookup"><span data-stu-id="68ec7-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="68ec7-109">Men funktionen **Åbn i et nyt vindue** gør det muligt for dig at få vist disse sider side om side, så du hurtigt kan udføre opgaver.</span><span class="sxs-lookup"><span data-stu-id="68ec7-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="68ec7-110">Hvis du fortsætter med det eksempel, der er nævnt ovenfor, så kan du, når du får vist linjerne, klikke på ikonet **Åbn i et nyt vindue**.</span><span class="sxs-lookup"><span data-stu-id="68ec7-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="68ec7-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="68ec7-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="68ec7-112">Når du klikker på ikonet **Åbn i et nyt vindue**, åbnes siden med linjer i en ny pop op-browser, og derefter navigerer den oprindelige browser tilbage i historikken til siden, der viste oversigten over kladder.</span><span class="sxs-lookup"><span data-stu-id="68ec7-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="68ec7-113">Du kan derefter få vist begge sider på samme tid.</span><span class="sxs-lookup"><span data-stu-id="68ec7-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="68ec7-114">Når du er færdig med at få vist en kladde, kan du ændre den valgte kladde på siden med journallisten, og så viser siden med linjer i pop op-vinduet automatisk linjerne i den nyligt valgte kladde.</span><span class="sxs-lookup"><span data-stu-id="68ec7-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="68ec7-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="68ec7-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="68ec7-116">Den dynamiske sammenkædning og opdatering sker på grund af de forbindelser, der findes mellem de data, der sikkerhedskopierer disse sider.</span><span class="sxs-lookup"><span data-stu-id="68ec7-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="68ec7-117">Hvis systemet ikke er opmærksom på relationen mellem dataene, opdateres pop up-vinduet ikke automatisk som reaktion på en ændring i det vindue, hvor den stammer fra.</span><span class="sxs-lookup"><span data-stu-id="68ec7-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="68ec7-118">Nogle sider har flere visninger som gittervisning, overskriftsvisning og detaljeret visning.</span><span class="sxs-lookup"><span data-stu-id="68ec7-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="68ec7-119">Ikonet **Åbn i et nyt vindue** bevirker, at hele siden skal åbnes i det nye browservindue.</span><span class="sxs-lookup"><span data-stu-id="68ec7-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="68ec7-120">Du kan derfor ikke have to visninger af den samme side parallelt, mens du bruger funktionen **Åbn i et nyt vindue**.</span><span class="sxs-lookup"><span data-stu-id="68ec7-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="68ec7-121">Næsten alle sådanne sider har dog en liste til navigation, som du kan bruge til at skifte mellem poster og opnå en lignende oplevelse.</span><span class="sxs-lookup"><span data-stu-id="68ec7-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="68ec7-122">Før du bruger funktionen **Åbn i et nyt vindue**, skal du konfigurere browserens pop op-blokering for at tillade pop op-vinduer fra URL-adressen på Finance and Operations-webstedet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="68ec7-123">Som et eksempel kan du tillade pop op-vinduer fra "\*.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="68ec7-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="68ec7-124">Funktionen **Åbn i et nyt vindue** er kun tilgængelig, når der er mere end én side åben i vinduet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="68ec7-125">Desuden lukkes pop-up-vinduet automatisk, når der ikke er flere sider åbent (når den sidste side i dette vindue er lukket).</span><span class="sxs-lookup"><span data-stu-id="68ec7-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="68ec7-126">Finance and Operations lukker også åbne sider, når du navigerer til et andet område i programmet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="68ec7-127">Derfor, hvis du har åbne pop op-vinduer og navigere til et andet område i programmet, lukkes pop op-vinduerne lukkes automatisk, fordi siderne i disse vinduer blev lukket af systemet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="68ec7-128">Topbjælken i pop op-vinduerne viser oplysninger om den virksomhed, som siden blev åbnet i, og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="68ec7-129">Pop op-vinduer er også afhængige af hovedbrowservinduet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68ec7-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="68ec7-130">Hvis hovedvinduet er lukket eller opdateres, bliver alle åbne pop op-vinduer skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="68ec7-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="68ec7-131">Det betyder, at du kan stadig få vist oplysninger i disse vinduer, men du kan ikke interagere med dem.</span><span class="sxs-lookup"><span data-stu-id="68ec7-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




