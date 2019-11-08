---
title: Hvor er varen brugt?
description: Dette emne forklarer, hvordan du får en oversigt over, hvor en vare bruges i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 511108e689c10e27a42253d95b02e5394f9eb713
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652350"
---
# <a name="item-where-used"></a><span data-ttu-id="2b917-103">Hvor er varen brugt?</span><span class="sxs-lookup"><span data-stu-id="2b917-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2b917-104">Du kan foretage en beregning for en bestemt vare for at få en oversigt over, hvor i Styring af aktiver varen er brugt.</span><span class="sxs-lookup"><span data-stu-id="2b917-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="2b917-105">Resultaterne viser den kontekst, som varen er blevet brugt i, i løbet af dens levetid.</span><span class="sxs-lookup"><span data-stu-id="2b917-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="2b917-106">Siden **Hvor er varen brugt?** kan åbnes fra hovedmenuen i Styring af aktiver, og den kan også åbnes fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="2b917-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="2b917-107">Aktivstykliste</span><span class="sxs-lookup"><span data-stu-id="2b917-107">Asset BOM</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="2b917-108">Reservedele i aktivtypestandarder</span><span class="sxs-lookup"><span data-stu-id="2b917-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

- [<span data-ttu-id="2b917-109">Varebudget på standardbudget for vedligeholdelsesjobtype</span><span class="sxs-lookup"><span data-stu-id="2b917-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="2b917-110">Vedligeholdelsesprognose for arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="2b917-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="2b917-111">Indkøbsrekvisition for arbejdsordre</span><span class="sxs-lookup"><span data-stu-id="2b917-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="2b917-112">Arbejdsordreindkøb</span><span class="sxs-lookup"><span data-stu-id="2b917-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="2b917-113">Oprette en beregning af, hvor en vare er brugt</span><span class="sxs-lookup"><span data-stu-id="2b917-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="2b917-114">Klik på **Styring af aktiver** > **Forespørgsler** > **Hvor er varen brugt?**, eller vælg knappen **Hvor er varen brugt?** på en af de ovennævnte sider.</span><span class="sxs-lookup"><span data-stu-id="2b917-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="2b917-115">Vælg i dialogboksen **Hvor er varen brugt?** den vare, der skal foretages en beregning for, i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="2b917-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="2b917-116">Du kan bruge feltet **Niveau** til at angive, hvor detaljerede varelinjerne skal være i forbindelse med arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="2b917-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="2b917-117">Hvis du f.eks. indsætter tallet "1" i feltet, og du har en arbejdsstedsstruktur med flere niveauer, vises alle varelinjer for et arbejdssted på det øverste niveau.</span><span class="sxs-lookup"><span data-stu-id="2b917-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="2b917-118">Derfor kan relationen/antallet på en linje være opsummeret fra arbejdssteder, der er placeret på et lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="2b917-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="2b917-119">Hvis du indsætter tallet "0" i feltet **Niveau**, kan du se et detaljeret resultat, der viser alle varelinjer på alle de arbejdsstedsniveauer, de er relateret til.</span><span class="sxs-lookup"><span data-stu-id="2b917-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2b917-120">Vælg "Ja" på de knapper i sektionen **Medtag**, du vil medtage i beregningen.</span><span class="sxs-lookup"><span data-stu-id="2b917-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="2b917-121">Klik på **OK** for at starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="2b917-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="2b917-122">Under fanen **Hvor er varen brugt?** skal vælge de relevante **Sammenlæg pr.**-knapper for at få vist det nødvendige detaljeringsniveau i beregningen.</span><span class="sxs-lookup"><span data-stu-id="2b917-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2b917-123">De valgte **Sammenlæg pr.**-knapper er fremhævet.</span><span class="sxs-lookup"><span data-stu-id="2b917-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="2b917-124">Klik på en knap for at aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="2b917-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="2b917-125">Hvis du vil have vist de dimensioner, der vedrører varen, skal du klikke på **Vis dimensioner** og vælge de dimensioner, der skal vises.</span><span class="sxs-lookup"><span data-stu-id="2b917-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="2b917-126">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b917-126">Example</span></span>

<span data-ttu-id="2b917-127">På nedenstående skærmbillede kan du se et eksempel på en beregning af Hvor er varen brugt? for varenummer "1000".</span><span class="sxs-lookup"><span data-stu-id="2b917-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Eksempel på beregning af, hvor en vare er brugt](media/12-controlling-and-reporting.png)

