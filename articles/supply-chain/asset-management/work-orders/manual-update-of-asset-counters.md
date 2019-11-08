---
title: Manuel opdatering af aktivtællere
description: I dette emne beskrives manuel opdatering af aktivtællere i Styring af aktiver.
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
ms.openlocfilehash: 3072ab204b53b16988d2973b28a697041cb84c27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626126"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="74896-103">Manuel opdatering af aktivtællere</span><span class="sxs-lookup"><span data-stu-id="74896-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="74896-104">Tællere bruges til at oprette registreringer på et aktiv, f.eks. registreringer af det antal timer, som aktivet har været i drift, eller det antal, der er produceret.</span><span class="sxs-lookup"><span data-stu-id="74896-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="74896-105">Den tællertype, der er valgt for en tæller, kan være angivet til at arve tællerværdier.</span><span class="sxs-lookup"><span data-stu-id="74896-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="74896-106">Indstillingen **Arv tællerværdier for aktiv** er med andre ord angivet til **Ja** i oversigtspanelet **Generelt** på siden **Tællere** (**Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**).</span><span class="sxs-lookup"><span data-stu-id="74896-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="74896-107">Hvis du i dette tilfælde opretter en ny tællerlinje af denne type, opdateres alle underordnede aktiver, der bruger samme tællertype, automatisk.</span><span class="sxs-lookup"><span data-stu-id="74896-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="74896-108">På siden **Alle aktiver** kan du oprette tællerregistreringer af timer eller antal for et aktiv ud fra dine aflæsninger af aktivet.</span><span class="sxs-lookup"><span data-stu-id="74896-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="74896-109">Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="74896-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="74896-110">Vælg aktivet, og vælg **Tællere** i handlingsrudegruppen **Forebyggende** under fanen **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="74896-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="74896-111">På siden **Aktivtællere** vises en liste over alle tidligere tællerregistreringer, der er foretaget på det valgte aktiv.</span><span class="sxs-lookup"><span data-stu-id="74896-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="74896-112">Vælg **Ny** for at oprette en ny registrering.</span><span class="sxs-lookup"><span data-stu-id="74896-112">Select **New** to create a registration.</span></span> <span data-ttu-id="74896-113">Aktiv-id indtastes automatisk i feltet **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="74896-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="74896-114">Vælg den relevante tæller i feltet **Tæller**.</span><span class="sxs-lookup"><span data-stu-id="74896-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="74896-115">Kun tællere, der er relateret til den aktivtype, der er valgt på aktivet, kan vælges.</span><span class="sxs-lookup"><span data-stu-id="74896-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="74896-116">Den relaterede enhed indsættes automatisk i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="74896-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="74896-117">Vælg dato og klokkeslæt for tællerregistreringen i feltet **Registreret**.</span><span class="sxs-lookup"><span data-stu-id="74896-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="74896-118">I feltet **Værdi** skal du angive nummeret siden sidste tællerregistrering.</span><span class="sxs-lookup"><span data-stu-id="74896-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="74896-119">Du kan også angive det samlede antal i feltet **Akkumuleret værdi**.</span><span class="sxs-lookup"><span data-stu-id="74896-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="74896-120">Vær opmærksom på følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="74896-120">Note the following points:</span></span>

- <span data-ttu-id="74896-121">Hvis du fysisk installerer en ny tæller på et aktiv, skal du registrere ændringen af aktivet på siden **Aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="74896-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="74896-122">Derefter skal du oprette to registreringslinjer, der har identiske tidsstemplinger.</span><span class="sxs-lookup"><span data-stu-id="74896-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="74896-123">Den første linje skal være for den tæller, du er ved at udskifte.</span><span class="sxs-lookup"><span data-stu-id="74896-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="74896-124">Markér afkrydsningsfeltet **Nulstil tæller** på den linje, der er relateret til den nye tæller.</span><span class="sxs-lookup"><span data-stu-id="74896-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="74896-125">I feltet **Totaler** er det samlede antal summen af tællertotalerne for alle registrerede værdier på den pågældende tællertype.</span><span class="sxs-lookup"><span data-stu-id="74896-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="74896-126">Hvis afkrydsningsfeltet **Nulstil tæller** er markeret på et aktiv ved hjælp af en vedligeholdelsesplan med intervaltypen "Én gang fra..." eller "Når nået...", er tælleren stadig aktiv på den nye tællerlinje, fordi du opretter en separat tællerlinje og starter forfra med en ny tæller.</span><span class="sxs-lookup"><span data-stu-id="74896-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="74896-127">I illustrationen nedenfor vises et eksempel på siden **Aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="74896-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Figur 1](media/11-work-orders.png)

<span data-ttu-id="74896-129">På siden **Aktivtællere** (**Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivtællere**) kan du foretage tællerregistreringer på flere aktiver på samme tid efter behov.</span><span class="sxs-lookup"><span data-stu-id="74896-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="74896-130">Du kan konfigurere et interval for at definere afvigelser i manuelle tællerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="74896-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="74896-131">Du kan også angive den type meddelelse, der vises, hvis registreringerne er uden for det angivne interval.</span><span class="sxs-lookup"><span data-stu-id="74896-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="74896-132">Du kan finde flere oplysninger om, hvordan du konfigurerer tællere, i [Tællere](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="74896-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

