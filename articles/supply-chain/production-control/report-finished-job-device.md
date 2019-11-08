---
title: Færdigmelde til en id-kontrolleret lokation fra jobkortenheden
description: Dette emne beskriver processen til fuldførelse af færdigvarer på en produktionsordre til et lager, når et id styrer lokationen.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572123"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="86be1-103">Færdigmelde til en id-kontrolleret lokation fra jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="86be1-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="86be1-104">Den proces, der kaldes færdigmelding, fuldfører færdigvarerne på en produktionsordre til lageret.</span><span class="sxs-lookup"><span data-stu-id="86be1-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="86be1-105">Hvis det færdige produkt er aktiveret til de avancerede lagerprocesser, færdigmeldes produktet til en lokation, der kaldes udlagringslokationen for produktionen.</span><span class="sxs-lookup"><span data-stu-id="86be1-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="86be1-106">Du kan finde oplysninger om, hvordan du konfigurerer udlagringslokationen for produktionen, under [Produktionsudlagringslokation](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="86be1-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="86be1-107">Du skal vælge et eksisterende id-nummer for at udføre denne opgave.</span><span class="sxs-lookup"><span data-stu-id="86be1-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="86be1-108">Hvis produktionsudlagringslokationen er konfigureret til at blive sporet på basis af id, skal id-nummeret inkluderes, når produktionsudlagringslokationen færdigmeldes.</span><span class="sxs-lookup"><span data-stu-id="86be1-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="86be1-109">Feltet **Id** vises i prompten **Rapport i gang** på siden **Jobkortenhed**.</span><span class="sxs-lookup"><span data-stu-id="86be1-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="86be1-110">Feltet er kun synligt i prompten **Rapport i gang**, når der rapporteres for den sidste operation i produktionsordren.</span><span class="sxs-lookup"><span data-stu-id="86be1-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="86be1-111">Feltet vises kun, hvis varen for produktionsordren er aktiveret til lokationsstyringsprocesserne.</span><span class="sxs-lookup"><span data-stu-id="86be1-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
