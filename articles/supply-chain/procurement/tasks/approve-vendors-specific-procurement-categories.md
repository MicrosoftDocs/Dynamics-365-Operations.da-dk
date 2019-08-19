---
title: Godkende kreditorer til specifikke indkøbskategorier
description: Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836330"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="d4d9b-103">Godkende kreditorer til specifikke indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="d4d9b-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4d9b-104">Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="d4d9b-105">Denne fremgangsmåde viser, hvordan du kan angive, at en leverandør er godkendt eller foretrukket for en bestemt indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="d4d9b-106">Denne opgave vil normalt udføres af en professionel indkøb.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="d4d9b-107">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="d4d9b-108">Gå til Indkøb og forsyning > Kreditorer > Alle kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d4d9b-109">Vælg den kreditor, du vil angive som en godkendt eller foretrukken leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="d4d9b-110">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="d4d9b-111">Klik på Kategorier.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-111">Click Categories.</span></span>
5. <span data-ttu-id="d4d9b-112">Klik på Tilføj kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-112">Click Add category.</span></span>
6. <span data-ttu-id="d4d9b-113">Vælg KONTOR OG SKRIVEBORDSTILBEHØR (KONTOR OG SKRIVEBORDSTILBEHØR) i feltet Kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="d4d9b-114">Vælg 'Foretrukket' i feltet Status for kreditorkategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="d4d9b-115">Det er muligt at angive mere end én foretrukket leverandør til en kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="d4d9b-116">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-116">Click Save.</span></span>
9. <span data-ttu-id="d4d9b-117">Gå til Indkøb og forsyning > Indkøbskategorier.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="d4d9b-118">Vælg 'FIRMAS INDKØBSKATEGORIER\KONTOR OG SKRIVEBORDSTILBEHØR i træet.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="d4d9b-119">Vis sektionen Kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="d4d9b-120">Kontroller, om den leverandør, du har valgt, vises som en foretrukket leverandør for kategorien Kontor og skrivebordstilbehør.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="d4d9b-121">Hvis du kører denne procedure som en opgaveguide, skal du muligvis klikke på knappen Lås op for at kunne rulle ned til listen over kreditorer.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="d4d9b-122">Det er også muligt at tilføje foretrukne og godkendte leverandører på denne side.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="d4d9b-123">Udvid 'KONTOR OG SKRIVEBORDSTILBEHØR' i træet.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="d4d9b-124">Vælg 'Saks' i træet.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="d4d9b-125">Vælg Nej i feltet Arv kreditorer fra overordnet kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="d4d9b-126">Vælg Ja i feltet Arv kreditorer fra overordnet kategori.</span><span class="sxs-lookup"><span data-stu-id="d4d9b-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

