---
title: Automatisk opdatering af aktivtællere
description: I dette emne beskrives automatisk opdatering af aktivtællere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 005b04bd4c3476356f30ba8e97564f83307a64c7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811734"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="5ca12-103">Automatisk opdatering af aktivtællere</span><span class="sxs-lookup"><span data-stu-id="5ca12-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ca12-104">Du kan finde oplysninger om manuel registrering af aktivtællere under [Manuel opdatering af aktivtællere](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5ca12-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="5ca12-105">Du kan finde oplysninger om, hvordan du konfigurerer aktivtællere, i [Tællere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5ca12-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="5ca12-106">Tællerværdier kan også opdateres automatisk fra produktionsregistreringer, baseret på produktionstimer eller produktionsantal (det producerede antal).</span><span class="sxs-lookup"><span data-stu-id="5ca12-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="5ca12-107">Denne opdatering udføres på siden **Opdater aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="5ca12-108">Du kan opdatere et eller flere aktiver ved at indstille én parameter, **Fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="5ca12-109">Denne parameter angiver startdatoen for produktionsregistreringer (produktionstimer eller produktionsantal).</span><span class="sxs-lookup"><span data-stu-id="5ca12-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="5ca12-110">Med andre ord angives den dato, hvor tællerværdierne skal opdateres fra.</span><span class="sxs-lookup"><span data-stu-id="5ca12-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="5ca12-111">Alle aktiver, der er relateret til en ressource *og* har aktivtællere, som er konfigureret til at blive opdateret på produceret antal eller produktionstimer, medtages i en automatisk opdatering.</span><span class="sxs-lookup"><span data-stu-id="5ca12-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="5ca12-112">Der oprettes nye tællerværdier.</span><span class="sxs-lookup"><span data-stu-id="5ca12-112">New counter values will be created.</span></span>

<span data-ttu-id="5ca12-113">For tællere, der er baseret på produktionsantallet, omfatter antallet både det antal, der er gyldigt, og det antal fejl, der er registreret.</span><span class="sxs-lookup"><span data-stu-id="5ca12-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="5ca12-114">Hvis den enhed, der bruges til registrering af produktionsantal, er forskellig fra den enhed, der bruges på tælleren, omregnes antallet, så det svarer til tællerenheden.</span><span class="sxs-lookup"><span data-stu-id="5ca12-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="5ca12-115">Som nævnt ovenfor kan automatiske tællere opdateres fra produktionsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="5ca12-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="5ca12-116">Det aktiv, som du automatisk vil opdatere tællere for, skal derfor være relateret til en ressource (maskine).</span><span class="sxs-lookup"><span data-stu-id="5ca12-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="5ca12-117">Når der er registreret producerede antal eller produktionstimer på ressourcen, kan du opdatere de relaterede aktivtællere.</span><span class="sxs-lookup"><span data-stu-id="5ca12-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="5ca12-118">Vælg **Styring af aktiver** > **Periodisk** > **Aktiver** > **Opdater aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="5ca12-119">Vælg startdatoen for den automatiske opdatering i feltet **Fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="5ca12-120">Datoen i dette felt er datoen for "igangværende arbejde" fra **Ruteposteringer** (**Produktionsstyring** > **Forespørgsler og rapporter** > **Produktion** > **Ruteposteringer** > **Fysisk dato**-felt).</span><span class="sxs-lookup"><span data-stu-id="5ca12-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="5ca12-121">I oversigtspanelet **Poster, der skal indgå** kan du vælge bestemte aktiver, aktivtyper eller ressourcer til den automatiske opdatering.</span><span class="sxs-lookup"><span data-stu-id="5ca12-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="5ca12-122">Vælg **filter**, og foretag de relevante valg.</span><span class="sxs-lookup"><span data-stu-id="5ca12-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="5ca12-123">I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.</span><span class="sxs-lookup"><span data-stu-id="5ca12-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="5ca12-124">I illustrationen nedenfor vises et eksempel på dialogboksen **Opdater aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Figur 1](media/12-work-orders.png)

5. <span data-ttu-id="5ca12-126">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-126">Select **OK**.</span></span> 

<span data-ttu-id="5ca12-127">Når den automatiske opdatering aktivtælleren er fuldført, kan du få vist de tællerregistreringer, der er relateret til aktivet på siden **Aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="5ca12-128">Vælge **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**, vælg aktivet, og vælg derefter **Tællere** i handlingsrudegruppen **Forebyggende** under fanen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="5ca12-129">På siden **Aktivaggregeret værdi** kan du få en oversigt over den seneste registrering, der er oprettet på alle tællertyper på alle aktiver.</span><span class="sxs-lookup"><span data-stu-id="5ca12-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="5ca12-130">Vælg **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivaggregeret værdi**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="5ca12-131">Denne side ligner siden **Aktivtællere**, men du kan ikke tilføje eller redigere registreringer.</span><span class="sxs-lookup"><span data-stu-id="5ca12-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="5ca12-132">Den er kun til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="5ca12-132">It's for overview only.</span></span>

<span data-ttu-id="5ca12-133">I illustrationen nedenfor vises et eksempel på siden **Aktivaggregeret værdi**.</span><span class="sxs-lookup"><span data-stu-id="5ca12-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Figur 2](media/13-work-orders.png)

<span data-ttu-id="5ca12-135">Vær opmærksom på følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="5ca12-135">Note the following points:</span></span>

- <span data-ttu-id="5ca12-136">Du kan stadig oprette manuelle tællerværdiregistreringer for tællertyper, der opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="5ca12-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="5ca12-137">Se afsnittet [Manuel opdatering af aktivtællere](../work-orders/manual-update-of-asset-counters.md) for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="5ca12-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="5ca12-138">Du kan oprette tællere, der er relateret til en anden tæller.</span><span class="sxs-lookup"><span data-stu-id="5ca12-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="5ca12-139">I dette tilfælde opdateres relaterede tællere automatisk, når en tæller opdateres.</span><span class="sxs-lookup"><span data-stu-id="5ca12-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="5ca12-140">Du kan finde flere oplysninger om, hvordan du konfigurerer relaterede tællere, i [Tællere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5ca12-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

