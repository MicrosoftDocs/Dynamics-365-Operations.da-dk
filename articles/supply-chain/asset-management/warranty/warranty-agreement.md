---
title: Garantiaftaler
description: I dette emne beskrives garantiaftaler i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7080af2059c9c9bcdd11ca0ee9c5e339cef69302
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021498"
---
# <a name="warranty-agreements"></a><span data-ttu-id="1fccb-103">Garantiaftaler</span><span class="sxs-lookup"><span data-stu-id="1fccb-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="1fccb-104">I Styring af aktiver kan du oprette garantibetingelser, der kan knyttes til et aktiv eller en aktivtype.</span><span class="sxs-lookup"><span data-stu-id="1fccb-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="1fccb-105">Der oprettes garantibetingelser for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="1fccb-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="1fccb-106">Der kan oprettes garanti, som giver fuld dækning eller en delvis dækning, og du kan konfigurere betingelser, der er relateret til timer, udgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="1fccb-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="1fccb-107">Det første trin er at oprette eventuelle leverandørgarantiaftaler, som du har for dit udstyr.</span><span class="sxs-lookup"><span data-stu-id="1fccb-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="1fccb-108">Derefter kan du knytte garantiaftaler til aktiver eller aktivtyper.</span><span class="sxs-lookup"><span data-stu-id="1fccb-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="1fccb-109">Leverandørgarantiaftaler bruges kun til orientering.</span><span class="sxs-lookup"><span data-stu-id="1fccb-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="1fccb-110">Hvis der er oprettet en leverandørgaranti på et aktiv, kan du se garantidækningsperioden for aktivet.</span><span class="sxs-lookup"><span data-stu-id="1fccb-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="1fccb-111">Oprette en garantiaftale</span><span class="sxs-lookup"><span data-stu-id="1fccb-111">Create a warranty agreement</span></span>

<span data-ttu-id="1fccb-112">En garantiaftale kan omfatte flere aftalelinjer, der dækker garantien for arbejdstimer, udgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="1fccb-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="1fccb-113">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Garanti**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="1fccb-114">Vælg **Ny** for at oprette et produkt.</span><span class="sxs-lookup"><span data-stu-id="1fccb-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="1fccb-115">Angiv et garanti-id i feltet **Garanti**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="1fccb-116">Angiv en beskrivelse i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="1fccb-117">I oversigtspanelet **Detaljer** indeholder feltet **Aktiver** antallet af aktive aktiver, der bruger garantiaftalen.</span><span class="sxs-lookup"><span data-stu-id="1fccb-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="1fccb-118">Udfør følgende trin i oversigtspanelet **Garantilinjer** for at tilføje linjer, der skal medtages i en garantiaftale:</span><span class="sxs-lookup"><span data-stu-id="1fccb-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="1fccb-119">Vælg **Tilføj linje** for at føje en ny betingelse til garantien.</span><span class="sxs-lookup"><span data-stu-id="1fccb-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="1fccb-120">Der indsættes automatisk et fortløbende linjenummer i feltet **Linje**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="1fccb-121">Vælg garantiperiodetypen i feltet **Periode**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="1fccb-122">Angiv et tal i feltet **Interval**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="1fccb-123">Dette felt definerer antallet af perioder, som garantien skal være gældende for.</span><span class="sxs-lookup"><span data-stu-id="1fccb-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="1fccb-124">Angiv dækningsprocenten for garantilinjen i feltet **Procent**.</span><span class="sxs-lookup"><span data-stu-id="1fccb-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="1fccb-125">Procenten angiver, hvor meget der dækkes af firmaet.</span><span class="sxs-lookup"><span data-stu-id="1fccb-125">The percentage indicates how much is covered by your company.</span></span>

![Garantiside](media/01-warranty.png)
