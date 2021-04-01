---
title: Styring af arbejdstimer
description: I dette emne beskrives styring af arbejdstimer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 482bee9dba22763a065c8aca93745f53f06f99be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253704"
---
# <a name="work-hour-control"></a><span data-ttu-id="5f485-103">Styring af arbejdstimer</span><span class="sxs-lookup"><span data-stu-id="5f485-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5f485-104">I Styring af arbejdstimer kan du beregne timer for at få et overblik over de faktiske timer i forhold til budgetterede timer på anlægsaktiver, arbejdssteder eller arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f485-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="5f485-105">De faktiske timer er baseret på bogførte transaktioner.</span><span class="sxs-lookup"><span data-stu-id="5f485-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="5f485-106">Styring af arbejdstimer for aktiver, arbejdssteder og arbejdsordrer</span><span class="sxs-lookup"><span data-stu-id="5f485-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="5f485-107">De beregninger, der foretages for aktiver, arbejdssteder og arbejdsordrer, er næsten identiske.</span><span class="sxs-lookup"><span data-stu-id="5f485-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="5f485-108">Den eneste forskel er, at for aktiver og arbejdssteder kan du også medtage underaktiver og underordnede arbejdssteder i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5f485-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="5f485-109">Datoen er den transaktionsdato, da registreringen blev foretaget.</span><span class="sxs-lookup"><span data-stu-id="5f485-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="5f485-110">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Styring af aktivtimer** eller **Timestyring for arbejdssted** eller **Styring af aktiver** > **Forespørgsler** > **Arbejdsordrer** > **Styring arbejdsordretimer**.</span><span class="sxs-lookup"><span data-stu-id="5f485-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="5f485-111">I dialogboksen **Styring af aktivtimer**.</span><span class="sxs-lookup"><span data-stu-id="5f485-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="5f485-112">Vælg en periode, der skal beregnes, i felterne **Fra dato** og **Til dato**, i **Styring af aktivtimer** / **Timestyring for arbejdssted** / **Styring arbejdsordretimer**.</span><span class="sxs-lookup"><span data-stu-id="5f485-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="5f485-113">Hvis det er nødvendigt, skal du vælge en **Økonomisk dimensionsopsætning**, der skal medtages i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5f485-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="5f485-114">Vælg "Ja" på til/fra-knappen **Spring over nul**, hvis du ikke vil have vist resultater, der indeholder nul timer.</span><span class="sxs-lookup"><span data-stu-id="5f485-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="5f485-115">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede timestyringslinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="5f485-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="5f485-116">Hvis du f.eks. indsætter tallet "1" i feltet, og du har et arbejdsstedshierarki med flere niveauer, vises alle timestyringslinjer for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="5f485-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="5f485-117">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle timestyringslinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="5f485-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="5f485-118">Vælg "Ja" i til/fra-knappen **Medtag underaktiver** for at få vist omkostninger, der er relateret til underaktiver som separate linjer.</span><span class="sxs-lookup"><span data-stu-id="5f485-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="5f485-119">Hvis du vil begrænse søgningen, kan du vælge bestemte aktiver / arbejdssteder / arbejdsordrer i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="5f485-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="5f485-120">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="5f485-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="5f485-121">Klik på **Sammenlæg pr.**-knapperne på siden **Styring af aktivtimer** for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="5f485-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5f485-122">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="5f485-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5f485-123">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="5f485-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="5f485-124">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5f485-124">Example</span></span>

<span data-ttu-id="5f485-125">I skærmbilledet herunder vises et eksempel på en beregning af **Styring af aktivtimer**.</span><span class="sxs-lookup"><span data-stu-id="5f485-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="5f485-126">I feltet **Oprindeligt budget** vises budgetterede timer fra arbejdsordrebudgettet.</span><span class="sxs-lookup"><span data-stu-id="5f485-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="5f485-127">I feltet **Faktiske timer** vises bogførte timer på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f485-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="5f485-128">I feltet **Bindende timer** vises det samlede antal timer, som dit firma er bundet til i forbindelse med arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f485-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Eksempel på beregning af Styring af aktivtimer](media/04-controlling-and-reporting.png)

<span data-ttu-id="5f485-130">Du kan også foretage en timeberegning ved at vælge flere aktiver i **Alle aktiver** eller **Aktive aktiver**.</span><span class="sxs-lookup"><span data-stu-id="5f485-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="5f485-131">Derefter skal du klikke på knappen **Timestyring** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="5f485-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="5f485-132">De valgte anlægsaktiver indsættes automatisk i feltet **Aktiv** i oversigtspanelet **Poster, der skal indgå**.</span><span class="sxs-lookup"><span data-stu-id="5f485-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="5f485-133">Klik på **OK** i dialogboksen **Styring af aktivtimer**, hvorefter beregningen for de valgte aktiver vises.</span><span class="sxs-lookup"><span data-stu-id="5f485-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="5f485-134">Den samme procedure kan udføres for arbejdssteder i **Alle arbejdssteder** eller **Aktive arbejdssteder** og for arbejdsordrer i **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="5f485-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]