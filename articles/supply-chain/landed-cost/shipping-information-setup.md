---
title: Opsætning af forsendelsesoplysninger
description: Dette emne beskriver, hvordan du konfigurerer forsendelsesoplysninger for modulet Landingsomkostninger.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500928"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="cc67a-103">Opsætning af forsendelsesoplysninger</span><span class="sxs-lookup"><span data-stu-id="cc67a-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cc67a-104">Dette emne beskriver, hvordan du konfigurerer forsendelsesoplysninger for modulet **Landingsomkostninger**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="cc67a-105">Beskrivelse af varer</span><span class="sxs-lookup"><span data-stu-id="cc67a-105">Description of goods</span></span>

<span data-ttu-id="cc67a-106">Beskrivelser af varer gør det lettere at identificere en fragt, forsendelsescontainer eller varefolio og varerne i den.</span><span class="sxs-lookup"><span data-stu-id="cc67a-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="cc67a-107">Du kan vælge en beskrivelse af varerne i forsendelsescontainerhovedet eller foliohovedet.</span><span class="sxs-lookup"><span data-stu-id="cc67a-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="cc67a-108">Hvis du vil arbejde med beskrivelser af varer, skal du gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Beskrivelse af varer**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="cc67a-109">Her kan du se, åbne, oprette og slette poster til varebeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="cc67a-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="cc67a-110">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="cc67a-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="cc67a-111">Felt</span><span class="sxs-lookup"><span data-stu-id="cc67a-111">Field</span></span> | <span data-ttu-id="cc67a-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-112">Description</span></span> |
|---|---|
| <span data-ttu-id="cc67a-113">Beskrivelse af varer</span><span class="sxs-lookup"><span data-stu-id="cc67a-113">Description of goods</span></span> | <span data-ttu-id="cc67a-114">Angiv et entydigt id-navn/-nummer for den varetype, som skal bruge denne beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="cc67a-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="cc67a-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-115">Description</span></span> | <span data-ttu-id="cc67a-116">Angiv en beskrivelse af varetypen i denne kategori.</span><span class="sxs-lookup"><span data-stu-id="cc67a-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="cc67a-117">Fartøjer</span><span class="sxs-lookup"><span data-stu-id="cc67a-117">Vessels</span></span>

<span data-ttu-id="cc67a-118">Et fartøj er det entydige navn på et skib eller fartøj, som fragtfirmaet eller agenturet bruger.</span><span class="sxs-lookup"><span data-stu-id="cc67a-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="cc67a-119">Når du opretter en fragt, skal du altid vælge eller angive et fartøj for den.</span><span class="sxs-lookup"><span data-stu-id="cc67a-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="cc67a-120">Hvis du ofte bruger de samme fartøjer, kan du gøre det hurtigere og nemmere at oprette en ny fragt ved at oprette en skibspost for hver af dem, hvilket giver brugerne mulighed for at vælge fartøjet på en liste i stedet for at angive navnet eller nummeret manuelt hver gang.</span><span class="sxs-lookup"><span data-stu-id="cc67a-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="cc67a-121">Du kan arbejde med fartøjer ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Fartøjer**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="cc67a-122">Her kan du se, åbne, oprette og slette poster til fartøjer.</span><span class="sxs-lookup"><span data-stu-id="cc67a-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="cc67a-123">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="cc67a-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="cc67a-124">Felt</span><span class="sxs-lookup"><span data-stu-id="cc67a-124">Field</span></span> | <span data-ttu-id="cc67a-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-125">Description</span></span> |
|---|---|
| <span data-ttu-id="cc67a-126">Fartøj</span><span class="sxs-lookup"><span data-stu-id="cc67a-126">Vessel</span></span> | <span data-ttu-id="cc67a-127">Angiv et entydigt id-navn/nummer for det fartøj, der skal bruges til transport af varer i en fragt.</span><span class="sxs-lookup"><span data-stu-id="cc67a-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="cc67a-128">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-128">Description</span></span> | <span data-ttu-id="cc67a-129">Angiv en beskrivelse af fartøjet.</span><span class="sxs-lookup"><span data-stu-id="cc67a-129">Enter a description of the vessel.</span></span> <span data-ttu-id="cc67a-130">Denne beskrivelse identificerer typisk navnet på skibet og fragtfirmaet/-agenten.</span><span class="sxs-lookup"><span data-stu-id="cc67a-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="cc67a-131">Leveringsmåde</span><span class="sxs-lookup"><span data-stu-id="cc67a-131">Mode of delivery</span></span> | <span data-ttu-id="cc67a-132">Vælg den leveringsmåde, som fartøjet anvender (f.eks. _Luft_, _Hav_ eller _Tog_).</span><span class="sxs-lookup"><span data-stu-id="cc67a-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="cc67a-133">Eksportører</span><span class="sxs-lookup"><span data-stu-id="cc67a-133">Exporters</span></span>

<span data-ttu-id="cc67a-134">Hver eksportørpost identificerer en leverandør eller eksportør, der kan defineres som leverandøren af en fragt.</span><span class="sxs-lookup"><span data-stu-id="cc67a-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="cc67a-135">Eksportøren kan tilknyttes en fragt og bruges til rapportering.</span><span class="sxs-lookup"><span data-stu-id="cc67a-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="cc67a-136">Du kan arbejde med eksportører ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Eksportører**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="cc67a-137">Her kan du se, åbne, oprette og slette poster til eksportører.</span><span class="sxs-lookup"><span data-stu-id="cc67a-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="cc67a-138">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="cc67a-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="cc67a-139">Felt</span><span class="sxs-lookup"><span data-stu-id="cc67a-139">Field</span></span> | <span data-ttu-id="cc67a-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-140">Description</span></span> |
|---|---|
| <span data-ttu-id="cc67a-141">Eksportør</span><span class="sxs-lookup"><span data-stu-id="cc67a-141">Exporter</span></span> | <span data-ttu-id="cc67a-142">Angiv et entydigt id-navn/nummer for eksportøren af de varer, der skal transporteres i en fragt.</span><span class="sxs-lookup"><span data-stu-id="cc67a-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="cc67a-143">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-143">Description</span></span> | <span data-ttu-id="cc67a-144">Angiv en beskrivelse af eksportøren.</span><span class="sxs-lookup"><span data-stu-id="cc67a-144">Enter a description of the exporter.</span></span> <span data-ttu-id="cc67a-145">Denne beskrivelse identificerer typisk det fulde navn på fragtfirmaet/-agenten.</span><span class="sxs-lookup"><span data-stu-id="cc67a-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="cc67a-146">Varekoder</span><span class="sxs-lookup"><span data-stu-id="cc67a-146">Commodity codes</span></span>

<span data-ttu-id="cc67a-147">Du kan bruge varekoder som en hjælp ved identifikation i tolden og til beregning af toldsatser for varer i en fragt.</span><span class="sxs-lookup"><span data-stu-id="cc67a-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="cc67a-148">Du kan vælge varekoder på siden **Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="cc67a-149">Du kan arbejde med varekoder ved at gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Varekoder**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="cc67a-150">Her kan du se, åbne, oprette og slette poster til varekoder.</span><span class="sxs-lookup"><span data-stu-id="cc67a-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="cc67a-151">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="cc67a-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="cc67a-152">Felt</span><span class="sxs-lookup"><span data-stu-id="cc67a-152">Field</span></span> | <span data-ttu-id="cc67a-153">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-153">Description</span></span> |
|---|---|
| <span data-ttu-id="cc67a-154">Varekode</span><span class="sxs-lookup"><span data-stu-id="cc67a-154">Commodity code</span></span> | <span data-ttu-id="cc67a-155">Angiv en entydig kode for denne varetype.</span><span class="sxs-lookup"><span data-stu-id="cc67a-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="cc67a-156">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-156">Description</span></span> | <span data-ttu-id="cc67a-157">Angiv en beskrivelse af varetypen.</span><span class="sxs-lookup"><span data-stu-id="cc67a-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="cc67a-158">Toldbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-158">Customs description</span></span>

<span data-ttu-id="cc67a-159">Toldbeskrivelser gør det lettere at identificere varer til toldformål.</span><span class="sxs-lookup"><span data-stu-id="cc67a-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="cc67a-160">Du kan vælge en toldbeskrivelse på siden **Frigivne produkter** eller på indkøbsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="cc67a-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="cc67a-161">Hvis du vil arbejde med toldbeskrivelser, skal du gå til **Landingsomkostninger \> Opsætning af forsendelsesoplysninger \> Toldbeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cc67a-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="cc67a-162">Her kan du se, åbne, oprette og slette poster til toldbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="cc67a-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="cc67a-163">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="cc67a-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="cc67a-164">Felt</span><span class="sxs-lookup"><span data-stu-id="cc67a-164">Field</span></span> | <span data-ttu-id="cc67a-165">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-165">Description</span></span> |
|---|---|
| <span data-ttu-id="cc67a-166">Toldbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-166">Customs description</span></span> | <span data-ttu-id="cc67a-167">Angiv en entydig kode for denne type af toldklassifikation.</span><span class="sxs-lookup"><span data-stu-id="cc67a-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="cc67a-168">Ofte vil denne kode være den officielle beskrivelse, der gives af en toldmyndighed for beskrivelsen og den kvalitative værdi af varerne.</span><span class="sxs-lookup"><span data-stu-id="cc67a-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="cc67a-169">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc67a-169">Description</span></span> | <span data-ttu-id="cc67a-170">Indtast en beskrivelse af toldklassifikationen.</span><span class="sxs-lookup"><span data-stu-id="cc67a-170">Enter a description of the customs classification.</span></span> |
