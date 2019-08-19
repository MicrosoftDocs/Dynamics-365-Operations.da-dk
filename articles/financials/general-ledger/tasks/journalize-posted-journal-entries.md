---
title: Journalisere bogførte kladdeposter
description: Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: cbf7ee8063487303cd4c8d2b76a8b44bacc86193
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846385"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="26e1f-103">Journalisere bogførte kladdeposter</span><span class="sxs-lookup"><span data-stu-id="26e1f-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26e1f-104">Denne procedure viser, hvordan du journaliserer bogførte kladdeposter.</span><span class="sxs-lookup"><span data-stu-id="26e1f-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="26e1f-105">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="26e1f-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="26e1f-106">Valider indstillingerne for journalisering under Finans > Opsætning Finans > Finansparametre.</span><span class="sxs-lookup"><span data-stu-id="26e1f-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="26e1f-107">Feltet Udvidet finanskladde kan være angivet til Ja eller Nej.</span><span class="sxs-lookup"><span data-stu-id="26e1f-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="26e1f-108">Hvis angivet til Ja, vil rapportens output være forskellig.</span><span class="sxs-lookup"><span data-stu-id="26e1f-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="26e1f-109">Vælg, om perioden kan lukkes, hvis journaliseringsprocessen endnu ikke er blevet kørt.</span><span class="sxs-lookup"><span data-stu-id="26e1f-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="26e1f-110">Hvis denne indstilling er angivet til Ja, kan perioden ikke lukkes, før journaliseringsprocessen er fuldført for den pågældende periode.</span><span class="sxs-lookup"><span data-stu-id="26e1f-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="26e1f-111">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="26e1f-111">Close the page.</span></span>
5. <span data-ttu-id="26e1f-112">Gå til Finans > Periodiske opgaver > Journalisering.</span><span class="sxs-lookup"><span data-stu-id="26e1f-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="26e1f-113">Klik på Filtrér.</span><span class="sxs-lookup"><span data-stu-id="26e1f-113">Click Filter.</span></span>
7. <span data-ttu-id="26e1f-114">Fremhæv de rækker med filtreringskriterier, som du vil definere.</span><span class="sxs-lookup"><span data-stu-id="26e1f-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="26e1f-115">Indtast eller vælg filtreringskriterierne i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="26e1f-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="26e1f-116">Klik på OK for at lukke filtreringssiden.</span><span class="sxs-lookup"><span data-stu-id="26e1f-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="26e1f-117">Klik på OK for at starte journaliseringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="26e1f-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="26e1f-118">Der genereres en rapport, når processen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="26e1f-118">A report will be generated after the process is complete.</span></span>  

