---
title: Angive standardbeskrivelser til automatisk bogføring
description: Dette emne forklarer, hvordan du kan konfigurere den standardtekst, der bruges til at beskrive de regnskabsposter, der bogføres automatisk i finans. Du kan angive standardbeskrivelsesteksten ved hjælp af en fritekst eller ved at vælge faste variabler.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622683"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="6f2e7-104">Angive standardbeskrivelser til automatisk bogføring</span><span class="sxs-lookup"><span data-stu-id="6f2e7-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="6f2e7-105">Dette emne forklarer, hvordan du kan konfigurere den standardtekst, der bruges til at beskrive de regnskabsposter, der bogføres automatisk i finans.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="6f2e7-106">Du kan angive standardbeskrivelsesteksten ved hjælp af en fritekst eller ved at vælge faste variabler.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="6f2e7-107">For visse transaktionstyper kan du i nogle lande/områder medtage tekst fra felter i Microsoft Dynamics AX-databasen, der er relateret til disse transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="6f2e7-108">Du kan finde en liste over transaktionstyperne og lande og områder i afsnittet [Valgfrit: Føje anden tekst til standardbeskrivelser](#optional-add-other-text-to-default-descriptions) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="6f2e7-109">Konfigurere standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="6f2e7-109">Set up default descriptions</span></span>

1. <span data-ttu-id="6f2e7-110">Gå til **Virksomhedsadministration** \> **Opsætning** \> **Standardbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="6f2e7-111">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="6f2e7-112">I feltet **Beskrivelse** skal du vælge den type transaktion, der skal oprettes en standardbeskrivelse til.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="6f2e7-113">I feltet **Sprog** skal du vælge det sprog, som denne beskrivelse gælder for.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="6f2e7-114">Indtast standardbeskrivelsen i feltet **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="6f2e7-115">Du kan skrive tekst i feltet, eller du kan bruge en eller flere af følgende fritekstvariabler:</span><span class="sxs-lookup"><span data-stu-id="6f2e7-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="6f2e7-116">**%1** – Tilføj transaktionsdatoen.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="6f2e7-117">**%2** – Tilføj en identifikator, der svarer til den dokumenttype, der bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="6f2e7-118">I forbindelse med transaktionstyper, der er knyttet til fakturaer, tilføjer variablen **%2** f.eks. fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="6f2e7-119">**%3** – Tilføj en identifikator, der er relateret til den dokumenttype, der bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="6f2e7-120">I forbindelse med transaktionstyper, der er knyttet til fakturaer, tilføjer variablen **%3** f.eks. debitorkontonummer.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="6f2e7-121">Valgfrit: Føje anden tekst til standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="6f2e7-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="6f2e7-122">For visse transaktionstyper kan du i nogle lande/områder medtage tekst i standardbeskrivelser, der kommer fra felter i dine data, der er relateret til disse transaktionstyper.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="6f2e7-123">Følgende lister viser de transaktionstyper og lande/områder, hvor denne indstilling er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="6f2e7-124">**Posteringstyper**</span><span class="sxs-lookup"><span data-stu-id="6f2e7-124">**Transaction types**</span></span>

<span data-ttu-id="6f2e7-125">Du kan føje anden tekst til standardbeskrivelser for transaktionstyper, der vedrører følgende dokumenttyper:</span><span class="sxs-lookup"><span data-stu-id="6f2e7-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="6f2e7-126">Debitorfakturaer</span><span class="sxs-lookup"><span data-stu-id="6f2e7-126">Customer invoices</span></span>
- <span data-ttu-id="6f2e7-127">Kreditnotaer til kunden</span><span class="sxs-lookup"><span data-stu-id="6f2e7-127">Customer credit notes</span></span>
- <span data-ttu-id="6f2e7-128">Debitorkontantbetalinger</span><span class="sxs-lookup"><span data-stu-id="6f2e7-128">Customer cash payments</span></span>
- <span data-ttu-id="6f2e7-129">Kreditorbetalinger</span><span class="sxs-lookup"><span data-stu-id="6f2e7-129">Vendor payments</span></span>
- <span data-ttu-id="6f2e7-130">Salgsordrer</span><span class="sxs-lookup"><span data-stu-id="6f2e7-130">Sales orders</span></span>
- <span data-ttu-id="6f2e7-131">Indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="6f2e7-131">Purchase orders</span></span>
- <span data-ttu-id="6f2e7-132">Lagerkladder</span><span class="sxs-lookup"><span data-stu-id="6f2e7-132">Inventory journals</span></span>
- <span data-ttu-id="6f2e7-133">Varedisponering</span><span class="sxs-lookup"><span data-stu-id="6f2e7-133">Master planning (MRP)</span></span>
- <span data-ttu-id="6f2e7-134">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="6f2e7-134">Fixed assets</span></span>

<span data-ttu-id="6f2e7-135">**Lande og områder**</span><span class="sxs-lookup"><span data-stu-id="6f2e7-135">**Countries and regions**</span></span>

<span data-ttu-id="6f2e7-136">Denne indstilling er kun tilgængelig for følgende lande og områder:</span><span class="sxs-lookup"><span data-stu-id="6f2e7-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="6f2e7-137">Brasilien</span><span class="sxs-lookup"><span data-stu-id="6f2e7-137">Brazil</span></span>
- <span data-ttu-id="6f2e7-138">Kina</span><span class="sxs-lookup"><span data-stu-id="6f2e7-138">China</span></span>
- <span data-ttu-id="6f2e7-139">Tjekkiet</span><span class="sxs-lookup"><span data-stu-id="6f2e7-139">Czech Republic</span></span>
- <span data-ttu-id="6f2e7-140">Østeuropa</span><span class="sxs-lookup"><span data-stu-id="6f2e7-140">Eastern Europe</span></span>
- <span data-ttu-id="6f2e7-141">Ungarn</span><span class="sxs-lookup"><span data-stu-id="6f2e7-141">Hungary</span></span>
- <span data-ttu-id="6f2e7-142">Indien</span><span class="sxs-lookup"><span data-stu-id="6f2e7-142">India</span></span>
- <span data-ttu-id="6f2e7-143">Japan</span><span class="sxs-lookup"><span data-stu-id="6f2e7-143">Japan</span></span>
- <span data-ttu-id="6f2e7-144">Litauen</span><span class="sxs-lookup"><span data-stu-id="6f2e7-144">Lithuania</span></span>
- <span data-ttu-id="6f2e7-145">Letland</span><span class="sxs-lookup"><span data-stu-id="6f2e7-145">Latvia</span></span>
- <span data-ttu-id="6f2e7-146">Polen</span><span class="sxs-lookup"><span data-stu-id="6f2e7-146">Poland</span></span>
- <span data-ttu-id="6f2e7-147">Rusland</span><span class="sxs-lookup"><span data-stu-id="6f2e7-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="6f2e7-148">Føje tekst til standardbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="6f2e7-148">Add text to default descriptions</span></span>

<span data-ttu-id="6f2e7-149">Når du har fuldført trinnene i afsnittet [Konfigurere standardbeskrivelser](#set-up-default-descriptions) tidligere i dette emne, skal du følge disse trin for at føje anden tekst til standardbeskrivelserne.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="6f2e7-150">Vælg **Tilføj** i oversigtspanelet **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="6f2e7-151">I feltet **Referencetabel** skal du vælge den databasetabel, hvorfra der skal føjes parameterdata til beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="6f2e7-152">I feltet **Referencefelt** skal du vælge det felt, hvorfra der skal føjes parameterdata til beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="6f2e7-153">Gentag trin 1-3 for at tilføje flere parametre.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-153">Repeat steps 1 through 3 to add more parameters.</span></span>
