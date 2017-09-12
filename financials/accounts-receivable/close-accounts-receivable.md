---
title: Luk Debitor
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2b2e827df0c679855af9624f8a2fb36cb23f359a
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="fb130-102">Luk Debitor</span><span class="sxs-lookup"><span data-stu-id="fb130-102">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="fb130-103">Følgende tabel indeholder de sider, der understøtter forretningsprocessen for afslutning af Debitor.</span><span class="sxs-lookup"><span data-stu-id="fb130-103">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="fb130-104">Hvis du vil åbne nogle af de sider, der er i følgende tabel, skal du angive oplysninger eller parameterindstillinger.</span><span class="sxs-lookup"><span data-stu-id="fb130-104">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="fb130-105">**Opgave for forretningsproceskomponent**</span><span class="sxs-lookup"><span data-stu-id="fb130-105">**Business process component task**</span></span>                   

<span data-ttu-id="fb130-106">Lukke perioder i finansregnskabet</span><span class="sxs-lookup"><span data-stu-id="fb130-106">Close periods in the general ledger</span></span>

| <span data-ttu-id="fb130-107">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="fb130-107">Page name</span></span>                            | <span data-ttu-id="fb130-108">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="fb130-108">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="fb130-109">Batchjob</span><span class="sxs-lookup"><span data-stu-id="fb130-109">Batch job</span></span>                             | <span data-ttu-id="fb130-110">Få vist eller opret batchjob.</span><span class="sxs-lookup"><span data-stu-id="fb130-110">View or create batch jobs.</span></span> <span data-ttu-id="fb130-111">Kørslerne kan ikke fuldføres, og du vil sikre, at al bogføring er udført.</span><span class="sxs-lookup"><span data-stu-id="fb130-111">Batch jobs might not be completed, and you want make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="fb130-112">Bekræft salgsordre</span><span class="sxs-lookup"><span data-stu-id="fb130-112">Confirm sales order</span></span>                   | <span data-ttu-id="fb130-113">Opdater salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fb130-113">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="fb130-114">Kursregulering</span><span class="sxs-lookup"><span data-stu-id="fb130-114">Foreign currency revaluation</span></span>          | <span data-ttu-id="fb130-115">Opret posteringer, som opdaterer værdien af åbne debitorposteringer i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="fb130-115">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="fb130-116">Journal</span><span class="sxs-lookup"><span data-stu-id="fb130-116">Journal</span></span>                              | <span data-ttu-id="fb130-117">Bogfør fakturaer, betalinger og egenveksler.</span><span class="sxs-lookup"><span data-stu-id="fb130-117">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="fb130-118">Kladdebilag</span><span class="sxs-lookup"><span data-stu-id="fb130-118">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="fb130-119">**Betalingskladde** – Opret, behandl og bogfør betalinger.</span><span class="sxs-lookup"><span data-stu-id="fb130-119">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="fb130-120">**Udsted vekseljournal** – Bogfør veksler.</span><span class="sxs-lookup"><span data-stu-id="fb130-120">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="fb130-121">**Protester vekseljournal** – Bogfør protesterede veksler.</span><span class="sxs-lookup"><span data-stu-id="fb130-121">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="fb130-122">**Genudsted vekseljournal** – Bogfør genudstedte veksler.</span><span class="sxs-lookup"><span data-stu-id="fb130-122">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="fb130-123">**Remitteringskladde** – Bogfør remitteringer.</span><span class="sxs-lookup"><span data-stu-id="fb130-123">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="fb130-124">**Udlign vekseljournal** – Bogfør udlignede veksler</span><span class="sxs-lookup"><span data-stu-id="fb130-124">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="fb130-125">Bogføring af følgeseddel</span><span class="sxs-lookup"><span data-stu-id="fb130-125">Packing slip posting</span></span>                 | <span data-ttu-id="fb130-126">Opdater følgesedler for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fb130-126">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="fb130-127">Bogfør fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="fb130-127">Post free text invoice</span></span>               | <span data-ttu-id="fb130-128">Bogfør fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="fb130-128">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="fb130-129">Bogføring af faktura</span><span class="sxs-lookup"><span data-stu-id="fb130-129">Posting invoice</span></span>                      | <span data-ttu-id="fb130-130">Bogfør fakturaer for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fb130-130">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="fb130-131">Bogføring af plukliste</span><span class="sxs-lookup"><span data-stu-id="fb130-131">Posting picking list</span></span>                 |<span data-ttu-id="fb130-132">Opdater pluklister for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fb130-132">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="fb130-133">**Opgave for forretningsproceskomponent**</span><span class="sxs-lookup"><span data-stu-id="fb130-133">**Business process component task**</span></span>   

<span data-ttu-id="fb130-134">Oprette og indsende EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="fb130-134">Create and submit the EU sales list</span></span>

| <span data-ttu-id="fb130-135">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="fb130-135">Page name</span></span>                            | <span data-ttu-id="fb130-136">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="fb130-136">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="fb130-137">EU-listesystem</span><span class="sxs-lookup"><span data-stu-id="fb130-137">EU sales list</span></span>                         | <span data-ttu-id="fb130-138">Indberet EU-salg til skattemyndighederne til momsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="fb130-138">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







