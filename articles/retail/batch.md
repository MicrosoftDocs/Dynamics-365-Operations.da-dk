---
title: Forbedret håndtering af batchsporede varer
description: I dette emne beskrives de forbedringer, der er foretaget i håndteringen af batches for batchsporede varer under bogføringsprocessen for detailopgørelse.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617383"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="60493-103">Forbedret håndtering af batchsporede varer</span><span class="sxs-lookup"><span data-stu-id="60493-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="60493-104">I Microsoft Dynamics 365 for Retail POS kan batchnumre ikke hentes til batchsporede varer på tidspunktet for salget.</span><span class="sxs-lookup"><span data-stu-id="60493-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="60493-105">For specifikke konfigurationer, når salg bogføres i hovedkontoret via kundeordrer eller opgørelsesbogføring, vil Microsoft Dynamics-systemet dog forvente, at der findes gyldige batchnumre til varer med batchsporing, og at de skal bruges i faktureringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="60493-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="60493-106">Hvis der er gyldige batchnumre for produkter, bruges de af faktureringsprocessen for kundeordren og faktureringsprocessen for salgsordren fra opgørelsesbogføring.</span><span class="sxs-lookup"><span data-stu-id="60493-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="60493-107">Ellers kan faktureringsprocessen for kundeordren ikke bogføres, og POS-brugeren modtager en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="60493-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="60493-108">Opgørelsesbogføringen går derefter i fejltilstand.</span><span class="sxs-lookup"><span data-stu-id="60493-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="60493-109">Denne fejltilstand forekommer, også selvom negativt lager er aktiveret for produkterne.</span><span class="sxs-lookup"><span data-stu-id="60493-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="60493-110">Forbedringer, der er foretaget i Microsoft Dynamics for Retail version 10.0.4 og senere, er med til at sikre, at kundeordrefakturering og salgsordrefakturering via opgørelsesbogføring ikke spærres for batchsporede varer, når negativt lager er aktiveret for disse varer, hvis lageret er 0 (nul), eller et batchnummer ikke er tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="60493-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="60493-111">Den nye funktionalitet bruger et standardbatch-id til salgslinjerne, når batchnumre ikke er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="60493-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="60493-112">Hvis du vil definere det standardbatch-id, der bruges til kundeordrer, skal du gå til siden **Detailparametre**, åbne fanen **Kundeordrer** i oversigtspanelet **Ordre** og udfylde feltet **Standardbatch-id**.</span><span class="sxs-lookup"><span data-stu-id="60493-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="60493-113">Hvis du vil definere det standardbatch-id, der bruges til salgsordrefakturering via opgørelsesbogføring, skal du gå til siden **Detailparametre**, åbne fanen **Postering** i oversigtspanelet **Opdatering af lager** og udfylde feltet **Standardbatch-id**.</span><span class="sxs-lookup"><span data-stu-id="60493-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="60493-114">Denne funktionalitet er kun tilgængelig, når avanceret lagerstyring er aktiveret for det specifikke lagersted og for varerne.</span><span class="sxs-lookup"><span data-stu-id="60493-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="60493-115">I en senere version understøtter funktionen også de scenarier, hvor den avancerede lagerstyring ikke bruges.</span><span class="sxs-lookup"><span data-stu-id="60493-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>