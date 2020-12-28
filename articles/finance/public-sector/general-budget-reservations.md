---
title: Generelle budgetreservationer
description: Dette emne indeholder oplysninger om generelle budgetreservationer i den offentlige sektor.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: bd57319ed4ae6c57c106be1ad0fdc93fe1941d29
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407720"
---
# <a name="general-budget-reservations"></a><span data-ttu-id="d8bfd-103">Generelle budgetreservationer</span><span class="sxs-lookup"><span data-stu-id="d8bfd-103">General budget reservations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8bfd-104">En *generel budgetreservation* er et dokument, der undertiden også kaldes en *forpligtelse*.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-104">A *general budget reservation* is a document that is sometimes also referred to as a *commitment*.</span></span> <span data-ttu-id="d8bfd-105">Offentlige myndigheder bruger ofte dette dokument til at afsætte eller øremærke budgetterede midler, så de ikke er tilgængelige til andre formål.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-105">Public sector entities often use this document to set aside or earmark budgeted funds so that they aren't available for other purposes.</span></span> <span data-ttu-id="d8bfd-106">Disse reservationer foretages typisk før, eventuelle leverandører er valgt til indkøbet.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-106">Typically, these reservations are made before any vendors have been selected for the purchase.</span></span> <span data-ttu-id="d8bfd-107">Ved hjælp af generelle budgetreservationer kan en organisation udtrykkeligt spore planlagte udgifter til administrations- og rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-107">By using general budget reservations, an organization can explicitly track planned expenditures for management and reporting purposes.</span></span> <span data-ttu-id="d8bfd-108">Hver enkelt indkøbsrekvisition, indkøbsordre eller kreditorfaktura, der er genereret, kan knyttes til mindst én generel budgetreservation.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-108">Each purchase requisition, purchase order, or vendor invoice that is generated can be associated with at least one general budget reservation.</span></span>

<span data-ttu-id="d8bfd-109">Generelle budgetreservationer er kun tilgængelige, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="d8bfd-109">General budget reservations are available only if the following conditions are met:</span></span>

- <span data-ttu-id="d8bfd-110">Du har version 8.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-110">You have version 8.1 or later.</span></span>
- <span data-ttu-id="d8bfd-111">Konfigurationsnøglerne **Offentlig sektor**, **Behæftelsesproces** og **Budgetreservationsproces** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-111">The **Public sector**, **Encumbrance process**, and **Pre-encumbrance process** configuration keys are turned on.</span></span>
- <span data-ttu-id="d8bfd-112">Du bruger bogføringsdefinitioner.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-112">You're using posting definitions.</span></span> <span data-ttu-id="d8bfd-113">(Du behøver dog ikke at bruge bogføringsdefinitioner, hvis du ikke aktiverer rammeaftaler).</span><span class="sxs-lookup"><span data-stu-id="d8bfd-113">(However, you don't have to use posting definitions if you don't activate commitment accounting.)</span></span>
- <span data-ttu-id="d8bfd-114">Konfigurationen af budgetstyring er aktiveret og konfigureret, og budgetstyring er slået til.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-114">The Budget control configuration is activated and configured, and budget control is turned on.</span></span>

<span data-ttu-id="d8bfd-115">Generelle budgetreservationer indeholder linjer, der indeholder detaljer om formålet med reservationen og de planlagte reserverede midler.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-115">General budget reservations contain lines that provide details about the purpose of the reservation and the planned reserved funds.</span></span> <span data-ttu-id="d8bfd-116">Disse oplysninger omfatter reservationens start- og slutdato.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-116">These details include the start and end dates for the reservation.</span></span> <span data-ttu-id="d8bfd-117">Du kan tilføje, ændre og slette linjer.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-117">You can add, change, and delete lines.</span></span> <span data-ttu-id="d8bfd-118">Du kan også angive forskellige oplysninger, f.eks. den anmodede vare, valutaen, enhedsprisen og antallet og det samlede beløb.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-118">You can also specify various details, such as the item that is requested, the currency, the unit price and quantity, and the total amount.</span></span> <span data-ttu-id="d8bfd-119">Generelle budgetreservationer er beregnet til brug af enheder i den offentlige sektor.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-119">General budget reservations are intended to be used by public sector entities.</span></span>

<span data-ttu-id="d8bfd-120">Enheder i den private sektor bruger udtrykket *budgetreservation* til at tale om behæftelser eller budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-120">Private sector entities use the term *budget reservation* to talk about encumbrances or pre-encumbrances.</span></span> <span data-ttu-id="d8bfd-121">Men i modsætning til generelle budgetreservationer er disse budgetreservationer ikke dokumenter.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-121">However, unlike general budget reservations, those budgets reservations aren't documents.</span></span>

<span data-ttu-id="d8bfd-122">Du kan oprette forskellige typer generelle budgetreservationer for at angive forskellige egenskaber og krav baseret på dine indkøbsbehov.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-122">You can create different types of general budget reservation to specify various characteristics and requirements, based on your purchasing needs.</span></span> <span data-ttu-id="d8bfd-123">Specifikationerne omfatter den arbejdsgang, der bruges til reservationen, og standardværdier.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-123">The characteristics include the workflow that is used for the reservation, and default values.</span></span> <span data-ttu-id="d8bfd-124">Du opretter f.eks. tre reservationstyper.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-124">For example, you create three reservation types.</span></span> <span data-ttu-id="d8bfd-125">Du bruger én type til indkøbsrekvisitioner, en anden type til indkøbsordrer og endnu en type til kreditorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-125">You use one type for purchase requisitions, another type for purchase orders, and another type for vendor invoices.</span></span>

<span data-ttu-id="d8bfd-126">I den generelle budgetreservation kan du også få vist regnskabsfordelinger og kladdelinjerne for reskontro for posteringen.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-126">In the general budget reservation, you can also view accounting distributions and subledger journal lines for the transaction.</span></span>

<span data-ttu-id="d8bfd-127">Hvis du bruger projektregnskab, kan du aktivere sporing af bindende omkostninger for generelle budgetreservationer.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-127">If you use project accounting, you can turn on tracking of committed costs for general budget reservations.</span></span>

<span data-ttu-id="d8bfd-128">Du kan overføre generelle budgetreservationer fra det ene regnskabsår til det andet.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-128">You can carry over general budget reservations from one fiscal year to the next.</span></span> <span data-ttu-id="d8bfd-129">Du kan også lukke eller færdiggøre en afsluttet eller udløbet generel budgetreservation i slutningen af året.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-129">You can also close or finalize a completed or expired general budget reservation at the end of the year.</span></span>

<span data-ttu-id="d8bfd-130">En generel budgetreservation eftergives på forskellige måder, afhængigt af det dokument, der refererer til den:</span><span class="sxs-lookup"><span data-stu-id="d8bfd-130">A general budget reservation is relieved differently, depending on the document that references it:</span></span>

- <span data-ttu-id="d8bfd-131">Hvis dokumentet er en indkøbsordre, eftergives reservationen, når indkøbsordren er *bekræftet*.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-131">If the document is a purchase order, the reservation is relieved when the purchase order is *confirmed*.</span></span>
- <span data-ttu-id="d8bfd-132">Hvis dokumentet er en faktura, som ikke henviser til en indkøbsordre eller købsaftale, eftergives den generelle budgetreservationen, når fakturaen *bogføres*.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-132">If the document is an invoice, and it doesn't reference a purchase order or purchase agreement, the general budget reservation is relieved when the invoice is *posted*.</span></span>
- <span data-ttu-id="d8bfd-133">Hvis dokumentet er en indkøbsrekvisition, eftergives reservationen, når indkøbsrekvisitionen er *godkendt*.</span><span class="sxs-lookup"><span data-stu-id="d8bfd-133">If the document is a purchase requisition, the reservation is relieved when the purchase requisition is *approved*.</span></span>
