---
title: Luk Debitor
description: Nedenstående emne indeholder de sider, der understøtter forretningsprocessen for afslutning af Debitor.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc3355f7fa6f72906e427203234de7ece27595e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835430"
---
# <a name="close-accounts-receivable"></a><span data-ttu-id="95e1b-103">Luk Debitor</span><span class="sxs-lookup"><span data-stu-id="95e1b-103">Close Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95e1b-104">Følgende tabel indeholder de sider, der understøtter forretningsprocessen for afslutning af Debitor.</span><span class="sxs-lookup"><span data-stu-id="95e1b-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="95e1b-105">Hvis du vil åbne nogle af de sider, der er i følgende tabel, skal du angive oplysninger eller parameterindstillinger.</span><span class="sxs-lookup"><span data-stu-id="95e1b-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="95e1b-106">**Opgave for forretningsproceskomponent**</span><span class="sxs-lookup"><span data-stu-id="95e1b-106">**Business process component task**</span></span>                   

<span data-ttu-id="95e1b-107">Lukke perioder i finansregnskabet</span><span class="sxs-lookup"><span data-stu-id="95e1b-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="95e1b-108">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="95e1b-108">Page name</span></span>                            | <span data-ttu-id="95e1b-109">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="95e1b-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="95e1b-110">Batchjob</span><span class="sxs-lookup"><span data-stu-id="95e1b-110">Batch job</span></span>                             | <span data-ttu-id="95e1b-111">Få vist eller opret batchjob.</span><span class="sxs-lookup"><span data-stu-id="95e1b-111">View or create batch jobs.</span></span> <span data-ttu-id="95e1b-112">Kørslerne kan ikke fuldføres, og du vil sikre, at al bogføring er udført.</span><span class="sxs-lookup"><span data-stu-id="95e1b-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="95e1b-113">Bekræft salgsordre</span><span class="sxs-lookup"><span data-stu-id="95e1b-113">Confirm sales order</span></span>                   | <span data-ttu-id="95e1b-114">Opdater salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="95e1b-115">Kursregulering</span><span class="sxs-lookup"><span data-stu-id="95e1b-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="95e1b-116">Opret posteringer, som opdaterer værdien af åbne debitorposteringer i udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="95e1b-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="95e1b-117">Journal</span><span class="sxs-lookup"><span data-stu-id="95e1b-117">Journal</span></span>                              | <span data-ttu-id="95e1b-118">Bogfør fakturaer, betalinger og egenveksler.</span><span class="sxs-lookup"><span data-stu-id="95e1b-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="95e1b-119">Kladdebilag</span><span class="sxs-lookup"><span data-stu-id="95e1b-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="95e1b-120">**Betalingskladde** – Opret, behandl og bogfør betalinger.</span><span class="sxs-lookup"><span data-stu-id="95e1b-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="95e1b-121">**Udsted vekseljournal** – Bogfør veksler.</span><span class="sxs-lookup"><span data-stu-id="95e1b-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="95e1b-122">**Protester vekseljournal** – Bogfør protesterede veksler.</span><span class="sxs-lookup"><span data-stu-id="95e1b-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="95e1b-123">**Genudsted vekseljournal** – Bogfør genudstedte veksler.</span><span class="sxs-lookup"><span data-stu-id="95e1b-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="95e1b-124">**Remitteringskladde** – Bogfør remitteringer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="95e1b-125">**Udlign vekseljournal** – Bogfør udlignede veksler</span><span class="sxs-lookup"><span data-stu-id="95e1b-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="95e1b-126">Bogføring af følgeseddel</span><span class="sxs-lookup"><span data-stu-id="95e1b-126">Packing slip posting</span></span>                 | <span data-ttu-id="95e1b-127">Opdater følgesedler for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="95e1b-128">Bogfør fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="95e1b-128">Post free text invoice</span></span>               | <span data-ttu-id="95e1b-129">Bogfør fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="95e1b-130">Bogføring af faktura</span><span class="sxs-lookup"><span data-stu-id="95e1b-130">Posting invoice</span></span>                      | <span data-ttu-id="95e1b-131">Bogfør fakturaer for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="95e1b-132">Bogføring af plukliste</span><span class="sxs-lookup"><span data-stu-id="95e1b-132">Posting picking list</span></span>                 |<span data-ttu-id="95e1b-133">Opdater pluklister for salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="95e1b-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="95e1b-134">**Opgave for forretningsproceskomponent**</span><span class="sxs-lookup"><span data-stu-id="95e1b-134">**Business process component task**</span></span>   

<span data-ttu-id="95e1b-135">Oprette og indsende EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="95e1b-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="95e1b-136">Sidenavn</span><span class="sxs-lookup"><span data-stu-id="95e1b-136">Page name</span></span>                            | <span data-ttu-id="95e1b-137">Anvendelse</span><span class="sxs-lookup"><span data-stu-id="95e1b-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="95e1b-138">EU-listesystem</span><span class="sxs-lookup"><span data-stu-id="95e1b-138">EU sales list</span></span>                         | <span data-ttu-id="95e1b-139">Indberet EU-salg til skattemyndighederne til momsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="95e1b-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]