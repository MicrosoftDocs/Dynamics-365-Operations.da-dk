---
title: Afslut en produktionsordre
description: Denne procedure viser, hvordan du afslutter en produktionsordre.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207065"
---
# <a name="end-a-production-order"></a><span data-ttu-id="60e9f-103">Afslut en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="60e9f-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60e9f-104">Denne procedure viser, hvordan du afslutter en produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="60e9f-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="60e9f-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="60e9f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="60e9f-106">Dette er den sidste procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="60e9f-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="60e9f-107">Afslut en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="60e9f-107">End a production order</span></span>
1. <span data-ttu-id="60e9f-108">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="60e9f-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="60e9f-109">Vælg en produktionsordre, som har statussen Færdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="60e9f-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="60e9f-110">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="60e9f-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="60e9f-111">Klik på Afslut.</span><span class="sxs-lookup"><span data-stu-id="60e9f-111">Click End.</span></span>
    * <span data-ttu-id="60e9f-112">På denne side kan du bekræfte, at du vil afslutte produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="60e9f-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="60e9f-113">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="60e9f-113">Click the General tab.</span></span>
5. <span data-ttu-id="60e9f-114">Indtast en dato i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="60e9f-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="60e9f-115">Vælg "Tildeling" i feltet Spildmetode.</span><span class="sxs-lookup"><span data-stu-id="60e9f-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="60e9f-116">Når du vælger metoden Tildeling, føjes omkostninger fra kasserede materialer til de færdige varer.</span><span class="sxs-lookup"><span data-stu-id="60e9f-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="60e9f-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="60e9f-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="60e9f-118">Valider beregningsresultater</span><span class="sxs-lookup"><span data-stu-id="60e9f-118">Validate calculation results</span></span>
1. <span data-ttu-id="60e9f-119">Klik på Administrer omkostninger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="60e9f-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="60e9f-120">Klik på Vis omkostningssammenligning.</span><span class="sxs-lookup"><span data-stu-id="60e9f-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="60e9f-121">Når du har afsluttet produktionsordren, kan du sammenligne den forkalkulerede kostpris i forhold til den realiserede kostpris for at få et overblik over produktionsafvigelser.</span><span class="sxs-lookup"><span data-stu-id="60e9f-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
