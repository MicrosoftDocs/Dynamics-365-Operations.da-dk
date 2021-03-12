---
title: Lastskabeloner
description: Dette emne beskriver, hvordan du kan konfigurere lastskabeloner, og hvordan du knytter en lastskabelon til en ny last.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646372"
---
# <a name="load-templates"></a><span data-ttu-id="573f5-103">Lastskabeloner</span><span class="sxs-lookup"><span data-stu-id="573f5-103">Load templates</span></span>

<span data-ttu-id="573f5-104">Når du opretter en ny last, kan du tildele en lastskabelon.</span><span class="sxs-lookup"><span data-stu-id="573f5-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="573f5-105">Lastskabelonen indeholder oplysninger om udstyr og om måleenheder, f.eks. højde, bredde, dybde og volumen for lasten.</span><span class="sxs-lookup"><span data-stu-id="573f5-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="573f5-106">Dette emne beskriver, hvordan du kan konfigurere lastskabeloner, og hvordan du knytter en lastskabelon til en ny last.</span><span class="sxs-lookup"><span data-stu-id="573f5-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="573f5-107">Konfigurere en lastskabelon</span><span class="sxs-lookup"><span data-stu-id="573f5-107">Set up a load template</span></span>

1. <span data-ttu-id="573f5-108">Gå til **Transportstyring \> Konfiguration \> Lastopbygning \> Lastskabelon**.</span><span class="sxs-lookup"><span data-stu-id="573f5-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="573f5-109">Vælg **Ny** i handlingsruden for at tilføje en ny skabelon eller **Rediger** for at redigere en eksisterende skabelon.</span><span class="sxs-lookup"><span data-stu-id="573f5-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="573f5-110">Angiv følgende felter i rækken for den nye eller den eksisterende skabelon:</span><span class="sxs-lookup"><span data-stu-id="573f5-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="573f5-111">**Id for lastskabelon** – Angiv et entydigt id for lastskabelonen.</span><span class="sxs-lookup"><span data-stu-id="573f5-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="573f5-112">**Udstyr** – Vælg det udstyr, der skal bruges til levering af lasten.</span><span class="sxs-lookup"><span data-stu-id="573f5-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="573f5-113">**Lasthøjde**, **Lastbredde** og **Lastdybde** – Angiv dimensionerne af lasten.</span><span class="sxs-lookup"><span data-stu-id="573f5-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="573f5-114">**Maks. tilladt lastvolumen** og **Maks. tilladt lastvægt** – Angiv den maksimale tilladte volumen og vægt for lasten.</span><span class="sxs-lookup"><span data-stu-id="573f5-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="573f5-115">**Maksimalt tilladte bruttovægt** – Angiv den maksimalt tilladte bruttovægt for lasten.</span><span class="sxs-lookup"><span data-stu-id="573f5-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="573f5-116">Lastens bruttovægt er inklusive både dens taravægt og dens lastvægt.</span><span class="sxs-lookup"><span data-stu-id="573f5-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="573f5-117">**Maksimalt antal tilladte fragtdele** – Angiv det maksimale antal fragtdele, som lasten kan indeholde.</span><span class="sxs-lookup"><span data-stu-id="573f5-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="573f5-118">**Udfør stabling af last på gulv** – Markér dette afkrydsningsfelt for at bruge gulvlast.</span><span class="sxs-lookup"><span data-stu-id="573f5-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="573f5-119">I et scenarie med gulvlastning stables kasser fra gulv til loft og væg til væg inden i containeren for at maksimere den indvendige kapacitet.</span><span class="sxs-lookup"><span data-stu-id="573f5-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="573f5-120">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="573f5-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="573f5-121">Knytte en lastskabelon til en ny last</span><span class="sxs-lookup"><span data-stu-id="573f5-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="573f5-122">Gå til **Transportstyring \> Planlægning \> Lastplanlægningspanel**.</span><span class="sxs-lookup"><span data-stu-id="573f5-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="573f5-123">I den øverste del af siden skal du vælge en af følgende faner afhængigt af, hvilken type kildedokument du opretter en last for: **Forsendelser**, **Salgslinjer**, **Overflytningslinjer** eller **Indkøbsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="573f5-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="573f5-124">Vælg det specifikke dokument, som du vil planlægge lasten for.</span><span class="sxs-lookup"><span data-stu-id="573f5-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="573f5-125">I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**.</span><span class="sxs-lookup"><span data-stu-id="573f5-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="573f5-126">I dialogboksen **Lastskabelon** skal du i feltet **Lastskabelons-id** vælge den skabelon, der skal anvendes.</span><span class="sxs-lookup"><span data-stu-id="573f5-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="573f5-127">Vælg **OK** for at anvende skabelonen.</span><span class="sxs-lookup"><span data-stu-id="573f5-127">Select **OK** to apply the template.</span></span>