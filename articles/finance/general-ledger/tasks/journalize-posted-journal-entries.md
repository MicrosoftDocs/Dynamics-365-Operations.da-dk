---
title: Journalisere bogførte kladdeposter
description: Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441489"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="accae-103">Journalisere bogførte kladdeposter</span><span class="sxs-lookup"><span data-stu-id="accae-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="accae-104">Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="accae-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="accae-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="accae-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="accae-106">Gå i **Navigationsrude** til **Moduler > Finans > Opsætning Finans > Finansparametre**.</span><span class="sxs-lookup"><span data-stu-id="accae-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="accae-107">Feltet **Udvidet finanskladde** kan være angivet til Ja eller Nej.</span><span class="sxs-lookup"><span data-stu-id="accae-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="accae-108">Hvis angivet til Ja, vil rapportens output være forskellig.</span><span class="sxs-lookup"><span data-stu-id="accae-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="accae-109">Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="accae-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="accae-110">Hvis denne indstilling er angivet til Ja, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="accae-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="accae-111">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="accae-111">Close the page.</span></span>
5. <span data-ttu-id="accae-112">Gå i **Navigationsrude** til **Moduler > Finans > Periodiske opgaver > Journalisering**.</span><span class="sxs-lookup"><span data-stu-id="accae-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="accae-113">Klik på **Filtrér**.</span><span class="sxs-lookup"><span data-stu-id="accae-113">Click **Filter**.</span></span>
7. <span data-ttu-id="accae-114">Fremhæv de rækker med filtreringskriterier, som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="accae-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="accae-115">Indtast eller vælg filtreringskriterierne i feltet **Kriterier**.</span><span class="sxs-lookup"><span data-stu-id="accae-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="accae-116">Klik på **OK** for at lukke filtreringssiden.</span><span class="sxs-lookup"><span data-stu-id="accae-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="accae-117">Klik på **OK** for at starte journaliseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="accae-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="accae-118">Der genereres en rapport, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="accae-118">A report will be generated after the process is complete.</span></span>  

