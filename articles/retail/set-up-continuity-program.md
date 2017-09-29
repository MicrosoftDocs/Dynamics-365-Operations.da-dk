---
title: Oprette et kontinuitetsprogram for et callcenter
description: I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00504b62237ac4f121d603d5144ffa4e71956cc3
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="41fa5-103">Oprette et kontinuitetsprogram for et callcenter</span><span class="sxs-lookup"><span data-stu-id="41fa5-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="41fa5-104">I denne artikel beskrives det, hvordan du kan konfigurere et kontinuitetsprogram for et call center.</span><span class="sxs-lookup"><span data-stu-id="41fa5-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="41fa5-105">I et kontinuitetsprogram, som er også kendt som et tilbagevendende ordreprogram, modtagerne kunderne regelmæssigt produktleverancer i henhold til en foruddefineret tidsplan.</span><span class="sxs-lookup"><span data-stu-id="41fa5-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="41fa5-106">Hver leverance kan indeholde et andet produkt, f.eks. månedens bog i en bogklub, eller det samme produkt kan sendes flere gange.</span><span class="sxs-lookup"><span data-stu-id="41fa5-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="41fa5-107">Hvis du vil konfigurere et kontinuitetsprogram, skal du udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="41fa5-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="41fa5-108">Angiv kontinuitetsparametrene på siden **Call center-parametre**.</span><span class="sxs-lookup"><span data-stu-id="41fa5-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="41fa5-109">Opret et kontinuitetsprogram, som angiver oplysninger som f.eks. betalingsplan, tidspunktet for leverancerne og om fakturering skal ske på forhånd.</span><span class="sxs-lookup"><span data-stu-id="41fa5-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="41fa5-110">Du skal også tilføje en liste over produkter, der indgår i kontinuitetsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="41fa5-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="41fa5-111">Hvert produkt modtager et hændelses-id-nummer, der tildeles fortløbende, startende med 1.</span><span class="sxs-lookup"><span data-stu-id="41fa5-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="41fa5-112">Hændelsen id'erne bestemmer den rækkefølge, produkter sendes i.</span><span class="sxs-lookup"><span data-stu-id="41fa5-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="41fa5-113">Hvis kunder modtager et andet produkt i hver leverance, sendes produkterne i sekventiel rækkefølge baseret på deres hændelses-id'er, begyndende med den aktuelle hændelse.</span><span class="sxs-lookup"><span data-stu-id="41fa5-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="41fa5-114">Hvis kunder modtager det samme produkt i hver leverance, indeholder listen kun ét produkt, der har et hændelses-id.</span><span class="sxs-lookup"><span data-stu-id="41fa5-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="41fa5-115">Den samme hændelse forekommer flere gange.</span><span class="sxs-lookup"><span data-stu-id="41fa5-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="41fa5-116">Du kan angive, hvor mange gange hver hændelse gentages.</span><span class="sxs-lookup"><span data-stu-id="41fa5-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="41fa5-117">Opret et overordnet produkt, der repræsenterer det kontinuitetsprogram, du oprettede i opgave 2.</span><span class="sxs-lookup"><span data-stu-id="41fa5-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="41fa5-118">Hvis du føjer produktet til en salgsordre, åbnes siden **Kontinuitet**.</span><span class="sxs-lookup"><span data-stu-id="41fa5-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="41fa5-119">Du kan derefter bruge denne side til at oprette den faktiske kontinuitetsrækkefølge.</span><span class="sxs-lookup"><span data-stu-id="41fa5-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="41fa5-120">Det overordnede produkt angiver ikke de enkelte produkter, som kunden modtager i hver leverance.</span><span class="sxs-lookup"><span data-stu-id="41fa5-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="41fa5-121">Når du har oprettet et kontinuitetsprogram som beskrevet ovenfor , kan du oprette en kontinuitetsordre for en debitor.</span><span class="sxs-lookup"><span data-stu-id="41fa5-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="41fa5-122">Du er muligvis nødt til at udføre følgende disse ekstra vedligeholdelsesopgaver.</span><span class="sxs-lookup"><span data-stu-id="41fa5-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="41fa5-123">**Opdater kontinuitetens aktuelle hændelsesperiode** – Opret et batchjob, der fortæller systemet, hvad den aktuelle hændelsesperiode er.</span><span class="sxs-lookup"><span data-stu-id="41fa5-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="41fa5-124">**Opret underordnede kontinuitetsordrer** – Opret underordnede ordrer fra den overordnede kontinuitetsordre.</span><span class="sxs-lookup"><span data-stu-id="41fa5-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="41fa5-125">**Behandl kontinuitetsbetalinger** – Behandl fakturering og meddelelser om betalinger, der er knyttet til kontinuitetssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="41fa5-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="41fa5-126">**Udvid om nødvendigt kontinuitetslinjer** – Udvid det antal gange, en kontinuitetshændelse kan gentages.</span><span class="sxs-lookup"><span data-stu-id="41fa5-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="41fa5-127">Gentagelsen af forsendelser kan derefter går ud over den grænse, der er angivet i feltet **Grænse for gentagelse af kontinuitet** i call center-parametrene.</span><span class="sxs-lookup"><span data-stu-id="41fa5-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="41fa5-128">**Udfør om nødvendigt en kontinuitetsopdatering** – Synkroniser ændringer mellem kontinuitetsprogrammet og de overordnede kontinuitetssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="41fa5-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="41fa5-129">**Luk overordnede kontinuitetslinjer og ordrer** – Luk kontinuitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="41fa5-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





