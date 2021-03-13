---
title: Oprette forbrugsrapporter
description: Dette emne forklarer, hvordan du opretter forbrugsrapporter i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e32924c71fd221caee4a7f413908120014ec8c5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022527"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="b365c-103">Oprette forbrugsrapporter</span><span class="sxs-lookup"><span data-stu-id="b365c-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b365c-104">Når du har oprettet og bogført forbrugsregistreringer på arbejdsordrer i aktivstyring, er der to rapporter tilgængelige til visning af detaljer om forbrug.</span><span class="sxs-lookup"><span data-stu-id="b365c-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="b365c-105">Forbrugsrapport over aktiv</span><span class="sxs-lookup"><span data-stu-id="b365c-105">Asset consumption report</span></span>

<span data-ttu-id="b365c-106">Når du har bogført forbrug på arbejdsordrer, kan du udskrive en rapport over aktivforbrug.</span><span class="sxs-lookup"><span data-stu-id="b365c-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="b365c-107">Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på aktiver.</span><span class="sxs-lookup"><span data-stu-id="b365c-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="b365c-108">Klik på **Styring af aktiver** > **Rapporter** > **Aktiver** > **Aktivforbrug**.</span><span class="sxs-lookup"><span data-stu-id="b365c-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="b365c-109">Vælg i dialogboksen **Aktivforbrug** de parametre og det detaljeringsniveau, du vil have vist, ved at vælge **Ja** på de relevante til/fra-knapper, og indsæt et arbejdssted i afsnittet **Vis**.</span><span class="sxs-lookup"><span data-stu-id="b365c-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="b365c-110">Du kan bruge feltet **Niveauer** til at angive, hvor detaljerede aktivlinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="b365c-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="b365c-111">Hvis du f.eks. indtaster tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle aktiver for et arbejdssted på det øverste niveau, og derfor kan timerne på en linje være opsummeret fra arbejdssteder, der findes på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="b365c-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="b365c-112">Hvis du indtaster tallet "0" i feltet **Niveauer**, kan du se et detaljeret resultat, der viser alle aktiver på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="b365c-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="b365c-113">Vælg **Ja** på til/fra-knappen **Sum på alle underaktiver** for at få vist summen for hvert underaktiv i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="b365c-114">Vælg et datointerval i sektionen **Datoer**.</span><span class="sxs-lookup"><span data-stu-id="b365c-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="b365c-115">I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.</span><span class="sxs-lookup"><span data-stu-id="b365c-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="b365c-116">Hvis det er nødvendigt, kan du vælge de specifikke aktiver, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="b365c-117">Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de aktiver, der skal medtages i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="b365c-118">Klik på **OK** for at oprette rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="b365c-119">Forbrugsrapport for arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="b365c-119">Work order consumption report</span></span>

<span data-ttu-id="b365c-120">Når du har bogført forbrug på arbejdsordrer, kan du udskrive en forbrugsrapport for arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b365c-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="b365c-121">Rapporten viser timer, timeomkostninger, vareomkostninger og udgifter, der er bogført på arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b365c-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="b365c-122">Klik på **Styring af aktiver** > **Rapporter** > **Arbejdsordrer** > **Forbrug af arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="b365c-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="b365c-123">Vælg i dialogboksen **Forbrug af arbejdsordre** de parametre, du vil medtage i rapporten, ved at vælge **Ja** i de relevante til/fra-knapper i sektionen **Vis**.</span><span class="sxs-lookup"><span data-stu-id="b365c-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="b365c-124">Vælg et datointerval i sektionen **Datoer**.</span><span class="sxs-lookup"><span data-stu-id="b365c-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="b365c-125">I oversigtspanelet **Destination** skal du vælge, om du vil have vist rapporten på skærmen, udskrive den eller gemme den som en fil eller mail.</span><span class="sxs-lookup"><span data-stu-id="b365c-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="b365c-126">Hvis det er nødvendigt, kan du vælge de specifikke arbejdsordrer, der skal vises i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="b365c-127">Klik på **Filter** i oversigtspanelet **Poster, der skal indgå**, og tilføj de arbejdsordrer, der skal medtages i rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="b365c-128">Klik på **OK** for at oprette rapporten.</span><span class="sxs-lookup"><span data-stu-id="b365c-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="b365c-129">Du kan også oprette en [arbejdsordrerapport](../work-orders/work-order-report.md), der indeholder flere oplysninger om arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="b365c-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

