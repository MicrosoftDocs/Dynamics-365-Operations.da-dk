---
title: Administrere en datakilde for finanspost for driftsregnskab
description: Du kan bruge denne procedure til at administrere datakilden i Finans for en finanspost i omkostningsregnskabet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMAXGeneralLedgerEntryProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88f5170610ea9b5634c4bf5da7079cacccdafe04
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441693"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="6cb9a-103">Administrere en datakilde for finanspost for driftsregnskab</span><span class="sxs-lookup"><span data-stu-id="6cb9a-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6cb9a-104">Du kan bruge denne procedure til at administrere datakilden i Finans for en finanspost i omkostningsregnskabet.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="6cb9a-105">Før du udfører denne opgave, skal du sørge for at afspille opgaveguiderne "Oprette en finanspost for omkostningsregnskab" og "Definere kontrolenheder for omkostninger".</span><span class="sxs-lookup"><span data-stu-id="6cb9a-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="6cb9a-106">Denne registrering bruger USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="6cb9a-107">Gå til Omkostningsregnskab > Opsætning Finans > Finansposter for omkostningsregnskab.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="6cb9a-108">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6cb9a-109">Klik på Faktiske versioner.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-109">Click Actual versions.</span></span>
4. <span data-ttu-id="6cb9a-110">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="6cb9a-111">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-111">Click General ledger.</span></span>
6. <span data-ttu-id="6cb9a-112">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-112">Click New.</span></span>
7. <span data-ttu-id="6cb9a-113">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="6cb9a-114">Indtast eller vælg en værdi i feltet Dataprovider.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="6cb9a-115">I dette eksempel skal du vælge Dynamics 365 Finance - Finansposter.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="6cb9a-116">Indtast eller vælg en værdi i feltet Dimension for omkostningselement.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6cb9a-117">Vælg Omkostningselementer i dette eksempel.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="6cb9a-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-118">Click Save.</span></span>
11. <span data-ttu-id="6cb9a-119">Klik på Konfigurer dataprovider.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="6cb9a-120">Indtast eller vælg en værdi i feltet Juridisk enhed.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="6cb9a-121">I dette eksempel skal du vælge USP2.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="6cb9a-122">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-122">Click New.</span></span>
14. <span data-ttu-id="6cb9a-123">Vælg Aktuelt i feltet Posteringslag.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="6cb9a-124">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6cb9a-124">Click OK.</span></span>

