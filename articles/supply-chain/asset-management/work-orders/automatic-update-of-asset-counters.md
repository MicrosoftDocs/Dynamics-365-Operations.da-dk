---
title: Automatisk opdatering af aktivtællere
description: I dette emne beskrives automatisk opdatering af aktivtællere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875574"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="4f910-103">Automatisk opdatering af aktivtællere</span><span class="sxs-lookup"><span data-stu-id="4f910-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4f910-104">I forrige afsnit beskrives manuel registrering af aktivtællere.</span><span class="sxs-lookup"><span data-stu-id="4f910-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="4f910-105">Opsætning af aktivtællere beskrives i [Tællere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="4f910-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="4f910-106">Tællerværdier kan også opdateres automatisk fra produktionsregistreringer, baseret på produktionstimer eller produktionsantal.</span><span class="sxs-lookup"><span data-stu-id="4f910-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="4f910-107">Dette gøres i **Opdater aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="4f910-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="4f910-108">Du kan opdatere et eller flere aktiver ved at indsætte én parameter, **Fra dato**.</span><span class="sxs-lookup"><span data-stu-id="4f910-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="4f910-109">Denne parameter angiver startdatoen for produktionsregistreringer (timer eller produceret antal), hvilket vil sige den startdato, hvorfra tællerværdier skal opdateres.</span><span class="sxs-lookup"><span data-stu-id="4f910-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="4f910-110">Alle aktiver, der er relateret til en ressource *og* har aktivtællere, som er konfigureret til at blive opdateret på basis af produceret antal eller produktionstimer, medtages i en automatisk opdatering, og der oprettes nye tællerværdier.</span><span class="sxs-lookup"><span data-stu-id="4f910-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="4f910-111">Ved tællere baseret på produktionsantal er det antal gode og fejlmeldte antal, der medtages i optællingen.</span><span class="sxs-lookup"><span data-stu-id="4f910-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="4f910-112">Hvis den enhed, der bruges til registrering af antal, er forskellig fra den enhed, der bruges på tælleren, omregnes antallet, så det svarer til tællerenheden.</span><span class="sxs-lookup"><span data-stu-id="4f910-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="4f910-113">Som nævnt ovenfor kan automatiske tællere opdateres fra produktionsregistreringer.</span><span class="sxs-lookup"><span data-stu-id="4f910-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="4f910-114">Det aktiv, som du automatisk vil opdatere tællere for, skal derfor være relateret til en ressource (maskine).</span><span class="sxs-lookup"><span data-stu-id="4f910-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="4f910-115">Følgende beskrivelser indeholder en oversigt over opsætning og behandling af produktionsordrer (i modulet **Produktionsstyring**), der bruges som grundlag for automatisk opdatering af tællere på et aktiv i modulet **Styring af aktiver**.</span><span class="sxs-lookup"><span data-stu-id="4f910-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="4f910-116">Når der er registreret producerede antal eller produktionstimer på ressourcen, kan du opdatere de relaterede aktivtællere.</span><span class="sxs-lookup"><span data-stu-id="4f910-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="4f910-117">Klik på **Styring af aktiver** > **Periodisk** > **Aktiver** > **Opdater aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="4f910-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="4f910-118">Vælg startdatoen for den automatiske opdatering i feltet **Fra-dato**.</span><span class="sxs-lookup"><span data-stu-id="4f910-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="4f910-119">Datoen i dette felt er datoen for "igangværende arbejde" fra **Ruteposteringer** (**Produktionsstyring** > **Forespørgsler og rapporter** > **Produktion** > **Ruteposteringer** > **Fysisk dato**-felt).</span><span class="sxs-lookup"><span data-stu-id="4f910-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="4f910-120">Hvis du vil vælge bestemte aktiver, aktivtyper eller ressourcer til den automatiske opdatering, skal du klikke på **Filter** i oversigtspanelet **Poster, der skal indgå** og foretage de relevante valg.</span><span class="sxs-lookup"><span data-stu-id="4f910-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="4f910-121">I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.</span><span class="sxs-lookup"><span data-stu-id="4f910-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Figur 1](media/12-work-orders.png)

5. <span data-ttu-id="4f910-123">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f910-123">Click **OK**.</span></span> <span data-ttu-id="4f910-124">Når den automatiske opdatering af aktivoptælleren er udført, kan du se de tællerregistreringer, der relateret til aktivet, i **Aktivtællere** (**Styring af aktiver** > **Generelt** > **Aktiver** > **Alle aktiver** > vælg aktiv > knappen **Tællere**).</span><span class="sxs-lookup"><span data-stu-id="4f910-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="4f910-125">I **Totaler for aktivtæller** kan du få en oversigt over den seneste registrering, der er oprettet på alle tællertyper på alle aktiver.</span><span class="sxs-lookup"><span data-stu-id="4f910-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="4f910-126">Klik på **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivaggregeret værdi**.</span><span class="sxs-lookup"><span data-stu-id="4f910-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="4f910-127">Visningen minder meget om **Aktivtællere**, men du kan ikke tilføje eller redigere registreringer i **Aktivaggregeret værdi**.</span><span class="sxs-lookup"><span data-stu-id="4f910-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="4f910-128">Den er kun til oversigten.</span><span class="sxs-lookup"><span data-stu-id="4f910-128">It is for overview only.</span></span>

![Figur 2](media/13-work-orders.png)


- <span data-ttu-id="4f910-130">Det er stadig muligt at oprette manuelle tællerværdiregistreringer for tællertyper, der opdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="4f910-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="4f910-131">Se afsnittet "Manuel opdatering af aktivtællere" for at få yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4f910-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="4f910-132">Du kan definere tællere, der er knyttet til en anden tæller, hvilket betyder, at når en tæller opdateres, opdateres relaterede tællere automatisk samtidigt.</span><span class="sxs-lookup"><span data-stu-id="4f910-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="4f910-133">Se emnet [Tællere](../setup-for-objects/counters.md) vedrørende opsætning af relaterede tællere.</span><span class="sxs-lookup"><span data-stu-id="4f910-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
