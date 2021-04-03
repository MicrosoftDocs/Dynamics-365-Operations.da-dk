---
title: Oversigt over kredit og opkrævninger
description: Dette emne indeholder en oversigt over funktionerne for kredit og opkrævninger.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6bba210bc282e031606acca4ad73e18d8b42167d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257627"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="1a790-103">Oversigt over kredit og opkrævninger</span><span class="sxs-lookup"><span data-stu-id="1a790-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a790-104">Du kan administrere kreditmaksimum for kunderne og udføre rykkeraktiviteter, når det bliver nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="1a790-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="1a790-105">Kreditstyring</span><span class="sxs-lookup"><span data-stu-id="1a790-105">Credit management</span></span>

<span data-ttu-id="1a790-106">Du kan bruge kundekreditstyring til at administrere kreditmaksimum og styre forløbet af salgsordrer via bogføringsprocessen ud fra de kreditregler, du opretter.</span><span class="sxs-lookup"><span data-stu-id="1a790-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="1a790-107">Kreditstyringsprocessen kan omfatte et eller flere af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="1a790-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="1a790-108">Opdatering af kreditattributter for kunder for at give yderligere oplysninger om deres kreditværdighed.</span><span class="sxs-lookup"><span data-stu-id="1a790-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="1a790-109">Oprettelse af kreditmaksimum for kunder ved hjælp af kreditmaksimumreguleringer.</span><span class="sxs-lookup"><span data-stu-id="1a790-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="1a790-110">Oprettelse af midlertidigt kreditmaksimum for kunder ved hjælp af kreditmaksimumreguleringer.</span><span class="sxs-lookup"><span data-stu-id="1a790-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="1a790-111">På denne måde kan du midlertidigt øge eller mindske kundens kreditmaksimum på basis af forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="1a790-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="1a790-112">Tilføjelse af oplysninger, der kan påvirke kreditmaksimum, f.eks. oplysninger om forsikring og garantier.</span><span class="sxs-lookup"><span data-stu-id="1a790-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="1a790-113">Oprettelse af kundekreditgrupper, der knytter kunder sammen, så de deler ét kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="1a790-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="1a790-114">Tildeling af risikovurderinger til kunderne med efterfølgende anvendelse af vurderinger til automatisk generering af kreditmaksimum for disse kunder via kreditmaksimumreguleringer.</span><span class="sxs-lookup"><span data-stu-id="1a790-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="1a790-115">Oprettelse af blokeringsregler, der sætter en ordre på hold under en eller flere bogføringsprocesser, baseret på faktorer som risiko, betalingsbetingelser, kreditmaksimum, forfaldne beløb og den procentdel af kreditmaksimum, der er brugt.</span><span class="sxs-lookup"><span data-stu-id="1a790-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="1a790-116">Administration af en liste over salgsordrer, der er på hold, gennemgang af årsagerne til ventepositionen og afhjælpning af problemerne.</span><span class="sxs-lookup"><span data-stu-id="1a790-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="1a790-117">Frigivelse af salgsordrer, så de fortsætter gennem bogføringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1a790-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="1a790-118">Konfiguration af en arbejdsgang for at administrere godkendelse af ændringer af kreditmaksimum og salgsordrefrigivelser.</span><span class="sxs-lookup"><span data-stu-id="1a790-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="1a790-119">Opkrævningsstyring</span><span class="sxs-lookup"><span data-stu-id="1a790-119">Collections management</span></span>

<span data-ttu-id="1a790-120">Siden **Rykkere** indeholder en centraliseret visning til administration af oplysninger om rykkere for debitorer.</span><span class="sxs-lookup"><span data-stu-id="1a790-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="1a790-121">De opkrævningsansvarlige kan bruge denne centraliserede visning til at administrere rykkere.</span><span class="sxs-lookup"><span data-stu-id="1a790-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="1a790-122">Inkassatorerne kan begynde rykkerprocessen enten fra debitorlisten, der genereres ved hjælp af foruddefinerede rykkerkriterier, eller fra siden **Debitorer**.</span><span class="sxs-lookup"><span data-stu-id="1a790-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="1a790-123">Før du begynder at oprette eller arbejde med rykkere, skal du kende følgende begreber:</span><span class="sxs-lookup"><span data-stu-id="1a790-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="1a790-124">Aldersfordelte øjebliksbillede for debitorer indeholder saldooplysninger på et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="1a790-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="1a790-125">Kundepuljer for rykkere hjælper dig med at organisere dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="1a790-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="1a790-126">Inkassatorer kan have deres egne kundepuljer.</span><span class="sxs-lookup"><span data-stu-id="1a790-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="1a790-127">Listesider organiserer kunder, aktiviteter og sager for rykkere.</span><span class="sxs-lookup"><span data-stu-id="1a790-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="1a790-128">Alle rykkeroplysningerne for en debitor findes på en side, og du kan udføre handlinger fra den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="1a790-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="1a790-129">Renter og gebyrer kan frafaldes, genindføres eller tilbageføres i ét trin.</span><span class="sxs-lookup"><span data-stu-id="1a790-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="1a790-130">Afskrivningsposteringer kan oprettes i ét trin.</span><span class="sxs-lookup"><span data-stu-id="1a790-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="1a790-131">Betalinger med ikke tilstrækkelige midler – NSF-betalinger (Non-sufficient Funds – USA) – kan behandles i ét trin.</span><span class="sxs-lookup"><span data-stu-id="1a790-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="1a790-132">Beskrivelser af disse begreber finder du i [Nøglebegreber for opkrævningsstyring](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="1a790-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a790-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1a790-133">Additional resources</span></span>

[<span data-ttu-id="1a790-134">Konfiguration af parametre for kundekreditstyring</span><span class="sxs-lookup"><span data-stu-id="1a790-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="1a790-135">Konfigurationsoplysninger for kundekreditstyring</span><span class="sxs-lookup"><span data-stu-id="1a790-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="1a790-136">Tilføje kreditstyringsoplysninger for en kunde</span><span class="sxs-lookup"><span data-stu-id="1a790-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="1a790-137">Kundekreditgrupper</span><span class="sxs-lookup"><span data-stu-id="1a790-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="1a790-138">Reguleringer af kundekreditmaksimum</span><span class="sxs-lookup"><span data-stu-id="1a790-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="1a790-139">Kredithold for salgsordrer</span><span class="sxs-lookup"><span data-stu-id="1a790-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="1a790-140">Periodiske opgaver for kundekreditstyring</span><span class="sxs-lookup"><span data-stu-id="1a790-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]