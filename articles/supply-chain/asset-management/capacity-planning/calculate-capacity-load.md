---
title: Beregn kapacitetsbelastning
description: Dette emne beskriver, hvordan du beregner kapacitetsbelastning i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3aa87f5594be079144142296cac977b0bfdd125e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022577"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="be364-103">Beregne kapacitetsbelastning</span><span class="sxs-lookup"><span data-stu-id="be364-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="be364-104">I Styring af aktiver kan du beregne kapacitetsbelastning på:</span><span class="sxs-lookup"><span data-stu-id="be364-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="be364-105">vedligeholdelsestidsplanslinjer</span><span class="sxs-lookup"><span data-stu-id="be364-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="be364-106">arbejdsordrer, der endnu ikke er planlagt</span><span class="sxs-lookup"><span data-stu-id="be364-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="be364-107">planlagte arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="be364-107">scheduled work orders</span></span>

<span data-ttu-id="be364-108">Dette er nyttigt, hvis du vil have en oversigt over forventet kapacitetsbelastning i en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="be364-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="be364-109">Beregning af kapacitetsbelastning kan foretages på alle aktiver eller udvalgte aktiver.</span><span class="sxs-lookup"><span data-stu-id="be364-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="be364-110">Du kan også foretage en beregning af aktiviteter med vedligeholdelsesnedetid eller arbejdsordrepuljer.</span><span class="sxs-lookup"><span data-stu-id="be364-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="be364-111">Klik på **Styring af aktiver** > **Forespørgsler** > **Kapacitetsbelastning** eller **Styring af aktiver** > **Generelt** > **Arbejdsordrepuljer** > **Alle arbejdsordrepuljer** / **Aktive arbejdsordrepuljer** > vælg arbejdsordrepulje på listen > knappen **Kapacitetsbelastning** eller **Styring af aktiver** > **Generelt** > **Aktiviteter med vedligeholdelsesnedetid** > **Alle aktiviteter med vedligeholdelsesnedetid** / **Aktive aktiviteter med vedligeholdelsesnedetid** > vælg vedligeholdelsesaktivitet på listen > knappen **Kapacitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="be364-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="be364-112">Vælg en periode til beregningen i felterne **Startdato/-klokkeslæt** og **Slutdato/-klokkeslæt** i dialogboksen **Beregn kapacitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="be364-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="be364-113">Vælg "Ja" på knappen **Medtag vedligeholdelsestidsplan**, hvis du vil medtage vedligeholdelsestidsplanlinjer i beregningen.</span><span class="sxs-lookup"><span data-stu-id="be364-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="be364-114">Vælg "Ja" på knappen **Medtag arbejdsordre**, hvis du vil medtage arbejdsordrejob i beregningen.</span><span class="sxs-lookup"><span data-stu-id="be364-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="be364-115">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede kapacitetsbelastningslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="be364-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="be364-116">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelsestidsplanslinjer og arbejdsordrer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="be364-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="be364-117">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelsestidsplanlinjer og alle arbejdsordrer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="be364-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="be364-118">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="be364-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="be364-119">I **Sammenlæg pr.**-grupperne skal du klikke på de relevante knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="be364-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="be364-120">I skærmbilledet nedenfor fremhæves de valgte **Sammenlæg pr.**-knapper med blå farve.</span><span class="sxs-lookup"><span data-stu-id="be364-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="be364-121">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="be364-121">Click on a button to activate or deactivate it.</span></span>

    ![Figur 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="be364-123">Hvis du kun vil fokusere på kapacitetsplanlægning i forbindelse med planlagte arbejdsordrer, skal du se [Beregne kapacitetsbelastning på planlagte arbejdsordrer](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="be364-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

