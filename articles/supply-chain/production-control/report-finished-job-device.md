---
title: Færdigmelde til en id-kontrolleret lokation fra jobkortenheden
description: I dette emne beskrives processen til fuldførelse af færdigvarer på en produktionsordre til et lager, når et id styrer lokationen.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211163"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="2098f-103">Færdigmelde til en id-kontrolleret lokation fra jobkortenheden</span><span class="sxs-lookup"><span data-stu-id="2098f-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="2098f-104">Den proces, der kaldes færdigmelding, fuldfører færdigvarerne på en produktionsordre til lageret.</span><span class="sxs-lookup"><span data-stu-id="2098f-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="2098f-105">Hvis det færdige produkt er aktiveret til de avancerede lagerprocesser, færdigmeldes produktet til en lokation, der kaldes udlagringslokationen for produktionen.</span><span class="sxs-lookup"><span data-stu-id="2098f-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="2098f-106">Du kan finde oplysninger om, hvordan du konfigurerer udlagringslokationen for produktionen, under [Produktionsudlagringslokation](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="2098f-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="2098f-107">Hvis udlagringslokationen for produktionen er kontrolleret af nummerplader, skal der angives en nummerplade, når færdigmeldingen rapporteres.</span><span class="sxs-lookup"><span data-stu-id="2098f-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="2098f-108">Feltet **Id** vises i prompten **Rapport i gang** på siden **Jobkortenhed**.</span><span class="sxs-lookup"><span data-stu-id="2098f-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="2098f-109">Feltet er kun synligt i prompten **Rapportfremgang**, når der rapporteres om den sidste operation i produktionsordren, og varen til produktionsordren er aktiveret for lagerstedets styringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="2098f-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="2098f-110">Der er to muligheder for at angive nummerpladen</span><span class="sxs-lookup"><span data-stu-id="2098f-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="2098f-111">Brugeren vælger et eksisterende nummerpladenummer i feltet nummerplade.</span><span class="sxs-lookup"><span data-stu-id="2098f-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="2098f-112">Nummerpladenummeret genereres automatisk fra en nummerserie og nulstilles til nummerpladefeltet.</span><span class="sxs-lookup"><span data-stu-id="2098f-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="2098f-113">Muligheden for automatisk at oprette nummerpladen konfigureres ved at vælge indstillingen **Generer nummerplade** på siden **Konfigurer jobkort for enheder**.</span><span class="sxs-lookup"><span data-stu-id="2098f-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
