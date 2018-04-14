--- 
title: "Genklassificer anlægsaktiver"
description: "Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 77497bc8cf50bb33c7e1fe1f9ea72ed0f1f3876e
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="e5536-103">Genklassificer anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="e5536-103">Reclassify fixed assets</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5536-104">Hvis du vil genklassificere et anlægsaktiv, skal du overføre det til en ny anlægsaktivgruppe eller tildele det et nyt anlægsaktivnummer i samme gruppe.</span><span class="sxs-lookup"><span data-stu-id="e5536-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="e5536-105">Når et anlægsaktiv genklassificeres:</span><span class="sxs-lookup"><span data-stu-id="e5536-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="e5536-106">• Alle værdimodeller for det eksisterende anlægsaktiv oprettes for det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="e5536-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="e5536-107">Oplysninger, der var oprettet for det oprindelige anlægsaktiv, kopieres til det nye anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="e5536-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="e5536-108">Status for det oprindelige anlægsaktivs værdimodeller er Lukket.</span><span class="sxs-lookup"><span data-stu-id="e5536-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="e5536-109">• Det nye anlægsaktivs nye værdimodeller indeholder datoen for genklassificeringen i feltet Anskaffelsesdato.</span><span class="sxs-lookup"><span data-stu-id="e5536-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="e5536-110">Datoen i feltet Afskrivning kopieres fra de oprindelige aktivoplysninger.</span><span class="sxs-lookup"><span data-stu-id="e5536-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="e5536-111">Hvis afskrivningen allerede er startet, vises datoen for genklassificeringen i feltet Dato, hvor afskrivning sidst blev udført.</span><span class="sxs-lookup"><span data-stu-id="e5536-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="e5536-112">• De eksisterende anlægsaktivposteringer for det oprindelige anlægsaktiv annulleres og oprettes for det nye anlægsaktiv igen.</span><span class="sxs-lookup"><span data-stu-id="e5536-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="e5536-113">Gå til Anlægsaktiver > Periodiske opgaver > Genklassificering.</span><span class="sxs-lookup"><span data-stu-id="e5536-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="e5536-114">I feltet Anlægsaktivgruppe skal du vælge den gruppe, som skal genklassificeres.</span><span class="sxs-lookup"><span data-stu-id="e5536-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="e5536-115">Vælg det anlægsaktiv, der skal genklassificeres, i feltet Nummer på anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="e5536-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="e5536-116">Vælg en gruppe, som det nye anlægsaktiv skal overføre til, i feltet Ny anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5536-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="e5536-117">Hvis den nye anlægsaktivgruppe er knyttet til en nummerserie, opdateres feltet Nyt nummer på anlægsaktivet med nummeret fra nummerserien for den nye anlægsaktivgruppe.</span><span class="sxs-lookup"><span data-stu-id="e5536-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="e5536-118">Ellers opdateres feltet Nyt nummer på anlægsaktivet med nummeret fra nummerserien, der er konfigureret på siden Parametre for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="e5536-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="e5536-119">Hvis der ikke er konfigureret en nummerserie på siden Parametre for anlægsaktiver, skal du angive et tal i feltet Nyt nummer på anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="e5536-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="e5536-120">Indtast en dato i feltet Dato for genklassificering.</span><span class="sxs-lookup"><span data-stu-id="e5536-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="e5536-121">Indtast eller vælg en værdi i feltet Bilagsserie.</span><span class="sxs-lookup"><span data-stu-id="e5536-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="e5536-122">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e5536-122">Click OK.</span></span>


