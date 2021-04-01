---
title: Oprette kontinuitetsprogrammer for callcentre
description: I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2428cafc45f074f7e2b4c3e59877079b8c1d4a92
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242955"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="c59f2-103">Oprette kontinuitetsprogrammer for callcentre</span><span class="sxs-lookup"><span data-stu-id="c59f2-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c59f2-104">I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.</span><span class="sxs-lookup"><span data-stu-id="c59f2-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="c59f2-105">I et kontinuitetsprogram, som er også kendt som et tilbagevendende ordreprogram, modtagerne kunderne regelmæssigt produktleverancer i henhold til en foruddefineret tidsplan.</span><span class="sxs-lookup"><span data-stu-id="c59f2-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="c59f2-106">Hver leverance kan indeholde et andet produkt, f.eks. månedens bog i en bogklub, eller det samme produkt kan sendes flere gange.</span><span class="sxs-lookup"><span data-stu-id="c59f2-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="c59f2-107">Hvis du vil konfigurere et kontinuitetsprogram, skal du udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="c59f2-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="c59f2-108">Angiv kontinuitetsparametrene på siden **Call center-parametre**.</span><span class="sxs-lookup"><span data-stu-id="c59f2-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="c59f2-109">Opret et kontinuitetsprogram, som angiver oplysninger som f.eks. betalingsplan, tidspunktet for leverancerne og om fakturering skal ske på forhånd.</span><span class="sxs-lookup"><span data-stu-id="c59f2-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="c59f2-110">Du skal også tilføje en liste over produkter, der indgår i kontinuitetsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="c59f2-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="c59f2-111">Hvert produkt modtager et hændelses-id-nummer, der tildeles fortløbende, startende med 1.</span><span class="sxs-lookup"><span data-stu-id="c59f2-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="c59f2-112">Hændelsen id'erne bestemmer den rækkefølge, produkter sendes i.</span><span class="sxs-lookup"><span data-stu-id="c59f2-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="c59f2-113">Hvis kunder modtager et andet produkt i hver leverance, sendes produkterne i sekventiel rækkefølge baseret på deres hændelses-id'er, begyndende med den aktuelle hændelse.</span><span class="sxs-lookup"><span data-stu-id="c59f2-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="c59f2-114">Hvis kunder modtager det samme produkt i hver leverance, indeholder listen kun ét produkt, der har et hændelses-id.</span><span class="sxs-lookup"><span data-stu-id="c59f2-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="c59f2-115">Den samme hændelse forekommer flere gange.</span><span class="sxs-lookup"><span data-stu-id="c59f2-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="c59f2-116">Du kan angive, hvor mange gange hver hændelse gentages.</span><span class="sxs-lookup"><span data-stu-id="c59f2-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="c59f2-117">Opret et overordnet produkt, der repræsenterer det kontinuitetsprogram, du oprettede i opgave 2.</span><span class="sxs-lookup"><span data-stu-id="c59f2-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="c59f2-118">Hvis du føjer produktet til en salgsordre, åbnes siden **Kontinuitet**.</span><span class="sxs-lookup"><span data-stu-id="c59f2-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="c59f2-119">Du kan derefter bruge denne side til at oprette den faktiske kontinuitetsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="c59f2-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="c59f2-120">Det overordnede produkt angiver ikke de enkelte produkter, som kunden modtager i hver leverance.</span><span class="sxs-lookup"><span data-stu-id="c59f2-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="c59f2-121">Når du har oprettet et kontinuitetsprogram som beskrevet ovenfor , kan du oprette en kontinuitetsordre for en debitor.</span><span class="sxs-lookup"><span data-stu-id="c59f2-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="c59f2-122">Du er muligvis nødt til at udføre følgende disse ekstra vedligeholdelsesopgaver.</span><span class="sxs-lookup"><span data-stu-id="c59f2-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="c59f2-123">**Opdater kontinuitetens aktuelle hændelsesperiode** – Opret et batchjob, der fortæller systemet, hvad den aktuelle hændelsesperiode er.</span><span class="sxs-lookup"><span data-stu-id="c59f2-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="c59f2-124">**Opret underordnede kontinuitetsordrer** – Opret underordnede ordrer fra den overordnede kontinuitetsordre.</span><span class="sxs-lookup"><span data-stu-id="c59f2-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="c59f2-125">**Behandl kontinuitetsbetalinger** – Behandl fakturering og meddelelser om betalinger, der er knyttet til kontinuitetssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c59f2-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="c59f2-126">**Udvid om nødvendigt kontinuitetslinjer** – Udvid det antal gange, en kontinuitetshændelse kan gentages.</span><span class="sxs-lookup"><span data-stu-id="c59f2-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="c59f2-127">Gentagelsen af forsendelser kan derefter går ud over den grænse, der er angivet i feltet **Grænse for gentagelse af kontinuitet** i call center-parametrene.</span><span class="sxs-lookup"><span data-stu-id="c59f2-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="c59f2-128">**Udfør om nødvendigt en kontinuitetsopdatering** – Synkroniser ændringer mellem kontinuitetsprogrammet og de overordnede kontinuitetssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c59f2-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="c59f2-129">**Luk overordnede kontinuitetslinjer og ordrer** – Luk kontinuitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="c59f2-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]