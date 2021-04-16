---
title: Behandle og spore kildedata
description: Al databehandling køres af job.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34612469f763cf1b30be46ff088605ae22883022
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840991"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="b5ff7-103">Behandle og spore kildedata</span><span class="sxs-lookup"><span data-stu-id="b5ff7-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5ff7-104">Al databehandling køres af job.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-104">All data processing is run by jobs.</span></span> <span data-ttu-id="b5ff7-105">Der oprettes en kladde for hvert job og dataprovider for at dokumentere, at processen blev kørt, og at posterne blev behandlet i det aktuelle job.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="b5ff7-106">Du kan bruge denne procedure til at konfigurere en datakilde og derefter spore oprindelsen til en bestemt omkostningspost.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="b5ff7-107">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="b5ff7-108">Før du udfører denne opgave, skal du sørge for at afspille følgende opgaveguider: "Oprette en finanspost for omkostningsregnskab", "Definere kontrolenheder for omkostninger" og "Administrere datakilde til finansposten for omkostningsregnskabet".</span><span class="sxs-lookup"><span data-stu-id="b5ff7-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="b5ff7-109">Gå til Omkostningsregnskab > Opsætning Finans > Finansposter for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="b5ff7-110">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b5ff7-111">Vælg den finanspost i omkostningsregnskabet, du oprettede tidligere.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="b5ff7-112">Klik på Faktiske versioner.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-112">Click Actual versions.</span></span>
4. <span data-ttu-id="b5ff7-113">Klik på Behandling af kildedata i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="b5ff7-114">Klik på Overførselskladder for finansposteringer.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="b5ff7-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b5ff7-116">Klik på Kladdeposteringer.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-116">Click Journal entries.</span></span>
8. <span data-ttu-id="b5ff7-117">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b5ff7-118">Klik på Omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-118">Click Cost entries.</span></span>
10. <span data-ttu-id="b5ff7-119">Klik på Kildepost.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-119">Click Source entry.</span></span>
11. <span data-ttu-id="b5ff7-120">Klik på Behandling af kildedata i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="b5ff7-121">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-121">Click General ledger.</span></span>
13. <span data-ttu-id="b5ff7-122">Indtast eller vælg en værdi i feltet Regnskabskalenderperiode.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="b5ff7-123">Vælg regnskabsårets 2017 periode 9 i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="b5ff7-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="b5ff7-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]