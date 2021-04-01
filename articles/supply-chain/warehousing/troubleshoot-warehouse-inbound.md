---
title: Foretage fejlfinding af indgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250876"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="de529-103">Foretage fejlfinding af indgående lagerstedsoperationer</span><span class="sxs-lookup"><span data-stu-id="de529-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de529-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de529-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="de529-105">Jeg får vist følgende fejlmeddelelse: "Kvalitetsordren %1 er blevet genereret.</span><span class="sxs-lookup"><span data-stu-id="de529-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="de529-106">Klyngeprofil blev ikke fundet. Kontrollér din konfiguration."</span><span class="sxs-lookup"><span data-stu-id="de529-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="de529-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="de529-107">Issue description</span></span>

<span data-ttu-id="de529-108">Denne fejlmeddelelse er relateret til en modtagelsesproces, hvor kvalitetsstyring (QMS) er slået til.</span><span class="sxs-lookup"><span data-stu-id="de529-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="de529-109">Afhængigt af konfigurationerne i dit miljø kan yderligere oplysninger om den transaktion, der genererer fejlmeddelelsen, måske løse problemet.</span><span class="sxs-lookup"><span data-stu-id="de529-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de529-110">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="de529-110">Issue resolution</span></span>

<span data-ttu-id="de529-111">Først skal du gennemse opsætningen for [klyngepluk](set-up-cluster-picking.md) og kontrollere, at dine klyngeprofiler er konfigureret korrekt.</span><span class="sxs-lookup"><span data-stu-id="de529-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="de529-112">Du kan ikke bruge et menupunkt til klyngepluk i mobilenheden, medmindre der er konfigureret klyngeprofiler.</span><span class="sxs-lookup"><span data-stu-id="de529-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="de529-113">Afhængigt af miljøet skal du muligvis også gennemse andre relaterede konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="de529-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="de529-114">Modtagelse af blandede id'er fungerer ikke for nogen dispositionskode undtagen Kredit.</span><span class="sxs-lookup"><span data-stu-id="de529-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de529-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="de529-115">Issue description</span></span>

<span data-ttu-id="de529-116">Når **Handling**-feltet for en dispositionskode er sat til *Kredit* eller *Kasseres*, kan du kun bruge menupunktet [Modtagelse af blandede id'er](mixed-license-plate-receiving.md) til at behandle returvarer.</span><span class="sxs-lookup"><span data-stu-id="de529-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de529-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="de529-117">Issue resolution</span></span>

<span data-ttu-id="de529-118">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="de529-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="de529-119">Aktuelt er det kun [dispositionskoder](../service-management/set-up-disposition-codes.md), hvor feltet **Handling** er indstillet til *Kredit* eller *Kasseres*, der understøttes til modtagelse af blandede id'er.</span><span class="sxs-lookup"><span data-stu-id="de529-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="de529-120">Når jeg kører den periodiske opgave Opdater produktkvitteringer, bekræftes ubekræftede indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="de529-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="de529-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="de529-121">Issue description</span></span>

<span data-ttu-id="de529-122">Når du har kørt den periodiske opgave *Opdater produktkvitteringer*, bekræfter systemet automatisk ubekræftede indkøbsordrer, der har lagertransaktionstatus *Registreret*.</span><span class="sxs-lookup"><span data-stu-id="de529-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="de529-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="de529-123">Issue resolution</span></span>

<span data-ttu-id="de529-124">En ny funktion til håndtering af indgående last, *Overtilgang af lastantal*, løser dette problem.</span><span class="sxs-lookup"><span data-stu-id="de529-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="de529-125">Hvis du aktivere denne funktion, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner (i deres viste rækkefølge):</span><span class="sxs-lookup"><span data-stu-id="de529-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="de529-126">Tilknyt lagertransaktioner med belastning for indkøbsordre</span><span class="sxs-lookup"><span data-stu-id="de529-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="de529-127">Overtilgang af lastantal</span><span class="sxs-lookup"><span data-stu-id="de529-127">Over receipt of load quantities</span></span>

<span data-ttu-id="de529-128">Du kan finde flere oplysninger under [Bogføre registrerede produktantal i forhold til indkøbsordrer](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="de529-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]