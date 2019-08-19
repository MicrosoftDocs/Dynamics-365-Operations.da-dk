---
title: Kritikalitetstyper for aktiver
description: I emnet forklares kritikalitetstyper for aktiver i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783157"
---
# <a name="asset-criticalities"></a><span data-ttu-id="7b298-103">Kritikaliteter for aktiver</span><span class="sxs-lookup"><span data-stu-id="7b298-103">Asset criticalities</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7b298-104">I emnet forklares kritikalitetstyper for aktiver i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="7b298-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="7b298-105">Aktivers kritikalitet er relateret til aktiver og overføres til arbejdsordrer.</span><span class="sxs-lookup"><span data-stu-id="7b298-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="7b298-106">Den kan ikke ændres på en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7b298-106">It can't be changed on a work order.</span></span> <span data-ttu-id="7b298-107">Aktivers kritikalitet bruges til at beregne arbejdsordrens kritikalitet i forbindelse med planlægningen af arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="7b298-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="7b298-108">Det bruges med andre ord til at beregne, i hvilket omfang et vedligeholdelsesjob på et aktiv påvirker produktionsplanen og produktiviteten i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="7b298-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="7b298-109">Du finder flere oplysninger om den opsætning, der er relateret til beregningen af rangeringsresultater for planlægning af arbejdsordre under [Parametre for Styring af aktiver](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7b298-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="7b298-110">Hvis du vil konfigurere kritikalitet, skal du først oprette de kritikalitetstyper, der bør bruges i opsætningen af aktiver.</span><span class="sxs-lookup"><span data-stu-id="7b298-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="7b298-111">Du kan derefter oprette aktivkritikaliteter.</span><span class="sxs-lookup"><span data-stu-id="7b298-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="7b298-112">Konfigurer kritikalitetstyper</span><span class="sxs-lookup"><span data-stu-id="7b298-112">Set up criticality types</span></span>

1. <span data-ttu-id="7b298-113">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **kritikalitetstyper**.</span><span class="sxs-lookup"><span data-stu-id="7b298-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="7b298-114">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="7b298-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="7b298-115">Indtast et tal, der angiver kritikaliteten, i feltet **Kritikalitet**.</span><span class="sxs-lookup"><span data-stu-id="7b298-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="7b298-116">Angiv et navn for kritikalitetstypen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7b298-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="7b298-117">Angiv en faktor i feltet **Faktor**.</span><span class="sxs-lookup"><span data-stu-id="7b298-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="7b298-118">Denne faktor bruges i forbindelse med beregning af arbejdsordreplanlægningen til at bestemme den kritikalitetspost, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="7b298-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="7b298-119">(Den post, der har den højeste faktor, bruges altid.) Denne indstilling er relevant, hvis der, som vist i følgende illustration, oprettes kritikalitetslinjer med samme kritikalitetsværdi.</span><span class="sxs-lookup"><span data-stu-id="7b298-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Figur 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="7b298-121">Opsætning af aktivkritikaliteter</span><span class="sxs-lookup"><span data-stu-id="7b298-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="7b298-122">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivkritikaliteter**.</span><span class="sxs-lookup"><span data-stu-id="7b298-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="7b298-123">Vælg **Ny** for at oprette en post.</span><span class="sxs-lookup"><span data-stu-id="7b298-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="7b298-124">Afhængigt af det påkrævede detaljeringsniveau for aktivkritikalitet skal du foretage relevante valg i felterne **Arbejdssted**, **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Jobtypekategori**, **Jobtype**, **Jobtypevariant** og **sagskrav**.</span><span class="sxs-lookup"><span data-stu-id="7b298-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7b298-125">Når en aktivkritikalitet er valgt, gennemgår Styring af aktiver alle aktivkritikalitetsposter for at kontrollere, om der er et muligt match.</span><span class="sxs-lookup"><span data-stu-id="7b298-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="7b298-126">Den kontrollerer altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="7b298-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="7b298-127">Med andre ord kontrollerer Styring af aktiver først **Jobkrav**.</span><span class="sxs-lookup"><span data-stu-id="7b298-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="7b298-128">Hvis der ikke findes et match, kontrolleres **Jobtypevarianten**.</span><span class="sxs-lookup"><span data-stu-id="7b298-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="7b298-129">Hvis der ikke findes et match, kontrolleres **Jobtypn** osv.</span><span class="sxs-lookup"><span data-stu-id="7b298-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="7b298-130">Som du kan se i sidens layout, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination.</span><span class="sxs-lookup"><span data-stu-id="7b298-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="7b298-131">Hvis der ikke findes et match, bruges posten "standard", som ikke har nogen markeringer.</span><span class="sxs-lookup"><span data-stu-id="7b298-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="7b298-132">I feltet **Kritikalitet** skal du vælge en af de kritikalitetskoder, som du oprettede under den forrige procedure.</span><span class="sxs-lookup"><span data-stu-id="7b298-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="7b298-133">Bemærkninger til opsætning af kritikalitet</span><span class="sxs-lookup"><span data-stu-id="7b298-133">Notes about criticality setup</span></span>

- <span data-ttu-id="7b298-134">Hvis du ændrer en aktivkritikalitet i denne opsætning, efter at du allerede har brugt den på en arbejdsordre, opdateres kritikaliteten på arbejdsordren ikke i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="7b298-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="7b298-135">Kritikaliteten på en arbejdsordre genberegnes, hver gang en arbejdsordrelinje føjes til eller slettes fra arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="7b298-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="7b298-136">Hvis en arbejdsordre indeholder flere arbejdsordrejobs, bruges den højeste kritikalitet i henhold til feltet **Faktor** på siden **Kritikalitetstyper** altid på arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="7b298-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="7b298-137">Generelt set kan aktivkritikalitet ændre sig over en periode.</span><span class="sxs-lookup"><span data-stu-id="7b298-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="7b298-138">Kritikalitet kan påvirkes af køb af nyt udstyr, renovering osv.</span><span class="sxs-lookup"><span data-stu-id="7b298-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="7b298-139">Overvej at revurdere dine aktivkritikaliteter med jævne mellemrum (f.eks. én gang om året eller hvert andet år) for at sikre, at dine kritikalitetsdefinitioner svarer til din aktuelle produktionsopsætning.</span><span class="sxs-lookup"><span data-stu-id="7b298-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
