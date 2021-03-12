---
title: Produktejere
description: Dette emne indeholder oplysninger om produktejere. En produktejer er en gruppe af brugere, der er ansvarlig for bestemte produkter. Det er kun medlemmer af gruppen, der kan frigive disse produkter. Produktejeren kan også bruges i godkendelsesarbejdsprocessen.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967327"
---
# <a name="product-owners"></a><span data-ttu-id="33ba0-106">Produktejere</span><span class="sxs-lookup"><span data-stu-id="33ba0-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33ba0-107">Produktejeren er en gruppe af brugere, der er ansvarlig for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="33ba0-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="33ba0-108">Når en produktejergruppe tildeles et produkt, er det kun medlemmerne af denne gruppe, der kan frigive produktet.</span><span class="sxs-lookup"><span data-stu-id="33ba0-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="33ba0-109">Produktejeren kan også bruges i godkendelsesarbejdsprocessen i styring af tekniske ændringer.</span><span class="sxs-lookup"><span data-stu-id="33ba0-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="33ba0-110">Produktejere er globale indstillinger.</span><span class="sxs-lookup"><span data-stu-id="33ba0-110">Product owners are global settings.</span></span> <span data-ttu-id="33ba0-111">Derfor er de tilgængelige for alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="33ba0-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="33ba0-112">Oprette en produktejergruppe</span><span class="sxs-lookup"><span data-stu-id="33ba0-112">Create a product owner group</span></span>

<span data-ttu-id="33ba0-113">Hvis du vil oprette en produktejergruppe og føje medlemmer til den, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="33ba0-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="33ba0-114">Gå til **Teknisk ændringsstyring \> Konfiguration \> Produktejere**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="33ba0-115">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="33ba0-116">Angiv et sigende gruppenavn i feltet **Produktejer**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="33ba0-117">Indtast en beskrivelse af gruppen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="33ba0-118">Tilføj de arbejdere, der skal være medlemmer af gruppen, i oversigtspanelet **Medlemmer**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="33ba0-119">Tildele en produktejer til et produkt</span><span class="sxs-lookup"><span data-stu-id="33ba0-119">Assign a product owner to a product</span></span>

<span data-ttu-id="33ba0-120">Følg disse trin, hvis du vil tildele en produktejer til et produkt.</span><span class="sxs-lookup"><span data-stu-id="33ba0-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="33ba0-121">Åbn siden **Produktdetaljer** for det relevante produkt eller produktmasteren.</span><span class="sxs-lookup"><span data-stu-id="33ba0-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="33ba0-122">I oversigtspanelet **Generelt** skal du angive navnet på den relevante produktejergruppe i feltet **Produktejer**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="33ba0-123">Mens en produktejer tildeles et produkt, kan kun medlemmerne af produktejergruppen redigere indstillingen for **Produktejer**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="33ba0-124">Produktets ejer er også synlig på siden **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="33ba0-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="33ba0-125">Produktejere og produktfrigivelser</span><span class="sxs-lookup"><span data-stu-id="33ba0-125">Product owners and product releases</span></span>

<span data-ttu-id="33ba0-126">Kun brugere fra et produkts produktejergruppe kan frigive produktet.</span><span class="sxs-lookup"><span data-stu-id="33ba0-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="33ba0-127">Der er dog en undtagelse, når produktet er en underordnet vare, og dets overordnede er frigivet af ejeren af dets overordnede.</span><span class="sxs-lookup"><span data-stu-id="33ba0-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="33ba0-128">Hvis produktet er en del af styklisten for et andet produkt, kontrollerer systemet ikke produktejeren af de enkelte varer på styklisten.</span><span class="sxs-lookup"><span data-stu-id="33ba0-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="33ba0-129">Det kontrollerer kun produktejeren for den overordnede vare.</span><span class="sxs-lookup"><span data-stu-id="33ba0-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="33ba0-130">Produkt X tildeles f.eks. produktejergruppen *Design skabe*.</span><span class="sxs-lookup"><span data-stu-id="33ba0-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="33ba0-131">Produkt X er også en del af styklisten for produkt Y, som er knyttet til produktejergruppen *Design højttalere*.</span><span class="sxs-lookup"><span data-stu-id="33ba0-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="33ba0-132">Hvis en bruger fra *Design højttalere*-produktejergruppen frigiver produkt Y og dets stykliste, frigives produkt X sammen med produkt y.</span><span class="sxs-lookup"><span data-stu-id="33ba0-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="33ba0-133">Produktejere og godkendelser</span><span class="sxs-lookup"><span data-stu-id="33ba0-133">Product owners and approvals</span></span>

<span data-ttu-id="33ba0-134">Da produktejere ved, om bestemte tekniske ændringer vil drage nytte af deres produkter, giver det ofte mening at inkludere dem som en del af godkendelsesprocessen i styring af tekniske ændringer.</span><span class="sxs-lookup"><span data-stu-id="33ba0-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="33ba0-135">Du kan implementere denne fremgangsmåde ved at konfigurere produktejerne som deltagerudbydere i arbejdsprocesser, der bruges til styring af tekniske ændringer.</span><span class="sxs-lookup"><span data-stu-id="33ba0-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="33ba0-136">Systemet tildeler derefter godkendelsesopgaver i arbejdsprocesserne baseret på produkterne i tekniske ændringsanmodninger og tekniske ændringsordrer.</span><span class="sxs-lookup"><span data-stu-id="33ba0-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="33ba0-137">Yderligere oplysninger finder du i [Administrere ændringer af tekniske produkter](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="33ba0-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
