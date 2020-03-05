---
title: Infokoder og infokodegrupper
description: Denne artikel indeholder en oversigt over oplysninger om infokoder, infokodegrupper, og hvordan de bruges.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 046204d36e2fc7a69129aaf7fe027b2abc7e8dd9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022068"
---
# <a name="info-codes-and-info-code-groups"></a><span data-ttu-id="c264e-103">Infokoder og infokodegrupper</span><span class="sxs-lookup"><span data-stu-id="c264e-103">Info codes and info code groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c264e-104">Denne artikel indeholder en oversigt over oplysninger om infokoder, infokodegrupper, og hvordan de bruges.</span><span class="sxs-lookup"><span data-stu-id="c264e-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="c264e-105">Infokoder giver mulighed for at registrere data ved et kasseapparat (POS).</span><span class="sxs-lookup"><span data-stu-id="c264e-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="c264e-106">Du kan bruge infokoder til at bede kassereren om at angive oplysninger under forskellige handlinger på salgsstedet, f-eks. varesalg, varereturnering eller valg af debitorer.</span><span class="sxs-lookup"><span data-stu-id="c264e-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="c264e-107">Kassereren kan vælge input fra en liste eller angive den som en kode, et tal, en dato eller tekst.</span><span class="sxs-lookup"><span data-stu-id="c264e-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="c264e-108">Du kan knytte infokoder til foruddefinerede butikshandlinger, detailvarer, betalingsmetoder, kunder eller specifikke POS-aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c264e-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="c264e-109">Du kan bruge infokoder til at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="c264e-109">You can use info codes to do the following:</span></span>

- <span data-ttu-id="c264e-110">Registrere flere oplysninger på transaktionstidspunktet, som f.eks. et flynummer eller årsagen til en returnering.</span><span class="sxs-lookup"><span data-stu-id="c264e-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
- <span data-ttu-id="c264e-111">Bed kassereren ved kasseapparatet om at vælge priser på bestemte produkter på en liste.</span><span class="sxs-lookup"><span data-stu-id="c264e-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
- <span data-ttu-id="c264e-112">Knytte en underkode til en infokode, hvor kassereren bliver bedt om at angive input, når der udføres en bestemt aktivitet.</span><span class="sxs-lookup"><span data-stu-id="c264e-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="c264e-113">Når en kunde returnerer et produkt, kan du spørge kassereren om, hvorfor produktet returneres.</span><span class="sxs-lookup"><span data-stu-id="c264e-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="c264e-114">Du kan derefter bruge underkoder til at få vist en liste over årsager, som kassereren kan vælge imellem.</span><span class="sxs-lookup"><span data-stu-id="c264e-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
- <span data-ttu-id="c264e-115">Sælge et produkt som almindeligt salg, et salg med rabat eller et gratis produkt.</span><span class="sxs-lookup"><span data-stu-id="c264e-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
- <span data-ttu-id="c264e-116">Bede kassereren om at angive en værdi eller vælge fra en liste med underkoder, når kasseapparatets pengeskuffe åbnes, uden at der sælges noget.</span><span class="sxs-lookup"><span data-stu-id="c264e-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="c264e-117">Infokodegruppe</span><span class="sxs-lookup"><span data-stu-id="c264e-117">Info codes group</span></span>

<span data-ttu-id="c264e-118">I Commerce kan du oprette grupper af infokoder.</span><span class="sxs-lookup"><span data-stu-id="c264e-118">In Commerce, you can create groups of info codes.</span></span> <span data-ttu-id="c264e-119">Infokodegrupper giver fleksibilitet ved at give dig mulighed for at definere færre infokoder og derefter bruge dem på en mere alsidig måde.</span><span class="sxs-lookup"><span data-stu-id="c264e-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="c264e-120">Du kan bruge infokodegrupper på følgende måder:</span><span class="sxs-lookup"><span data-stu-id="c264e-120">You can use info code groups in the following ways:</span></span>

- <span data-ttu-id="c264e-121">Definere færre infokoder og nemt bruge dem igen.</span><span class="sxs-lookup"><span data-stu-id="c264e-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="c264e-122">Infokoder, der er inkluderet i infokodegrupper, har ingen foruddefinerede afhængigheder i forhold til andre infokoder.</span><span class="sxs-lookup"><span data-stu-id="c264e-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="c264e-123">Du kan medtage den samme infokode i flere infokodegrupper og derefter bruge prioritering for at vise de samme infokoder i en rækkefølge, der giver mening i en given situation.</span><span class="sxs-lookup"><span data-stu-id="c264e-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
- <span data-ttu-id="c264e-124">Sammenkæd infokoder med andre infokoder eller infokodegrupper for at indsamle oplysninger om et produkt eller en postering uden at skulle definere en separat infokode eller sammenkædet infokode for hvert scenarie.</span><span class="sxs-lookup"><span data-stu-id="c264e-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="c264e-125">Eksempler på infokoder</span><span class="sxs-lookup"><span data-stu-id="c264e-125">Info code examples</span></span>

<span data-ttu-id="c264e-126">**Eksempel 1: Genbrug infokoder**</span><span class="sxs-lookup"><span data-stu-id="c264e-126">**Example 1: Reuse info codes**</span></span>

<span data-ttu-id="c264e-127">Du kan sammenkæde infokæder på en måde, så hvis én infokode udløses, udløses en anden infokode omgående derefter.</span><span class="sxs-lookup"><span data-stu-id="c264e-127">You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="c264e-128">Når du f.eks. sælger bestemte produkter, foretrækker du, at ekspedienten tilbyder kunden at købe batterier eller en produktgaranti.</span><span class="sxs-lookup"><span data-stu-id="c264e-128">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="c264e-129">For andre produkter vil du gerne have, at ekspedienten spørger kunden, om han/hun vil købe batterier, og indhenter kundens postnummer.</span><span class="sxs-lookup"><span data-stu-id="c264e-129">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="c264e-130">Hvis du opretter sammenkædede infokoder for disse scenarier, skal du konfigurere alle variationer af infokoden, så kassereren bliver bedt om at spørge efter de rigtige oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c264e-130">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="c264e-131">Hvis du bruger infokodegrupper, kan almindelige infokoder, som f.eks. at spørge efter batterier, konfigureres én gang og derefter genbruges i flere infokodegrupper.</span><span class="sxs-lookup"><span data-stu-id="c264e-131">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="c264e-132">Du kan også bruge prioritering i infokodegrupperne for at identificere rækkefølgen, hvori anmodningerne vises.</span><span class="sxs-lookup"><span data-stu-id="c264e-132">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>

<span data-ttu-id="c264e-133">**Eksempel 2: Sammenkæd infokoder med infokodegrupper**</span><span class="sxs-lookup"><span data-stu-id="c264e-133">**Example 2: Link info codes to info code groups**</span></span>

<span data-ttu-id="c264e-134">Når du sælger bestemte produkter, f.eks. mobilenheder, vil det altid være i din interesse at indsamle bestemte oplysninger såsom telefonnummer, mobiludstyrs-id (MEID) og serienummer.</span><span class="sxs-lookup"><span data-stu-id="c264e-134">When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="c264e-135">Det vil dog også være i din interesse at indsamle forskellige oplysninger til en tablet i forhold til en mobiltelefon.</span><span class="sxs-lookup"><span data-stu-id="c264e-135">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="c264e-136">Du kan oprette en infokodegruppe, der omfatter anmodninger om telefonnummer, MEID og serienummeret, og derefter sammenkæde infokodegruppen med en individuel infokode.</span><span class="sxs-lookup"><span data-stu-id="c264e-136">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="c264e-137">Når den produktspecifikke infokode udløses, kan infokodegruppen udløses derefter, så du kan indsamle generelle data uden at skulle definere flere sæt af sammenkædede infokoder for hver enhed.</span><span class="sxs-lookup"><span data-stu-id="c264e-137">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>