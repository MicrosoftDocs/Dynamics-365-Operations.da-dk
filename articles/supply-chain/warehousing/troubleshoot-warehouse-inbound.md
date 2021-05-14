---
title: Foretage fejlfinding af indgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920981"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="98e62-103">Foretage fejlfinding af indgående lagerstedsoperationer</span><span class="sxs-lookup"><span data-stu-id="98e62-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98e62-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="98e62-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="98e62-105">Jeg får vist følgende fejlmeddelelse: "Kvalitetsordren %1 er blevet genereret.</span><span class="sxs-lookup"><span data-stu-id="98e62-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="98e62-106">Klyngeprofil blev ikke fundet. Kontrollér din konfiguration."</span><span class="sxs-lookup"><span data-stu-id="98e62-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e62-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="98e62-107">Issue description</span></span>

<span data-ttu-id="98e62-108">Denne fejlmeddelelse er relateret til en modtagelsesproces, hvor kvalitetsstyring (QMS) er slået til.</span><span class="sxs-lookup"><span data-stu-id="98e62-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="98e62-109">Afhængigt af konfigurationerne i dit miljø kan yderligere oplysninger om den transaktion, der genererer fejlmeddelelsen, måske løse problemet.</span><span class="sxs-lookup"><span data-stu-id="98e62-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e62-110">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="98e62-110">Issue resolution</span></span>

<span data-ttu-id="98e62-111">Først skal du gennemse opsætningen for [klyngepluk](set-up-cluster-picking.md) og kontrollere, at dine klyngeprofiler er konfigureret korrekt.</span><span class="sxs-lookup"><span data-stu-id="98e62-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="98e62-112">Du kan ikke bruge et menupunkt til klyngepluk i mobilenheden, medmindre der er konfigureret klyngeprofiler.</span><span class="sxs-lookup"><span data-stu-id="98e62-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="98e62-113">Afhængigt af miljøet skal du muligvis også gennemse andre relaterede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="98e62-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="98e62-114">Modtagelse af blandede id'er fungerer ikke for nogen dispositionskode undtagen Kredit.</span><span class="sxs-lookup"><span data-stu-id="98e62-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e62-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="98e62-115">Issue description</span></span>

<span data-ttu-id="98e62-116">Når **Handling**-feltet for en dispositionskode er sat til *Kredit* eller *Kasseres*, kan du kun bruge menupunktet [Modtagelse af blandede id'er](mixed-license-plate-receiving.md) til at behandle returvarer.</span><span class="sxs-lookup"><span data-stu-id="98e62-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e62-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="98e62-117">Issue resolution</span></span>

<span data-ttu-id="98e62-118">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="98e62-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="98e62-119">Aktuelt er det kun [dispositionskoder](../service-management/set-up-disposition-codes.md), hvor feltet **Handling** er indstillet til *Kredit* eller *Kasseres*, der understøttes til modtagelse af blandede id'er.</span><span class="sxs-lookup"><span data-stu-id="98e62-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="98e62-120">Når jeg kører den periodiske opgave Opdater produktkvitteringer, bekræftes ubekræftede indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="98e62-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e62-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="98e62-121">Issue description</span></span>

<span data-ttu-id="98e62-122">Når du har kørt den periodiske opgave *Opdater produktkvitteringer*, bekræfter systemet automatisk ubekræftede indkøbsordrer, der har lagertransaktionstatus *Registreret*.</span><span class="sxs-lookup"><span data-stu-id="98e62-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e62-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="98e62-123">Issue resolution</span></span>

<span data-ttu-id="98e62-124">En ny funktion til håndtering af indgående last, *Overtilgang af lastantal*, løser dette problem.</span><span class="sxs-lookup"><span data-stu-id="98e62-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="98e62-125">Hvis du aktivere denne funktion, skal du gå til arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner (i deres viste rækkefølge):</span><span class="sxs-lookup"><span data-stu-id="98e62-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="98e62-126">Tilknyt lagertransaktioner med belastning for indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="98e62-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="98e62-127">Overtilgang af lastantal</span><span class="sxs-lookup"><span data-stu-id="98e62-127">Over receipt of load quantities</span></span>

<span data-ttu-id="98e62-128">Du kan finde flere oplysninger under [Bogføre registrerede produktantal i forhold til indkøbsordrer](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="98e62-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="98e62-129">Når jeg registrerer indgående ordrer, modtager jeg følgende fejlmeddelelse: "Antallet er ikke gyldigt".</span><span class="sxs-lookup"><span data-stu-id="98e62-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="98e62-130">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="98e62-130">Issue description</span></span>

<span data-ttu-id="98e62-131">Hvis feltet **Politik for nummerpladegruppering** er indstillet til *Brugerdefineret* for et menupunkt på en mobilenhed, som bruges til at registrere indgående ordrer, får du vist en fejlmeddelelse ("Antallet er ikke gyldigt"), og du kan ikke fuldføre registreringen.</span><span class="sxs-lookup"><span data-stu-id="98e62-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="98e62-132">Problemårsag</span><span class="sxs-lookup"><span data-stu-id="98e62-132">Issue cause</span></span>

<span data-ttu-id="98e62-133">Når *Brugerdefineret* bruges som nummerpladegrupperingspolitik, opdeles den indgående lagerbeholdning i separate nummerplader, som angivet af enhedsseriegruppen.</span><span class="sxs-lookup"><span data-stu-id="98e62-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="98e62-134">Hvis der bruges batch- eller serienumre til at spore den vare, der modtages, skal antallene for hver batch eller serie angives pr. nummerplade, der registreres.</span><span class="sxs-lookup"><span data-stu-id="98e62-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="98e62-135">Hvis det antal, der er angivet for nummerplade, overstiger det antal, der stadig skal modtages for de aktuelle dimensioner, får du vist fejlmeddelelsen.</span><span class="sxs-lookup"><span data-stu-id="98e62-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98e62-136">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="98e62-136">Issue resolution</span></span>

<span data-ttu-id="98e62-137">Når du registrerer en vare ved hjælp af menupunktet på en mobilenhed, hvor feltet **Politik for nummerpladegruppering** er angivet til *Brugerdefineret*, kan systemet kræve, at du bekræfter eller angiver nummerpladenumre, batchnumre eller serienumre.</span><span class="sxs-lookup"><span data-stu-id="98e62-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="98e62-138">På siden til bekræftelse af nummerplade vil systemet vise det antal, der er tildelt den aktuelle nummerplade.</span><span class="sxs-lookup"><span data-stu-id="98e62-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="98e62-139">På batch- eller seriebekræftelsessiderne viser systemet det antal, der stadig skal modtages på den aktuelle nummerplade.</span><span class="sxs-lookup"><span data-stu-id="98e62-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="98e62-140">Der findes også et felt, hvor du kan angive det antal, der skal registreres for denne kombination af nummerplade og batch- eller serienummer.</span><span class="sxs-lookup"><span data-stu-id="98e62-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="98e62-141">Hvis det er tilfældet, skal du sikre dig, at det antal, der registreres for nummerpladen, ikke overstiger det antal, der stadig skal modtages.</span><span class="sxs-lookup"><span data-stu-id="98e62-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="98e62-142">Hvis der genereres for mange nummerplader ved indgående ordreregistrering, kan værdien i feltet **Politik for nummerpladegruppering** ændres til *Nummerpladegruppering*, og derfor kan der tildeles en ny enhedsseriegruppe til varen, eller indstillingen af **Nummerpladegruppering** for enhedsseriegruppen kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="98e62-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
