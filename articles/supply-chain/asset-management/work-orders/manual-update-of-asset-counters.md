---
title: Manuel opdatering af aktivtællere
description: I dette emne beskrives manuel opdatering af aktivtællere i Styring af aktiver.
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
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875569"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="e2089-103">Manuel opdatering af aktivtællere</span><span class="sxs-lookup"><span data-stu-id="e2089-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e2089-104">Tællere bruges til at oprette registreringer på et aktiv, f.eks. antallet af timer i drift eller antallet af producerede varer.</span><span class="sxs-lookup"><span data-stu-id="e2089-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="e2089-105">Hvis den tællertype, der er valgt for en tæller, er indstillet til at arve tællerværdier (**Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere** > **Generelt**-oversigtspanelet > **Arv tællerværdier for aktiv**-til/fra knappen indstillet til "ja"), opdateres alle de underordnede aktiver, der bruger samme tællertype, automatisk, når du opretter en ny tællerlinje af denne type.</span><span class="sxs-lookup"><span data-stu-id="e2089-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="e2089-106">I **Alle aktiver** kan du oprette registreringer af timer eller antal optællinger for et aktiv ud fra dine aflæsninger af aktivet.</span><span class="sxs-lookup"><span data-stu-id="e2089-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="e2089-107">Klik på **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="e2089-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e2089-108">Vælg aktivet på listen, og klik på **Tællere**.</span><span class="sxs-lookup"><span data-stu-id="e2089-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="e2089-109">I formularen **Aktivtællere** vises en liste over alle tidligere tællerregistreringer på det valgte aktiv.</span><span class="sxs-lookup"><span data-stu-id="e2089-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="e2089-110">Klik på **Ny** for at oprette en registrering.</span><span class="sxs-lookup"><span data-stu-id="e2089-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="e2089-111">Aktiv-id'et indsættes automatisk.</span><span class="sxs-lookup"><span data-stu-id="e2089-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="e2089-112">Vælg den relevante tæller i feltet **Tæller**.</span><span class="sxs-lookup"><span data-stu-id="e2089-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="e2089-113">Kun tællere, der er relateret til den aktivtype, der er valgt på aktivet, er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="e2089-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="e2089-114">Den relaterede enhed indsættes automatisk i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="e2089-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="e2089-115">Vælg dato og klokkeslæt for tællerregistreringen.</span><span class="sxs-lookup"><span data-stu-id="e2089-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="e2089-116">Indsæt tallet i feltet **Værdi** siden sidste tællerregistrering, eller indsæt det samlede optalte antal i feltet **Akkumuleret værdi**.</span><span class="sxs-lookup"><span data-stu-id="e2089-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="e2089-117">Hvis du fysisk installerer en ny tæller på et aktiv, skal du registrere ændringen af aktivet i **Aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="e2089-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="e2089-118">Derefter skal du oprette to registreringslinjer med identiske tidsstempler, og på linjen angående den nye tæller, skal du markere afkrydsningsfeltet **Nulstil tæller**.</span><span class="sxs-lookup"><span data-stu-id="e2089-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="e2089-119">Når du opretter de to registreringslinjer, skal den første linje være for den tæller, du udskifter.</span><span class="sxs-lookup"><span data-stu-id="e2089-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="e2089-120">I feltet **Totaler** er det samlede antal summen af tællertotalen for alle registrerede værdier på den pågældende tællertype.</span><span class="sxs-lookup"><span data-stu-id="e2089-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="e2089-121">Hvis afkrydsningsfeltet **Nulstil tæller** er markeret på et aktiv ved hjælp af en vedligeholdelsesplan med intervaltypen "En gang fra..." eller "Når nået...", er tælleren stadig aktiv på den nye tællerlinje, fordi du opretter en separat tællerlinje og starter forfra med en ny tæller.</span><span class="sxs-lookup"><span data-stu-id="e2089-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Figur 1](media/11-work-orders.png)


<span data-ttu-id="e2089-123">Hvis du har brug for at foretage tællerregistrering på flere anlægsaktiver, kan det gøres i **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivtællere**.</span><span class="sxs-lookup"><span data-stu-id="e2089-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="e2089-124">Du kan oprette et interval for at definere afvigelser i manuelle tællerregistreringer og den type meddelelse, der skal vises, hvis registreringer ligger uden for det angivne interval.</span><span class="sxs-lookup"><span data-stu-id="e2089-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="e2089-125">Se emnet [Tællere](../setup-for-objects/counters.md) vedrørende opsætning af tællere.</span><span class="sxs-lookup"><span data-stu-id="e2089-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
