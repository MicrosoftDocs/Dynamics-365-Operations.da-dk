--- 
title: "Journalisere bogførte kladdeposter"
description: "Denne procedure viser, hvordan du journaliserer bogførte kladdeposter."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 253794b4eb44cb5fa6f946caa96ec39a477c061e
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="294fd-103">Journalisere bogførte kladdeposter</span><span class="sxs-lookup"><span data-stu-id="294fd-103">Journalize posted journal entries</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="294fd-104">Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="294fd-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="294fd-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="294fd-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="294fd-106">Valider indstillingerne for journalisering under Finans > Opsætning Finans > Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="294fd-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="294fd-107">Feltet Udvidet finanskladde kan være angivet til Ja eller Nej.</span><span class="sxs-lookup"><span data-stu-id="294fd-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="294fd-108">Hvis angivet til Ja, vil rapportens output være forskellig.</span><span class="sxs-lookup"><span data-stu-id="294fd-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="294fd-109">Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="294fd-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="294fd-110">Hvis denne indstilling er angivet til Ja, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="294fd-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="294fd-111">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="294fd-111">Close the page.</span></span>
5. <span data-ttu-id="294fd-112">Gå til Finans > Periodiske opgaver > Journalisering.</span><span class="sxs-lookup"><span data-stu-id="294fd-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="294fd-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="294fd-113">Click Filter.</span></span>
7. <span data-ttu-id="294fd-114">Fremhæv de rækker med filtreringskriterier, som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="294fd-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="294fd-115">Indtast eller vælg filtreringskriterierne i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="294fd-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="294fd-116">Klik på OK for at lukke filtreringssiden.</span><span class="sxs-lookup"><span data-stu-id="294fd-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="294fd-117">Klik på OK for at starte journaliseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="294fd-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="294fd-118">Der genereres en rapport, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="294fd-118">A report will be generated after the process is complete.</span></span>  


