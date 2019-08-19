---
title: Aktivmålinger
description: Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver.
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
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783161"
---
# <a name="asset-measures"></a><span data-ttu-id="0ed7e-103">Aktivmålinger</span><span class="sxs-lookup"><span data-stu-id="0ed7e-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0ed7e-104">Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="0ed7e-105">Aktivmålingstyper bruges til at foretage målingsregistreringer på aktiver, for eksempel med hensyn til antal produktionstimer eller antal, der produceres på aktivet.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="0ed7e-106">Aktivtyper er relateret til aktivmålingstyperne.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="0ed7e-107">Det betyder, at en aktivmåling kun kan bruges på et aktiv, hvis aktivaktivmålingen er konfigureret på den aktivtype, der bruges på aktivet.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="0ed7e-108">Før du kan foretage målingsregistreringer på aktiver, skal du først oprette de aktivmålingstyper, du vil bruge i **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="0ed7e-109">Derefter kan du oprette målingsregistreringer for aktiver i **Aktivmålinger**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="0ed7e-110">Aktivmålinger kan anvendes på vedligeholdelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="0ed7e-111">En vedligeholdelsesplanlinje kan være af typen "Tæller", for eksempel vedrørende antallet af produktionstimer eller producerede mængder.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="0ed7e-112">En registrering af aktivmåling kan opdateres manuelt eller automatisk baseret på produktionstimer eller producerede antal.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="0ed7e-113">En aktivmåling kan konfigureres til at bruge en af tre opdateringsmetoder (valgt i feltet **Opdater** i **Tællere**):</span><span class="sxs-lookup"><span data-stu-id="0ed7e-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="0ed7e-114">Manuel – du skal registrere værdier for aktivmåling manuelt.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="0ed7e-115">Produktionstimer – tælleren opdateres automatisk baseret på antallet af produktionstimer.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="0ed7e-116">Produktionsantal – tælleren opdateres automatisk baseret på det producerede antal.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="0ed7e-117">Hvis der bruges producerede mængder, medtages *alle* registrerede varer i målingsregistreringen, både god mængde fejlmængde.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="0ed7e-118">Det er altid muligt at foretage manuelle registreringer af aktivmåling, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="0ed7e-119">Oprette tællertyper for registreringer af aktivtæller</span><span class="sxs-lookup"><span data-stu-id="0ed7e-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="0ed7e-120">Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="0ed7e-121">Vælg **Ny** for at oprette en ny type af aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="0ed7e-122">Indsæt et id i feltet **Tæller** og et tællernavn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="0ed7e-123">I oversigtspanelet **Generelt** skal du vælge en måleenhed i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="0ed7e-124">Vælg den opdateringsmetode, der skal bruges til aktivmålingen, i feltet **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="0ed7e-125">Vælg "Ja" på knappen **Arv tællerværdier**, hvis underordnede aktiver i en aktivstruktur automatisk skal arve de registreringer af aktivmåling, der er foretaget på det overordnede aktiv.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="0ed7e-126">I feltet **Samlet aggregat** skal du vælge den opsummeringsmetode, der skal bruges til en aktivmåling ved hjælp af denne aktivmålingstype.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="0ed7e-127">"Sum" er standardvalget, der bruges til løbende at lægge registrerede værdier til den samlede værdi.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="0ed7e-128">"Gennemsnit" kan bruges, hvis en aktivmåling er sat op til at overvåge en tærskel, for eksempel med hensyn til temperatur, vibrationer eller slitage på et aktiv.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="0ed7e-129">I feltet **Afvigelse over** skal du indsætte det øverste niveau i procent for validering, hvis manuelle registreringer af aktivmåling er inden for et forventet interval.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="0ed7e-130">Valideringen er baseret på en lineær stigning i eksisterende registreringer af aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="0ed7e-131">I feltet **Afvigelse under** skal du indsætte det nederste niveau i procent for validering, hvis manuelle registreringer af aktivmåling er inden for et forventet interval.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="0ed7e-132">Valideringen er baseret på et lineært fald i eksisterende registreringer af aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="0ed7e-133">I feltet **Type** skal du vælge den typemeddelelse (oplysninger, advarsel, fejl), der skal vises, hvis afvigelser uden for det definerede interval indtræffer, når du foretager manuelle registreringer af aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="0ed7e-134">Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge aktivmålingen.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="0ed7e-135">I oversigtspanelet **Relaterede aktivmålinger** skal du tilføje de aktivmålinger, der skal opdateres automatisk, når denne aktivmåling opdateres.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="0ed7e-136">En relateret aktivmåling opdateres kun automatisk, hvis den relaterede aktivmåling har den aktivtype, som den er relateret til, i opsætningen af aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="0ed7e-137">For eksempel: Du konfigurerer en aktivmåling for "Produktionstimer" og tilføjer aktivtypen "Lastbilmotor".</span><span class="sxs-lookup"><span data-stu-id="0ed7e-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="0ed7e-138">Når denne aktivmåling opdateres, opdateres en relateret tæller "Olie" også med de samme værdier for aktivmåling.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="0ed7e-139">Opsætningen i **Tællere** omfatter opsætningen på "Timer".</span><span class="sxs-lookup"><span data-stu-id="0ed7e-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="0ed7e-140">På aktivmålingen "Olie" bør aktivtypen "Lastbilmotor" også føjes til oversigtspanelet **Aktivtyper** for at sikre aktivmålingens relation.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="0ed7e-141">Se skærmbilleder nedenfor med et eksempel på opsætningen af Timer og Olie som aktivmålinger.</span><span class="sxs-lookup"><span data-stu-id="0ed7e-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="0ed7e-142">Når aktivtyper føjes til en aktivmålingstype i **Tællere**, føjes denne aktivmåling automatisk til aktivtyperne i oversigtspanelet **Tællere** i [Aktivtyper](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="0ed7e-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Figur 1](media/071-setup-for-objects.png)


