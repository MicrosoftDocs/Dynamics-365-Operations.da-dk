---
title: Vedligeholdelsesstatus
description: I dette emne forklares, hvordan du beregner vedligeholdelsesstatus i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5bac42d5cdc62361ee9a562e59bafa09ca7a215
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018490"
---
# <a name="maintenance-status"></a><span data-ttu-id="179e5-103">Vedligeholdelsesstatus</span><span class="sxs-lookup"><span data-stu-id="179e5-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="179e5-104">I Styring af aktiver kan du foretage en oversigtsberegning for en specifik periode til nye, aktive og fuldførte aktiviteter for vedligeholdelsesanmodninger, arbejdsordrer og vedligeholdelsesnedetid.</span><span class="sxs-lookup"><span data-stu-id="179e5-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="179e5-105">Du kan også se antallet af fuldførte betingelsesvurderinger for den samme periode.</span><span class="sxs-lookup"><span data-stu-id="179e5-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="179e5-106">Brug denne beregning til at få et overblik over arbejdsbyrder i forbindelse med indgående og fuldførte vedligeholdelsesanmodninger og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="179e5-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="179e5-107">Foretage en beregning af vedligeholdelsesstatus</span><span class="sxs-lookup"><span data-stu-id="179e5-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="179e5-108">Klik på **Styring af aktiver** > **Forespørgsler** > **Vedligeholdelsesstatus**.</span><span class="sxs-lookup"><span data-stu-id="179e5-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="179e5-109">I dialogboksen **Beregn status** skal du vælge det tidsinterval, du vil foretage beregningen for, i felterne **Fra-dato** og **Til-dato**.</span><span class="sxs-lookup"><span data-stu-id="179e5-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="179e5-110">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede vedligeholdelseslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="179e5-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="179e5-111">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle vedligeholdelseslinjer for et arbejdssted på det øverste niveau, og derfor kan status på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="179e5-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="179e5-112">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle vedligeholdelseslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="179e5-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="179e5-113">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="179e5-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="179e5-114">Klik på **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="179e5-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="179e5-115">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="179e5-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="179e5-116">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="179e5-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="179e5-117">Husk at klikke på knappen **Opdater** for at opdatere beregningen, hver gang du foretager ændringer ved at aktivere eller deaktivere **Sammenlæg pr.**-knapper eller ved at foretage en beregning for en ny periode.</span><span class="sxs-lookup"><span data-stu-id="179e5-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="179e5-118">Klik på **Status**, hvis du vil oprette en ny vedligeholdelsesstatusberegning.</span><span class="sxs-lookup"><span data-stu-id="179e5-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="179e5-119">De resultater, der vises i **Vedligeholdelsesstatus**, omfatter kun vedligeholdelsesanmodninger og arbejdsordrer, der har en faktisk startdato og -klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="179e5-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="179e5-120">Slutdato og -klokkeslæt kan være tomt.</span><span class="sxs-lookup"><span data-stu-id="179e5-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="179e5-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="179e5-121">Example 1</span></span>

<span data-ttu-id="179e5-122">I nedenstående skærmbillede er knapperne **År** og **Måned** aktiveret.</span><span class="sxs-lookup"><span data-stu-id="179e5-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="179e5-123">Når disse indstillinger for **Sammenlæg pr.** er valgt, får du et generelt overblik på månedlig basis af arbejdsbyrde og gennemløb i forbindelse med vedligeholdelsesanmodninger og arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="179e5-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Eksempel på månedlig arbejdsbyrde](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="179e5-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="179e5-125">Example 2</span></span>

<span data-ttu-id="179e5-126">I skærmbilledet nedenfor er der tilføjet oplysninger om arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="179e5-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="179e5-127">Nu er det muligt at sammenligne arbejdsbyrder og gennemløb på tværs af arbejdssteder, som kan repræsentere geografiske placeringer, fabrikker eller arbejdsområder.</span><span class="sxs-lookup"><span data-stu-id="179e5-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Eksempel på månedlig arbejdsbyrde med arbejdssteder](media/14-controlling-and-reporting.png)

