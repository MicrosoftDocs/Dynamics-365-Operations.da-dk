---
title: Godkende kreditorer til specifikke indkøbskategorier
description: Dette emne forklarer, hvordan du kan godkende kreditorer for bestemte indkøbskategorier i Dynamics 365 for Finance and Operations.
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
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
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867143"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="17617-103">Godkende kreditorer til specifikke indkøbskategorier</span><span class="sxs-lookup"><span data-stu-id="17617-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17617-104">Dette emne forklarer, hvordan du kan godkende kreditorer for bestemte indkøbskategorier i Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="17617-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="17617-105">Når en indkøbsrekvisition oprettes, kan det være et krav, at der skal vælges en godkendt eller foretrukken leverandør, afhængigt af hvordan indkøbspolitikkerne er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="17617-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="17617-106">Denne fremgangsmåde viser, hvordan du kan angive, at en leverandør er godkendt eller foretrukket for en bestemt indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="17617-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="17617-107">Denne opgave vil normalt udføres af en professionel indkøb.</span><span class="sxs-lookup"><span data-stu-id="17617-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="17617-108">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="17617-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="17617-109">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Kreditorer > Alle kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="17617-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="17617-110">Vælg den kreditor, du vil angive som en godkendt eller foretrukken leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="17617-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="17617-111">Vælg **Generelt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="17617-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="17617-112">Vælg **Kategorier**.</span><span class="sxs-lookup"><span data-stu-id="17617-112">Select **Categories**.</span></span>
5. <span data-ttu-id="17617-113">Vælg **Tilføj kategori**.</span><span class="sxs-lookup"><span data-stu-id="17617-113">Select **Add category**.</span></span>
6. <span data-ttu-id="17617-114">Vælg **KONTOR OG SKRIVEBORDSTILBEHØR (KONTOR OG SKRIVEBORDSTILBEHØR)** i feltet **Kategori**.</span><span class="sxs-lookup"><span data-stu-id="17617-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="17617-115">Vælg **Foretrukket** i feltet **Status for kreditorkategori**.</span><span class="sxs-lookup"><span data-stu-id="17617-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="17617-116">Det er muligt at angive mere end én foretrukket leverandør til en kategori.</span><span class="sxs-lookup"><span data-stu-id="17617-116">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="17617-117">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="17617-117">Select **Save**.</span></span>
9. <span data-ttu-id="17617-118">Gå i navigationsruden til **Moduler > Indkøb og forsyning > Indkøbskategorier**.</span><span class="sxs-lookup"><span data-stu-id="17617-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="17617-119">Vælg **FIRMAS INDKØBSKATEGORIER\KONTOR OG SKRIVEBORDSTILBEHØR** i træet.</span><span class="sxs-lookup"><span data-stu-id="17617-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="17617-120">Udvid sektionen **Kreditorer**.</span><span class="sxs-lookup"><span data-stu-id="17617-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="17617-121">Kontrollér, om den leverandør, du har valgt, vises som en foretrukken leverandør for kategorien Kontor og skrivebordstilbehør.</span><span class="sxs-lookup"><span data-stu-id="17617-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="17617-122">Hvis du kører denne procedure som en opgaveguide, skal du muligvis vælge knappen **Lås op** for at kunne rulle ned til listen over kreditorer.</span><span class="sxs-lookup"><span data-stu-id="17617-122">If you’re running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="17617-123">Det er også muligt at tilføje foretrukne og godkendte leverandører på denne side.</span><span class="sxs-lookup"><span data-stu-id="17617-123">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="17617-124">Udvid **KONTOR OG SKRIVEBORDSTILBEHØR** i træet, og vælg **Saks**.</span><span class="sxs-lookup"><span data-stu-id="17617-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="17617-125">Vælg **Nej** i feltet **Arv kreditorer fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="17617-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="17617-126">Vælg **Ja** i feltet **Arv kreditorer fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="17617-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

