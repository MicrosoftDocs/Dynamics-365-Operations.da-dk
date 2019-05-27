---
title: Konfigurere klyngepluk
description: Dette emne beskriver, hvordan du konfigurerer klyngepluk og anvender varebekræftelse sammen med klyngepluk.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558994"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="9d7f9-103">Konfigurere klyngepluk</span><span class="sxs-lookup"><span data-stu-id="9d7f9-103">Set up cluster picking</span></span>

<span data-ttu-id="9d7f9-104">Dette emne beskriver, hvordan arbejderne skal kunne bruge deres mobilenheder til at gruppere plukkearbejde i klynger, så de kan plukke varer fra et enkelt sted til flere arbejdsordrer på samme tid.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="9d7f9-105">Dette kaldes *klyngepluk*.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="9d7f9-106">Om klyngepluk</span><span class="sxs-lookup"><span data-stu-id="9d7f9-106">About cluster picking</span></span>

<span data-ttu-id="9d7f9-107">Når arbejdsordrer er frigivet til lagerstedet, kan arbejderen bruge en mobilenhed til at tildele ordrer til en klynge.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="9d7f9-108">Klyngen organiserer plukkearbejdet for arbejderen.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="9d7f9-109">Når en arbejdsordre er tildelt til en klynge, skal arbejderen bruge klyngepluk til at udføre plukkearbejdet for ordren.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="9d7f9-110">Arbejderen kan ikke bruge andre plukkemetoder.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="9d7f9-111">Hvis en arbejdsordre er tildelt til en klynge ved en fejl, skal arbejderen bryde klyngen op og derefter oprette den igen.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="9d7f9-112">Hvis det er nødvendigt, kan en arbejder sende en klynge til en anden arbejder.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="9d7f9-113">Dette ændrer statussen på klyngen til Bestået.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="9d7f9-114">Når arbejderen bruger en mobilenhed til at angive, at plukning og læg på lager-arbejde er fuldført, skal forsendelsen eller lasten skal bekræftes i Dynamics 365 for Finance and Operations-klienten.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="9d7f9-115">Konfigurere klyngepluk</span><span class="sxs-lookup"><span data-stu-id="9d7f9-115">Set up cluster picking</span></span>

<span data-ttu-id="9d7f9-116">Hvis du vil aktivere klyngepluk, skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="9d7f9-117">**Klyngeprofiler** – Angiv, om der automatisk skal oprettes klynge-id'er, antallet af positioner, der skal bruges, hvornår klynger skal brydes, og hvordan rækkefølgen af plukarbejdet skal angives og bekræftes.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="9d7f9-118">**Arbejdsskabeloner** – Definer, hvordan du opretter plukarbejde til klyngepluk.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="9d7f9-119">**Lokationsvejledninger** – Angiv, hvor du kan plukke varer fra, og hvor du kan placere dem.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="9d7f9-120">**Menupunkter i mobilenhed** – Konfigurer et menupunkt på en mobilenhed til at bruge eksisterende arbejde, der er pålagt ved hjælp af klyngepluk.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="9d7f9-121">Du skal tilføje menupunktet til en mobilenhedmenu, så den vises på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="9d7f9-122">**Parametre til lokationsstyring** – Angiv den nummerserie, der skal bruges, hvis du vil generere id'er til klynger.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="9d7f9-123">Konfigurere en klyngeprofil</span><span class="sxs-lookup"><span data-stu-id="9d7f9-123">Set up a cluster profile</span></span>

<span data-ttu-id="9d7f9-124">Du kan konfigurere en klyngeprofil på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="9d7f9-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="9d7f9-125">Klik på **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Klyngeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="9d7f9-126">Klik på **Ny** for at oprette en ny profil.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="9d7f9-127">Klik på **Opret klynge** og under **Klyngesortering**, skal du klikke på **Ny** for at konfigurere sorteringskriterier for klyngen.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="9d7f9-128">Sorteringskriteriet styrer den rækkefølge, som arbejderen skal udføre plukkearbejdet i.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="9d7f9-129">Du kan tilføje lige så mange kriterier, der er behov for.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="9d7f9-130">I feltet **Løbenummer** skal du angive et nummer for at definere den rækkefølge, som sorteringskriterierne behandles i.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="9d7f9-131">Vælg det felt, der skal bestemme sorteringen, i feltet **Feltnavn**.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="9d7f9-132">Hvis du f.eks. vælger **WMSLocationId**, sorteres arbejdet efter den lokation.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="9d7f9-133">Vælg en af følgende indstillinger i feltet **Sortering**.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="9d7f9-134">**Indstilling**</span><span class="sxs-lookup"><span data-stu-id="9d7f9-134">**Option**</span></span>     | <span data-ttu-id="9d7f9-135">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="9d7f9-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7f9-136">**Stigende**</span><span class="sxs-lookup"><span data-stu-id="9d7f9-136">**Ascending**</span></span>  | <span data-ttu-id="9d7f9-137">Plukarbejdet sorteres i stigende rækkefølge ud fra sorteringskriterierne.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="9d7f9-138">Hvis du f.eks. bruger feltet **WMSLocationId** som sorteringskriterier og dit lokations-id er 1, 2, 3 og 4, plukker du først fra lokation 4.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="9d7f9-139">**Faldende**</span><span class="sxs-lookup"><span data-stu-id="9d7f9-139">**Descending**</span></span> | <span data-ttu-id="9d7f9-140">Plukarbejdet sorteres i faldende rækkefølge ud fra sorteringskriterierne.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="9d7f9-141">Hvis du f.eks. bruger feltet **WMSLocationId** som sorteringskriterier og dit lokations-id er 1, 2, 3 og 4, plukker du først fra lokation 1.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="9d7f9-142">Varebekræftelse</span><span class="sxs-lookup"><span data-stu-id="9d7f9-142">Item confirmation</span></span>

<span data-ttu-id="9d7f9-143">Når der anvendes en klyngepluk, er varebekræftelse afgørende for kontrol af de varer, der føjes til klynger.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="9d7f9-144">Du kan kontrollere varer i klyngepluk under klyngeplukprocessen.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="9d7f9-145">Opsætningen er baseret på opsætningen af produktets stregkode.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="9d7f9-146">Konfigurer varekontrol med klyngepluk</span><span class="sxs-lookup"><span data-stu-id="9d7f9-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="9d7f9-147">I et menupunkt på en mobilenhed skal du åbne opsætningsformularen for arbejdsbekræftelse: **Lokationsstyring** \> **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="9d7f9-148">Åbn **Konfiguration af arbejdsbekræftelse** fra menupunktet på mobilenheden.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="9d7f9-149">Indstillingen **Bekræftelse af produkt** gør det muligt at kontrollere hver enkelt vare på lageret fra mobilenheden, når den scannes.</span><span class="sxs-lookup"><span data-stu-id="9d7f9-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
