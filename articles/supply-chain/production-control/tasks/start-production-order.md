---
title: Starte en produktionsordre
description: Denne procedure viser, hvordan du starter en produktionsordre i produktionen.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9822dd66876ef8ed6bbcd5846a39d69d2446d7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981064"
---
# <a name="start-a-production-order"></a><span data-ttu-id="0e413-103">Starte en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="0e413-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e413-104">Denne procedure viser, hvordan du starter en produktionsordre i produktionen.</span><span class="sxs-lookup"><span data-stu-id="0e413-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="0e413-105">Tids- og materialeforbrug rapporteres i denne proces.</span><span class="sxs-lookup"><span data-stu-id="0e413-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="0e413-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="0e413-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0e413-107">Dette er den femte procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="0e413-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="0e413-108">Starte en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="0e413-108">Start a production order</span></span>
1. <span data-ttu-id="0e413-109">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="0e413-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="0e413-110">Vælg en produktionsordre, som har statussen Frigivet.</span><span class="sxs-lookup"><span data-stu-id="0e413-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="0e413-111">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e413-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="0e413-112">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="0e413-112">Click Start.</span></span>
    * <span data-ttu-id="0e413-113">På denne side kan du bekræfte start af produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="0e413-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="0e413-114">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="0e413-114">Click the General tab.</span></span>
5. <span data-ttu-id="0e413-115">I feltet Fra opr.nr.</span><span class="sxs-lookup"><span data-stu-id="0e413-115">In the From Oper.</span></span> <span data-ttu-id="0e413-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="0e413-116">No.</span></span> <span data-ttu-id="0e413-117">skal du skrive "10".</span><span class="sxs-lookup"><span data-stu-id="0e413-117">field, enter '10'.</span></span>
6. <span data-ttu-id="0e413-118">Vælg "Altid" i feltet Automatisk ruteforbrug.</span><span class="sxs-lookup"><span data-stu-id="0e413-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="0e413-119">Klik på afkrydsningsfeltet Bogfør rutekort nu.</span><span class="sxs-lookup"><span data-stu-id="0e413-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="0e413-120">Vælg "Altid" i feltet Automatisk styklisteforbrug.</span><span class="sxs-lookup"><span data-stu-id="0e413-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="0e413-121">Klik på afkrydsningsfeltet Bogfør plukliste nu.</span><span class="sxs-lookup"><span data-stu-id="0e413-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="0e413-122">Klik på afkrydsningsfeltet Udskriv plukliste nu.</span><span class="sxs-lookup"><span data-stu-id="0e413-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="0e413-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e413-123">Click OK.</span></span>
    * <span data-ttu-id="0e413-124">Dette er den udskrevne plukliste, som viser de materialer, der er brugt til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="0e413-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="0e413-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e413-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="0e413-126">Valider pluklisten</span><span class="sxs-lookup"><span data-stu-id="0e413-126">Validate the picking list</span></span>
1. <span data-ttu-id="0e413-127">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e413-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="0e413-128">Klik på Plukliste.</span><span class="sxs-lookup"><span data-stu-id="0e413-128">Click Picking list.</span></span>
3. <span data-ttu-id="0e413-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0e413-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0e413-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e413-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0e413-131">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0e413-131">Click Edit.</span></span>
6. <span data-ttu-id="0e413-132">Angiv et nummer i feltet Forbrug.</span><span class="sxs-lookup"><span data-stu-id="0e413-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="0e413-133">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="0e413-133">Click Post.</span></span>
8. <span data-ttu-id="0e413-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e413-134">Click OK.</span></span>
    * <span data-ttu-id="0e413-135">I pluklistejournalen bogføres de materialer, der forbruges af produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="0e413-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="0e413-136">Før du bogfører journalen, kan du foretage justeringer, hvis der er en forskel mellem den forkalkulerede mængde og den faktiske forbrugte mængde.</span><span class="sxs-lookup"><span data-stu-id="0e413-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="0e413-137">Klik på fanen GridPanel.</span><span class="sxs-lookup"><span data-stu-id="0e413-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="0e413-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0e413-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="0e413-139">Bekræft rutekortjournalen</span><span class="sxs-lookup"><span data-stu-id="0e413-139">Verify the route card journal</span></span>
1. <span data-ttu-id="0e413-140">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0e413-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="0e413-141">Klik på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="0e413-141">Click Route card.</span></span>
3. <span data-ttu-id="0e413-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="0e413-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0e413-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="0e413-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0e413-144">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="0e413-144">Click Edit.</span></span>
6. <span data-ttu-id="0e413-145">Angiv et tal i feltet Timer.</span><span class="sxs-lookup"><span data-stu-id="0e413-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="0e413-146">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="0e413-146">Click Post.</span></span>
8. <span data-ttu-id="0e413-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0e413-147">Click OK.</span></span>
    * <span data-ttu-id="0e413-148">I rutekortkladden registreres den tid, der er brugt på de enkelte operationer.</span><span class="sxs-lookup"><span data-stu-id="0e413-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="0e413-149">Antal gode og fejl kan også rapporteres.</span><span class="sxs-lookup"><span data-stu-id="0e413-149">Good and error quantity can also be reported.</span></span>  
