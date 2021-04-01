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
ms.openlocfilehash: 3934db907c137f25c39c5769f96f0807eb597e37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231858"
---
# <a name="start-a-production-order"></a><span data-ttu-id="1056b-103">Starte en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="1056b-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1056b-104">Denne procedure viser, hvordan du starter en produktionsordre i produktionen.</span><span class="sxs-lookup"><span data-stu-id="1056b-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="1056b-105">Tids- og materialeforbrug rapporteres i denne proces.</span><span class="sxs-lookup"><span data-stu-id="1056b-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="1056b-106">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="1056b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1056b-107">Dette er den femte procedure ud af syv, der beskriver produktionsordrelivscyklussen.</span><span class="sxs-lookup"><span data-stu-id="1056b-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="1056b-108">Starte en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="1056b-108">Start a production order</span></span>
1. <span data-ttu-id="1056b-109">Gå til Produktionsstyring > Produktionsordrer > Alle produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="1056b-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="1056b-110">Vælg en produktionsordre, som har statussen Frigivet.</span><span class="sxs-lookup"><span data-stu-id="1056b-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="1056b-111">Klik på Produktionsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1056b-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="1056b-112">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="1056b-112">Click Start.</span></span>
    * <span data-ttu-id="1056b-113">På denne side kan du bekræfte start af produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="1056b-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="1056b-114">Klik på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="1056b-114">Click the General tab.</span></span>
5. <span data-ttu-id="1056b-115">I feltet Fra opr.nr.</span><span class="sxs-lookup"><span data-stu-id="1056b-115">In the From Oper.</span></span> <span data-ttu-id="1056b-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="1056b-116">No.</span></span> <span data-ttu-id="1056b-117">skal du skrive "10".</span><span class="sxs-lookup"><span data-stu-id="1056b-117">field, enter '10'.</span></span>
6. <span data-ttu-id="1056b-118">Vælg "Altid" i feltet Automatisk ruteforbrug.</span><span class="sxs-lookup"><span data-stu-id="1056b-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="1056b-119">Klik på afkrydsningsfeltet Bogfør rutekort nu.</span><span class="sxs-lookup"><span data-stu-id="1056b-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="1056b-120">Vælg "Altid" i feltet Automatisk styklisteforbrug.</span><span class="sxs-lookup"><span data-stu-id="1056b-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="1056b-121">Klik på afkrydsningsfeltet Bogfør plukliste nu.</span><span class="sxs-lookup"><span data-stu-id="1056b-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="1056b-122">Klik på afkrydsningsfeltet Udskriv plukliste nu.</span><span class="sxs-lookup"><span data-stu-id="1056b-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="1056b-123">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1056b-123">Click OK.</span></span>
    * <span data-ttu-id="1056b-124">Dette er den udskrevne plukliste, som viser de materialer, der er brugt til produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="1056b-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="1056b-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1056b-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="1056b-126">Valider pluklisten</span><span class="sxs-lookup"><span data-stu-id="1056b-126">Validate the picking list</span></span>
1. <span data-ttu-id="1056b-127">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1056b-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="1056b-128">Klik på Plukliste.</span><span class="sxs-lookup"><span data-stu-id="1056b-128">Click Picking list.</span></span>
3. <span data-ttu-id="1056b-129">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1056b-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1056b-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1056b-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1056b-131">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="1056b-131">Click Edit.</span></span>
6. <span data-ttu-id="1056b-132">Angiv et nummer i feltet Forbrug.</span><span class="sxs-lookup"><span data-stu-id="1056b-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="1056b-133">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="1056b-133">Click Post.</span></span>
8. <span data-ttu-id="1056b-134">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1056b-134">Click OK.</span></span>
    * <span data-ttu-id="1056b-135">I pluklistejournalen bogføres de materialer, der forbruges af produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="1056b-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="1056b-136">Før du bogfører journalen, kan du foretage justeringer, hvis der er en forskel mellem den forkalkulerede mængde og den faktiske forbrugte mængde.</span><span class="sxs-lookup"><span data-stu-id="1056b-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="1056b-137">Klik på fanen GridPanel.</span><span class="sxs-lookup"><span data-stu-id="1056b-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="1056b-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1056b-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="1056b-139">Bekræft rutekortjournalen</span><span class="sxs-lookup"><span data-stu-id="1056b-139">Verify the route card journal</span></span>
1. <span data-ttu-id="1056b-140">Klik på Vis i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1056b-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="1056b-141">Klik på Rutekort.</span><span class="sxs-lookup"><span data-stu-id="1056b-141">Click Route card.</span></span>
3. <span data-ttu-id="1056b-142">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="1056b-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1056b-143">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1056b-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1056b-144">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="1056b-144">Click Edit.</span></span>
6. <span data-ttu-id="1056b-145">Angiv et tal i feltet Timer.</span><span class="sxs-lookup"><span data-stu-id="1056b-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="1056b-146">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="1056b-146">Click Post.</span></span>
8. <span data-ttu-id="1056b-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1056b-147">Click OK.</span></span>
    * <span data-ttu-id="1056b-148">I rutekortkladden registreres den tid, der er brugt på de enkelte operationer.</span><span class="sxs-lookup"><span data-stu-id="1056b-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="1056b-149">Antal gode og fejl kan også rapporteres.</span><span class="sxs-lookup"><span data-stu-id="1056b-149">Good and error quantity can also be reported.</span></span>  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]