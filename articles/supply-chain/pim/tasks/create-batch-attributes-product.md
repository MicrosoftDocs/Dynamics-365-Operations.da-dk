--- 
title: Oprette batchattributter for et produkt
description: "Denne fremgangsmåde viser, hvordan du opretter en batchattribut, tildeler standardværdiintervaller og medtager attributten i en gruppe."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5694ac4ec47b446c19681bfb5c6b07ff82f4575f
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="3ab59-103">Oprette batchattributter for et produkt</span><span class="sxs-lookup"><span data-stu-id="3ab59-103">Create batch attributes for a product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ab59-104">Denne fremgangsmåde viser, hvordan du opretter en batchattribut, tildeler standardværdiintervaller og medtager attributten i en gruppe.</span><span class="sxs-lookup"><span data-stu-id="3ab59-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="3ab59-105">Det demodatafirma, der bruges til at oprette denne procedure, er USP2-firmaet.</span><span class="sxs-lookup"><span data-stu-id="3ab59-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="3ab59-106">Gå til Lagerstyring > Opsætning > Batch > Batchattributter.</span><span class="sxs-lookup"><span data-stu-id="3ab59-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="3ab59-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3ab59-107">Click New.</span></span>
3. <span data-ttu-id="3ab59-108">Skriv en værdi i feltet Attribut.</span><span class="sxs-lookup"><span data-stu-id="3ab59-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="3ab59-109">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3ab59-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3ab59-110">Vælg "Del" i feltet Attributtype.</span><span class="sxs-lookup"><span data-stu-id="3ab59-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="3ab59-111">Denne procedure bruger typen Del til at aktivere decimalværdier.</span><span class="sxs-lookup"><span data-stu-id="3ab59-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="3ab59-112">Du kan vælge andre attributtyper.</span><span class="sxs-lookup"><span data-stu-id="3ab59-112">You can select other attribute types.</span></span> <span data-ttu-id="3ab59-113">Hvis du vælger typen Fasttekst, skal du indtaste værdier i fasttekstlisten, før du kan angive en værdi i feltet Mål.</span><span class="sxs-lookup"><span data-stu-id="3ab59-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="3ab59-114">Angiv et tal i feltet Minimum.</span><span class="sxs-lookup"><span data-stu-id="3ab59-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="3ab59-115">Angiv et tal i feltet Maksimum.</span><span class="sxs-lookup"><span data-stu-id="3ab59-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="3ab59-116">Angiv et tal i feltet Multiplum.</span><span class="sxs-lookup"><span data-stu-id="3ab59-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="3ab59-117">Skriv en værdi i feltet Mål.</span><span class="sxs-lookup"><span data-stu-id="3ab59-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="3ab59-118">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3ab59-118">Click Save.</span></span>
11. <span data-ttu-id="3ab59-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3ab59-119">Close the page.</span></span>
12. <span data-ttu-id="3ab59-120">Gå til Lagerstyring > Opsætning > Batch > Batchattributgrupper.</span><span class="sxs-lookup"><span data-stu-id="3ab59-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="3ab59-121">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3ab59-121">Click New.</span></span>
14. <span data-ttu-id="3ab59-122">Indtast en værdi i feltet Attributgruppe.</span><span class="sxs-lookup"><span data-stu-id="3ab59-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="3ab59-123">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3ab59-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="3ab59-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3ab59-124">Click Save.</span></span>
17. <span data-ttu-id="3ab59-125">Klik på Gruppeattributter.</span><span class="sxs-lookup"><span data-stu-id="3ab59-125">Click Group attributes.</span></span>
18. <span data-ttu-id="3ab59-126">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="3ab59-126">Click New.</span></span>
19. <span data-ttu-id="3ab59-127">Klik på rullelisten i feltet Attribut for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="3ab59-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3ab59-128">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3ab59-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="3ab59-129">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3ab59-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3ab59-130">En attribut kan medtages i en af grupperne.</span><span class="sxs-lookup"><span data-stu-id="3ab59-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="3ab59-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="3ab59-131">Click Save.</span></span>
23. <span data-ttu-id="3ab59-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3ab59-132">Close the page.</span></span>


