---
title: Aktivmålinger
description: Dette emne beskriver, hvordan du opretter typer af aktivmålinger i Styring af aktiver.
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
ms.openlocfilehash: bc6b9e944a7ecf6b769a8e3c2f9b1fbafaa60734
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626102"
---
# <a name="counters"></a><span data-ttu-id="21736-103">Tællere</span><span class="sxs-lookup"><span data-stu-id="21736-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21736-104">Dette emne beskriver, hvordan du opretter tællertyper i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="21736-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="21736-105">Tællertyper bruges til at foretage tællerregistreringer på aktiver, for eksempel antal produktionstimer eller antal, der produceres på aktivet.</span><span class="sxs-lookup"><span data-stu-id="21736-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="21736-106">Aktivtyper er relateret til tællertyperne.</span><span class="sxs-lookup"><span data-stu-id="21736-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="21736-107">Det betyder, at en tæller kun kan bruges på et aktiv, hvis tælleren er konfigureret på den aktivtype, der bruges på aktivet.</span><span class="sxs-lookup"><span data-stu-id="21736-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="21736-108">Før du kan foretage tællerregistreringer på aktiver, skal du først oprette de tællertyper, du vil bruge, i **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="21736-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="21736-109">Derefter kan du oprette tællerregistreringer for aktiver i **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="21736-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="21736-110">Tællere kan anvendes på vedligeholdelsesplaner.</span><span class="sxs-lookup"><span data-stu-id="21736-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="21736-111">En vedligeholdelsesplanlinje kan være af typen "Tæller", for eksempel vedrørende antallet af produktionstimer eller producerede mængder.</span><span class="sxs-lookup"><span data-stu-id="21736-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="21736-112">En tællerregistrering kan opdateres manuelt eller automatisk baseret på produktionstimer eller producerede antal.</span><span class="sxs-lookup"><span data-stu-id="21736-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="21736-113">En tæller kan konfigureres til at bruge en af tre opdateringsmetoder (valgt i feltet **Opdater** i **Tællere**):</span><span class="sxs-lookup"><span data-stu-id="21736-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="21736-114">Manuel – du skal registrere tællerværdier manuelt.</span><span class="sxs-lookup"><span data-stu-id="21736-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="21736-115">Produktionstimer – tælleren opdateres automatisk baseret på antallet af produktionstimer.</span><span class="sxs-lookup"><span data-stu-id="21736-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="21736-116">Produktionsantal – tælleren opdateres automatisk baseret på det producerede antal.</span><span class="sxs-lookup"><span data-stu-id="21736-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="21736-117">Hvis der bruges producerede mængder, medtages *alle* registrerede varer i tællerregistreringen, både antal gode og antal fejl.</span><span class="sxs-lookup"><span data-stu-id="21736-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="21736-118">Det er altid muligt at foretage manuelle tællerregistreringer, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="21736-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="21736-119">Oprette tællertyper for registreringer af aktivtæller</span><span class="sxs-lookup"><span data-stu-id="21736-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="21736-120">Vælg **Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="21736-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="21736-121">Vælg **Ny** for at oprette en ny tællertype.</span><span class="sxs-lookup"><span data-stu-id="21736-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="21736-122">Indsæt et id i feltet **Tæller** og et tællernavn i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="21736-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="21736-123">I oversigtspanelet **Generelt** skal du vælge en tællerenhed i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="21736-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="21736-124">Vælg den opdateringsmetode, der skal bruges til tælleren, i feltet **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="21736-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="21736-125">Vælg "Ja" på knappen **Arv tællerværdier**, hvis underordnede aktiver i en aktivstruktur automatisk skal arve de tællerregistreringer, der er foretaget på det overordnede aktiv.</span><span class="sxs-lookup"><span data-stu-id="21736-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="21736-126">I feltet **Samlet aggregat** skal du vælge den opsummeringsmetode, der skal bruges til en tæller ved hjælp af denne tællertype.</span><span class="sxs-lookup"><span data-stu-id="21736-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="21736-127">"Sum" er standardvalget, der bruges til løbende at lægge registrerede værdier til den samlede værdi.</span><span class="sxs-lookup"><span data-stu-id="21736-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="21736-128">"Gennemsnit" kan bruges, hvis en tæller er sat op til at overvåge en tærskel, for eksempel med hensyn til temperatur, vibrationer eller slitage på et aktiv.</span><span class="sxs-lookup"><span data-stu-id="21736-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="21736-129">I feltet **Afvigelse over** skal du indsætte det øverste niveau i procent for validering, hvis manuelle tællerregistreringer er inden for et forventet interval.</span><span class="sxs-lookup"><span data-stu-id="21736-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="21736-130">Valideringen er baseret på en lineær stigning i eksisterende tællerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="21736-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="21736-131">I feltet **Afvigelse under** skal du indsætte det nederste niveau i procent for validering, hvis manuelle tællerregistreringer er inden for et forventet interval.</span><span class="sxs-lookup"><span data-stu-id="21736-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="21736-132">Valideringen er baseret på et lineært fald i eksisterende tællerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="21736-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="21736-133">I feltet **Type** skal du vælge den typemeddelelse (oplysninger, advarsel, fejl), der skal vises, hvis afvigelser uden for det definerede interval indtræffer, når du foretager manuelle tællerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="21736-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="21736-134">Brug oversigtspanelet **Aktivtyper** til at tilføje de aktivtyper, der skal bruge tælleren.</span><span class="sxs-lookup"><span data-stu-id="21736-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="21736-135">I oversigtspanelet **Relaterede aktivtællere** skal du tilføje den tæller, der skal opdateres automatisk, når denne tæller opdateres.</span><span class="sxs-lookup"><span data-stu-id="21736-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="21736-136">En relateret tæller opdateres kun automatisk, hvis den relaterede tæller har den aktivtype, som den er relateret til, i tælleropsætningen.</span><span class="sxs-lookup"><span data-stu-id="21736-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="21736-137">For eksempel: Du konfigurerer en tæller for "Produktionstimer" og tilføjer aktivtypen "Lastbilmotor".</span><span class="sxs-lookup"><span data-stu-id="21736-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="21736-138">Når denne tæller opdateres, opdateres en relateret tæller "Olie" også med de samme tællerværdier.</span><span class="sxs-lookup"><span data-stu-id="21736-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="21736-139">Opsætningen i **Tællere** omfatter opsætningen på "Timer".</span><span class="sxs-lookup"><span data-stu-id="21736-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="21736-140">På tælleren "Olie" bør aktivtypen "Lastbilmotor" også føjes til oversigtspanelet **Aktivtyper** for at sikre tællerrelationen.</span><span class="sxs-lookup"><span data-stu-id="21736-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="21736-141">Se skærmbilleder nedenfor med et eksempel på opsætningen af Timer og Olie som tællere.</span><span class="sxs-lookup"><span data-stu-id="21736-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="21736-142">Når aktivtyper føjes til en tællertype i **Tællere**, føjes denne tæller automatisk til aktivtyperne i oversigtspanelet **Tællere** i [Aktivtyper](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="21736-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Figur 1](media/071-setup-for-objects.png)

